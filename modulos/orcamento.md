---
title: "Orçamento"
nav_order: 8
parent: "Módulos"
permalink: /modulos/orcamento/
task: gerir-orcamento-anual
role: [presidente, tesoureiro, gestor-centro-custo]
routes: [/orcamento]
screenshots: [orcamento-elaboracao, orcamento-previsto-realizado, orcamento-reconciliacao]
source_docs: [PRODUCT.md#orcamento]
last_verified: 2026-07-26
status: publicado
---

O módulo de **Orçamento** é onde a OSC monta o seu **orçamento anual** — quanto pretende arrecadar e quanto pretende gastar ao longo do ano, organizado por **centro de custo** e por **categoria** — e depois acompanha, mês a mês, o **previsto contra o realizado**. É a ferramenta que transforma "a gente vai vendo como fica" em "a gente combinou onde queria chegar e sabe, a qualquer momento, se está no caminho".

> Acesse pelo menu **Orçamento**.

> 💡 **Por que isso importa**
>
> A maioria das OSCs sabe quanto gastou — mas só *depois*. O orçamento anual inverte isso: no começo do ano a diretoria decide **onde quer investir** e **quanto cada área pode gastar**, e ao longo dos meses o sistema mostra quem está dentro, quem está apertado e quem já estourou. Sem orçamento, o pedido "podemos gastar mais R$ 2.000 no projeto X?" não tem resposta objetiva. Com orçamento, tem: dá para ver o quanto do previsto para aquele centro de custo já foi consumido, e decidir com número na mão. É planejamento e prestação de contas no mesmo lugar.

## Conceitos essenciais

> 📖 **Conceito · Orçamento é bússola, não cadeado**
>
> O RIT360 Financeiro **alerta, não bloqueia**. Passar do previsto num centro de custo ou categoria não trava lançamentos, não impede pagamentos, não cancela nada. O sistema mostra o sinal (amarelo, vermelho), avisa quem precisa saber e deixa a decisão com as pessoas. A vida da OSC é imprevista — surge uma emergência, um financiador atrasa, um custo dobra. O orçamento serve para você **enxergar** isso cedo e agir, não para ser um muro que atrapalha o trabalho. É bússola, não cadeado. (E não é um ERP: não emite nota, não controla estoque — é planejamento financeiro anual.)

> 📖 **Conceito · Previsto × Realizado**
>
> **Previsto** é o que você planejou no início do ano: "vamos arrecadar R$ 120.000 e gastar R$ 30.000 com o centro de custo Administração". **Realizado** é o que de fato aconteceu, calculado a partir das movimentações registradas. A graça do módulo está em ver os dois lado a lado, a qualquer momento: previsto para o ano, realizado até agora, e o quanto disso já foi consumido em percentual.

> 📖 **Conceito · Baseline (linha de base)**
>
> Quando um orçamento é aprovado, ele vira o **baseline** — a versão "oficial" e congelada contra a qual todo o acompanhamento é feito. Depois de virar baseline, ele não muda sozinho: qualquer alteração passa por uma **revisão** com motivo registrado. Isso garante que o "previsto" que você compara com o realizado é sempre o número que a diretoria de fato aprovou, e não algo editado no meio do caminho sem ninguém saber.

> 📖 **Conceito · Linha de contingência**
>
> Além das receitas e despesas planejadas, cada centro de custo pode ter uma **linha de contingência** — uma reserva para o imprevisto daquela área. É a forma honesta de orçar: em vez de fingir que nada vai sair do script, você separa uma folga explícita. Quando o imprevisto chega, ele consome a contingência (que estava prevista), em vez de estourar o orçamento de surpresa.

## O ciclo do orçamento

O orçamento passa por quatro fases ao longo do ano:

| Fase | O que acontece |
|---|---|
| 📝 **Elaborar** | Montar o orçamento do ano — receitas e despesas previstas por centro de custo e categoria |
| ✅ **Aprovar** | A diretoria aprova; o orçamento vira o **baseline** congelado |
| 📊 **Acompanhar** | Ao longo do ano, comparar o previsto com o realizado e agir sobre os alertas |
| 🔒 **Fechar** | No fim do exercício, reconciliar tudo e **encerrar o ano**, guardando o histórico |

As seções a seguir seguem essa ordem.

## Elaborar o orçamento

[![Elaboração do orçamento anual](/assets/screenshots/orcamento-elaboracao.png)](/assets/screenshots/orcamento-elaboracao.png)
*Elaboração do orçamento anual — receitas e despesas previstas por centro de custo e categoria*

Para montar um orçamento:

1. No menu, abra **Orçamento**.
2. Escolha o **ano** do orçamento (o ano seguinte, tipicamente, montado nos últimos meses do ano corrente).
3. Lance as **receitas previstas** — o que a OSC pretende arrecadar — e as **despesas previstas** — o que pretende gastar — cada linha vinculada a um **centro de custo** e a uma **categoria**.
4. Para cada linha, informe o **valor anual**. O sistema **distribui automaticamente** esse valor pelos 12 meses (divisão igual), e você pode **ajustar mês a mês** quando o gasto não é uniforme — por exemplo, concentrar a despesa de um evento no mês em que ele acontece.
5. Se quiser, adicione a **linha de contingência** de cada centro de custo (a reserva para imprevistos daquela área).
6. Acompanhe, no rodapé, o **resultado previsto** — a diferença entre o total de receitas e o total de despesas previstas, indicando **superávit** (sobra) ou **déficit** (falta) planejado para o ano.

> 💡 **Distribuir por 12 e ajustar depois**
>
> Comece sempre pelo valor anual — é mais fácil pensar "vamos gastar uns R$ 24.000 no ano com o aluguel" do que preencher 12 campos. O sistema divide em R$ 2.000/mês. Só então você ajusta os meses que fogem do padrão: o 13º do funcionário em dezembro, a taxa anual que cai em março, o gasto do evento em setembro. O resto pode ficar na média.

### Gerar automaticamente a partir do histórico

Quando a sua OSC já tem **pelo menos dois anos** de movimentações registradas, o módulo oferece a opção **Gerar automaticamente**: em vez de partir da folha em branco, o RIT360 Financeiro monta um rascunho do orçamento baseado no que a OSC de fato arrecadou e gastou nos anos anteriores, por centro de custo e categoria. Você recebe uma base realista e só ajusta o que mudou — muito mais rápido do que digitar tudo do zero.

> ✓ **Dica · Gere, depois questione linha por linha**
>
> A geração automática é um ótimo ponto de partida, não a palavra final. Ela repete o passado; o seu trabalho é decidir o que muda no ano que vem — o projeto novo que entra, a fonte de recurso que acaba, a economia que você quer fazer. Gere o rascunho, e então percorra cada linha perguntando "isso ainda faz sentido para o ano que vem?".

## Acompanhar: previsto × realizado

[![Acompanhamento previsto contra realizado](/assets/screenshots/orcamento-previsto-realizado.png)](/assets/screenshots/orcamento-previsto-realizado.png)
*Acompanhamento — semáforo de saúde por centro de custo e categoria, previsto contra realizado*

Depois de aprovado, o orçamento vira painel de acompanhamento. Para cada **centro de custo** e cada **categoria**, você vê o previsto para o ano, o realizado até agora e um **semáforo de saúde**:

- 🟢 **Verde** — dentro do previsto, folga confortável.
- 🟡 **Amarelo** — consumo alto, chegando perto do limite (passou de **80%** do previsto).
- 🔴 **Vermelho** — estourou o previsto (passou de **100%**).

O semáforo deixa a diretoria enxergar de relance onde está o aperto, sem abrir linha por linha — e agir a tempo, não no fim do ano.

> 📖 **Conceito · A regra "projeto vence"**
>
> Uma mesma despesa pode pertencer a dois "baldes" ao mesmo tempo: o **centro de custo** (a área da OSC que a executou) e o **projeto** (a iniciativa que a motivou). Para não contar o mesmo gasto duas vezes e não inflar artificialmente o centro de custo, o RIT360 Financeiro aplica a regra **"projeto vence"**: quando um gasto está vinculado a um projeto, ele conta no **orçamento do projeto**, e **não** entra no realizado do centro de custo. Na prática: o dinheiro que a área gastou "por causa de um projeto" aparece na conta do projeto (que tem orçamento próprio), e o centro de custo fica com o que gastou no seu dia a dia comum. Assim cada balde reflete só o que é dele, e a soma não engana.

## Aprovar e revisar

O orçamento tem um ciclo de aprovação parecido com o dos demais fluxos da OSC:

| Status | Significado |
|---|---|
| 📝 **Rascunho** | Em elaboração — livremente editável, ainda não é o baseline |
| 🟡 **Em aprovação** | Enviado; aguardando o voto dos aprovadores elegíveis |
| 🟢 **Aprovado** | Vira o **baseline** congelado; passa a valer para o acompanhamento |

Enquanto está em **rascunho**, você edita à vontade. Ao enviar para **aprovação**, os aprovadores configurados decidem. Uma vez **aprovado**, o orçamento congela como baseline.

### Revisar um orçamento aprovado

A vida muda ao longo do ano, e às vezes o orçamento precisa mudar junto — entrou uma verba nova, um projeto foi cancelado, um custo disparou. Para isso existe a **revisão**:

- Toda revisão **exige um motivo**, que fica registrado na trilha de auditoria. Não dá para mexer no baseline sem dizer por quê.
- Ajustes **pequenos** (abaixo de um limiar configurável pela OSC) são aplicados direto.
- Ajustes **acima do limiar** voltam para **aprovação** — a diretoria precisa concordar de novo antes de o novo número valer.

> 📖 **Conceito · O limiar de revisão**
>
> O **limiar** é o tamanho de mudança que a OSC considera "grande o bastante para precisar de nova aprovação". Ele é configurável (ver [Configurações → Fluxo de Aprovações → aba Orçamento](/configuracoes/aprovacoes/#aba-orcamento)). A ideia: correções pequenas — arredondar uma linha, remanejar R$ 200 entre categorias — não deveriam parar o trabalho de todo mundo esperando aprovação. Já uma mudança grande — cortar 20% do orçamento de uma área, dobrar a previsão de uma despesa — muda o combinado com a diretoria e merece um novo "sim" formal. O limiar é onde a sua OSC traça essa linha.

## Fechar o exercício

[![Reconciliação e encerramento do orçamento](/assets/screenshots/orcamento-reconciliacao.png)](/assets/screenshots/orcamento-reconciliacao.png)
*Reconciliação — planejado, projetos e não alocado, antes de encerrar o exercício*

No fim do ano, o orçamento tem uma visão de **reconciliação** que junta as três origens do que foi realizado:

- **Planejado** — o realizado que caiu nos centros de custo e categorias que você orçou.
- **Projetos** — o realizado que pertence a projetos (lembrando a regra "projeto vence": esse gasto conta aqui, não no centro de custo).
- **Não alocado** — movimentações que aconteceram fora do que foi orçado, sem centro de custo ou categoria previstos.

A reconciliação fecha a conta: mostra que a soma das partes bate com o total de fato movimentado no ano, sem sobra nem furo.

Quando o ano acaba e a prestação de contas está pronta, você usa **Encerrar o exercício**: o orçamento é **congelado** definitivamente e guardado como histórico. Fica disponível para consulta e comparação, mas não é mais editado.

> ⚠️ **Atenção · Encerrar o exercício é definitivo**
>
> Encerrar o ano congela o orçamento como registro histórico — depois disso ele não é mais editável. Faça o encerramento só quando o ano estiver de fato fechado (todas as movimentações registradas, a prestação de contas concluída). Antes disso, mantenha o orçamento aberto para acompanhar e revisar normalmente.

## Relatórios e planilha

O módulo conversa com planilhas e relatórios para caber no fluxo que a sua OSC já usa:

- **Exportar e importar em XLSX** — leve o orçamento para uma planilha (Excel, Google Sheets) para trabalhar offline, discutir com a diretoria ou preparar em conjunto, e depois **importe de volta**. Útil para OSCs que montam o orçamento em reunião, na planilha, antes de oficializar no sistema.
- **Relatório de execução** — um relatório do previsto × realizado do ano, exportável em **PDF** (para anexar à prestação de contas ou enviar a financiadores) e em **Excel** (para análise).
- **Execução por Centro de Custo na prestação de contas** — a prestação de contas da OSC ganhou uma seção **"Execução por Centro de Custo"**, mostrando, para cada área, o previsto, o realizado e o quanto foi consumido. Ver [Relatórios → Exportação](/modulos/relatorios/#exportacao).

## Alertas automáticos

O RIT360 Financeiro avisa **sozinho** quando um centro de custo ou categoria passa dos limites do previsto:

- Ao ultrapassar **80%** do previsto — aviso de que o consumo está alto (semáforo amarelo).
- Ao ultrapassar **100%** do previsto — aviso de que estourou (semáforo vermelho).

Os avisos vão para o **gestor do centro de custo** (quem responde por aquela área) e para o **tesoureiro** (quem cuida do financeiro consolidado) — as duas pessoas que precisam decidir o que fazer. Você não precisa ficar olhando o painel todo dia: o sistema chama a sua atenção quando algo pede atenção.

> 💡 As preferências de canal (e-mail, no app) desses avisos seguem as configurações de notificação de cada pessoa, em [Meu Perfil](/configuracoes/perfil/).

## Quem pode o quê

O acesso ao orçamento acompanha os papéis financeiros da OSC:

| Papel | No orçamento |
|---|---|
| **Presidente** | Elabora, revisa, aprova e encerra — tudo, em todos os centros de custo |
| **Tesoureiro** | Elabora e revisa — tudo, em todos os centros de custo |
| **Gestor de Centro de Custo** | Elabora e acompanha **apenas o(s) seu(s) centro(s) de custo** |
| **Diretor, Comissão Fiscal, Coordenador, Voluntário** | **Veem** o orçamento (dentro do seu nível de acesso ao financeiro), mas não elaboram |

- **Ver** o orçamento é amplo: todos com acesso ao financeiro enxergam o previsto × realizado, cada um dentro do recorte que já têm (o Gestor de Centro de Custo vê o seu CC; os demais, conforme o seu papel).
- **Elaborar e gerenciar** cabe a quem opera o financeiro: Presidente e Tesoureiro no consolidado; o Gestor de Centro de Custo, restrito à sua área.
- **Aprovar** depende da permissão de aprovação de orçamento (`budget.approve`), configurada em [Fluxo de Aprovações → aba Orçamento](/configuracoes/aprovacoes/#aba-orcamento).

Ver [Papéis e Permissões](/papeis/) para o quadro completo.

## Boas práticas

> ✓ **Dica · Monte o orçamento do ano que vem em novembro**
>
> Não deixe para janeiro. Nos últimos meses do ano você já tem quase o ano fechado como base, sabe o que arrecadou e gastou, e consegue projetar o próximo com dados reais. Use **Gerar automaticamente** (se tiver dois anos de histórico), ajuste para o que muda, e leve para a diretoria aprovar antes de o ano começar. Assim janeiro já começa com bússola.

> ✓ **Dica · Contingência de verdade, não zero**
>
> Orçamento sem contingência é orçamento que vai estourar. Toda OSC tem imprevisto — um equipamento que quebra, um custo que sobe, uma oportunidade que aparece. Reserve uma linha de contingência por centro de custo (uma folga de 5% a 10% do previsto costuma ser saudável). É mais honesto orçar a folga do que fingir que ela não existe e depois explicar o "estouro".

> ⚠️ **Atenção · Revisar não é apagar o histórico**
>
> Quando você revisa o orçamento, o motivo fica registrado e o baseline anterior não some — a trilha mostra o que mudou, quando e por quê. Isso protege a OSC: numa auditoria ou prestação de contas, dá para explicar cada ajuste. Não veja a exigência de motivo como burocracia; é o que faz o orçamento ser levado a sério.

## Por onde seguir

- [**Movimentações**](/modulos/movimentacoes/) — de onde vem o "realizado" que o orçamento acompanha.
- [**Projetos**](/modulos/projetos/) — onde os gastos de projeto são orçados e acompanhados (regra "projeto vence").
- [**Relatórios**](/modulos/relatorios/) — o relatório de execução e a prestação de contas com Execução por Centro de Custo.
- [**Configurações → Fluxo de Aprovações → aba Orçamento**](/configuracoes/aprovacoes/#aba-orcamento) — quem aprova, quórum, limiar de revisão e alertas.
- [**Papéis e Permissões**](/papeis/) — quem vê, quem elabora e quem aprova o orçamento.
