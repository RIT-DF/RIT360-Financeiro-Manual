---
title: "Painel"
nav_order: 1
parent: "Módulos"
permalink: /modulos/painel/
---

A **tela inicial** é a primeira coisa que você vê após o login, e responde três perguntas separadas, em três abas: **Painel** (o que urge hoje), **Saúde 360** (como a OSC está) e **Previsão** (para onde ela vai). As três dividem o mesmo cabeçalho e o mesmo selo de pontos de atenção — você troca de aba sem perder o contexto.

[![Painel](/assets/screenshots/painel-visao-geral.png)](/assets/screenshots/painel-visao-geral.png)
*Aba Painel — contas e resumo do mês, fluxo de caixa, pendências e pontos de atenção*

> 💡 **Por que isso importa**
>
> A maioria das ferramentas financeiras te despeja em uma lista enorme de lançamentos no login. A tela inicial inverte isso: **mostra primeiro o que importa para você decidir o próximo passo**, e separa três tipos de pergunta que normalmente ficam misturados — o que precisa de ação agora (Painel), se a organização está saudável (Saúde 360) e o que vem pela frente (Previsão). Tesoureiro vê quantos reembolsos esperam pagamento; presidente vê pedidos aguardando aprovação; voluntário vê seus próprios reembolsos pendentes. Resultado: você gasta menos tempo procurando informação, mais tempo decidindo.

## As três abas

- **[Painel](#aba-painel)** — a aba padrão ao entrar. O que precisa da sua atenção hoje: saldo das contas, resumo do mês, pendências por papel e pontos de atenção recentes.
- **[Saúde 360](#saude-360)** — quatro respostas sobre a saúde financeira da OSC: quanto está livre para usar, quanto já está comprometido, por quanto tempo o caixa aguenta, e quais projetos estão fora do ritmo.
- **[Previsão](#previsao)** — a projeção de saldo dos próximos meses, com os mesmos filtros de Relatórios (tipo, projeto, conta, categoria, centro de custo).

Quando existe algum aviso **grave** em aberto, um selo no topo da tela mostra quantos são, em qualquer uma das três abas. Clicar nesse selo leva direto ao bloco de Pontos de atenção, na aba Painel.

## Aba Painel

De cima para baixo, a aba Painel tem quatro blocos:

1. **Contas** e **Este mês** — uma linha por conta com o saldo, e o líquido no rodapé; ao lado, o resumo de receitas, despesas e resultado do mês.
2. **Fluxo de caixa** — gráfico com os últimos 6 meses, comparando receitas e despesas.
3. **Pendências** — três colunas lado a lado: **Pedidos de Compra e Pagamento**, **Reembolsos** e **Projetos**, cada uma com o que está pendente para o seu papel.
4. **Pontos de atenção** — avisos sobre o que saiu do padrão recentemente (ver seção própria abaixo).

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
>
> O saldo por conta também **não conta pagamento marcado para uma data futura** — um lançamento com data de pagamento em, digamos, três dias, só entra no saldo quando essa data chegar. A regra vale igual aqui, em Movimentações, no formulário de novo lançamento e em Configurações › Contas: os quatro lugares mostram o mesmo número para hoje.

> ⚠️ **Atenção · Ver o saldo é uma permissão à parte**
>
> Se o seu cargo não tem a permissão **Ver saldo das contas**, este bloco continua aparecendo, mas no lugar do valor você lê uma frase avisando que não tem permissão para ver o saldo, e a quem pedir. A regra vale igualmente em Movimentações, no formulário de novo lançamento, em Configurações → Contas Bancárias e na aba Saúde 360. Quem administra a organização ajusta isso em [Cargos e permissões](/configuracoes/cargos/#permissao-ver-saldo).

### Este mês

O card **Este mês** mostra o **resultado do que já aconteceu de fato** — receitas recebidas menos despesas pagas, pela data do pagamento. Não é mais uma mistura de realizado com previsto: se uma despesa deste mês ainda não foi paga, ela **não entra** no resultado; se uma receita esperada ainda não caiu na conta, ela também fica de fora.

O que venceu e ainda não foi resolvido não some da tela — aparece **à parte**, logo abaixo do resultado, com as duas pontas separadas: quanto **venceu e não foi pago** e quanto **venceu e não foi recebido**. Antes da v1.80.1 os dois números viravam um só, somando coisas opostas (uma despesa em aberto e uma receita em aberto se cancelavam parcialmente no mesmo total); agora cada ponta aparece com o próprio valor.

> 💡 **Por que isso importa**
>
> Um resultado que mistura o que já aconteceu com o que só está previsto engana: uma conta de luz que ainda não venceu não deveria "piorar" o resultado do mês antes da hora, e uma doação só prometida não deveria "melhorá-lo" antes de cair na conta. Separando realizado de pendente, o card responde exatamente "como fechou o mês até agora" — e a informação sobre o que está atrasado continua visível, só que sem embaralhar com o resultado.

> ℹ️ **Observação**
>
> Ficam **fora** da conta os lançamentos **cancelados** e o **par de estorno**: quando um lançamento é estornado, o sistema cria um lançamento contrário para anulá-lo — os dois somam zero e nenhum dos dois entra no resumo. São valores que não representam dinheiro que entrou ou saiu de fato.

## Bloco 2 · Fluxo de caixa

Logo abaixo do primeiro bloco, um gráfico mostra os **últimos 6 meses** de movimentação, comparando o total de receitas e de despesas mês a mês. É a leitura rápida de tendência: a OSC está entrando numa fase de aperto ou de folga? As despesas estão subindo mais rápido que as receitas?

## Bloco 3 · Pendências

Três colunas lado a lado — **Pedidos de Compra e Pagamento**, **Reembolsos** e **Projetos** — cada uma em um card com suas pendências como linhas clicáveis. O que aparece depende do seu papel — você só vê pendências relacionadas ao que pode resolver. Clicar em uma linha leva direto à lista já filtrada pelo status correspondente.

### Pedidos de Compra e Pagamento

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

Fechando a aba Painel, o bloco de **Pontos de atenção** mostra o que saiu do padrão, considerando os **últimos 30 dias** — não o período que você escolheria em Relatórios, mas uma janela curta e fixa, pensada para "o que aconteceu recentemente que merece uma olhada". Esses avisos moram só aqui: Relatórios não tem mais uma aba própria para eles (ver [Relatórios](/modulos/relatorios/)).

O bloco mostra até **quatro avisos**. Havendo mais, um link **Ver todos** abre a lista inteira **na própria tela**, sem levar para outro módulo. Cada aviso é clicável e leva direto ao que ele aponta — o lançamento, a categoria, o fornecedor.

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
> O déficit projetado **só aparece aqui**, no bloco de Pontos de atenção do Painel — não é repetido em nenhum outro lugar. Para a projeção completa mês a mês, com todos os filtros, use a [aba Previsão](#previsao), logo ao lado do Painel.

A regra vem **ligada por padrão**, com antecedência de **6 meses** (configurável para 3, 6 ou 12), em **Configurações → Relatórios → Regras de pontos de atenção** — junto com as demais regras (ver [Configuração das regras de atenção](/modulos/relatorios/#configuracao-das-regras-de-atencao)).

No rodapé do bloco de Pontos de atenção, um link indica onde ajustar as regras — visível só para quem tem permissão de mexer nelas.

> ✓ **Dica · Use o Painel como rotina de manhã**
>
> 5 minutos no Painel todo dia (ou toda segunda de manhã) substituem 1 hora de garimpo no final do mês. **Olhe contas e resumo, leia pendências, confira os pontos de atenção, decida o que precisa decidir, fecha.** Em OSC bem gerida, o Painel não tem cards com números altos parados ali há semanas — pendência só fica parada quando ninguém olhou.

## Saúde 360

[![Aba Saúde 360, com os quatro blocos: disponível, comprometido, fôlego de caixa e projetos fora do ritmo](/assets/screenshots/painel-saude360.png)](/assets/screenshots/painel-saude360.png)
*Aba Saúde 360 — quanto está livre, quanto está comprometido, por quanto tempo o caixa aguenta, e os projetos fora do ritmo*

Enquanto o Painel responde "o que precisa de mim hoje", a **Saúde 360** responde "como a OSC está, de forma geral" — quatro blocos, cada um com uma pergunta central:

### Quanto está livre para usar

Separa o **disponível** (uso livre) do **restrito** (carimbado para um destino específico — uma emenda, um convênio, uma conta de uso restrito) e do **passivo** (o que está no cartão de crédito, a pagar). É a resposta para "posso gastar isso, ou já tem dono?" — gastar do carimbado como se fosse livre é o erro mais caro que uma OSC comete com verba de projeto.

Sem a permissão **Ver saldo das contas** (ver [Cargos e permissões](/configuracoes/cargos/#permissao-ver-saldo)), este bloco some do jeito costumeiro dos valores e mostra a frase de permissão negada no lugar dos números.

### Quanto já está comprometido e ainda não saiu

Soma o que a organização **já deve**: pedidos de compra e pagamento aprovados aguardando pagamento, reembolsos aprovados aguardando pagamento, e despesas previstas em aberto. É dinheiro que, mesmo ainda no caixa, já tem destino — contar com ele para outra coisa é o caminho mais curto para um aperto de caixa surpresa.

### Por quanto tempo o caixa aguenta

Projeta quantos meses faltam até o saldo projetado ficar negativo, considerando o que já está agendado e, quando necessário, a média dos meses anteriores — o mesmo cálculo por trás do [aviso de déficit projetado](#novo-aviso-deficit-projetado-no-fluxo-de-caixa) do Painel, aqui apresentado como resposta direta em vez de alerta.

### Se algum projeto está fora do ritmo

Lista os projetos que estão **fora do ritmo esperado** entre prazo e orçamento — tanto os que gastam ou atrasam além do ritmo quanto os que estão com **prazo e dinheiro sobrando** (execução murcha, não só estouro). Cada projeto fora do ritmo mostra o motivo em uma frase, sem precisar abrir o projeto para entender.

> 💡 **Por que isso importa**
>
> "Prazo e dinheiro sobrando" parece bom à primeira vista, mas costuma ser sintoma de projeto **parado** — verba captada e não executada, prazo que passou sem que ninguém tenha dado falta. A Saúde 360 trata isso como ponto de atenção, não como conquista, porque financiador cobra execução, não sobra.

## Previsão

[![Aba Previsão, com filtros, escolha de horizonte e a tabela de meses projetados](/assets/screenshots/painel-previsao.png)](/assets/screenshots/painel-previsao.png)
*Aba Previsão — saldo projetado mês a mês, com receita e despesa estimada ou já agendada*

A **Previsão** projeta o saldo dos próximos meses, mês a mês, com um gráfico e uma tabela mostrando receita e despesa projetadas (marcadas como **Estimado** quando vêm de média histórica, ou **Agendado** quando já existe um lançamento futuro real por trás do número).

- **Horizonte** — 3, 6 ou 12 meses. Horizontes maiores exigem mais histórico de movimentação da OSC para liberar; sem histórico suficiente, a projeção soma só o que já está agendado e avisa que é isso que está mostrando, em vez de aparecer vazia.
- **Filtros** — Tipo, Projeto, Conta, Categoria e Centro de custo, os mesmos filtros que Relatórios usa. Dá para projetar o caixa de um projeto específico, não só o consolidado da OSC.

> ⚠️ **Atenção · Confie mais em horizontes curtos**
>
> Quanto mais distante o mês projetado, mais a previsão depende de média histórica em vez de compromisso real já agendado — e mais ela erra. O aviso "Projeção baseada em histórico parcial" aparece quando a OSC ainda não tem meses suficientes de dados para o horizonte escolhido; nesse caso, prefira um horizonte menor ou leia o número como estimativa grosseira, não como compromisso.

## Por onde seguir

- **Movimentações** — para registrar novas entradas/saídas ou conferir movimentos do período.
- **Pagamentos e Reembolsos** — para resolver as pendências marcadas nos cards.
- **Projetos** — para acompanhar a saúde e o financeiro das iniciativas da OSC.
- **Relatórios** — para a análise completa do período, com todos os filtros.
- **Configurações → Relatórios** — para ajustar ou desligar regras de pontos de atenção.
- **Meu Perfil → Notificações** — para receber alerta quando uma pendência sua aparecer (em vez de depender de abrir o sistema).
