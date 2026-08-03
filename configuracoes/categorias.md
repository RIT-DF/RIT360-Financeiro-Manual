---
title: "Categorias"
nav_order: 5
parent: "Configurações da Organização"
permalink: /configuracoes/categorias/
---

> Disponível para **Presidente (admin)** e **Tesoureiro**.

A página **Categorias** organiza as categorias contábeis e os centros de custo da OSC — o esqueleto da sua contabilidade gerencial.

[![Configurações — Categorias](/assets/screenshots/config-categorias.png)](/assets/screenshots/config-categorias.png)
*Configurações — Categorias e centros de custo*

> 💡 **Por que isso importa**
>
> Categoria é o que **faz o relatório financeiro fazer sentido**. Sem categoria, você tem 200 lançamentos no mês e nenhuma resposta sobre "para onde vai o dinheiro?". Com categoria ruim (inconsistente, duplicada, vaga), o relatório engana mais do que ajuda. Com categoria boa (enxuta, consistente, semântica), o relatório responde sozinho — você vê em 30 segundos quanto a OSC gastou com aluguel, quanto com material, quanto recebeu de doação, quanto de mensalidade. **Tempo investido em organizar categorias é o investimento de melhor retorno** que uma OSC pode fazer no RIT360 Financeiro.

A página tem 3 abas: **Receitas**, **Despesas** e **Centros de custo**.

## Receitas

Categorias para classificar entradas financeiras. Exemplos típicos de OSC:

- Doações
- Mensalidades de associados
- Subvenções e editais
- Arrecadação de eventos
- Venda de produtos (lojinha)
- Patrocínio
- Rendimentos financeiros

## Despesas

Categorias para classificar saídas. Exemplos:

- Aluguel
- Conta de luz, água, internet
- Material didático
- Material de escritório
- Combustível e transporte
- Alimentação
- Salários e encargos
- Manutenção
- Marketing e comunicação

## Centros de custo

> 📖 **Conceito · Categoria vs Centro de custo**
>
> **Categoria** classifica a *natureza* do lançamento (o que foi gasto/recebido): "aluguel", "doação", "combustível". **Centro de custo** classifica a *origem ou destino organizacional*: "Sede", "Filial Norte", "Coordenação de Eventos", "Diretoria de Comunicação". Os dois são independentes — um lançamento pode ter categoria "Combustível" e centro de custo "Filial Norte" simultaneamente. Centro de custo é opcional na maioria dos lançamentos; categoria é (quase sempre) obrigatória.

OSC pequena geralmente não precisa de centros de custo. OSC com **múltiplas frentes operacionais** (sede + filiais; várias coordenações; diretorias com orçamentos separados) ganha muito ao usar.

### Responsáveis pelo centro de custo
{: #responsaveis-pelo-centro-de-custo }

Ao **criar** ou **editar** um centro de custo, o formulário traz a seção **Responsáveis pelo centro de custo** — uma lista dos membros da OSC com uma caixa de seleção para cada. Marque quem responde por aquele centro de custo e salve.

> 📖 **Você já pode designar quem ainda não ativou o acesso**
>
> Um membro recém-cadastrado, que ainda não definiu a senha do primeiro acesso, já aparece nesta lista e pode ser marcado como responsável — sem esperar ele entrar no sistema pela primeira vez. O nome vem com a marca discreta **"· acesso pendente"**. A pessoa só passa a *operar* o centro de custo depois de ativar o acesso.

[![Responsáveis pelo centro de custo](/assets/screenshots/config-cc-responsaveis.png)](/assets/screenshots/config-cc-responsaveis.png)
*Editar centro de custo — seção "Responsáveis pelo centro de custo"*

> ⚠️ **Importante · Atribuir responsável não basta sozinho**
>
> Marcar alguém como responsável por um centro de custo **só concede acesso se a pessoa também tiver o cargo Gestor de Centro de Custo**. São duas coisas complementares: o **cargo** (em Configurações → Usuários → Editar papéis) diz que a pessoa *pode* gerir centros de custo; o **vínculo de responsável** aqui diz *quais* centros de custo. Faltando o cargo, o nome pode até estar marcado aqui, mas a pessoa não enxerga nem opera o centro de custo. Ver [Papéis e Permissões → Gestor de Centro de Custo](/papeis/#gestor-de-centro-de-custo).

Com o cargo e o vínculo em dia, o Gestor de Centro de Custo passa a **criar e editar** lançamentos daquele CC e a **ver** as movimentações e relatórios recortados a ele — sem acesso ao restante do financeiro da OSC. Presidente e Tesoureiro continuam enxergando **todos** os centros de custo, independentemente dessa lista.

### Coluna "Gestor(es)" na lista
{: #coluna-gestores }

A lista da aba **Centros de custo** tem uma coluna **"Gestor(es)"** que mostra, de relance, quem responde por cada centro — sem precisar abrir **Editar**. Centros sem responsável aparecem com **"—"**; quando há mais de um, a lista exibe o **primeiro nome com um "+N"**, e a lista completa aparece ao passar o mouse por cima.

[![Lista de centros de custo com a coluna Gestor(es)](/assets/screenshots/config-cc-lista-gestores.png)](/assets/screenshots/config-cc-lista-gestores.png)
*A coluna "Gestor(es)" mostra o responsável de cada centro de custo (ou "—" quando não há).*
> ✓ **Dica · Confira os responsáveis de relance**
>
> Essa coluna é o jeito rápido de auditar quem está no comando de cada área: um centro de custo importante com "—" na coluna Gestor(es) é sinal de que falta atribuir responsável (ou que quem foi atribuído ainda não tem o cargo Gestor de Centro de Custo).

## Template de categorias

Para começar rapidamente, clique em **Aplicar template**. O RIT360 Financeiro tem modelos prontos por tipo de OSC — há templates para **Grupo Escoteiro, Associação, Instituto, Fundação, ONG, Coletivo e Cooperativa**, cada um com as categorias de receita e despesa típicas daquele perfil. Escolha o modelo mais próximo da sua organização; aplicar o template importa as categorias do modelo para a sua OSC, sem apagar o que você já tinha.

> ✓ **Dica · Comece com template, depois afine**
>
> Você nunca acerta a lista perfeita de categorias na primeira tentativa. Comece com um template próximo ao perfil da sua OSC, opere por 1-2 meses, e ajuste o que **não bater** com sua realidade: renomeie categorias confusas, una categorias que viraram redundantes, crie categoria nova quando 5+ lançamentos foram para "Outros". Lista enxuta vence lista exaustiva — categoria que aparece 2× no ano não vale ter como categoria separada.

> ⚠️ **Atenção · Nome de categoria pode virar informação pública**
>
> Se a sua OSC usa a [Página Pública](/configuracoes/pagina-publica/) de transparência, os **nomes das categorias aparecem lá** — no bloco "De onde vem, para onde vai". Uma categoria chamada *"Acordo trabalhista — Fulano"* ou *"Auxílio jurídico caso X"* vira texto público junto com o valor. Antes de publicar, leia a lista inteira com olhos de quem é de fora e prefira nomes **descritivos e impessoais** ("Despesas jurídicas", "Auxílio a beneficiários"). Categorização inconsistente também fica visível — vale conferir na prévia.

> ⚠️ **Atenção · Cuidado ao renomear categoria em uso**
>
> Renomear uma categoria atinge **retroativamente** todos os lançamentos que já a usavam — eles passam a aparecer com o novo nome em relatórios e listagens. Geralmente isso é o que você quer (ajustou o nome para algo mais claro), mas pense duas vezes antes de renomear uma categoria que já foi referenciada em prestação de contas externa.

## Hierarquia de categorias

O RIT360 Financeiro suporta **categorias-mãe com sub-categorias** — útil para agrupar afins sem perder granularidade. Exemplo:

- Loja Virtual (categoria-mãe)
  - Camisetas
  - Canecas
  - Doações pelo site

O modo automático de integração com WooCommerce (em Configurações → Organização) usa exatamente esse padrão: cria sub-categorias sob a categoria-mãe escolhida para cada categoria do WC.

## Por onde seguir

- **Movimentações** — onde as categorias aparecem nos formulários de novo lançamento e nos filtros da lista.
- **Reembolsos** e **Pedidos de Pagamento** — onde as categorias de despesa são usadas para classificar as solicitações.
- **Configurações → Organização → Integrações** — onde a categoria-mãe do WooCommerce é configurada.
