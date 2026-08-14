---
title: "Integrações"
nav_order: 8
parent: "Configurações da Organização"
permalink: /configuracoes/integracoes/
---

> Disponível para quem tem a capacidade **Integrações** — na prática, quem administra a organização.

## Para que serve

A tela **Integrações** permite que a sua OSC libere, para um **sistema parceiro** (um site institucional, um painel de doadores, uma ferramenta interna da organização), a leitura do **próprio resumo financeiro** — sem dar acesso à plataforma e sem criar um usuário para ninguém de fora.

É diferente da [Página Pública](/configuracoes/pagina-publica/): a Página Pública é um endereço aberto para qualquer pessoa ver; a integração é um **canal técnico**, autenticado por credencial, para outro sistema **consultar os números** e exibi-los do jeito que fizer sentido para ele.

## Como gerar uma credencial

1. Em **Configurações → Integrações**, clique em **Gerar nova credencial**.
2. Dê um nome que identifique o uso (ex.: "Site institucional", "Painel do conselho").
3. A credencial aparece **uma única vez**, na hora da criação.

> ⚠️ **Atenção · A credencial não pode ser recuperada depois**
>
> Assim que você sai da tela (ou atualiza a página), o valor completo da credencial **não é mostrado de novo em lugar nenhum** — nem para você, nem para o suporte. Copie e guarde num lugar seguro (cofre de senhas da OSC) antes de sair da tela. Se perder, a única saída é **revogar** aquela credencial e **gerar uma nova**, e então atualizar o sistema parceiro com o valor novo.

## Como revogar

Na lista de credenciais, escolha **Revogar** na credencial que não deve mais funcionar. A revogação vale **a partir da chamada seguinte** e é **definitiva** — não existe "reativar", só gerar uma credencial nova.

Revogue sempre que: a integração deixar de ser usada, houver suspeita de vazamento, ou a pessoa/empresa responsável pelo sistema parceiro mudar.

## O que a lista mostra

Para cada credencial gerada, a tela mostra:

- **Nome** dado na criação
- **Data de criação**
- **Último uso** (quando a credencial foi usada pela última vez para consultar dados)
- **Situação** (ativa ou revogada)

## Trate como senha

> ⚠️ **A credencial dá acesso de leitura aos números financeiros da sua organização**
>
> Quem tiver a credencial em mãos consegue consultar o resumo financeiro da OSC pela API, sem precisar de login. Compartilhe apenas com quem vai efetivamente configurar o sistema parceiro, nunca por canal inseguro (não cole em grupo de WhatsApp, chat público, planilha compartilhada sem controle de acesso). Se a pessoa responsável pela integração sair da organização, revogue e gere uma nova.

---

## Para quem desenvolve o sistema parceiro

Esta seção é o contrato técnico da API. Ela é a mesma para qualquer organização que gerar uma credencial — a organização em si nunca é um parâmetro da chamada, ela vem embutida na credencial.

### Especificação OpenAPI

Além desta descrição em prosa, existe a especificação formal em **OpenAPI 3.1**, disponível em:

```
https://docs.financeiro.rit360.org.br/assets/api/integration-finance-summary.yaml
```

Ela pode ser usada para gerar cliente automaticamente (ex.: `openapi-generator`, `openapi-typescript`) e é a **fonte formal do contrato** — o que está descrito em prosa nesta página é o mesmo contrato, em texto corrido.

### Endpoint

```
GET https://jswyzxutdkrbrleotklo.supabase.co/functions/v1/integration_finance_summary
```

Existe apenas este endpoint.

> ⚠️ **O endereço das funções não é o mesmo do aplicativo.** O RIT360 Financeiro é um serviço único (não há instalação por cliente), então o endereço acima vale para todas as organizações — mas ele aponta para o servidor de funções, não para `financeiro.rit360.org.br`. Chamar o endereço do aplicativo devolve **HTTP 200 com a página HTML do sistema**, não os dados: parece que funcionou e não funcionou. Use exatamente o endereço acima.

### Autenticação

Cabeçalho `Authorization: Bearer <credencial>`.

Formato da credencial: `rit_` seguido de 8 caracteres hexadecimais, `_` e mais 64 caracteres hexadecimais.

### Parâmetros de consulta

| Parâmetro | Obrigatório | Descrição |
|---|---|---|
| `from` | Sim | Data inicial do período, no formato `AAAA-MM-DD` |
| `to` | Sim | Data final do período, no formato `AAAA-MM-DD` — deve ser igual ou posterior a `from` |
| `group_by` | Não | `category` ou `project` — abre a composição do período por categoria ou por projeto |

Não há parâmetro de organização: ela é determinada sempre pela credencial usada na chamada.

### Exemplo de chamada

```
curl -H "Authorization: Bearer rit_3b95e9fe_..." \
  "https://jswyzxutdkrbrleotklo.supabase.co/functions/v1/integration_finance_summary?from=2026-07-01&to=2026-07-31"
```

### Exemplo de resposta

```json
{
  "organization_id": "c121b5a6-...",
  "period": { "from": "2026-07-01", "to": "2026-07-31" },
  "currency": "BRL",
  "balance": { "total": 82643.47 },
  "realized": { "receitas": 595.02, "despesas": 7790, "resultado": -7194.98 },
  "budget": [
    { "fiscal_year": 2026, "available": false, "reason": "sem_versao_vigente_aprovada" }
  ],
  "group_by": null,
  "breakdown": null
}
```

Com `group_by=category` (ou `project`), o campo `group_by` ecoa o valor pedido e `breakdown` passa a trazer uma lista de itens, cada um com `id`, `name`, `receitas` e `despesas`. **A soma dos itens da quebra fecha exatamente com os totais de `realized`** — é uma garantia da API, não uma aproximação.

### Sobre o orçamento

O orçamento do RIT360 Financeiro é **anual**. O campo `budget` traz um item para cada exercício coberto pelo período consultado. Quando não existe uma versão de orçamento aprovada e vigente para aquele ano, o item vem com `available: false` e o motivo em `reason` — o campo **nunca vem zerado** nesse caso, justamente para não sugerir que o orçamento é igual a zero.

### Respostas

| Código | Significado |
|---|---|
| `200` | Sucesso |
| `401` | Credencial ausente, inválida ou revogada |
| `403` | Escopo insuficiente para a operação pedida |
| `422` | Período ou `group_by` inválido |
| `429` | Limite de requisições excedido (ver `Retry-After`) |
| `500` | Falha interna |

Toda resposta de erro traz um corpo com `error_code` e `message`.

### Limite de requisições

**60 requisições por hora, por credencial.** Contam apenas as requisições **atendidas com sucesso** (resposta `200`). Recusas — por credencial inválida, por parâmetro inválido ou pelo próprio limite — não realimentam a janela, então um cliente mal configurado não fica bloqueado indefinidamente por insistir.

Sobre os cabeçalhos, atenção ao que vem em cada caso:

- na resposta `200`, vêm `X-RateLimit-Limit` e `X-RateLimit-Remaining`, com o limite total e quanto resta na janela;
- na resposta `429`, vêm `X-RateLimit-Limit` e `Retry-After`, este último com os segundos a esperar antes de tentar de novo;
- nas demais respostas de erro (`401`, `403`, `422`, `500`) **não vem nenhum cabeçalho de limite**.

Ou seja: não use a presença desses cabeçalhos para decidir se houve erro — use o código de resposta.

### O que a API nunca devolve

Assim como a Página Pública, esta API trabalha **só com totais**. Ela nunca devolve:

- Lançamento individual
- Contraparte (quem pagou, quem recebeu)
- Nome de pessoa física
- Chave Pix ou dados bancários
- CPF
- Nome de fornecedor
- Anexos ou comprovantes

Isso não é uma limitação temporária — é a garantia que permite a qualquer OSC liberar essa integração sem avaliar risco de exposição de dado pessoal caso a caso.

## Por onde seguir

- **[Página Pública](/configuracoes/pagina-publica/)** — o outro canal de transparência, para leitura humana e sem autenticação.
- **[Módulos → Relatórios](/modulos/relatorios/)** — a visão interna completa dos mesmos números.
