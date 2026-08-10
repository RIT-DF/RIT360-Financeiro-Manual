---
title: "Painel"
nav_order: 1
parent: "Módulos"
permalink: /modulos/painel/
---

O **Painel** é a primeira tela após o login — a visão de cockpit da sua OSC. Em uma única página, de cima para baixo, você vê quanto dinheiro tem disponível, como o caixa evoluiu nos últimos meses, os atalhos para as pendências que precisam da sua atenção e os pontos fora do padrão que valem uma olhada — tudo ajustado ao seu papel.

[![Painel](/assets/screenshots/painel-visao-geral.png)](/assets/screenshots/painel-visao-geral.png)
*Painel principal — contas e resumo do mês, fluxo de caixa, pendências e pontos de atenção*

> 💡 **Por que isso importa**
>
> A maioria das ferramentas financeiras te despeja em uma lista enorme de lançamentos no login. O Painel inverte isso: **mostra primeiro o que importa para você decidir o próximo passo** — saldo, resumo, pendências por papel, o que está fora do padrão. Tesoureiro vê quantos reembolsos esperam pagamento; presidente vê pedidos aguardando aprovação; voluntário vê seus próprios reembolsos pendentes. Resultado: você gasta menos tempo procurando informação, mais tempo decidindo.

## Como o Painel está organizado

De cima para baixo, o Painel tem cinco blocos:

1. **Contas** e **Este mês** — uma linha por conta com o saldo, e o líquido no rodapé; ao lado, o resumo de receitas, despesas e resultado do mês.
2. **Fluxo de caixa** — gráfico com os últimos 6 meses, comparando receitas e despesas.
3. **Pendências** — três colunas lado a lado: **Pedidos de pagamento**, **Reembolsos** e **Projetos**, cada uma com o que está pendente para o seu papel.
4. **Pontos de atenção** — avisos sobre o que saiu do padrão recentemente (ver seção própria abaixo).

Quando existe algum aviso **grave** em aberto, um selo no topo da tela mostra quantos são. Clicar nesse selo leva direto ao bloco de Pontos de atenção, no fim da página — sem precisar rolar procurando.

## Checklist "Primeiros passos" (para quem administra a OSC) {#checklist-primeiros-passos-para-quem-administra-a-osc}

Se você é **admin da organização** e ela ainda está no início da configuração, o Painel mostra um card **"Primeiros passos"** logo no topo, com os itens principais para deixar a OSC pronta para operar:

- **Cadastrar uma conta bancária**
- **Adicionar a equipe** (convidar usuários)
- **Lançar o primeiro movimento**

Cada item **se marca sozinho** conforme você faz — não precisa voltar aqui para confirmar nada. O card também traz links de apoio para **revisar os dados da OSC** e as **categorias e centros de custo**, que fazem parte da mesma preparação inicial (o roteiro completo está em [Primeiros Passos da Organização](/primeiros-passos/organizacao/)).

> ✓ **O card some sozinho**
>
> Assim que os itens principais são concluídos, o card desaparece do Painel — ele existe só para orientar o início, não fica ocupando espaço depois que a OSC já está operando. Se preferir, também dá para **dispensar o card** a qualquer momento, mesmo sem ter concluído tudo.

## Bloco 1 · Contas e Este mês

O primeiro bloco do Painel traz, lado a lado, as contas da OSC e o resumo do mês.

### Contas

Uma linha por conta financeira da OSC (corrente, poupança, cartão, caixa interno, etc.) com o **saldo atual** de cada uma. No rodapé da lista, o **líquido** soma todas as contas ativas.

> 📖 **Conceito · Como o saldo é calculado**
>
> O saldo é calculado em tempo real a partir das movimentações financeiras: soma de receitas pagas menos despesas pagas, considerando o saldo inicial da conta. **Movimentações pendentes não entram no saldo** — só somam quando você marca como pagas. Isso bate com a realidade do extrato bancário: o que você tem hoje é o que efetivamente entrou e ainda não saiu, não o que está previsto.

### Este mês

Três cards rápidos com:

- **Receitas** do mês — total de receitas do mês atual, já recebidas ou ainda em aberto
- **Despesas** do mês — total de despesas do mês atual, mesma regra
- **Saldo do mês** — diferença entre as duas

Útil para responder de relance: "como foi o mês até agora?"

> ℹ️ **Observação**
>
> Este resumo considera o **mês inteiro** (do dia 1º ao último dia) e usa o **mesmo critério de data das demais telas**: o que já foi **pago ou recebido** entra pelo mês do **pagamento**; o que ainda está **em aberto** entra pelo mês do **vencimento**. Ou seja, ele mistura de propósito o que já aconteceu com o que ainda vai acontecer no mês — mas cada lançamento é contado no mês certo. Por isso este bloco e as **contas** ao lado podem mostrar números diferentes: as contas refletem só o dinheiro que já entrou ou saiu; o resumo do mês inclui também o que ainda está previsto.
>
> Ficam **fora** da conta os lançamentos **cancelados** e o **par de estorno**: quando um lançamento é estornado, o sistema cria um lançamento contrário para anulá-lo — os dois somam zero e nenhum dos dois entra no resumo. São valores que não representam dinheiro que entrou ou saiu de fato.

## Bloco 2 · Fluxo de caixa

Logo abaixo do primeiro bloco, um gráfico mostra os **últimos 6 meses** de movimentação, comparando o total de receitas e de despesas mês a mês. É a leitura rápida de tendência: a OSC está entrando numa fase de aperto ou de folga? As despesas estão subindo mais rápido que as receitas?

## Bloco 3 · Pendências

Três colunas lado a lado — **Pedidos de Pagamento**, **Reembolsos** e **Projetos** — cada uma em um card com suas pendências como linhas clicáveis. O que aparece depende do seu papel — você só vê pendências relacionadas ao que pode resolver. Clicar em uma linha leva direto à lista já filtrada pelo status correspondente.

### Pedidos de Pagamento

- **Solicitado por mim** — seus próprios pedidos pendentes (todos os papéis veem os próprios)
- **Aguardando aprovação** — somente para aprovadores elegíveis
- **Aprovados aguardando pagamento** — somente para o tesoureiro (e o presidente)

### Reembolsos

- **Meus reembolsos pendentes** — rascunhos e rejeitados aguardando reenvio (todos os papéis veem os próprios)
- **Aguardando aprovação** — somente para aprovadores elegíveis (Presidente, Tesoureiro e quem mais a OSC configurar)
- **Aguardando pagamento** — somente para o tesoureiro

### Projetos

Quando a OSC usa o módulo de [Projetos](/modulos/projetos/), a terceira coluna mostra: quantos **projetos ativos** existem, a **saúde dos ativos** (quantos saudáveis, em atenção e críticos) e um destaque para os que **precisam de atenção**. É a visão de portfólio em uma linha — para a diretoria saber, sem abrir projeto por projeto, se algo está pegando fogo.

> 📖 **Conceito · O Painel se adapta ao seu papel**
>
> Cada linha respeita o que você pode resolver. Um voluntário vê só "Solicitado por mim" / "Meus reembolsos pendentes"; um aprovador vê as linhas de aprovação; o tesoureiro vê também o que está "aguardando pagamento". Se uma das colunas não tiver nenhuma linha para o seu papel, ela simplesmente não aparece. Cada coluna do Painel ganhou ainda um ícone e um detalhe de cor para você localizar a informação mais rápido.

## Bloco 4 · Pontos de atenção

Fechando a tela, o Painel mostra os mesmos avisos que antes só existiam dentro de [Relatórios → aba Atenção](/modulos/relatorios/#atencao), agora considerando os **últimos 30 dias** — não o período que você escolheria em Relatórios, mas uma janela curta e fixa, pensada para "o que aconteceu recentemente que merece uma olhada".

O bloco mostra até **quatro avisos**. Havendo mais, um link **Ver todos** leva à aba Atenção dos Relatórios, já com esse mesmo período de 30 dias aplicado. Cada aviso é clicável e leva direto ao que ele aponta — o lançamento, a categoria, o fornecedor.

Quem tem permissão de administrar as configurações financeiras vê, no próprio aviso, a opção de **desligar aquele tipo de alerta**. Atenção: esse desligamento **vale para toda a organização**, não só para quem clicou — o texto do aviso deixa isso explícito antes de você confirmar.

O bloco **só aparece quando há algum aviso** nos últimos 30 dias — sem avisos, o Painel simplesmente termina no bloco de Pendências. Só vê este bloco quem tem permissão de ver Relatórios (Presidente, Tesoureiro e Comissão Fiscal).

### Novo aviso · Déficit projetado no fluxo de caixa

Este é o aviso mais recente: ele avisa quando o caixa da sua OSC caminha para ficar **negativo** em algum mês futuro, considerando o que já está agendado e, quando necessário, a média dos meses anteriores.

O aviso vem em dois tons, dependendo da certeza da conta:

- **Grave e afirmativo** — quando os compromissos **já agendados no sistema**, sozinhos, já levam o caixa a ficar negativo. Aqui a conta está fechada, independente de qualquer histórico: é dinheiro que já está programado para sair e não tem receita programada suficiente para cobrir.
- **Mais leve e condicional** — quando o caixa só fica negativo se você considerar a **média dos meses anteriores** como guia do que ainda deve acontecer. O texto do aviso deixa claro que está usando essa média, para você calibrar o quanto confiar nele.

Em ambos os casos, o aviso informa **em que mês** o caixa fica negativo, **de quanto é a falta** e **sobre o que a conta foi feita** (o que está agendado, e se entrou a média histórica).

> ⚠️ **Atenção · Este aviso só aparece no Painel**
>
> Diferente das outras quatro regras de atenção, o déficit projetado **não aparece na aba Atenção dos Relatórios** — ele é exclusivo do Painel. Se você foi procurar esse aviso em Relatórios e não achou, não é bug: é onde ele mora. Para a projeção completa mês a mês, use a [aba Previsão](/modulos/relatorios/#previsao-forecast) de Relatórios.

A regra vem **ligada por padrão**, com antecedência de **6 meses** (configurável para 3, 6 ou 12), em **Configurações → Relatórios → Regras de pontos de atenção** — junto com as demais regras (ver [Configuração das regras de atenção](/modulos/relatorios/#configuracao-das-regras-de-atencao)).

No rodapé do bloco de Pontos de atenção, um link indica onde ajustar as regras — visível só para quem tem permissão de mexer nelas.

> ✓ **Dica · Use o Painel como rotina de manhã**
>
> 5 minutos no Painel todo dia (ou toda segunda de manhã) substituem 1 hora de garimpo no final do mês. **Olhe contas e resumo, leia pendências, confira os pontos de atenção, decida o que precisa decidir, fecha.** Em OSC bem gerida, o Painel não tem cards com números altos parados ali há semanas — pendência só fica parada quando ninguém olhou.

## Por onde seguir

- **Movimentações** — para registrar novas entradas/saídas ou conferir movimentos do período.
- **Pagamentos e Reembolsos** — para resolver as pendências marcadas nos cards.
- **Projetos** — para acompanhar a saúde e o financeiro das iniciativas da OSC.
- **Relatórios → Atenção** — para ver todos os avisos, não só os últimos 30 dias.
- **Configurações → Relatórios** — para ajustar ou desligar regras de pontos de atenção.
- **Meu Perfil → Notificações** — para receber alerta quando uma pendência sua aparecer (em vez de depender de abrir o sistema).
