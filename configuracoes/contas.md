---
title: "Contas Bancárias"
nav_order: 4
parent: "Configurações da Organização"
permalink: /configuracoes/contas/
---

> Disponível para **Presidente (admin)** e **Tesoureiro**.

A página **Contas Bancárias** lista as contas financeiras da sua OSC e permite cadastrar novas, editar dados existentes e desativar contas que saíram de uso.

[![Configurações — Contas](/assets/screenshots/config-contas.png)](/assets/screenshots/config-contas.png)
*Configurações — Contas financeiras*

> 💡 **Por que isso importa**
>
> "Conta financeira" no RIT360 Financeiro não é só **conta bancária**. É qualquer lugar onde a OSC guarda dinheiro: a conta corrente do banco, a poupança, o caixa interno em dinheiro vivo, o cartão de crédito da OSC, a conta no Mercado Pago para recebimentos online, o saldo no PayPal. Cada um desses é uma "conta" diferente, e mantê-los separados no RIT360 Financeiro **faz a contabilidade bater com a realidade** — você sabe quanto tem em cada lugar, e o saldo total consolidado reflete a posição real da OSC.

## Tipos de conta suportados

- **Corrente** — conta bancária de uso geral
- **Poupança** — conta poupança vinculada
- **Caixa** — caixa interno físico (notas e moedas guardadas na sede)
- **Cartão de crédito** — o cartão da OSC, tratado como **dívida** (passivo); ver o conceito abaixo
- **Cartão Pré-pago** — quando há saldo pré-pago vinculado
- **Investimento** — aplicações, CDB
- **Fundo** — cotas de fundos de investimento
- **Outro** — para casos não cobertos (PayPal, Mercado Pago, gateway de pagamento, etc.)

[![Cadastro de conta tipo Cartão de crédito](/assets/screenshots/manual-conta-cartao-credito.png)](/assets/screenshots/manual-conta-cartao-credito.png)
*Cadastro de uma conta do tipo Cartão de crédito*

> 📖 **Conceito · Cartão de crédito é dívida, não dinheiro guardado**
>
> As demais contas guardam dinheiro que a OSC **tem** (ativos). O cartão de crédito é o contrário: representa dinheiro que a OSC **deve** (passivo). Por isso ele entra de forma diferente no saldo consolidado, que passa a mostrar **Ativos** e **Passivos** em blocos separados e o **Líquido** — o que sobra depois de descontar o que se deve.
>
> Na prática: uma **compra no cartão** é lançada como despesa na conta do cartão (aumenta a dívida); o **pagamento da fatura** é uma **transferência** da conta bancária para o cartão (reduz a dívida). OSCs que não cadastram nenhum cartão de crédito não veem diferença nenhuma no consolidado.
>
> [![Saldo consolidado com Ativos e Passivos](/assets/screenshots/manual-saldos-ativos-passivos.png)](/assets/screenshots/manual-saldos-ativos-passivos.png)
> *Saldo consolidado separando Ativos, Passivos e Líquido*

## Adicionar nova conta

Clique em **+ Nova conta**. Preencha:

- **Nome** — descritivo (ex: "Banco do Brasil — CC", "Mercado Pago — Vendas WC")
- **Tipo** — da lista acima
- **Saldo inicial** — quanto tem na conta no momento do cadastro
- **Data de abertura** — quando a conta começou a ser usada pela OSC (não a data de criação no RIT360 Financeiro)
- **Conta padrão da organização** (opcional) — ver a seção **Conta padrão**, abaixo
- **Dados bancários** (opcional, recolhível) — banco, agência e demais dados, quando aplicável
- **Personalização** (opcional, recolhível) — uma **cor** e um **ícone** para a conta; ver a seção **Personalização**, abaixo

[![Editar conta — conta padrão e personalização](/assets/screenshots/config-contas-editar.png)](/assets/screenshots/config-contas-editar.png)
*Cadastro/edição de conta — alternar conta padrão e definir cor e ícone*

> 📖 **Conceito · Saldo inicial e data de abertura**
>
> Quando você cadastra uma conta nova no RIT360 Financeiro, ela precisa saber qual era o saldo no momento em que sua OSC começou a usá-la no sistema. **Não é o saldo de hoje** — é o saldo na data de abertura. O RIT360 Financeiro usa esse valor como ponto de partida para calcular saldos futuros somando receitas e subtraindo despesas pagas. Se você está migrando de planilha para o RIT360 Financeiro, **a data de abertura é o dia que você começa a registrar no RIT360 Financeiro**, e o saldo inicial é o que estava na conta naquele dia.

## Ações por conta

- **Definir padrão / Remover padrão** — marca (ou desmarca) a conta como **padrão da organização**; ver abaixo
- **Editar** — alterar nome, banco, tipo, cor e ícone (não o saldo — saldo só muda via movimentações)
- **Desativar / Reativar** — uma conta desativada não aparece em filtros e formulários, mas seu histórico permanece preservado

> ⚠️ **Atenção · Conta com movimentações não pode ser excluída**
>
> O RIT360 Financeiro **não permite excluir conta que tem movimentações registradas** — só desativar. Motivo: excluir destruiria a história contábil dessas movimentações ("essa receita foi para qual conta?"). Para "encerrar" uma conta na prática, **desative**. As movimentações ficam intactas no histórico, e a conta desativada não aparece nos formulários de novo lançamento.

## Conta padrão

Uma das contas pode ser marcada como **conta padrão da organização**. A conta padrão é **pré-selecionada automaticamente ao criar um novo lançamento** — assim, quem registra movimentações não precisa escolher a conta toda vez (é só mudar quando for outra).

- **Apenas uma** conta pode ser a padrão por vez. Ao definir uma nova padrão, a anterior deixa de ser.
- Marque pela ação **Definir padrão** na lista, ou pelo interruptor **Conta padrão da organização** ao criar/editar a conta.
- A conta padrão exibe o selo **Padrão** na lista de contas.
- Se você **desativar** a conta que era a padrão, ela deixa de ser padrão automaticamente — defina outra.

> ✓ **Dica · Aponte para a conta que mais movimenta**
>
> Defina como padrão a conta por onde passa o grosso do dia a dia (geralmente a conta corrente principal). Como ela já vem selecionada no novo lançamento, você economiza um passo na maioria dos registros e reduz o risco de lançar na conta errada por desatenção.

## Personalização (cor e ícone)

Na seção **Personalização** do cadastro da conta, você pode definir uma **cor** (em hexadecimal) e um **ícone** para a conta. A cor vira um **acento visual** nos cartões de saldo — no **Painel**, na lista de movimentações e nos relatórios —, ajudando a distinguir as contas de relance.

> ✓ **Dica · Cores ajudam a bater o olho**
>
> Dar a cada conta uma cor própria (azul para o banco, verde para o caixa, roxo para a poupança) faz o Painel ficar legível num instante — você identifica de qual conta é cada saldo sem precisar ler o nome. É opcional, mas vale o minuto de configuração.

## Saldo em tempo real

Cada conta na lista mostra o **saldo atual**, calculado em tempo real a partir das movimentações pagas. Quando você marca uma receita ou despesa como paga em Movimentações, o saldo aqui atualiza imediatamente.

> ✓ **Dica · Concilie mensalmente contra o extrato bancário**
>
> No final de cada mês, abra o extrato do banco e o saldo da conta correspondente aqui no RIT360 Financeiro. Eles devem bater **centavos por centavos**. Diferenças apontam para lançamento esquecido, valor digitado errado, ou taxa que não foi registrada. Corrigir mensalmente é fácil; descobrir 6 meses depois é pesadelo.

## Dados bancários de quem recebe {#dados-bancarios-de-quem-recebe}

Além das contas da própria OSC, o sistema guarda os **dados bancários de quem recebe** um pagamento — o CPF do titular, a chave Pix, o banco, a agência e a conta que você informa num lançamento de despesa, num pedido de pagamento ou num reembolso. Esses dados têm regras próprias, definidas aqui nesta página.

### Quem vê os dados completos

- **Quem tem permissão de pagar** vê CPF, chave Pix, banco, agência e conta **por inteiro**, como sempre viu — no lançamento, no pedido de pagamento e no reembolso.
- **Quem não tem** vê apenas os **últimos dígitos** (por exemplo, `•••.•••.123-45`) — o suficiente para conferir de qual conta se trata, sem expor o número inteiro.
- O **nome de quem recebe continua visível para todos**.
- Quem **preenche** os dados ao criar um lançamento, pedido ou reembolso continua digitando normalmente — a regra vale para consultar, não para informar.
- A **exportação dos dados da organização** segue a mesma regra: quem não pode pagar recebe os dados mascarados.

A permissão de pagar é ajustada em [Cargos e permissões](/configuracoes/cargos/#permissao-pagar).

> ✓ **Dica · Ver mascarado não apaga nada**
>
> Se você editar um lançamento (mudar a descrição, o valor, a categoria) **sem mexer no bloco de dados de pagamento**, os dados originais ficam intactos — mesmo que você os esteja vendo mascarados. Não existe risco de "salvar por cima" com as bolinhas.

### Descarte automático depois do pagamento

Passado um prazo contado a partir da **conclusão do pagamento**, o sistema **apaga sozinho** os dados bancários do favorecido.

- **O que é apagado:** CPF do titular, chave Pix, banco, agência, conta e dígito.
- **O que permanece:** valor, descrição, datas, categoria, centro de custo, projeto, anexos, situação e **o nome de quem recebeu**. O histórico contábil e a prestação de contas **não se perdem**.
- **Pagamentos ainda não concluídos nunca são tocados**, por mais antigos que sejam — esses dados ainda vão ser usados para transferir.

### Escolher o prazo

O prazo é definido pela organização, aqui em **Configurações → Contas Bancárias**:

1. Localize o cartão **Descarte dos dados bancários de quem recebe** na página.
2. Em **Prazo após a conclusão do pagamento**, escolha **30, 90, 180 ou 365 dias**. O padrão é **90 dias** — quem não mexer em nada se comporta como 90.
3. Logo abaixo, a tela mostra **quantos registros já estariam vencidos** com o prazo escolhido, separados por lançamentos, reembolsos e pedidos de pagamento — assim você sabe o efeito imediato da escolha antes de confirmar.
4. Clique em **Salvar prazo**.

O descarte é **definitivo e acontece sem aviso**: são dados que já cumpriram a finalidade para a qual foram coletados.

**Não existe a opção de guardar para sempre**: passado o prazo escolhido, o descarte acontece.

> 💡 **Por que isso importa**
>
> Esses dados existem para uma finalidade única: fazer a transferência. Cumprida a finalidade, não há motivo para continuar guardando o CPF e a conta de um fornecedor ou de um voluntário — sobretudo porque quem recebe muitas vezes **não tem conta no sistema** para pedir a remoção por conta própria. Guardar só o tempo necessário é o comportamento correto e reduz o que a sua OSC teria a proteger num incidente.

> ⚠️ **Atenção · Registro sem dados bancários não é erro**
>
> Ao abrir um lançamento, pedido ou reembolso antigo, você pode encontrar o cartão **Dados de pagamento** sem os dados, com o aviso de que *"os dados bancários foram removidos depois que o pagamento foi concluído, por já terem cumprido sua finalidade"*. Isso é o descarte automático funcionando — **não é falha do sistema nem dado perdido**. Se precisar pagar de novo para a mesma pessoa, peça os dados novamente e registre no novo lançamento.

### Quando alguém pede a exclusão dos próprios dados

Quem pede a exclusão da própria conta passa a ter apagados também os dados bancários que informou em **reembolsos já pagos**. Os reembolsos continuam no histórico da organização, com valor, descrição, datas, comprovantes e aprovações. **Reembolsos ainda não pagos mantêm os dados**, para que a OSC consiga concluir a transferência — e são apagados depois, pelo prazo normal de descarte.

## Por onde seguir

- **Movimentações** — onde as contas aparecem como destino/origem dos lançamentos.
- **Painel** — onde os saldos consolidados das contas ativas aparecem.
- **[Cargos e permissões](/configuracoes/cargos/#permissao-pagar)** — onde se define quem pode pagar (e, por consequência, quem vê os dados bancários completos).
- **Configurações → Organização → Integrações → WooCommerce** — onde você define qual conta recebe receitas da loja online.
