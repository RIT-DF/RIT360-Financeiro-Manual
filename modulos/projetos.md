---
title: "Projetos"
nav_order: 6
parent: "Módulos"
permalink: /modulos/projetos/
---

O módulo de **Projetos** é onde a OSC planeja, executa, acompanha e encerra suas iniciativas — um evento, uma obra, uma campanha, um edital, um serviço continuado. Cada projeto reúne, num só lugar, o **planejamento** (escopo, equipe, orçamento, marcos, riscos), a **execução** (tarefas, comunicação, evidências), o **financeiro vinculado** (despesas, receitas, pedidos e reembolsos do projeto) e o **encerramento** (avaliação, lições aprendidas e relatório final).

> 💡 **Por que isso importa**
>
> OSC séria não trata "todo dinheiro como uma coisa só". Cada projeto tem orçamento próprio, um financiador que vai pedir prestação de contas específica, uma equipe responsável e um prazo. Misturar tudo no caixa geral cria dois problemas: (1) **a prestação de contas vira pesadelo**, porque você precisa recortar depois o que foi do projeto e o que não foi; e (2) **a decisão fica cega**, porque você não sabe se o projeto está dentro do orçamento e no prazo até o último mês. O módulo de Projetos resolve isso: você vincula cada despesa, tarefa e marco ao projeto desde o começo, e o sistema te mostra a qualquer momento como ele está de saúde.

## O que é gerir projetos numa OSC

Boa parte do trabalho de uma OSC acontece em **iniciativas com começo, meio e fim**: o acampamento de inverno, a reforma da sede, a campanha do agasalho, o projeto aprovado num edital de cultura. Cada uma dessas iniciativas é um **projeto** — tem um objetivo, um prazo, um dinheiro reservado e pessoas responsáveis.

Gerir um projeto é responder, ao longo do caminho, a três perguntas simples:

- **Vamos conseguir entregar o que prometemos?** (escopo e marcos)
- **O dinheiro vai dar?** (orçamento × gasto real)
- **O que pode dar errado e o que já estamos fazendo a respeito?** (riscos)

Quem responde a essas perguntas *no fim do projeto* já chegou tarde. Quem responde *durante* consegue corrigir a rota — pedir mais prazo, remanejar orçamento, acionar um plano B. É exatamente para isso que serve este módulo.

> 📖 **Conceito · Projeto × caixa geral da OSC**
>
> O financeiro do projeto **não é uma caixinha separada do banco**. O dinheiro continua sendo o da OSC, nas mesmas contas. O que o projeto faz é **rotular** as movimentações: "esta despesa de R$ 300 em material foi do Acampamento". Assim você vê o recorte do projeto sem deixar de ver o todo.

## O modelo de gestão de projetos do RIT360 Financeiro

O RIT360 Financeiro organiza cada projeto em torno de um **ciclo de vida** e de **três fases de trabalho**. Você não precisa preencher tudo — comece pelo essencial e detalhe conforme o projeto avança.

### O ciclo de vida

Todo projeto caminha por uma sequência de status, com aprovações nos momentos-chave:

| Status | O que significa |
|---|---|
| **Em planejamento** | A equipe está montando escopo, equipe e orçamento. |
| **Aguardando aprovação inicial** | O coordenador pediu autorização para iniciar; falta a aprovação da OSC. |
| **Em execução** | Aprovado e rodando. É aqui que as tarefas andam e o dinheiro se movimenta. |
| **Aguardando encerramento** | A execução terminou; falta a avaliação final e a aprovação do encerramento. |
| **Concluído** | Encerrado e avaliado. Fica como histórico e prestação de contas. |
| **Pausado** | Temporariamente parado (sem cancelar). Os lembretes e cobranças congelam. |
| **Cancelado** | Encerrado sem conclusão (o projeto não vai mais acontecer). |

> 📖 **Conceito · Por que pedir aprovação para iniciar e para encerrar**
>
> Os dois "portões" de aprovação (iniciar e encerrar) existem para dar **governança** sem burocratizar o resto. Aprovar a abertura significa: "a diretoria concorda com este escopo e este orçamento". Aprovar o encerramento significa: "a diretoria reconhece que este projeto acabou, com este resultado e esta prestação de contas". Entre os dois portões, a equipe trabalha com autonomia. Quem aprova é configurável pela OSC, como nos demais fluxos.

### Quem aprova, e o que fazer se não houver ninguém
{: #quem-aprova-e-o-que-fazer-se-nao-houver-ninguem }

Quem pode aprovar a abertura e o encerramento de um projeto é definido pela organização em **Configurações → Fluxo de Aprovações → aba Projetos** — por papel (Presidente e Tesoureiro, por padrão) ou por pessoas específicas. Ver [Fluxo de Aprovações → Aprovação de projetos](/configuracoes/aprovacoes/#aprovacao-de-projetos-aba-projetos).

Ao **solicitar aprovação** (na abertura) ou **solicitar encerramento**, a tela do projeto passa a mostrar **quem está apto a aprovar**. Se você for uma dessas pessoas, a tela avisa e traz o botão de aprovar ali mesmo — não é preciso perguntar à diretoria quem decide, nem procurar em outro lugar.

[![Projeto "Aguardando aprovação inicial", com o aviso "Você aprova este projeto" e o botão Aprovar abertura em destaque](/assets/screenshots/manual-projetos-aguardando-aprovacao-inicial-desktop.png)](/assets/screenshots/manual-projetos-aguardando-aprovacao-inicial-desktop.png)
*Projeto aguardando aprovação inicial — quem pode aprovar vê o botão em destaque*

[![O mesmo aviso no celular](/assets/screenshots/manual-projetos-aguardando-aprovacao-inicial-mobile.png)](/assets/screenshots/manual-projetos-aguardando-aprovacao-inicial-mobile.png)
*O mesmo aviso, no celular*

> ⚠️ **Atenção · Quem propõe, normalmente, não aprova**
>
> A regra geral é que quem solicita a abertura ou o encerramento **não é quem aprova** — é a segunda pessoa conferindo que dá valor à aprovação. A exceção é a OSC com **uma única pessoa habilitada** a aprovar: nesse caso, ela pode aprovar o próprio projeto, porque impedir isso travaria o projeto indefinidamente. Havendo mais de uma pessoa apta, a regra de quatro olhos volta a valer — mesmo que a organização tenha ligado o ajuste **"Permitir auto-aprovação"** em Configurações → Fluxo de Aprovações (ver [Fluxo de Aprovações](/configuracoes/aprovacoes/#aprovacao-de-projetos-aba-projetos)).
>
> Ao **solicitar aprovação** sendo você a única pessoa habilitada, o sistema mostra uma confirmação avisando disso antes de concluir — para você já saber, na hora de enviar, que a aprovação vai cair na sua própria mão.

> ⚠️ **Atenção · Se ninguém puder aprovar**
>
> Pode acontecer de a organização ficar **sem nenhuma pessoa habilitada** a aprovar projetos — por exemplo, quando a única pessoa indicada teve o vínculo com a OSC encerrado. Nesse caso, a tela do projeto avisa que é uma situação a resolver e leva direto para **Configurações → Fluxo de Aprovações**, para que alguém com acesso a essa página indique um aprovador. Sem isso, o projeto fica parado em "Aguardando aprovação" sem ninguém conseguir liberá-lo.

> ✓ **Dica · OSC pequena, indique um segundo aprovador**
>
> Se a sua organização tem só uma pessoa na administração, vale conferir em **Configurações → Fluxo de Aprovações → aba Projetos** quem está indicado como aprovador de projetos. Ter **uma segunda pessoa** — mesmo que raramente precise aprovar — mantém a conferência de quatro olhos, que é o motivo de a aprovação existir. Foi exatamente a falta dessa segunda pessoa, numa OSC onde a presidente era a única aprovadora possível, que deixou um projeto esperando uma aprovação que só ela mesma podia dar.

### As três fases de trabalho

Dentro do projeto, o trabalho se organiza em abas que correspondem às fases:

1. **Planejamento** — o que vamos fazer, com quem, com quanto e com quais riscos.
2. **Execução** — fazer acontecer: tarefas, comunicação da equipe, evidências do que foi feito.
3. **Encerramento** — avaliar o resultado, registrar o que aprendemos e gerar o relatório final.

Há ainda uma aba de **Resumo** (a visão de uma página do projeto), uma de **Financeiro** (o dinheiro do projeto) e uma de **Relatório** (os números do projeto nos relatórios da OSC).

### A saúde do projeto

A cada projeto o RIT360 Financeiro atribui um **indicador de saúde** — um semáforo (🟢 Saudável, 🟡 Atenção, 🔴 Crítico) com uma pontuação de 0 a 100. Ele combina três sinais:

- **Prazo** — o projeto está dentro da janela prevista?
- **Orçamento** — o gasto está dentro do que foi previsto?
- **Riscos** — há riscos materializados ou sem tratamento?

> 💡 **Por que isso importa**
>
> O semáforo é o que transforma "uma porção de projetos" em **gestão de portfólio**. No Painel, a diretoria vê de relance quantos projetos estão saudáveis e quais pedem atenção — sem abrir um por um. É a diferença entre descobrir que um projeto estourou o orçamento *no dia da prestação de contas* e descobrir *a tempo de fazer algo*.

## Conceitos essenciais
{: #conceitos-essenciais }

> 📖 **Conceito · Tipo do projeto**
>
> Ao criar, você escolhe o **tipo**: Evento, Obra, Campanha, Produto/Serviço, Programa, ou "Começar do zero" (sem modelo, você monta tudo). O tipo adapta a experiência: um **Evento** ganha campo de número de participantes e a **calculadora de taxa de inscrição**; cada tipo (exceto "Começar do zero") já vem com uma sugestão de **marcos-modelo** e de **riscos típicos** — uma Obra sugere marcos como "Início da execução / Conclusão da obra / Vistoria"; um Evento sugere "Divulgação / Evento realizado / Prestação de contas"; um **Programa** sugere "Plano do programa aprovado / Início do atendimento / Primeira avaliação de metas / Relatório do período", com riscos como demanda acima da capacidade de atendimento, interrupção do financiamento e rotatividade de equipe. Você usa as sugestões que quiser e adiciona as suas.
>
> **Programa** é o tipo certo para uma linha de atendimento ou serviço **que se repete**, com metas e público definido — um programa de passagens para pacientes, uma cesta básica mensal, um atendimento continuado. Ele se distingue dos demais pela natureza do trabalho: um **Evento** tem data marcada e acaba nela; uma **Obra** entrega algo físico e acaba quando a entrega é feita; uma **Campanha** é um esforço pontual de arrecadação ou mobilização; já um **Programa** é uma atividade contínua, sem um único marco de "pronto" — o que ele tem, como todo projeto, é um **período** (início e fim) dentro do qual ele roda.
>
> ⚠️ **Não existe projeto sem data de término — nem para um Programa de longa duração.** Todo projeto no RIT360 Financeiro tem início e fim, porque é o período que baliza o orçamento, as metas e a prestação de contas do exercício. Se o seu programa é para durar anos, isso não é problema: coloque uma **data de término distante**, compatível com o horizonte real do programa (por exemplo, o fim do exercício seguinte, ou a data prevista de revisão do plano). Quando o período terminar e o programa continuar, você **edita as datas** (ver "Editar o projeto após a criação" abaixo) e segue — não precisa recriar o projeto nem perder o histórico.

> 📖 **Conceito · Papel no projeto**
>
> Dentro de um projeto, cada pessoa tem um **papel no projeto**, que é diferente do papel dela na OSC. Quem conduz é o **Coordenador do projeto** — pode editar escopo, equipe, marcos e riscos, gerenciar tarefas e solicitar despesas. Demais integrantes **contribuem** (assumem tarefas, comentam, anexam evidências) mas não mudam o planejamento. Um voluntário comum da OSC pode ser coordenador de um projeto específico; um tesoureiro pode ser só integrante de outro. O acesso ao projeto respeita esse papel.

## A lista de projetos

[![Lista de projetos em desktop](/assets/screenshots/manual-projetos-01-lista.png)](/assets/screenshots/manual-projetos-01-lista.png)
*Lista de projetos em desktop — cada linha mostra tipo, status, saúde e período*

> 🎥 **Vídeo tutorial · Criei um projeto: quem aprova?**
>
> Esta tela tem um vídeo curto (sem áudio, com legendas) mostrando o caminho de um projeto até ficar aprovado — clique no ícone de vídeo, no canto direito do cabeçalho. Veja todos os vídeos disponíveis em [Vídeos tutoriais dentro do app](/primeiros-passos/#videos-tutoriais).

A tela **Projetos** lista as iniciativas da OSC. No **computador** (telas a partir de 1024 px), a lista é uma **tabela** com as colunas **Nome**, **Tipo**, **Status**, **Saúde** (o semáforo + pontuação) e **Período**. No **celular**, a mesma informação vira **cards** verticais. Clique em qualquer projeto para abrir o detalhe.

No topo você tem **busca por nome** e filtros por **Status**, **Tipo** e **Saúde** — úteis para, por exemplo, ver só os projetos em execução que estão em atenção.

O botão **Novo projeto** abre um **assistente de 3 passos** (tipo e identidade · período · financeiro essencial), com textos de ajuda em cada etapa e o aviso de que você ficará registrado como coordenador do projeto. Para um Evento, o assistente pede o número estimado de participantes; o texto se adapta ao tipo escolhido. Convidar outras pessoas para a equipe é feito depois, já com o projeto criado (ver "Equipe" na aba Planejamento). No último passo, o botão **Criar projeto** conclui — e o projeto nasce **Em planejamento**, ainda ajustável antes de você pedir a aprovação de abertura.

### Sair no meio do cadastro não perde o preenchimento
{: #rascunho-do-cadastro-de-projeto }

[![Aviso "Rascunho recuperado do seu dispositivo", com o botão Descartar, e o assistente restaurado no passo 2 de 3](/assets/screenshots/manual-projetos-rascunho-recuperado-desktop.png)](/assets/screenshots/manual-projetos-rascunho-recuperado-desktop.png)
*Reabrindo "Novo projeto" depois de sair no meio do passo 2 — o rascunho volta de onde parou*

[![O mesmo aviso no celular](/assets/screenshots/manual-projetos-rascunho-recuperado-mobile.png)](/assets/screenshots/manual-projetos-rascunho-recuperado-mobile.png)
*O mesmo aviso, no celular*

> 💡 **Por que isso importa**
>
> Preencher escopo, período e orçamento essencial de um projeto novo leva alguns minutos, e é comum ser interrompido no meio — uma ligação, uma reunião, o celular que trava no seletor de arquivo. Antes, fechar a aba nesse momento significava perder tudo e começar de novo. Agora não perde.

Enquanto você preenche o assistente de **Novo projeto**, o RIT360 Financeiro salva um **rascunho automaticamente no seu dispositivo** — sem precisar clicar em nada para isso acontecer. Se você fechar a aba, recarregar a página ou o navegador cair no meio do preenchimento, ao voltar em **Projetos → Novo projeto** o assistente **restaura os campos e o passo em que você estava**, com um aviso no topo: *"Rascunho recuperado do seu dispositivo. Continue de onde parou."*

- **O rascunho é só seu, e só naquele aparelho.** Ele fica guardado no navegador do dispositivo onde você estava digitando — não vai para o servidor, não aparece para outra pessoa da equipe, e não existe se você abrir o assistente num computador ou celular diferente.
- **Descartar** — o aviso de rascunho recuperado tem um botão para isso: começa o assistente do zero, limpo, sem o que estava preenchido antes.
- **O rascunho some quando o projeto é criado** — ao concluir o assistente com sucesso, o rascunho local é apagado; ele não fica sobrando para reaparecer num próximo projeto novo.

> ✓ **Dica · O rascunho não substitui salvar de vez em quando em telas longas**
>
> Fora do assistente de projeto, o mesmo mecanismo guarda rascunho local em outros formulários longos do RIT360 Financeiro (novo lançamento, reembolso, pedido de pagamento). Ele é uma rede de segurança contra fechamento acidental — não um lugar para deixar um cadastro pela metade por dias; prefira concluir ou descartar.

## Arquivar e desarquivar um projeto
{: #arquivar-projeto }

[![Lista de projetos com o contador de arquivados e o atalho para vê-los](/assets/screenshots/manual-projetos-11-arquivados-contador.png)](/assets/screenshots/manual-projetos-11-arquivados-contador.png)
*A lista de projetos esconde os arquivados por padrão — um contador diz quantos estão escondidos, com atalho para vê-los*

> 💡 **Por que isso importa**
>
> Toda OSC acumula projetos concluídos ou cancelados há anos, e eles não deixam de existir — continuam valendo para o fechamento do exercício, para relatórios e para o histórico. O problema é a **lista do dia a dia**: depois de alguns anos, ela vira uma rolagem enorme de coisa que já acabou, e achar o projeto que está rodando agora fica mais difícil a cada mês. **Arquivar** resolve isso sem apagar nada — tira o projeto do caminho de quem trabalha hoje, sem tirá-lo da história da organização.

> 📖 **Conceito · Arquivar não é um status do projeto**
>
> Arquivado **não entra** no ciclo de vida (Em planejamento → Em execução → Concluído, etc. — ver acima). É uma marcação **à parte**, que existe **por cima** de qualquer status. Um projeto Concluído pode estar arquivado ou não; um projeto ainda Em execução também pode ser arquivado, se a OSC decidir tirá-lo da vista por algum motivo. Desarquivar devolve o projeto **exatamente como estava** — o status que ele tinha antes de ser arquivado não muda em nada.

### Como arquivar

Cada projeto da lista tem um botão de **Arquivar** (individual). Se o projeto ainda está **ativo** — em planejamento, aguardando aprovação, em execução, aguardando encerramento ou pausado —, a confirmação avisa disso antes de deixar seguir, porque arquivar um projeto em andamento tira as pessoas dele do radar.

> ⚠️ **Atenção · Arquivar um projeto ativo não pausa nem cancela o trabalho**
>
> O projeto continua no status em que estava — só some das telas que listam "o que está acontecendo agora". Se a intenção é **parar** o projeto temporariamente, use **Pausar** no ciclo de vida (ver acima), não Arquivar. Se a intenção é **encerrar sem concluir**, use **Cancelar**. Arquivar é sobre visibilidade; Pausar e Cancelar são sobre o andamento do próprio projeto.

### Arquivar vários de uma vez

[![Seleção múltipla na lista de projetos com a barra de ações em lote](/assets/screenshots/manual-projetos-12-arquivar-lote.png)](/assets/screenshots/manual-projetos-12-arquivar-lote.png)
*Projetos selecionados e a barra de ações em lote — Arquivar, com a contagem de quantos serão afetados*

Marque o checkbox de cada projeto (ou selecione todos de uma vez) para arquivar vários juntos — útil ao início de um exercício novo, para tirar de circulação de uma só vez os projetos concluídos no ano anterior. A confirmação diz **quantos projetos** serão afetados antes de você seguir.

[![Painel de resultado da ação em lote sobre projetos](/assets/screenshots/manual-projetos-13-arquivar-lote-resultado.png)](/assets/screenshots/manual-projetos-13-arquivar-lote-resultado.png)
*Resultado da ação em lote — projetos arquivados, recusados por regra e com falha, cada um com o motivo*

Depois de confirmar, um painel de resultado mostra, separadamente, o que foi **concluído**, o que foi **recusado por regra** e o que **falhou** — o mesmo modelo usado nas ações em lote de [Tarefas e Evidências](#tarefas-selecao-em-lote), acima. O painel fica na tela; releia antes de fechar se o lote for grande.

### O que muda ao arquivar

- **Deixa de ser oferecido** ao lançar uma despesa, pedir pagamento, pedir reembolso ou importar lançamentos por planilha — o projeto não aparece mais nas listas de "vincular a um projeto".
- **Sai do menu e dos cartões do Painel**, que mostram só o que está em andamento.
- **Sai da [página pública de transparência](/configuracoes/pagina-publica/)**, se a OSC publica projetos — mesmo que o projeto estivesse marcado para aparecer lá (ver [Escolher quais projetos aparecem na página pública](/configuracoes/pagina-publica/#escolher-projetos), abaixo).
- **Para de gerar lembretes automáticos** — tarefa atrasada, marco vencido, cobrança de status update. Ninguém recebe mais aviso sobre um projeto que já não está em foco.

### O que não muda

- **O fechamento orçamentário do exercício** continua contando o projeto normalmente.
- **Relatórios e filtros de histórico** continuam enxergando o projeto — arquivar não apaga nem esconde dado financeiro já lançado.

> ✓ **Dica · O passado não muda porque alguém arquivou**
>
> Arquivar é uma decisão sobre **o que aparece hoje**, nunca sobre **o que aconteceu**. Se você está prestando contas de um exercício encerrado, pode arquivar os projetos daquele ano sem medo: o relatório de prestação de contas, o fechamento orçamentário e o histórico de movimentações continuam íntegros e completos.

### Editar um projeto arquivado

[![Projeto arquivado com o botão Editar desativado](/assets/screenshots/manual-projetos-14-arquivado-editar-bloqueado.png)](/assets/screenshots/manual-projetos-14-arquivado-editar-bloqueado.png)
*Num projeto arquivado, o botão **Editar** do bloco Identidade aparece desativado, e o selo "Arquivado" fica ao lado do status*

O **nome e os dados de identificação** de um projeto arquivado ficam **congelados**: o botão **Editar** fica desativado enquanto ele estiver arquivado. Para mudar qualquer coisa, **desarquive** primeiro — use **Reabrir**, no topo da página do projeto.

Se você chegar direto ao endereço de edição de um projeto arquivado ou encerrado — por um link salvo ou pelo histórico do navegador — a tela explica que o projeto está arquivado (ou encerrado) e que é preciso reabri-lo antes de editar, com um botão para voltar à página do projeto.

> ⚠️ **Atenção · Congelado é de propósito, não é bug**
>
> A trava existe para que um projeto arquivado — inclusive um já Concluído, já prestado — não mude de nome ou de dado de identificação **em silêncio**, sem que a decisão de reabri-lo seja explícita. Precisa corrigir algo? Desarquive, edite, e arquive de novo se quiser.

### Quem pode arquivar e desarquivar

Arquivar e desarquivar são ações de quem **administra os projetos da organização** (Presidente, Tesoureiro) — e também do **coordenador daquele projeto específico** (ver "Papel no projeto", acima): mesmo sem administrar os demais projetos da OSC, quem coordena um projeto pode arquivá-lo e desarquivá-lo. O que abre esse acesso é o **vínculo de coordenador naquele projeto**, não o papel da pessoa na organização — ver o quadro em [Papéis e Permissões](/papeis/#quadro-de-permissoes-por-papel).

## A aba Resumo

[![Aba Resumo do projeto](/assets/screenshots/manual-projetos-02-resumo.png)](/assets/screenshots/manual-projetos-02-resumo.png)
*Resumo — identidade, saúde com os três sinais, próximos marcos e último status update*

O **Resumo** é a visão de uma página: a **identidade** do projeto (tipo, status, datas, coordenadores), o cartão de **saúde** com os três sinais (Prazo, Orçamento, Riscos), os **próximos marcos** e o **último status update** publicado pela coordenação. É a tela para olhar de manhã e saber, em segundos, como o projeto está.

No topo do detalhe ficam as **ações de ciclo de vida** disponíveis para o status atual (ex.: *Solicitar aprovação*, *Pausar*, *Solicitar encerramento*, *Cancelar projeto*), e, ao lado delas, o botão **Editar** — ver "Editar o projeto após a criação", abaixo.

### Editar o projeto após a criação

[![Editar a identidade do projeto](/assets/screenshots/manual-projetos-editar.png)](/assets/screenshots/manual-projetos-editar.png)
*Edição da identidade: nome, descrição, tipo, datas e categorias permitidas*

Projetos mudam durante a execução — troca a coordenação, a data escorrega, o escopo se ajusta. Por isso os dados de identidade **podem ser editados depois de criados**, pelo botão **Editar**, no **cabeçalho do projeto** — ao lado das ações de ciclo de vida (ver "A aba Resumo", acima), alcançável **de qualquer aba**, não só da aba Resumo. No celular ele entra no mesmo menu **Mais ações** das transições de status. Dá para ajustar **nome, descrição, tipo, datas de início e fim e as categorias permitidas** (e, em projetos do tipo Evento, o número de participantes esperados).

### Escolher as categorias permitidas
{: #escolher-as-categorias-permitidas }

> 📖 **Conceito · Categorias permitidas são uma restrição, não uma lista de inclusão**
>
> É o ponto que mais confunde: marcar categorias aqui **não adiciona** opções ao projeto — **restringe** quais categorias de despesa ele aceita. **Lista vazia significa "todas as categorias são aceitas"**, inclusive as que a OSC criar depois de hoje. Marcar uma ou mais categorias tira o projeto desse modo aberto e passa a aceitar só o que estiver marcado — nem as futuras entram automaticamente.

Tanto na criação quanto na edição, a lista de **categorias permitidas** do projeto vem com uma **busca por nome** e dois botões: **Marcar todas** e **Desmarcar todas**. Com uma busca ativa, os próprios botões mudam de nome — passam a ser **Marcar todas as encontradas** e **Desmarcar as N encontradas** — porque aí eles valem só sobre o que a busca está mostrando, e não sobre a lista inteira. É o próprio botão dizendo o que vai fazer antes de você clicar. Abaixo da lista, um texto conta sempre quantas categorias estão marcadas — ou avisa que nenhuma está, e que por isso todas são aceitas.

[![Categorias permitidas com busca ativa: botões "Marcar todas as encontradas" e "Desmarcar as N encontradas", e o aviso de categorias marcadas fora da busca](/assets/screenshots/manual-projetos-categorias-busca-desktop.png)](/assets/screenshots/manual-projetos-categorias-busca-desktop.png)
*Busca ativa filtrando "material" — os botões mudam de nome e o aviso mostra o que está marcado fora da busca*

[![A mesma tela no celular](/assets/screenshots/manual-projetos-categorias-busca-mobile.png)](/assets/screenshots/manual-projetos-categorias-busca-mobile.png)
*A mesma tela, no celular*

> ⚠️ **Atenção · Com a busca ativa, "Desmarcar" só limpa o que está na tela**
>
> Se você digitou algo na busca, o botão vira **Desmarcar as N encontradas** — e ele desmarca só as categorias que a busca está mostrando naquele momento, não a lista inteira. Já aconteceu de alguém achar que tinha limpado tudo, sem perceber que categorias marcadas fora da busca continuavam marcadas — e o projeto continuou restrito a elas. Para desmarcar tudo de verdade: **limpe o texto da busca antes** de clicar em Desmarcar todas, ou use o texto de contagem abaixo da lista para confirmar que chegou a zero. Se sobrar algo marcado fora da busca atual, a tela mostra um aviso e um botão extra — **Desmarcar todas (N)** — que limpa a seleção inteira de uma vez, independente da busca.

> ✓ **Dica · Projeto que aceita quase tudo**
>
> Um projeto com orçamento amplo, que aceita quase todas as categorias da OSC, não precisa mais ser marcado categoria por categoria. Filtre pelas poucas que **não** devem entrar, marque todas as outras e depois desmarque as exceções — ou o caminho inverso, filtrando pelo que deve entrar. Lembrando que deixar a lista **vazia** é a forma mais simples de aceitar tudo, inclusive categorias que a OSC ainda vai criar.

> ⚠️ **Atenção · Se uma categoria não puder ser aceita**
>
> Ao salvar, o sistema confere cada categoria escolhida antes de gravar. Havendo alguma que não pode ser aceita, a mensagem diz **o motivo exato**, categoria por categoria: **apagada do cadastro** (foi excluída em Configurações → Categorias — ver [Excluir categorias e centros de custo](/configuracoes/categorias/#excluir-categorias-e-centros-de-custo)) ou **de outra organização**. Remova a categoria apontada da lista, escolha a categoria certa e salve de novo.

### Quando uma categoria não é aceita pelo projeto
{: #quando-uma-categoria-nao-e-aceita-pelo-projeto }

Um projeto com lista de categorias permitidas (acima) só aceita lançamento cuja categoria esteja **nessa** lista. Sempre que você tenta ligar um lançamento a um projeto assim — lançando, editando, corrigindo dados de um lançamento pago, pedindo reembolso ou pagamento, ou vinculando lançamentos já existentes (ver **[Vincular lançamentos existentes](#vincular-lançamentos-existentes)**, abaixo) — e a categoria não está na lista, a ação é recusada com **uma mensagem única**, em qualquer um desses lugares:

> *"A categoria "Material de construção" não está entre as permitidas por este projeto. Para usá-la, abra o projeto, vá em Identidade › Categorias permitidas e inclua a categoria — depois refaça este lançamento."*

- **A mensagem nomeia a categoria** — a sua, não uma lista genérica de "categoria inválida". Havendo mais de uma categoria recusada de uma vez (lançamento com valor dividido entre categorias), a mensagem nomeia até três e resume o resto ("e mais N").
- **O caminho que ela indica é sempre o mesmo:** abrir o projeto, ir em **Identidade → Categorias permitidas** (ver [Escolher as categorias permitidas](#escolher-as-categorias-permitidas), acima) e incluir a categoria que faltou — depois repetir a ação que foi recusada.
- **Nada é gravado enquanto a recusa não for resolvida.** O lançamento continua como estava antes da tentativa — sem projeto, no projeto anterior, ou fora da correção que você tentou fazer.

> ✓ **Dica · Duas saídas, dependendo do que faz mais sentido**
>
> Encontrou a recusa? Você tem duas opções, não uma só: **incluir a categoria** na lista de permitidas do projeto (quando ela realmente deveria caber ali), ou **trocar a categoria do lançamento** (quando foi ela que saiu errada). A mensagem só aponta o conflito — qual dos dois lados corrigir é uma decisão sua.

**Mudanças que exigem reaprovação.** A regra depende do estado do projeto:

- **Projeto ainda não aprovado** — você edita direto, qualquer campo.
- **Projeto com abertura já aprovada** — mudanças de **nome, descrição e categorias permitidas valem na hora**, sem esperar aprovação de ninguém; já as que afetam **prazo ou escopo** (datas, tipo, número de participantes esperados) entram como uma **alteração proposta, aguardando reaprovação**. O projeto **continua rodando com os valores atuais** (do prazo/escopo) e um aviso mostra a mudança proposta (de → para). Quem aprova pode **aprovar** ou **rejeitar**; quem propôs pode **cancelar** a proposta. As pessoas certas são avisadas pelos canais que escolherem nas preferências de notificação. Ao salvar, a mensagem de confirmação diz separadamente o que **já valeu** e o que **foi enviado para aprovação** — nunca dá a entender que tudo foi aplicado de uma vez.

> 📖 **Conceito · Categorias permitidas saíram da reaprovação**
>
> Até pouco tempo, mudar as categorias permitidas de um projeto já aprovado também gerava uma proposta pendente, junto com tipo, datas e participantes. Isso mudou: hoje a mudança de categorias **vale na hora**, porque restringir ou liberar categorias não altera o prazo nem o escopo aprovado do projeto — é ajuste de conformidade contábil, não decisão que precise da segunda pessoa. Se o projeto tinha uma proposta pendente que só pedia mudança de categorias, ela passou a aparecer como **desnecessária**, com um botão para descartar.

> ⚠️ **Atenção · Toda mudança de identidade pede um motivo, de pelo menos 10 caracteres**
>
> Editar direto, propor mudança num projeto já aprovado, aprovar a proposta ou rejeitá-la: nos **quatro** caminhos, o campo **Motivo** é obrigatório, com no mínimo **10 caracteres** — a tela não deixa confirmar antes disso. Ao **propor** uma mudança, o motivo fica visível para quem for aprovar, ao lado do de→para de cada campo alterado; ao **aprovar** ou **rejeitar**, o motivo de quem decidiu fica registrado junto com a decisão. Em qualquer um dos quatro, o texto fica guardado na trilha do projeto — quem revisar depois vê não só o que mudou, mas **por que**.
>
> *Exemplo de motivo ao propor:* "O acampamento foi adiado e o período precisou ser ajustado." *Exemplo ao aprovar:* "Nova data confirmada com a diretoria." *Exemplo ao rejeitar:* "A nova data conflita com outro evento já confirmado."

**Avisos antes de salvar.** Sem apagar nada, o sistema avisa quando uma edição pode ter efeito colateral: ao **remover uma categoria** que já tem lançamentos, ao **encurtar as datas** deixando lançamentos fora do novo período, ou ao **trocar o tipo** de um projeto que já tem dados específicos. Em todos os casos você vê o aviso e **confirma antes de seguir**.

> 💡 **Por que isso importa · Mudar sem perder o controle**
>
> Editar livremente um projeto já aprovado abriria brecha para alterar prazo e escopo sem ninguém saber; travar tudo obrigaria a recriar o projeto a cada ajuste. O caminho do meio — **nome/descrição livres, prazo/escopo sob reaprovação** — deixa o trabalho fluir e mantém o rastro de quem mudou o quê e quando, que é o que a diretoria precisa na hora de prestar contas.

## A aba Planejamento

[![Aba Planejamento](/assets/screenshots/manual-projetos-03-planejamento.png)](/assets/screenshots/manual-projetos-03-planejamento.png)
*Planejamento — escopo, equipe, marcos, riscos (com severidade) e partes interessadas*

O Planejamento reúne cinco blocos:

- **Escopo** — três campos em linguagem direta: **Objetivos** (o que o projeto quer alcançar), **Critérios de sucesso** (como saberemos que deu certo) e **O que NÃO faz parte** (para evitar mal-entendidos). Cada campo traz um exemplo.
- **Equipe** — quem participa e em que papel. Você adiciona membros, muda papéis e remove. O sistema garante que o projeto sempre tenha **pelo menos um coordenador**. Quem deixou a organização continua listado, marcado como **ex-membro**; quem apenas está com o acesso desativado aparece como **"Desativado"** (ver logo abaixo). Dá para **adicionar várias pessoas de uma vez**, todas com o mesmo papel — ver "Adicionar várias pessoas à equipe" logo abaixo.
- **Marcos** — as entregas/etapas com data prevista. Você pode marcar como atingido, reagendar e usar o **modelo de marcos** sugerido pelo tipo do projeto. Marcos pendentes que passam da data viram "perdidos" e alimentam a saúde do projeto.
- **Riscos** — o que pode dar errado, com **Probabilidade** (Baixa/Média/Alta) e **Impacto** (Alto/Médio/Baixo). Quando os dois estão definidos, o risco mostra um selo de **severidade** (Probabilidade × Impacto), de Baixa a Alta — para você priorizar. Você pode marcar um risco como **materializado** ou **mitigado**.
- **Partes interessadas (stakeholders)** — pessoas e organizações externas relevantes (financiador, parceiro, poder público) e o canal de contato.

> ✓ **Dica · Risco bom é risco escrito antes**
>
> O valor do bloco de riscos não está em prever o futuro — está em **combinar antecipadamente o que faremos se acontecer**. Um risco "Atraso na entrega do fornecedor — Probabilidade Média, Impacto Alto, mitigação: confirmar prazo por escrito e ter fornecedor reserva" vale mais do que dez reuniões de pânico depois que o fornecedor sumiu. Escreva os 3 ou 4 riscos óbvios logo no planejamento.

### Adicionar várias pessoas à equipe

Ao adicionar gente ao projeto, você pode **selecionar várias pessoas de uma vez** e atribuir a todas o **mesmo papel**. Se quiser papéis diferentes para pessoas diferentes, faça a operação em duas vezes — uma leva para cada papel.

Se alguma das pessoas selecionadas não puder entrar (por exemplo, já está na equipe ou não pertence mais à organização), **as demais entram normalmente**: a operação não é cancelada por causa de uma pessoa. O sistema mostra, **pessoa por pessoa**, quem entrou na equipe e, para quem não entrou, o motivo.

### Quem saiu da organização continua na equipe

Quando alguém deixa a organização, **ela não desaparece dos projetos de que participou**. O nome continua na equipe, com o papel que tinha no projeto, acompanhado do selo **"Ex-membro da organização"** — e o mesmo aviso aparece ao lado do nome na lista de **coordenadores**, no Resumo.

Essa participação passa a ser **só registro**: não dá mais para mudar o papel dela nem removê-la da equipe pela tela. E a pessoa **não aparece mais como opção** para novas atribuições — não é oferecida ao **adicionar gente à equipe**, ao escolher o **responsável por uma tarefa** nem na lista de **menções (`@`) do mural**.

O histórico, porém, continua consultável: quem saiu **permanece no filtro de responsáveis** das tarefas, para você conseguir ver o que aquela pessoa tocou enquanto esteve no projeto.

### E quem só está com o acesso desativado?

É uma situação diferente, e a equipe agora **mostra a diferença**: quem continua vinculado à OSC mas está com o **acesso desativado** aparece com o selo **"Desativado"** ao lado do papel no projeto — não com o selo de ex-membro. Enquanto estiver assim, o papel dessa pessoa no projeto **não é editável pela tela**.

A distinção importa na hora de entender por que alguém sumiu do projeto no dia a dia: **desativado** é reversível (basta reativar o acesso em Configurações → Usuários e a pessoa volta a atuar); **ex-membro** é definitivo — a pessoa saiu da organização e a participação virou só registro.

> 💡 **Por que isso importa · Participação é registro histórico**
>
> Duas coisas diferentes se confundem quando alguém sai: o **acesso** (que deve cessar na hora — quem não é mais da OSC não deve poder entrar, coordenar nem receber tarefa) e o **registro** de que aquela pessoa trabalhou no projeto (que a OSC precisa guardar). Apagar o nome da equipe resolveria o primeiro problema criando um pior: tarefas e decisões órfãs, e uma prestação de contas que não consegue dizer quem fez o quê. Por isso o RIT360 Financeiro **corta o acesso e preserva o registro** — o selo "Ex-membro" é exatamente essa distinção aparecendo na tela.

## A aba Execução

[![Aba Execução](/assets/screenshots/manual-projetos-04-execucao.png)](/assets/screenshots/manual-projetos-04-execucao.png)
*Execução — tarefas em Kanban, mural de comunicação e evidências*

É onde o projeto acontece no dia a dia. Três blocos:

**Tarefas.** Liste o que precisa ser feito, com responsável, prazo e vínculo a um marco. Você alterna entre **Lista** e **Kanban** (quadro com as colunas A fazer · Em andamento · Concluída · Abandonada). Cada cartão tem **botões de ação diretos** — iniciar, concluir, reabrir, abandonar, editar, remover (editar e remover apenas para a coordenação). Uma tarefa pode ir de **qualquer status para qualquer outro** (inclusive voltar de Concluída para Em andamento); só ao **abandonar** o sistema pede uma justificativa.

### Concluir, reabrir, abandonar ou remover várias tarefas de uma vez {#tarefas-selecao-em-lote}

Na visualização em **Lista**, marque o checkbox de cada tarefa que quiser (ou selecione todas de uma vez) para agir sobre várias ao mesmo tempo, em vez de repetir o mesmo clique tarefa por tarefa — útil depois de fechar uma etapa inteira do projeto, quando várias tarefas terminam juntas.

[![Lista de tarefas com seleção múltipla e a barra de ações em lote](/assets/screenshots/manual-projetos-tarefas-selecao-lote.png)](/assets/screenshots/manual-projetos-tarefas-selecao-lote.png)
*Tarefas selecionadas e a barra de ações em lote no rodapé — Concluir, Reabrir, Abandonar e Remover*

Uma barra de ações aparece no rodapé com **Concluir**, **Reabrir**, **Abandonar** e **Remover** (as duas últimas, só para a coordenação — mesma regra da ação individual). Ao **abandonar** em lote, o sistema pede **um único motivo**, que vale para todas as tarefas marcadas — não um por tarefa.

Depois de confirmar, um painel de resultado fica na tela mostrando, separadamente, o que foi **concluído**, o que foi **recusado por regra** e o que **falhou**:

[![Painel de resultado da ação em lote sobre tarefas](/assets/screenshots/manual-projetos-tarefas-lote-resultado.png)](/assets/screenshots/manual-projetos-tarefas-lote-resultado.png)
*Resultado da ação em lote — itens concluídos, recusados e com falha, cada um com o motivo*

> 📖 **Conceito · "Recusado" não é erro — é o sistema aplicando a regra**
>
> Uma tarefa **já concluída** não pode ser "concluída" de novo; uma **já abandonada** não pode ser reaberta pela mesma ação que reabre uma em andamento. Quando isso acontece dentro de um lote, aquela tarefa não é ignorada em silêncio: ela aparece no painel como **recusada, com o motivo** — por exemplo, "já estava concluída". O restante do lote que não tinha esse problema é processado normalmente. Esse mesmo painel — concluído, recusado por regra, falhou — é o modelo usado em toda ação em lote do RIT360 Financeiro; você vai encontrá-lo de novo em [Evidências](#evidencias-selecao-em-lote), abaixo.
>
> **O painel permanece na tela** depois da ação — não é um aviso rápido que some sozinho. Se o lote for grande, releia com calma antes de fechar.

**Comunicação (Mural).** A linha do tempo do projeto. Reúne, no mesmo lugar, os **eventos do sistema** (mudou de status, entrou alguém na equipe, tarefa concluída) e os **comentários** da equipe. Você escreve um comentário, **menciona** alguém com `@` (a pessoa é notificada) e filtra por **Todos / Eventos do sistema / Comentários / Status updates**. O autor ou a coordenação pode remover um comentário — ele fica marcado como "removido", sem apagar o histórico.

**Status update.** Um recado periódico da coordenação sobre o andamento (o que avançou, o que está pendente, próximos passos). Se o projeto fica muitos dias sem um update, o RIT360 Financeiro lembra a coordenação.

**Evidências.** Anexos que comprovam o que foi feito — fotos do evento, documentos, vídeos. Cada projeto tem um espaço próprio de armazenamento. Quem enviou um anexo pode removê-lo dentro de uma **janela de 24 horas** após o envio; passado esse prazo, só a **coordenação** do projeto remove.

### Remover várias evidências de uma vez {#evidencias-selecao-em-lote}

Marque o checkbox de cada evidência que quiser remover (ou selecione todas de uma vez) e confirme pela barra de ações no rodapé — útil quando sobra um lote de fotos ou documentos enviados por engano ou já substituídos.

[![Lista de evidências com seleção múltipla e a barra de remover em lote](/assets/screenshots/manual-projetos-evidencias-selecao-lote.png)](/assets/screenshots/manual-projetos-evidencias-selecao-lote.png)
*Evidências selecionadas e o botão "Remover selecionadas" no rodapé*

Vale a mesma regra de sempre: **coordenação remove qualquer evidência; quem enviou, só dentro das 24 horas**. Uma evidência fora dessa janela, marcada por quem não é coordenador, não trava o lote inteiro — ela aparece **recusada, com o motivo**, no mesmo painel de resultado descrito em [Tarefas, acima](#tarefas-selecao-em-lote).

> ✓ **Dica · O mural é a memória do projeto**
>
> Em OSC, a equipe muda: voluntário entra, coordenador sai, a diretoria roda. O mural preserva **a história contável e a história humana** do projeto no mesmo lugar — quem decidiu o quê, quando, e por quê. Na hora de prestar contas ou de fazer o próximo projeto parecido, ele vale ouro.

## A aba Financeiro

[![Aba Financeiro](/assets/screenshots/manual-projetos-05-financeiro.png)](/assets/screenshots/manual-projetos-05-financeiro.png)
*Financeiro do projeto — registrar despesa, pendentes de aprovação, orçamento e lançamentos vinculados*

> 🎥 **Vídeo tutorial · Vincular lançamentos a um projeto**
>
> Esta tela tem um vídeo curto (sem áudio, com legendas) mostrando como ligar receitas e despesas ao projeto certo — clique no ícone de vídeo, no canto direito do cabeçalho. Veja todos os vídeos disponíveis em [Vídeos tutoriais dentro do app](/primeiros-passos/#videos-tutoriais).

O Financeiro mostra o dinheiro do projeto sem tirar nada do caixa geral da OSC:

- **Registrar despesa do projeto** — abre um **reembolso** ou um **pedido de compra e pagamento** já vinculado a este projeto. A solicitação segue o **fluxo normal de aprovação** da OSC.
- **Vincular lançamentos existentes** — atribui a este projeto movimentações que já foram lançadas e ainda não tinham projeto. Ver **[Vincular lançamentos existentes](#vincular-lançamentos-existentes)**, abaixo.
- **Receitas e Despesas** — os valores realizados e previstos de receita e despesa vinculadas ao projeto. Se o projeto ainda não tem nenhuma receita lançada, aparece zerado, com a frase "Nenhuma receita vinculada a este projeto ainda.".
- **Orçamento do projeto** — previsto, gasto e sobra do projeto **como um todo**, em três números. Ver [Orçamento do projeto](#orcamento-do-projeto), abaixo.
- **Quem paga este projeto** — de onde vem o dinheiro: uma ou mais **fontes** (caixa geral, receitas próprias, financiador), cada uma com o seu período, e o **plano de trabalho** de cada financiador. Ver [Quem paga este projeto](#quem-paga-este-projeto), abaixo.
- **Aguardando aprovação** — lista os pedidos e reembolsos do projeto que **ainda não foram aprovados** (com o selo "Aguardando Aprovação" ou "Rascunho"). Clique para abrir o pedido. **Esses pendentes não entram nos totais** — servem só para você saber o que já foi solicitado e **não pedir o mesmo pagamento duas vezes**. Quando aprovados, saem daqui e passam a contar como movimentação vinculada.
- **Lançamentos vinculados** — as movimentações já atribuídas ao projeto, com filtros. Cada linha mostra o **valor** e acompanha a **situação do lançamento conforme ele evolui**: aparece quando é vinculado (previsto), muda para **pago** quando o pagamento é registrado e para **estornado** se for revertido — sempre na mesma linha, sem duplicar. Assim toda a equipe do projeto enxerga, em um só lugar, o que já foi previsto, o que foi efetivamente pago e o que foi estornado, com os valores visíveis a todos os membros.

> ✓ **Dica · Todo mundo vê o dinheiro do projeto**
>
> Os lançamentos vinculados e seus valores ficam visíveis para **todos os membros do projeto**, não só para a coordenação. Isso mantém a equipe alinhada sobre quanto já foi gasto e evita a sensação de "caixa-preta" que costuma minar a confiança em iniciativas coletivas.

### Vincular lançamentos existentes
{: #vincular-lançamentos-existentes }

[![Janela "Vincular lançamentos existentes", com o filtro por conta, a faixa "N pode ser vinculado; M têm categoria fora das permitidas" e a lista de não elegíveis expandida, com a caixa desabilitada e o motivo em laranja](/assets/screenshots/manual-projetos-vincular-lancamentos-desktop.png)](/assets/screenshots/manual-projetos-vincular-lancamentos-desktop.png)
*Vincular lançamentos existentes — os não elegíveis aparecem com o motivo, mas não podem ser marcados*

[![A mesma janela no celular](/assets/screenshots/manual-projetos-vincular-lancamentos-mobile.png)](/assets/screenshots/manual-projetos-vincular-lancamentos-mobile.png)
*A mesma janela, no celular*

Ao clicar em **Vincular lançamentos existentes**, a janela lista as movimentações da organização que **ainda não têm projeto** — com busca por título ou contraparte e um **filtro por conta bancária**, útil quando a OSC segrega uma conta por projeto (ver [Conta com projeto e centro de custo padrão](/modulos/movimentacoes/#conta-com-projeto-e-centro-de-custo-padrao), em Movimentações) e você quer vincular só o que passou por aquela conta.

A janela **conta**, o tempo todo, quantos lançamentos da lista **podem** e quantos **não podem** ser vinculados — a mesma regra de [Quando uma categoria não é aceita pelo projeto](#quando-uma-categoria-nao-e-aceita-pelo-projeto), acima: um projeto com categorias permitidas só aceita lançamento cuja categoria esteja na lista. Por padrão, a lista mostra só os elegíveis; um botão **"Mostrar os N não elegíveis"** traz os demais para conferência, com a caixa de seleção **desabilitada** em cada um — dá para ver por que ficaram de fora, mas não para marcá-los sem resolver o motivo primeiro.

- **Cada lançamento não elegível mostra o motivo na própria linha** — "Categoria fora das permitidas por este projeto — autorize-a em Identidade › Categorias permitidas para vincular."
- **Selecionar todos** marca só os elegíveis da lista filtrada no momento — nunca os desabilitados.
- O botão de confirmação já diz quantos serão vinculados ("Vincular 4 lançamentos"), e some se nada estiver selecionado.

> ⚠️ **Atenção · Nenhum lançamento cabe no projeto? A tela explica por quê**
>
> Se, depois de filtrar, **nenhum** lançamento da lista puder ser vinculado, a janela não mostra uma lista vazia sem contexto — ela diz que este projeto só aceita algumas categorias e que nenhum dos lançamentos está nelas, e aponta o caminho: abrir o projeto, ir em **Identidade › Categorias permitidas** e incluir as categorias que faltam. Um link permite ver os não elegíveis mesmo assim, para você conferir de qual categoria se trata antes de decidir.

> ✓ **Dica · Filtre por conta antes de vincular um lote grande**
>
> Numa OSC com muitas contas e vários projetos rodando ao mesmo tempo, filtrar por conta antes de selecionar reduz o risco de vincular ao projeto errado um lançamento de outra iniciativa que só coincide de estar sem projeto ainda.

**Quem pode:** vincular lançamentos exige o papel de **Coordenador do projeto** (ver **Conceitos essenciais**, acima). Projeto **concluído ou cancelado** não recebe novos vínculos por aqui, do mesmo jeito que não recebe pelo [Corrigir dados de um lançamento pago](/modulos/movimentacoes/#corrigir-os-dados-de-um-lançamento-pago) nem pela [atribuição em lote](/modulos/movimentacoes/#atribuir-projeto-em-lote).

### Calculadora de taxa de evento (projetos do tipo Evento)

[![Calculadora de taxa](/assets/screenshots/manual-projetos-06-calculadora.png)](/assets/screenshots/manual-projetos-06-calculadora.png)
*Calculadora de taxa — simula a taxa por pagante a partir de custos, isentos, voluntários e a regra de pagamento*

Para um **Evento**, a aba Financeiro tem a sub-aba **Calcular taxa**, que ajuda a definir **quanto cobrar de inscrição** para o evento se pagar. Você informa os **custos previstos**, um **fundo de reserva** (%), um **custo por participante** (o gasto marginal por pessoa atendida — kit, alimentação, material), e quantos serão **pagantes**, **isentos** e **voluntários e/ou equipe de serviço**. A calculadora mostra, em tempo real, a **taxa por pagante**, a **receita prevista** e a sobra.

> 📖 **Conceito · Quem não paga, alguém cobre**
>
> A lógica é simples e justa: os **pagantes** cobrem o custo fixo do evento **mais** o custo de cabeça de quem é atendido mas não paga a própria inscrição (isentos e, conforme a regra, voluntários). Por isso, ao aumentar o número de isentos, a taxa por pagante sobe — o custo deles foi redistribuído. A **regra de pagamento dos voluntários** (rateado, taxa cheia, com desconto, ou a OSC paga) muda como o voluntário entra nessa conta; a descrição da regra escolhida aparece logo abaixo do seletor. Com "custo por participante" igual a zero, a taxa volta a ser o simples rateio do custo entre os pagantes.

Você pode **salvar** simulações no histórico, **adotar uma como taxa oficial** do evento ou **marcar o evento como gratuito**.

## Orçamento do projeto
{: #orcamento-do-projeto }

O bloco **Orçamento do projeto**, na aba Financeiro, mostra três números do projeto **como um todo**: **Previsto**, **Gasto** e **Sobra**. Quem coordena o projeto pode **editar o total previsto** a qualquer momento, pelo botão **Editar total**.

[![Bloco Orçamento do projeto com Previsto, Gasto e Sobra, e o diálogo "Editar total previsto" aberto](/assets/screenshots/manual-projetos-orcamento-editar-total-desktop.png)](/assets/screenshots/manual-projetos-orcamento-editar-total-desktop.png)
*Orçamento do projeto — Previsto, Gasto e Sobra, com o diálogo de edição do total aberto*

[![O bloco Orçamento do projeto no celular](/assets/screenshots/manual-projetos-orcamento-mobile.png)](/assets/screenshots/manual-projetos-orcamento-mobile.png)
*O mesmo bloco, no celular*

Este número não se divide por categoria nem por conta — é a visão rápida de "o projeto está dentro do orçamento?". O detalhe **por financiador** — o que cada um aprovou, quanto já foi gasto de cada rubrica — vive no **plano de trabalho** de cada fonte, a seguir.

## Quem paga este projeto
{: #quem-paga-este-projeto }

> 💡 **Por que isso importa**
>
> Todo projeto de OSC tem uma resposta para "de onde vem esse dinheiro?" — só que ela raramente é uma resposta só. Um acampamento pode começar com o caixa geral, ganhar um patrocínio no meio do caminho e ainda vender uma rifa. Um convênio de dois anos pode terminar e o projeto continuar por conta própria. O RIT360 Financeiro trata isso como o que é: uma **lista de fontes**, cada uma valendo por um **período**, em vez de uma única resposta fixa escolhida na criação do projeto.

Cada projeto tem uma lista de **fontes** — de onde vem o dinheiro que o financia. Uma fonte é de um destes três tipos:

| Tipo | Exemplo | Pede plano de trabalho? | Conta exclusiva? |
|---|---|---|---|
| **Caixa geral da organização** | dinheiro próprio da OSC | Opcional, se a OSC quiser acompanhar mesmo assim | Não |
| **Receitas do próprio projeto** | festa, bazar, doação dirigida ao projeto | Não | Não |
| **Financiador** | edital, convênio, termo de fomento, emenda parlamentar, patrocínio | Sim, no sentido de que é para isso que ele serve | Opcional — pergunta-se se o financiador exige |

[![Bloco "Quem paga este projeto" com dois financiadores e o caixa geral](/assets/screenshots/manual-projetos-fontes-01-lista.png)](/assets/screenshots/manual-projetos-fontes-01-lista.png)
*"Quem paga este projeto" — dois financiadores e o caixa geral da OSC, cada um com seu período, o recebido, o gasto e o próprio plano de trabalho*

### Acrescentar ou editar uma fonte
{: #acrescentar-ou-editar-uma-fonte }

Clique em **Acrescentar fonte** (ou **Editar fonte**, numa já existente). Preencha:

- **Tipo** — um dos três da tabela acima;
- **Nome do financiador** — obrigatório só para o tipo Financiador (para os demais, um nome é opcional, útil quando há mais de uma receita própria a distinguir);
- **Instrumento** (opcional) — o edital, convênio ou termo de fomento que identifica a fonte para quem for auditar depois;
- **Início** e **Fim** — o período em que a fonte vale. Deixe o fim vazio enquanto ela ainda estiver ativa;
- **O financiador exige conta só para este dinheiro?** — marque se sim, e escolha a **conta exclusiva** daquela fonte.

> 📖 **Conceito · O período é o que resolve entrada e saída de financiador no meio do caminho**
>
> Um projeto pode ter várias fontes ao mesmo tempo, e cada uma tem um começo e (quando aplicável) um fim. É assim que o RIT360 Financeiro cobre os dois casos comuns: o projeto que **começa** com recursos próprios e ganha um financiador depois, e o que **perde** o convênio na metade e segue por conta própria — em nenhum dos dois casos é preciso apagar ou recriar nada, só acrescentar a fonte nova ou encerrar a antiga.

> ✓ **Dica · Conta exclusiva é sobre o financiador, não sobre a OSC**
>
> Marque "conta só para este dinheiro" quando for o **financiador** que exige — é comum em convênio e termo de fomento, porque facilita a prestação de contas dele. Se a exigência é só uma preferência interna da sua OSC, você pode abrir a conta exclusiva mesmo assim; a diferença é que, para o caixa geral e para receitas próprias, isso quase nunca é necessário.

### Projetos antigos foram convertidos automaticamente

Todo projeto que já existia antes desta versão ganhou, automaticamente, uma **primeira fonte** — refletindo como ele já estava declarado (caixa geral, ou com receitas próprias). Nada foi perdido nem precisa ser refeito; a lista de fontes só passou a aparecer na tela.

### Projeto sem financiador

Se o seu projeto só usa caixa geral e receitas próprias — sem nenhum financiador —, a aba Financeiro mostra só o **Orçamento do projeto** (acima) e uma frase convidando a acrescentar um financiador, quando fizer sentido:

> *"Entrou dinheiro de edital, convênio ou patrocínio? Acrescente o financiador em 'Quem paga este projeto', e o sistema passa a acompanhar o plano de trabalho dele."*

Nada fica escondido: a tela simplesmente não mostra plano de trabalho até existir um financiador para ter um.

### Encerrar uma fonte
{: #encerrar-fonte }

Encerrar uma fonte é **só marcar uma data de fim** — não existe uma operação especial de "cancelar financiador". Clique em **Encerrar fonte** e confirme.

- **Nada do que já foi lançado com aquela fonte desaparece ou muda.** As despesas continuam identificadas como daquela fonte, no plano de trabalho dela e na aba Financeiro.
- **A fonte deixa de ser oferecida** em lançamentos novos a partir da data de encerramento.
- **Uma fonte encerrada continua visível** para consulta — a organização não perde o histórico nem o plano de trabalho dela.
- Se o projeto continuar depois do encerramento, é só acrescentar outra fonte (o caixa geral, outro financiador) para cobrir o que vem a partir de então.

> 💡 **Por que isso importa**
>
> É comum um convênio acabar e o projeto seguir rodando com outro dinheiro, ou terminar de fato. Tratar isso como "encerrar uma fonte com data", em vez de uma decisão especial e irreversível, deixa a prestação de contas daquele financiador intacta e não obriga a OSC a decidir, na hora do encerramento, o que vai acontecer com o projeto depois.

> ✓ **Dica · Fonte encerrada continua emitindo prestação de contas**
>
> Encerrar não tira o botão **Prestação de contas** da fonte (ver [Prestação de contas de uma fonte](#prestacao-de-contas-por-fonte), abaixo). Você continua podendo emitir o documento dela — inclusive anos depois, para uma auditoria ou uma cópia perdida — com o mesmo período que ela cobriu enquanto esteve ativa.

## Prestação de contas de uma fonte
{: #prestacao-de-contas-por-fonte }

> 💡 **Por que isso importa**
>
> Prestar contas a um financiador é provar, com números e documento, quanto ele repassou, quanto foi gasto em cada item do plano de trabalho e quanto sobrou ou foi devolvido — para o edital, o convênio, a emenda ou o patrocínio, **daquela fonte específica**, não da OSC inteira. Sem isso, prestar contas significa recortar manualmente as movimentações do projeto que pertencem àquele financiador em particular, separando-as do que veio do caixa geral ou de outro financiador do mesmo projeto — trabalho que se repete a cada prestação e que é fácil de errar. O RIT360 Financeiro monta esse documento pronto, pela própria fonte.
>
> **Exemplo:** o Instituto Exemplo tem um projeto de reforço escolar financiado por dois convênios ao mesmo tempo — a Prefeitura (R$ 40.000, já encerrado) e uma fundação privada (R$ 25.000, ainda em execução). Ao prestar contas à Prefeitura, a coordenadora abre a fonte "Prefeitura — Convênio 12/2025" e emite a prestação de contas **só dela**: o documento não mistura o dinheiro da fundação, mesmo que as duas fontes financiem o mesmo projeto ao mesmo tempo.

Cada fonte de um projeto — ativa ou já encerrada — tem o botão **Prestação de contas**, no bloco [Quem paga este projeto](#quem-paga-este-projeto), na aba Financeiro. Ele abre uma janela para escolher o **período**: por padrão, do **início da fonte** até o **fim dela** (se já encerrada) ou até **hoje** (se ainda ativa) — mas você pode estreitar ou alargar as datas antes de confirmar.

[![Janela "Prestação de contas de {fonte}", com os campos De/Até e o botão Emitir prestação de contas](/assets/screenshots/manual-projetos-prestacao-contas-fonte-desktop.png)](/assets/screenshots/manual-projetos-prestacao-contas-fonte-desktop.png)
*Prestação de contas de uma fonte — escolha o período e emita o documento*

Ao confirmar, o documento é **preparado em segundo plano** — o mesmo comportamento de todo relatório do RIT360 Financeiro, já visto no [relatório de encerramento do projeto](#a-aba-encerramento): abre uma página de acompanhamento, e o download começa sozinho quando o PDF fica pronto (você pode fechar a aba, porque o link também chega por aviso). O documento pronto fica guardado na área **[Documentos](/modulos/documentos/)**, com o tipo **"Prestação de contas por fonte"**.

### O que vem no documento

Na ordem:

1. **Capa** — organização, projeto, financiador, instrumento (o edital/convênio, quando informado) e período; e, quando a fonte tem conta exclusiva, o nome da conta.
2. **Resumo** — recebido do financiador, gasto, devolvido e saldo, em quatro números.
3. **Repasses recebidos** — cada valor que entrou daquela fonte, no período.
4. **Plano de trabalho vigente**, item a item — para cada rubrica, o aprovado original, o aprovado vigente (depois de aditivos e remanejamentos), o gasto e o saldo, com as despesas daquele item listadas por baixo. Rubrica **acima do plano** ganha um selo de aviso.
5. **Histórico do plano** — as versões aprovadas (original e aditivos) e os remanejamentos do período, cada um com data, valor, justificativa e se há documento anexado.
6. **Despesas fora do plano de trabalho** — as que usam categoria não associada a nenhum item.
7. **Despesas sem item escolhido** — as que ficaram associadas à fonte sem alguém ter escolhido a rubrica.
8. **Devoluções ao financiador** — o que foi devolvido no período (ver [Devolução é despesa da fonte, não estorno](#corrigir-depois-quem-pagou-este-lancamento), acima).
9. **Despesas do projeto sem fonte definida no período** — um alerta de que esses lançamentos não entram nos números acima e precisam ser corrigidos para a prestação fechar certo.
10. **Anexo "de → para"** — a ligação, vigente em cada data, entre os itens do plano e as categorias da organização que contam para eles.

> 📖 **Conceito · Seção vazia não some — ela diz "Nada no período"**
>
> Uma fonte sem devolução no período, ou sem nenhuma despesa fora do plano, continua mostrando a seção correspondente — só que com o aviso **"Nada no período"**, em vez de simplesmente pular a seção. É assim que quem lê a prestação sabe que aquele item foi checado e deu zero, não que o documento esqueceu de olhar.

> ⚠️ **Atenção · Fonte sem plano de trabalho traz um documento mais simples**
>
> Uma fonte do tipo **Caixa geral** ou **Receitas do próprio projeto** que nunca teve plano de trabalho cadastrado (ver [Plano de trabalho](#plano-de-trabalho), abaixo) gera a prestação **sem** as seções de plano, histórico, fora do plano, sem item escolhido e "de → para" — ficam só capa, resumo, repasses, devoluções e despesas sem fonte definida. Nada é inventado para preencher espaço.

### Quem pode emitir

Quem **coordena o projeto** (ver [Papel no projeto](#conceitos-essenciais), acima) ou tem a **permissão de ver relatórios** da organização. Sem nenhum dos dois, o botão **Prestação de contas** não aparece naquela fonte.

### Quando dá errado

- **"Você não pode emitir a prestação de contas desta fonte."** — sua permissão mudou, ou você não é mais coordenador daquele projeto. Peça a alguém com acesso.
- **"Confira as datas do período: a data final não pode ser anterior à inicial."** — ajuste o período antes de confirmar; a própria janela já avisa isso antes de você clicar em Emitir.
- **"A geração de documentos não está configurada. Avise o suporte."** — falha de infraestrutura da organização, não algo que se resolve tentando de novo.
- **"Não foi possível pedir a prestação de contas agora. Tente novamente."** — instabilidade momentânea; tente de novo em instantes.

### Um atalho a partir da lista de contas

Uma fonte com **conta exclusiva** (ver [Acrescentar ou editar uma fonte](#acrescentar-ou-editar-uma-fonte), acima) aparece também em **Configurações → Contas Bancárias**: a linha da conta mostra a que fonte e a que projeto ela atende, e quem pode emitir a prestação encontra o mesmo botão ali — ver [Contas Bancárias → Conta exclusiva de uma fonte](/configuracoes/contas/#conta-exclusiva-de-uma-fonte). Útil quando você parte da conta, não do projeto, para achar a prestação de um financiador.

## Plano de trabalho (plano de aplicação)
{: #plano-de-trabalho }

> 💡 **Por que isso importa**
>
> Quando um financiador aprova um projeto, ele aprova um **plano de trabalho** (ou plano de aplicação): quanto pode ser gasto em cada item, com o nome que **ele** usa — "material de consumo", "serviços de terceiros", "pessoal" — que raramente é igual às categorias que a sua OSC já usa no dia a dia. Prestar contas significa provar, item por item do plano, quanto foi gasto e em quê. O RIT360 Financeiro faz essa amarração uma vez, no próprio plano — o "de → para" entre os itens do financiador e as categorias da sua organização — em vez de você remontar essa conta à mão toda vez que uma prestação de contas vence.

Cada **financiador** tem o seu próprio plano de trabalho. O **caixa geral** também pode ter um, se a OSC quiser acompanhar internamente sem financiador nenhum de fora.

[![Plano de trabalho de um financiador, com item, gasto e categorias associadas](/assets/screenshots/manual-projetos-fontes-02-plano.png)](/assets/screenshots/manual-projetos-fontes-02-plano.png)
*Plano de trabalho (plano de aplicação) de um convênio — cada item com o gasto e o aprovado, as categorias da organização que contam para ele e o aviso de despesa fora do plano*

### Criar o plano de trabalho de uma fonte

Na fonte, clique em **Criar plano de trabalho**. Para cada **item do plano de trabalho (rubrica)**, informe:

- o **nome** exatamente como o financiador chama aquele item (não precisa ser o nome de uma categoria sua);
- o **valor aprovado**;
- quais **categorias da organização** contam para ele — o "de → para".

> 📖 **Conceito · Item do plano × categoria da organização**
>
> O item do plano de trabalho **não é** uma categoria da sua OSC — é o item que consta no plano aprovado pelo financiador, com o valor que ele autorizou. As categorias que você já usa continuam existindo do jeito que sempre existiram; o "de → para" é só a ponte entre as duas coisas. Uma categoria sua pode contar para **mais de um** item do mesmo plano (por exemplo, "Consultoria" e "Oficinas" dividindo o item "Serviços de terceiros") — nesse caso, o lançamento pergunta de qual item é a despesa. Um item pode não ter nenhuma categoria associada ainda — nesse caso, também é perguntado.

**Exemplo:** o Termo de fomento 045/2026 aprovou três itens — "Material de consumo" (R$ 8.000), "Serviços de terceiros" (R$ 15.000) e "Pessoal" (R$ 30.000). A OSC associa "Material de escritório", "Material de limpeza" e "Alimentação" ao item "Material de consumo" — três categorias suas contando para o mesmo item do financiador.

### Aditivo: quando o financiador aprova um plano novo

Quando o financiador aprova um plano novo — valor maior, itens novos — clique em **Registrar aditivo**. O aditivo entra como **versão nova** do plano; a versão anterior fica guardada exatamente como estava, e os remanejamentos seguintes passam a valer sobre a versão vigente.

### Remanejamento: mover valor entre itens do mesmo plano

Clique em **Remanejar** para passar valor aprovado de um item para outro **do mesmo plano de trabalho**. Preencha:

- **Sai de** e **Vai para** — os dois itens, do mesmo plano;
- **Valor** e **Data**;
- **Justificativa** (obrigatória, com pelo menos 10 caracteres) — explique por que o valor mudou de item, para quem for ler depois;
- **Documento do financiador** (opcional) — o ofício, e-mail ou termo em que o financiador aceitou a mudança.

> ✓ **Dica · O documento não é obrigatório, mas é o que prova a mudança numa auditoria**
>
> Guardar o documento aqui é escolha da sua organização — o remanejamento vale sem ele, com só a justificativa. Mas é esse documento que, numa auditoria do financiador, mostra que a mudança foi de fato aceita por quem tinha autoridade para aceitá-la, e não apenas decidida internamente pela OSC. Anexando-o, ele fica junto do remanejamento no histórico do plano, pronto para quando for pedido.

> ⚠️ **Atenção · Remanejamento é só dentro do mesmo plano**
>
> Tirar dinheiro do plano de um financiador para cobrir um item de **outro** financiador não é remanejamento — é outro dinheiro, e não é isso que esta tela faz. O remanejamento move valor aprovado só entre itens do plano de trabalho da **mesma** fonte.

### Ver histórico

O botão **Ver histórico**, no plano de trabalho de cada fonte, mostra a sequência completa: o **plano aprovado original**, cada **aditivo**, cada **remanejamento** (com a justificativa e se há documento anexado) e as mudanças no **"de → para"** das categorias — cada uma com a data em que passou a valer. É como ver o plano em qualquer dia do passado, e é o material pronto para uma prestação de contas ou uma auditoria.

[![Histórico do plano de trabalho, com versões, remanejamentos e mudanças de categoria](/assets/screenshots/manual-projetos-fontes-03-historico.png)](/assets/screenshots/manual-projetos-fontes-03-historico.png)
*Histórico do plano de trabalho — versões aprovadas, remanejamentos (com justificativa e indicação de documento, quando houver) e as categorias ligadas a cada rubrica, com data*

> 📖 **Conceito · O plano aprovado nunca é sobrescrito**
>
> Mudar o "de → para" de um item não altera o valor que o financiador aprovou — só muda, a partir daquela data, em qual item as despesas daquela categoria passam a contar. A prestação de contas usa o "de → para" vigente na data de cada despesa, e o histórico mostra quando ele mudou.

### Fora do plano de trabalho

Uma despesa cuja categoria **não está associada a nenhum item** do plano vigente daquela fonte é paga normalmente, e fica marcada como **fora do plano de trabalho** — com aviso na hora e um atalho para incluir a categoria num item. Ela aparece assim tanto na tela do plano quanto numa futura prestação de contas: **é aviso, não pendência** — nada trava por causa disso.

### Acima do plano: risco de glosa, nunca retenção

Se uma despesa faz um item **passar do valor aprovado**, o pagamento acontece normalmente — o RIT360 Financeiro **nunca retém nem recusa** um pagamento por isso. O que aparece é um aviso, no item e no lançamento, de que o valor está acima do aprovado e que o **financiador pode glosar** a despesa. O atalho para **Remanejar** fica à mão, junto do aviso.

<!-- CAPTURA PENDENTE: item do plano de trabalho com gasto acima do aprovado — aviso "Já foi gasto mais do que o previsto nesta rubrica..." e o botão Remanejar. Rota /projetos/{id}?aba=financeiro, no Instituto Exemplo (projeto Oficina de Artesanato), desktop. Precisa de uma despesa que passe do aprovado de uma rubrica. Arquivo esperado: manual-projetos-fontes-04-acima-do-plano.png -->

> ⚠️ **Por que o sistema não trava o pagamento acima da rubrica**
>
> O RIT360 Financeiro é um sistema de **gestão financeira**, não o guardião do que o financiador vai aceitar. Travar o pagamento seria decidir, no lugar do financiador, que aquela despesa não pode acontecer — e isso não é uma decisão que o sistema tem elementos para tomar: pode ser um remanejamento a caminho, um gasto que a OSC decidiu assumir por fora, ou uma negociação já em curso com o financiador. O sistema **avisa o risco** (a glosa é uma possibilidade real) e **registra** o fato (o aviso fica na tela e na prestação de contas) — quem decide o que fazer é quem coordena o projeto e, no fim das contas, o próprio financiador.

### As categorias permitidas do projeto continuam separadas

Ter plano de trabalho **não liga** a restrição de [categorias permitidas](#escolher-as-categorias-permitidas) do projeto. São duas coisas diferentes: o plano de trabalho acompanha, por financiador, quanto foi gasto em cada item; as categorias permitidas restringem, no nível do projeto inteiro, quais categorias ele aceita. Um projeto pode ter plano de trabalho sem nenhuma categoria permitida configurada (aceitando todas), e vice-versa.

## De qual fonte e de qual item sai cada despesa
{: #de-qual-fonte-e-item }

Ao lançar ou pagar uma despesa do projeto, o RIT360 Financeiro decide **fonte** e **item do plano** sozinho quando não há dúvida, pergunta quando há, e avisa (sem travar) quando falta informação:

- **Fonte com conta exclusiva** — automático: a despesa saiu daquela conta, então é daquela fonte.
- **Mais de uma fonte possível** (nenhuma com conta exclusiva, ou mais de uma cabendo) — o lançamento pergunta, no bloco **"De qual dinheiro sai este lançamento"**, sugerindo a mais provável.
- **Categoria associada a um item só** — automático.
- **Categoria associada a mais de um item, ou fonte com itens sem categoria** — o lançamento pergunta o item, sugerindo o provável.
- **Categoria não associada a nenhum item** — a despesa é paga e marcada [fora do plano de trabalho](#plano-de-trabalho), sem perguntar (não há o que escolher).

<!-- CAPTURA PENDENTE: bloco "De qual dinheiro sai este lançamento" no formulário de novo lançamento (ou edição), mostrando os seletores de Fonte e de Rubrica do plano de trabalho quando há mais de uma opção, e o aviso de risco de glosa. Rota /movimentacoes/novo com um projeto de financiador com plano de trabalho e mais de uma fonte/item possível, viewport desktop e mobile.
Tentativa registrada em 11/09/2026 (sessão de captura do manual): montei, no Instituto Exemplo, um projeto (Oficina de Artesanato) com DUAS fontes sem conta exclusiva (Caixa geral e o financiador "Instituto Parceiro Educacional"), cada uma com um item de plano de trabalho usando a MESMA categoria ("Material de escritório"), para forçar a ambiguidade que o texto acima descreve. Mesmo assim, o formulário de novo lançamento só mostrou a caixa "Esta despesa é uma devolução ao financiador", sem os seletores de Fonte/Rubrica — e a chamada de rede `resolve_movement_funding` sempre voltou com uma fonte e um item já decididos, sem pedir confirmação. Não decidido se é um caso que o sistema realmente resolve sozinho por alguma regra de desempate não documentada aqui, ou se a tela do seletor não está implementada neste cenário. Quem retomar: comece conferindo o código-fonte da resolução (RPC `resolve_movement_funding`) antes de tentar mais combinações de dados de teste. -->

**Parcelas e recorrências herdam a escolha** feita no lançamento — todas as ocorrências criadas junto passam a valer para a mesma fonte e item, exceto as que caem fora do período de validade da fonte escolhida.

### Lançamento sem fonte definida

Se a despesa não tem conta que identifique a fonte e há mais de uma possível (ou nenhuma), o lançamento mostra um aviso pedindo confirmação:

> *"Este lançamento ficará sem fonte definida: ele fica de fora da prestação de contas de qualquer fonte e vai precisar ser corrigido para a prestação fechar certo. Confirmo mesmo assim."*

Você confirma e o lançamento segue normalmente — **nada é bloqueado**. A aba "Quem paga este projeto" também avisa, à parte, quantos lançamentos do projeto ainda estão sem fonte.

### Corrigir depois: "Quem pagou este lançamento"
{: #corrigir-depois-quem-pagou-este-lancamento }

Escolheu errado, ou quer completar um lançamento que ficou sem fonte? Abra o lançamento — o bloco **"Quem pagou este lançamento"** aparece em qualquer movimentação vinculada a um projeto, seja **despesa**, **receita** ou **transferência**, e deixa trocar a **fonte** a qualquer momento.

[![Bloco "Quem pagou este lançamento" numa despesa, com os seletores de Fonte e Rubrica do plano de trabalho](/assets/screenshots/manual-projetos-fontes-05-quem-pagou-desktop.png)](/assets/screenshots/manual-projetos-fontes-05-quem-pagou-desktop.png)
*"Quem pagou este lançamento" numa despesa — fonte e rubrica já resolvidas automaticamente pelo sistema*

[![O mesmo bloco no celular](/assets/screenshots/manual-projetos-fontes-05-quem-pagou-mobile.png)](/assets/screenshots/manual-projetos-fontes-05-quem-pagou-mobile.png)
*O mesmo bloco, no celular*

> ⚠️ **Atenção · Rubrica e devolução só existem em despesa**
>
> Numa **receita** ou numa **transferência**, o bloco mostra só o seletor de **Fonte** — sem o item do plano de trabalho e sem a caixa de devolução ao financiador. Faz sentido: rubrica é *onde* uma despesa consumiu o plano de trabalho, e devolução é dinheiro que **volta** ao financiador — nenhum dos dois se aplica a dinheiro que está **entrando** (receita) ou só mudando de conta dentro da própria organização (transferência). Nesses dois tipos, o bloco serve só para você saber (e registrar) de qual fonte veio ou para qual fonte foi aquele lançamento.

[![Bloco "Quem pagou este lançamento" numa receita, mostrando só o seletor de Fonte — sem rubrica nem caixa de devolução](/assets/screenshots/manual-projetos-fontes-06-quem-pagou-receita-desktop.png)](/assets/screenshots/manual-projetos-fontes-06-quem-pagou-receita-desktop.png)
*Numa receita, o bloco só pergunta a fonte — sem rubrica nem devolução, que só existem em despesa*

[![O mesmo bloco no celular](/assets/screenshots/manual-projetos-fontes-06-quem-pagou-receita-mobile.png)](/assets/screenshots/manual-projetos-fontes-06-quem-pagou-receita-mobile.png)
*O mesmo bloco, no celular*

> ✓ **Dica · Devolução é despesa da fonte, não estorno**
>
> Precisou devolver dinheiro ao financiador (por exemplo, um saldo que sobrou no fim do convênio)? Marque a caixa **"É uma devolução de recurso ao financiador"** no próprio lançamento de devolução — não estorne a despesa original. A devolução fica registrada como um movimento próprio daquela fonte, e a prestação de contas dela mostra as duas pontas: o que foi gasto e o que foi devolvido.

## A aba Relatório

[![Aba Relatório do projeto](/assets/screenshots/manual-projetos-10-relatorio.png)](/assets/screenshots/manual-projetos-10-relatorio.png)
*Relatório do projeto — receitas e despesas por categoria, com gráficos e exportação*

A aba **Relatório** mostra os números do projeto dentro dos relatórios financeiros da OSC: **receitas e despesas por categoria**, com gráficos de distribuição, abas de **Atenção** e **Previsão**, escolha de período e **exportação**. Os [Relatórios](/modulos/relatorios/) gerais também ganharam um **filtro por projeto**, para você recortar receitas, despesas e gráficos por uma iniciativa específica.

## A aba Encerramento
{: #a-aba-encerramento }

[![Wizard de encerramento](/assets/screenshots/manual-projetos-07-encerramento-wizard.png)](/assets/screenshots/manual-projetos-07-encerramento-wizard.png)
*Encerramento — assistente de avaliação guiado por passos*

Quando a execução termina, o **Encerramento** conduz a coordenação por um **assistente de avaliação**: os objetivos foram alcançados (sim / parcial / não)? Os critérios de sucesso foram atendidos? Como foi o engajamento da equipe? Quantas pessoas foram atendidas? Quais foram os pontos altos, os pontos a melhorar e a **lição mais importante**?

### Como preencher bem cada campo

A qualidade do encerramento depende do que é escrito nos campos de texto — é isso que alimenta o relatório final e o acervo de **Lições Aprendidas** da OSC. Cada campo do assistente traz, na própria tela, uma orientação curta e um exemplo. O guia abaixo detalha o que torna cada resposta útil:

- **Objetivos — comentário:** explique *por que* o resultado foi esse (o que ajudou ou atrapalhou), em vez de só repetir a nota. *Exemplo: "Batemos os 80 atendimentos, mas só após remarcar por chuva; a parceria com a escola foi decisiva."*
- **Critérios de sucesso — comentário:** diga quais critérios foram atingidos e quais ficaram de fora, com número quando houver. *Exemplo: "Os 3 critérios de qualidade foram atingidos; o de prazo não — entregamos 2 semanas depois."*
- **Engajamento — comentário:** aponte o que sustentou ou minou o engajamento (pessoas, rotina, comunicação). *Exemplo: "O grupo no WhatsApp com tarefas semanais manteve todos ativos; faltou um responsável fixo para o financeiro."*
- **Imprevistos:** registre o que saiu do plano e, principalmente, *como a equipe reagiu*. *Exemplo: "O fornecedor de som cancelou na véspera; conseguimos um empréstimo com outra OSC parceira em 1 dia."*
- **Pontos altos:** o que deu certo e *vale repetir*. Itens curtos e acionáveis, que outra equipe possa copiar. *Exemplos: "Reunião de 15 min toda segunda manteve todos alinhados." · "Convite enviado 3 semanas antes lotou as vagas."*
- **Pontos a melhorar:** o que atrapalhou e *o que fazer diferente* — foco na ação, não na culpa. *Exemplo: "Começamos a divulgação tarde — abrir inscrições com 1 mês de antecedência."*
- **Lição mais importante** (obrigatória): um aprendizado que você levaria para qualquer projeto, completando *"Se eu fizesse de novo, eu ___"*. *Exemplo: "…fecharia o orçamento com 20% de folga, porque imprevistos sempre aparecem."*
- **Recomendação:** um conselho direto para quem for tocar algo parecido, completando *"Quem fizer um projeto parecido deve ___"*. *Exemplo: "…confirmar o local por escrito com 1 mês de antecedência."*

> 💡 **Dica:** escreva pensando no próximo coordenador, que não viveu o projeto. Frases curtas e concretas valem mais que parágrafos genéricos.

[![Relatório de encerramento](/assets/screenshots/manual-projetos-08-encerramento-relatorio.png)](/assets/screenshots/manual-projetos-08-encerramento-relatorio.png)
*Relatório de encerramento — visão consolidada de tudo que o projeto produziu*

A partir dessa avaliação e de tudo que o projeto registrou, o RIT360 Financeiro monta um **relatório de encerramento** consolidado — identificação, resumo financeiro, saúde final, marcos, tarefas, contribuição da equipe, riscos materializados, evidências, status updates, partes interessadas e a avaliação do coordenador. Esse relatório pode ser **exportado em PDF** para a prestação de contas. Antes de finalizar, é possível gerar um **relatório parcial** (marcado como rascunho); ao **finalizar**, a saúde e os números ficam "congelados" como o retrato final do projeto.

Tanto o relatório parcial quanto o final são montados **em segundo plano**: ao pedir o PDF, abre uma página de acompanhamento que mostra "Gerando…" e **o download começa sozinho** quando o documento fica pronto — você pode fechar a aba, porque **o link também chega no seu e-mail**.

[![Página de acompanhamento do relatório do projeto](/assets/screenshots/projeto-relatorio-acompanhamento.png)](/assets/screenshots/projeto-relatorio-acompanhamento.png)
*O relatório do projeto é gerado em segundo plano e baixado automaticamente pela página de acompanhamento.*

**O PDF de encerramento continua disponível mesmo depois que o projeto é encerrado.** Quando o projeto já está **Concluído** (ou Cancelado) e o encerramento foi finalizado, o botão **Baixar PDF do encerramento** permanece à mão em dois lugares: na própria aba **Encerramento** (abaixo do relatório) e na aba **Relatório**, ao lado do "Gerar relatório parcial". Assim você recupera o relatório final para a prestação de contas a qualquer momento, sem precisar reabrir o projeto.

[![Botão Baixar PDF do encerramento num projeto concluído](/assets/screenshots/projeto-encerrado-baixar-pdf.png)](/assets/screenshots/projeto-encerrado-baixar-pdf.png)
*Num projeto já concluído, a aba Encerramento mantém o botão "Baixar PDF do encerramento" ao final do relatório.*

O botão de PDF de encerramento aparece para quem **coordena** o projeto (coordenação, presidência/administração ou tesouraria). Quem tem permissão de exportar dados — como a **comissão fiscal** — não gera o relatório final, mas consegue **baixar** um que já tenha sido gerado.

> 💡 **Por que isso importa**
>
> A maioria das OSCs nunca **fecha** um projeto de verdade — o evento acaba, todo mundo vai embora cansado, e o aprendizado se perde. O encerramento estruturado obriga a parar 20 minutos e responder "deu certo? por quê? o que faríamos diferente?". As **lições aprendidas** viram patrimônio da OSC: o próximo coordenador de evento começa lendo o que o anterior aprendeu, em vez de repetir os mesmos tropeços. E o PDF resolve, de uma vez, a prestação de contas para o financiador.

### O acervo de Lições Aprendidas

[![Lições aprendidas da OSC](/assets/screenshots/manual-projetos-09-licoes.png)](/assets/screenshots/manual-projetos-09-licoes.png)
*Lições aprendidas — o acervo consolidado de tudo que os projetos encerrados ensinaram*

Cada encerramento alimenta um **acervo de Lições Aprendidas** da OSC, acessível pelo botão **Lições aprendidas** no topo da lista de projetos. Ali ficam reunidas, de todos os projetos concluídos, as **boas práticas** (o que deu certo e vale repetir), os **pontos a melhorar**, as **lições** mais importantes e as **recomendações** para quem for tocar algo parecido. É a memória institucional da OSC: antes de começar um projeto novo, vale a pena passar os olhos no que os anteriores já ensinaram.

> ✓ **Dica · Comece pequeno: escopo, orçamento total e 3 marcos**
>
> Não trave o projeto tentando preencher tudo. Para começar, bastam: um **escopo** em uma frase, um **orçamento total**, três ou quatro **marcos** com data e os **riscos óbvios**. O resto você detalha conforme anda. Projeto bem gerido não é o mais preenchido — é o que você **olha toda semana**.

> ✓ **Dica · Use o "Registrar despesa" de dentro do projeto**
>
> Quando a despesa é do projeto, peça o reembolso ou o pagamento **pelo botão do próprio projeto**, não pelo módulo geral. Assim ele já nasce vinculado, aparece nos pendentes do projeto e cai no orçamento certo — sem você precisar lembrar de marcar o projeto depois.

> ⚠️ **Atenção · Pendente não é gasto**
>
> A seção "Aguardando aprovação" mostra o que foi **solicitado**, não o que foi **pago**. Esses valores **não** entram no realizado do projeto até serem aprovados. Use a seção para evitar pedir o mesmo pagamento duas vezes — mas lembre que o orçamento só é consumido quando a despesa é, de fato, aprovada e paga.

## Glossário rápido

- **Projeto** — iniciativa da OSC com objetivo, prazo, orçamento e equipe (evento, obra, campanha, edital, serviço).
- **Arquivado** — marcação à parte do ciclo de vida: tira o projeto das listas ativas, do menu, do Painel, da página pública e dos lembretes automáticos, sem apagar nada. Continua valendo para orçamento, relatórios e histórico. Desarquivar devolve tudo como estava; enquanto arquivado, nome e dados de identificação não podem ser editados.
- **Tipo do projeto** — categoria que adapta a experiência: Evento, Obra, Campanha, Produto/Serviço, Programa ou "Começar do zero". Evento ganha calculadora de taxa e participantes; cada tipo (exceto "Começar do zero") tem marcos-modelo e riscos típicos sugeridos.
- **Programa** — tipo de projeto para uma linha de atendimento ou serviço que se repete, com metas e público definido; ao contrário de Evento (data marcada) ou Obra (entrega física), não tem um único marco de conclusão — tem um período, que pode ser longo.
- **Ciclo de vida** — a sequência de status do projeto (Em planejamento → Aguardando aprovação → Em execução → Aguardando encerramento → Concluído; além de Pausado e Cancelado).
- **Coordenador do projeto** — papel no projeto que conduz o planejamento, as tarefas e as solicitações financeiras.
- **Ex-membro da organização** — pessoa que saiu da OSC e permanece na equipe do projeto apenas como registro histórico: não recebe novas atribuições e não pode ser editada nem removida da equipe.
- **Desativado** — pessoa que continua vinculada à OSC, mas com o acesso suspenso. Aparece na equipe com esse selo; volta a atuar assim que o acesso é reativado.
- **Saúde** — semáforo (Saudável/Atenção/Crítico) que resume Prazo, Orçamento e Riscos.
- **Marco** — entrega ou etapa com data prevista.
- **Severidade do risco** — Probabilidade × Impacto, para priorizar riscos.
- **Status update** — recado periódico da coordenação sobre o andamento.
- **Evidência** — anexo que comprova algo feito no projeto.
- **Taxa de inscrição** — valor cobrado dos pagantes de um evento, calculado pela calculadora de taxa.
- **Relatório de encerramento** — documento consolidado gerado ao finalizar o projeto, exportável em PDF.
- **Fonte de recurso** — de onde vem o dinheiro do projeto: caixa geral da organização, receitas do próprio projeto ou financiador (edital, convênio, termo de fomento, emenda, patrocínio). Cada uma vale por um período. Ver [Quem paga este projeto](#quem-paga-este-projeto).
- **Plano de trabalho (plano de aplicação)** — o plano aprovado por um financiador para o projeto, com um valor por item. Cada financiador tem o seu; o caixa geral pode ter um, se a OSC quiser. Ver [Plano de trabalho](#plano-de-trabalho).
- **Item do plano de trabalho (rubrica)** — cada linha do plano de trabalho: um nome (o que o financiador usa), um valor aprovado e as categorias da organização que contam para ele.
- **De → para** — a ligação entre um item do plano de trabalho e as categorias da organização que contam para ele. Cada plano tem o seu próprio; a mesma categoria pode ir para itens diferentes em planos de financiadores diferentes.
- **Aditivo** — quando o financiador aprova um plano novo (valor maior, itens novos); entra como versão nova do plano, sem apagar a anterior.
- **Remanejamento** — mudança de quanto um item do plano pode receber, movendo valor aprovado de um item para outro do **mesmo** plano, com justificativa obrigatória e documento opcional.
- **Glosa** — quando o financiador recusa (não reconhece como despesa válida) um gasto que passou do valor aprovado num item do plano de trabalho. O RIT360 Financeiro avisa o risco; quem decide se a despesa é aceita é o financiador.
- **Fora do plano de trabalho** — despesa cuja categoria não está associada a nenhum item do plano vigente daquela fonte. É paga normalmente e aparece como aviso, nunca como pendência.
- **Acima do plano** — despesa que faz um item do plano passar do valor aprovado. É paga normalmente, com aviso de risco de glosa.
- **Categoria não permitida** — recusa que aparece sempre que se tenta ligar um lançamento (lançar, editar, corrigir, vincular, pedir reembolso ou pagamento) a um projeto cujas categorias permitidas não incluem a categoria daquele lançamento. Ver [Quando uma categoria não é aceita pelo projeto](#quando-uma-categoria-nao-e-aceita-pelo-projeto) — independente do plano de trabalho.
- **Prestação de contas por fonte** — o documento que reúne o que uma fonte recebeu, gastou e devolveu, item a item do plano de trabalho dela, para entregar ao financiador. Emitido pelo botão **Prestação de contas** da fonte, fica guardado em [Documentos](/modulos/documentos/). Ver [Prestação de contas de uma fonte](#prestacao-de-contas-por-fonte).
- **Rascunho local** — cópia do que você está preenchendo num formulário longo (como o cadastro de projeto), guardada automaticamente no seu dispositivo para sobreviver a um fechamento acidental. Some quando o cadastro é concluído; não é enviada ao servidor nem visível a outra pessoa. Ver [Sair no meio do cadastro não perde o preenchimento](#rascunho-do-cadastro-de-projeto).

## Por onde seguir

- **Movimentações** — onde os lançamentos vivem; o financeiro do projeto se apoia neles. Ver [De qual dinheiro sai este lançamento](/modulos/movimentacoes/#de-qual-dinheiro-sai-este-lancamento), [Baixa em lote com lançamentos de projetos diferentes](/modulos/movimentacoes/#baixa-em-lote-projetos-diferentes) e [Atribuir projeto a vários lançamentos de uma vez](/modulos/movimentacoes/#atribuir-projeto-em-lote).
- **Configurações → Contas Bancárias** — para definir o [projeto e o centro de custo padrão de uma conta](/configuracoes/contas/#projeto-e-centro-de-custo-padrao-da-conta).
- **Reembolsos** e **Pedidos de Compra e Pagamento** — os fluxos que o botão "Registrar despesa do projeto" aciona; a mesma pergunta de fonte e item aparece ali.
- **Relatórios** — agora com filtro por projeto.
- **Saúde 360** — onde a saúde de todos os projetos aparece de relance.
- **Papéis e Permissões** — para entender o papel de Coordenador de Projeto na OSC.
- **Documentos** — onde toda prestação de contas por fonte já emitida fica guardada. Ver [Documentos → Tipos de documento cobertos](/modulos/documentos/#tipos-de-documento-cobertos).
- **Configurações → Contas Bancárias** — o atalho para emitir a prestação de uma fonte com conta exclusiva a partir da lista de contas.
