---
title: "Fluxo de Aprovações"
nav_order: 6
parent: "Configurações da Organização"
permalink: /configuracoes/aprovacoes/
---

> Disponível para **Presidente (admin)** e **Tesoureiro**.

A página **Fluxo de Aprovações** define **quem pode aprovar** reembolsos e pedidos de pagamento da OSC, e **quantos votos são necessários** para aprovar. Acessada por **Configurações → Fluxo de Aprovações** (a URL é `/configuracoes/aprovacoes`).

[![Configurações — Fluxo de Aprovações](/assets/screenshots/config-workflow.png)](/assets/screenshots/config-workflow.png)
*Configurações — Fluxo de aprovações*

> 💡 **Por que isso importa**
>
> Em OSC sem regra clara de aprovação, ou ninguém aprova nada (e despesas acontecem por inércia, sem controle) ou todo mundo aprova tudo (e a aprovação vira carimbo automático, sem real avaliação). **O fluxo bem configurado** define exatamente quem tem mandato para autorizar saída de dinheiro, quantos precisam concordar, e como o sistema lida com casos atípicos (auto-aprovação, situações onde o solicitante é também aprovador). Isso protege a OSC de gastos não autorizados e protege os aprovadores de questionamento futuro.

A página tem **três abas**: **Pagamentos e Reembolsos** (reembolsos e pedidos de pagamento, com regras próprias mas a mesma lógica), **Projetos** (aprovação de abertura e encerramento de projetos) e **Orçamento** (aprovação e revisão do orçamento anual). As seções abaixo descrevem a aba de Pagamentos e Reembolsos; as abas de Projetos e Orçamento são descritas no fim.

## Aprovações necessárias (quórum)

Define quantos votos positivos são necessários para aprovar:

- **1 voto** — um aprovador elegível decide. Mais ágil; típico de OSC menor ou despesas de menor valor.
- **2 votos** — duas pessoas precisam aprovar. Mais controle; típico de OSC maior ou quando há regra estatutária de aprovação dupla.

> 📖 **Conceito · Quórum 2 e aprovação parcial**
>
> Com quórum 2, depois do primeiro voto positivo, o reembolso ou pedido entra em "Aguardando aprovação parcial" — os outros aprovadores elegíveis recebem notificação de que falta um voto. Quando o segundo voto positivo chega, o status muda para Aprovado. Com o padrão de **1 reprovação para barrar** (ver a seção seguinte), **se um aprova e outro rejeita, prevalece a rejeição** — princípio conservador: na dúvida, não autoriza.

> ℹ️ **Aprovar e reprovar são contas separadas**
>
> "1 voto" ou "2 votos" é o número de aprovações necessárias para **liberar** o pagamento. Quantas **reprovações** são necessárias para **barrar** é um ajuste próprio, logo abaixo — e vem configurado como **1**, o comportamento de sempre.

## Reprovações necessárias para barrar

Define quantas reprovações são necessárias para **encerrar** um pedido de pagamento ou reembolso como reprovado. Você escolhe de **1** até o **número de pessoas aptas a aprovar** na sua organização.

**O padrão é 1** — uma única reprovação barra a solicitação na hora, exatamente como sempre funcionou. Se você não mexer aqui, nada muda.

Quando a organização exige **mais de uma**:

- Enquanto o número exigido **não é alcançado**, a solicitação **continua aguardando aprovação** e as demais pessoas aptas seguem podendo votar — a reprovação isolada não encerra nada.
- As telas do pedido e do reembolso mostram **quantas reprovações já existem e quantas faltam**, do mesmo jeito que já mostram o progresso das aprovações.
- O **solicitante só é avisado no desfecho definitivo**: enquanto a solicitação está viva, ele não recebe aviso de reprovação.
- Se a solicitação chegar a um ponto em que **não há mais como reunir as aprovações necessárias** — porque não restam pessoas suficientes sem voto —, ela é **encerrada como reprovada**, em vez de ficar parada para sempre.
- Quando houver mais de uma reprovação, o **motivo apresentado ao solicitante reúne os motivos de todos os votos contrários**.

> ⚠️ **Atenção · O voto é definitivo**
>
> Aprovar ou reprovar **não pode ser desfeito** — e a tela avisa isso antes de você confirmar, nos dois casos. Se mudar de ideia depois, o caminho é o de sempre: o solicitante corrige e reenvia, e uma nova rodada de votos começa do zero.

> 📖 **Conceito · Por que dar peso à reprovação**
>
> O comportamento de origem — uma reprovação barra tudo — parte de um princípio conservador: liberar dinheiro exige acordo, barrar não precisa de unanimidade. Ele funciona bem na maioria das OSCs, e por isso continua sendo o padrão. Mas em organizações com muitos aprovadores, ou com conselho grande e opiniões divergentes, ele dá a **uma só pessoa** o poder de encerrar sozinha uma solicitação que o restante da diretoria aprovaria. Exigir duas ou três reprovações é a forma de dizer: "para barrar também é preciso acordo". Escolha conforme a sua governança — não existe resposta certa universal.

> ✓ **Dica · Suba junto com o quórum, não isoladamente**
>
> Se a sua OSC exige 1 aprovação, mantenha 1 reprovação: exigir 2 reprovações com quórum 1 cria um desequilíbrio estranho (aprovar é mais fácil que barrar). Faz mais sentido subir os dois lados quando a organização cresce — quórum 2 e 2 reprovações, por exemplo.

## Papéis elegíveis para aprovar

Lista de papéis que podem votar em aprovações. Default: **Presidente** e **Tesoureiro**.

A OSC pode optar por incluir outros papéis (Coordenador de Projeto, por exemplo) ou restringir (apenas Presidente). Depende da governança estatutária e da maturidade operacional.

## Pessoas específicas como aprovadores

Além dos papéis, você pode adicionar **pessoas individuais** como aprovadores — independentemente do papel atual delas. Útil para casos como:

- Conselheiro fiscal que não é tesoureiro mas precisa avaliar despesas
- Membro do comitê de finanças que aprova compras acima de certo valor
- Pessoa em transição entre papéis que precisa manter capacidade de aprovação temporariamente

Você pode indicar como aprovador até um **membro recém-cadastrado que ainda não ativou o acesso** — o nome aparece na lista com a marca **"· acesso pendente"**. Ele passa a *aprovar de fato* apenas depois de concluir o primeiro acesso.

> ✓ **Dica · Use papéis primeiro, exceções como exceções**
>
> A regra de "papéis aprovadores" cobre 95% dos casos da maioria das OSCs. **Pessoas específicas** são o mecanismo de exceção — use com parcimônia. Lista de aprovadores individuais com 8 nomes é sintoma de governança confusa: ou simplifique para papéis bem definidos, ou ajuste papéis no Cadastro de Usuários para cobrir esses casos.

## Gestor de centro de custo como aprovador

Além dos papéis e das pessoas específicas, a OSC pode permitir que o **gestor de um centro de custo** aprove os pagamentos e reembolsos **do próprio centro de custo que ele gerencia**. O ajuste fica no bloco **Quem pode aprovar** e começa **desligado** — cada OSC liga conforme o seu estatuto.

Quando ligado, o gestor **soma-se** aos aprovadores já definidos (papéis + pessoas): ele passa a contar como aprovador elegível **apenas** para os itens do centro de custo sob sua responsabilidade, e **não** altera o número de aprovações exigidas nem os papéis configurados.

> ✓ **Dica · Ligue só se o estatuto delegar ao gestor de CC**
>
> Em OSCs onde só a diretoria eleita autoriza saída de dinheiro (por exemplo, "quaisquer 2 diretores"), mantenha **desligado** — o gestor de CC coordena a área, mas não tem mandato de aprovação. Ligue quando o estatuto (ou a prática combinada) de fato delega ao responsável do centro de custo a autorização das despesas da sua área.

## Quem pode solicitar pedidos de pagamento

[![Bloco "Quem pode solicitar pagamentos", com o link para o editor de cargos](/assets/screenshots/config-aprovacoes-quem-solicita.png)](/assets/screenshots/config-aprovacoes-quem-solicita.png)
*O bloco não lista mais papéis: aponta para a permissão no editor de cargos, e mantém os dois ajustes por escopo*

Quem pode **criar** pedidos de pagamento não é mais definido aqui: é a permissão **Solicitar pedido de pagamento**, no editor de [Cargos e permissões](/configuracoes/cargos/#permissao-solicitar-pedido). **Presidente** e **Tesoureiro** sempre podem, em qualquer organização; a **Comissão Fiscal** nunca pode; qualquer outro cargo — inclusive um que a sua OSC tenha criado — o Presidente libera lá, cargo por cargo.

Nesta página continuam os dois ajustes **por escopo**, que valem **além** da permissão do cargo e servem para um caso diferente: dar a alguém a possibilidade de solicitar, mas **só** para a área que essa pessoa gerencia — mesmo que o cargo dela não tenha a permissão geral.

- **Gestor de centro de custo solicita do próprio centro de custo** — quando ligado, o gestor pode criar pedidos **apenas** do centro de custo que gerencia.
- **Coordenador de projeto solicita do próprio projeto** — quando ligado, o coordenador pode criar pedidos **apenas** dos projetos que coordena.

> ✓ **Nada muda se você não mexer em nada**
>
> Quem já podia solicitar pedido de pagamento — pelo papel ou por um destes dois ajustes — continua podendo. A migração para a permissão por cargo preservou o que já estava configurado; nenhuma organização ficou sem ninguém autorizado a solicitar.

Voluntários não podem criar pedidos de pagamento (só reembolsos), por princípio: pedido de pagamento implica usar dinheiro da OSC, e voluntário sem papel específico não tem mandato para isso.

> 📖 **Conceito · Solicitar por escopo, não em aberto**
>
> Presidente e Tesoureiro respondem pela OSC inteira, então solicitam sem restrição. Já o gestor de centro de custo e o coordenador de projeto respondem por **uma parte** — faz sentido que solicitem despesas **da sua parte**, não de qualquer área. Ao restringir cada um ao seu domínio, o pedido nasce já no lugar certo, e ninguém autoriza gasto fora do que administra. (Isso vale só para **pedidos de pagamento**; reembolso continua aberto a qualquer membro.)

> 📖 **Conceito · Solicitante nunca aprova o próprio pedido**
>
> Independentemente da configuração de papéis aprovadores, o RIT360 Financeiro **bloqueia automaticamente** o solicitante de votar no próprio reembolso ou pedido — a aprovação é gesto de controle externo, faz sentido apenas se alguém **diferente** do solicitante revisa. A exceção é quando o solicitante é o único aprovador elegível (OSC muito pequena); aí o RIT360 Financeiro permite a auto-aprovação mas **marca explicitamente** no audit log como `self_approved` para revisão futura.

## Aprovação de projetos (aba Projetos)

[![Fluxo de aprovação de projetos](/assets/screenshots/manual-config-aprovacoes-projetos.png)](/assets/screenshots/manual-config-aprovacoes-projetos.png)
*Aba Projetos — quem aprova a abertura e o encerramento de projetos*

A aba **Projetos** define **quem pode aprovar a abertura e o encerramento** de um projeto — os dois "portões" do ciclo de vida do módulo de [Projetos](/modulos/projetos/). Diferente de pagamentos e reembolsos, aqui **não há quórum** (a aprovação é de uma pessoa elegível); você define:

- **Papéis elegíveis para aprovar projetos** — default: Presidente e Tesoureiro.
- **Pessoas específicas como aprovadores** — membros individuais, independentemente do papel. Membros **somente leitura** no módulo (Comissão Fiscal, Dirigente) **não podem** ser aprovadores de projeto.
- **Permitir auto-aprovação** — quando ligado, o próprio solicitante pode aprovar a abertura ou o encerramento **apenas se for o único aprovador elegível** da OSC (mesma lógica conservadora dos demais fluxos: a auto-aprovação fica registrada na auditoria).

> 💡 **Por que isso importa**
>
> Os dois portões dão governança ao projeto sem engessar o dia a dia: aprovar a **abertura** é a diretoria concordando com o escopo e o orçamento; aprovar o **encerramento** é reconhecer que o projeto acabou, com aquele resultado e aquela prestação de contas. Entre os dois, a equipe trabalha com autonomia.

## Aprovação de orçamento (aba Orçamento) {#aba-orcamento}

[![Fluxo de aprovação de orçamento](/assets/screenshots/orcamento-config-aprovacao.png)](/assets/screenshots/orcamento-config-aprovacao.png)
*Aba Orçamento — quem aprova, quórum, limiar de revisão e alertas*

A aba **Orçamento** define as regras de governança do [orçamento anual](/modulos/orcamento/) da OSC:

- **Papéis e pessoas elegíveis para aprovar** — quem pode dar o "sim" a um orçamento enviado para aprovação e às revisões que voltam para aprovação. É a permissão `budget.approve`. Default: Presidente e Tesoureiro. Você pode adicionar pessoas individuais, como nos demais fluxos.
- **Quórum** — quantos votos positivos são necessários para aprovar (1 ou 2), mesma lógica de aprovação parcial da aba de Pagamentos e Reembolsos.
- **Permitir auto-aprovação** — quando ligado, quem enviou o orçamento pode aprová-lo **apenas se for o único aprovador elegível** da OSC (mesma lógica conservadora dos demais fluxos: a auto-aprovação fica registrada na auditoria como `self_approved`).
- **Limiar de revisão** — o tamanho de mudança a partir do qual uma revisão do orçamento aprovado **volta para aprovação** em vez de ser aplicada direto. Ajustes abaixo do limiar entram na hora; acima dele, exigem novo "sim" da diretoria. Toda revisão, grande ou pequena, exige um **motivo** registrado na auditoria.
- **Alertas de execução** — a partir de quais percentuais do previsto o sistema avisa (padrão: **80%** e **100%**) e para quem (gestor do centro de custo e tesoureiro).

> 💡 **Por que isso importa**
>
> O orçamento só é levado a sério se mudá-lo tiver um custo proporcional ao tamanho da mudança. Sem limiar, ou toda correção de centavo trava esperando aprovação (e ninguém usa), ou qualquer um reescreve o orçamento sem controle (e o "previsto" perde o sentido). O limiar é onde a sua OSC diz: "correção pequena segue; mudança grande precisa a diretoria concordar de novo". Combinado com o motivo obrigatório em toda revisão, isso mantém o baseline confiável para a prestação de contas.

> ✓ **Dica · Calibre o limiar pelo porte da OSC**
>
> Numa OSC pequena, um limiar em valor absoluto baixo faz quase toda revisão voltar para aprovação — vira fricção. Numa OSC grande, um limiar alto deixa passar mudanças relevantes sem revisão. Ajuste ao seu porte: o limiar deve capturar "mudanças que mexem no combinado com a diretoria", não cada pequeno remanejamento entre categorias.

## Boas práticas

> ✓ **Dica · Comece simples, complique conforme cresce**
>
> OSC com 5 pessoas: quórum 1, Presidente + Tesoureiro como aprovadores. Decisão rápida, controle suficiente para o porte. Quando a OSC crescer para 20+ pessoas ou começar a movimentar valores maiores, então sim subir para quórum 2 e ampliar a lista de aprovadores. Quórum 2 numa OSC de 5 pessoas vira fricção sem ganho real de controle.

> ⚠️ **Atenção · Mudanças aqui se aplicam a partir de agora, não retroativamente**
>
> Reembolsos e pedidos **já aprovados** ficam como estavam. A nova configuração só afeta solicitações futuras. Se você quer alterar uma aprovação passada (ex: para revisar uma autorização questionável), use o mecanismo de **estorno** em Movimentações para reverter o lançamento financeiro correspondente, sem mexer no histórico de aprovações.

## Por onde seguir

- **Configurações → Usuários** — onde os papéis são atribuídos aos membros.
- **Reembolsos** e **Pedidos de Pagamento** — onde o fluxo configurado aqui é aplicado.
- **Projetos** — onde a aprovação de abertura e encerramento configurada na aba Projetos é aplicada.
- **[Orçamento](/modulos/orcamento/)** — onde a aprovação, o limiar de revisão e os alertas configurados na aba Orçamento são aplicados.
- **Papéis e Permissões** — para visão geral de quem pode fazer o quê.
