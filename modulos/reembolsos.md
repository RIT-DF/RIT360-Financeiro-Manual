---
title: "Reembolsos"
nav_order: 4
parent: "Módulos"
permalink: /modulos/reembolsos/
---

O módulo de **Reembolsos** é onde voluntários, dirigentes e colaboradores **pedem de volta o dinheiro que tiraram do próprio bolso** para comprar alguma coisa em nome da OSC — combustível do voluntário que levou o material para o evento, lanche da reunião pago pela secretária, papelaria comprada pela coordenadora porque acabou no dia.

> Acesse pelo menu **Pagamentos e Reembolsos → aba Reembolsos**.

> 💡 **Por que isso importa**
>
> Reembolso parece uma operação simples — "fulano gastou, OSC paga de volta" — mas é o ponto onde **mais coisas dão errado em OSC sem controle**: gente que reembolsou e ninguém anotou, comprovante que sumiu, valor que ficou maior do que combinado, dirigente que aprovou para si mesmo sem registro. O módulo de Reembolsos resolve isso com um fluxo simples: **quem pediu, quem aprovou, quanto, com qual comprovante, e quando foi pago — tudo registrado, com auditoria**. Resultado: voluntário recebe rápido, a OSC tem transparência, a diretoria dorme em paz.

## Conceitos essenciais

> 📖 **Conceito · Reembolso ≠ Pedido de Compra e Pagamento**
>
> **Reembolso** é para despesa que **já aconteceu**: alguém gastou do bolso e quer receber de volta. **Pedido de Compra e Pagamento** é para despesa que **vai acontecer**: a OSC vai pagar uma conta de luz, um fornecedor, um boleto. Os dois fluxos têm aprovação, mas a lógica é diferente: no reembolso o dinheiro entrou no caixa de quem pagou, ele só quer ser ressarcido; no pedido o dinheiro ainda está na OSC, e a aprovação autoriza a saída. Use **Reembolso** quando a nota fiscal está em nome de uma pessoa física e o pagamento já aconteceu. Use **Pedido de Compra e Pagamento** quando o pagamento ainda vai ser feito (geralmente em nome da OSC).

> 📖 **Conceito · Quórum e papéis aprovadores**
>
> A OSC configura em **Configurações → Fluxo de Aprovações** quantos votos são necessários para aprovar um reembolso (1 ou 2) e quais papéis podem votar (Presidente, Diretor de Finanças, etc.) — opcionalmente também pessoas específicas além do papel. Com quórum **1**, o primeiro aprovador elegível que vota define a decisão. Com quórum **2**, são necessários dois votos positivos. A organização configura também **quantas reprovações barram** o reembolso (padrão: **1**) — com o padrão, se um aprova e outro rejeita, prevalece a rejeição; ver [Rejeitado](#rejeitado). Solicitantes não votam nos próprios reembolsos (o RIT360 Financeiro bloqueia automaticamente quando há outros elegíveis).

> 📖 **Conceito · Auto-aprovação**
>
> Em OSCs pequenas, pode acontecer de o único aprovador elegível ser o próprio solicitante (ex: o presidente é também o único diretor financeiro e foi ele quem fez a compra). Nesses casos, o RIT360 Financeiro **permite a auto-aprovação** — caso contrário o fluxo trava — mas **marca explicitamente o evento** no histórico de auditoria como `self_approved`. A diretoria e auditoria conseguem identificar essas situações com filtro e responder se houve abuso. Conforme a OSC cresce, novos papéis aprovadores são cadastrados e auto-aprovações naturalmente diminuem.

> 📖 **Conceito · Status do reembolso**
>
> O ciclo de vida normal é **Rascunho → Aguardando aprovação → Aprovado → Pago**. **Rejeitado** é desvio do caminho aprovado — mas o solicitante pode editar e reenviar quantas vezes precisar. **Cancelado** é o desvio que o próprio solicitante escolhe — ver [Retirar uma solicitação enviada](#retirar-solicitacao), abaixo.

| Status | Significado |
|---|---|
| ⬜ **Rascunho** | Salvo mas não enviado — só o solicitante vê |
| 🟡 **Aguardando aprovação** | Enviado, esperando voto dos aprovadores elegíveis |
| 🟢 **Aprovado** | Aprovado, aguardando confirmação de pagamento pelo tesoureiro |
| 🔴 **Rejeitado** | Reprovado com motivo registrado — pode ser editado e reenviado |
| 💙 **Pago** | Pagamento confirmado; movimentação financeira correspondente está em Movimentações |
| ⬛ **Cancelado** | Retirado pelo próprio solicitante antes de ser aprovado — pode ser enviado de novo, mesmo sem alterar nada |

## Lista de reembolsos

[![Lista de reembolsos](/assets/screenshots/manual-05-reembolsos-lista.png)](/assets/screenshots/manual-05-reembolsos-lista.png)
*Lista de reembolsos em desktop*

[![Reembolsos no celular](/assets/screenshots/mobile-reembolsos.png)](/assets/screenshots/mobile-reembolsos.png)
*Reembolsos no celular — cards de resumo em grade 2×2, sub-abas roláveis horizontalmente e lista em cards verticais*

A lista mostra todos os reembolsos da organização. Cada papel vê um recorte diferente:

- **Presidente, Tesoureiro e demais aprovadores** veem **todos** os reembolsos da OSC
- **Voluntários e solicitantes não-aprovadores** veem **apenas os próprios**

Cada aba mostra a contagem entre parênteses (ex: "Aguardando aprovação (3)") — útil para ver rapidamente o que está pendente.

### Ao abrir Pagamentos e Reembolsos, você já cai na fila certa {#aterrissagem-na-fila}

[![As duas abas de Pagamentos e Reembolsos, Pedidos de compra e pagamento e Reembolsos, cada uma mostrando quantas solicitações aguardam a aprovação da pessoa logada](/assets/screenshots/pagamentos-fila-abas-contagem.png)](/assets/screenshots/pagamentos-fila-abas-contagem.png)
*Cada aba do topo mostra quantas solicitações aguardam especificamente a sua aprovação — aqui, 1 pedido e 3 reembolsos*

Se você é aprovador e tem solicitações esperando o seu voto, clicar em **Pagamentos e Reembolsos** no menu já abre direto na aba **Aguardando aprovação** — sem precisar navegar até lá. Isso vale **entre as duas abas do módulo**: se as suas pendências estão em Reembolsos, você cai lá mesmo que o link tenha vindo de um contexto de Pedidos de Compra e Pagamento, e vice-versa. Sem nada para aprovar, a tela abre normalmente na lista geral.

Cada uma das duas abas do topo (Pedidos de Compra e Pagamento, Reembolsos) mostra, ao lado do nome, **quantas solicitações aguardam a sua aprovação naquele módulo especificamente** — é esse número, e não a contagem geral da aba interna "Aguardando aprovação (3)", que responde "o que sobrou para eu resolver".

> ⚠️ **Atenção · Se a tela não conseguir confirmar que você é aprovador**
>
> Checar se você está apto a aprovar depende de consultar o servidor. Quando essa checagem falha — problema passageiro de rede, por exemplo —, a tela avisa que **não conseguiu confirmar** e oferece **tentar novamente**, em vez de simplesmente não mostrar a fila nem os botões de aprovar (o que antes parecia dizer "não há nada para aprovar", quando na verdade a checagem é que tinha falhado). Se isso persistir depois de tentar de novo, é queda de conexão ou instabilidade do servidor, não falta de permissão — atualize a página ou tente mais tarde.

> 💡 **A lista carrega por página.** Em organizações com muitos reembolsos, a tela não traz o histórico inteiro de uma vez — ela carrega aos poucos, conforme você navega. Os **filtros continuam valendo sobre o conjunto inteiro**, não só sobre a página aberta: filtrar por período ou por status busca em todos os reembolsos da organização, não só nos que já apareceram na tela.

**Colunas (desktop):** Data da despesa, Descrição, Valor, Status, Solicitante, Ações. Quando o reembolso já tem um lançamento vinculado (aprovado ou pago), o código curto desse lançamento aparece abaixo da descrição — útil para localizá-lo rapidamente em Movimentações.

No **celular**, a lista vira **cards verticais** otimizados para toque, com toda a informação empilhada — descrição em destaque, valor à direita, data da despesa, solicitante, badge de status e botões de aprovar/reprovar quando aplicável. Sem precisar rolar lateralmente para ver o status ou as ações. Mesmo padrão usado em Movimentações e Pedidos de Compra e Pagamento.

Nas abas **Aprovado** e **Pago** há um filtro de período (mês atual, mês anterior, trimestre, ano etc.), igual ao de Movimentações, sempre aberto no **mês atual** por padrão. As abas **Aguardando aprovação**, **Rascunho** e **Rejeitado** não usam esse filtro — mostram sempre tudo, para nada que precise da sua atenção ficar escondido fora do período selecionado.

### Cards de resumo no topo

Acima das abas de filtro de status, aparecem até quatro cards de resumo, exibidos **conforme o seu papel** (você só vê os que fazem sentido para você). Cada card é um **atalho clicável** para a lista filtrada correspondente. Útil para responder de relance: "o que precisa de atenção agora?".

- **Aguardando aprovação** — aparece para quem é aprovador elegível (Presidente, Tesoureiro e demais papéis configurados); conta os reembolsos da OSC que estão **na fila de aprovação** (não só os que dependem de você — a aprovação é por quórum e papel).
- **Aprovados aguardando pagamento** — aparece para o Tesoureiro e Administrador; conta reembolsos com status Aprovado que ainda não viraram movimentação paga.
- **Solicitado no período** — sempre visível; conta reembolsos submetidos no mês corrente.
- **Pago no período** — sempre visível; conta reembolsos pagos no mês corrente.

> ℹ️ **O card "Aguardando aprovação" mostra o mesmo número da aba de mesmo nome** — os reembolsos da OSC na fila de aprovação. Ele **não** é uma "fatia pessoal": como a aprovação é por **quórum e papel**, qualquer aprovador elegível pode votar. Para saber o que já foi votado e quanto falta, abra o **detalhe** de cada reembolso — lá aparece o progresso ("1 de 2 aprovações · falta 1").

### Ações inline na lista

Nas linhas com status "Aguardando aprovação", aprovadores elegíveis veem os botões ✓ **Aprovar** e ✕ **Rejeitar** diretamente na linha — para resolver pendências rápidas sem entrar no detalhe. O dialog de cada ação pede um campo: opcional para aprovar (comentário), obrigatório para rejeitar (motivo).

> ✓ **Dica · Use a aba "Aguardando aprovação" como caixa de entrada**
>
> Se você é aprovador, faça da aba "Aguardando aprovação" sua rotina diária de 5 minutos. Reembolso aprovado rápido é diferencial de OSC bem gerida — voluntário não fica de pires na mão esperando duas semanas para receber R$ 60 de combustível.

### Aprovar vários de uma vez {#selecao-em-lote}

Quando há muitos reembolsos aguardando aprovação — depois de um evento grande, por exemplo —, aprovar um a um consome a manhã inteira. Marque o checkbox de cada linha que você já conferiu e decidiu aprovar; uma barra de ações aparece no rodapé da lista:

[![Barra de ações em lote, com dois reembolsos selecionados](/assets/screenshots/reemb-selecao-lote.png)](/assets/screenshots/reemb-selecao-lote.png)
*"2 itens selecionados nesta página · Total R$ 106,78" e o botão "Aprovar selecionados"*

Antes de confirmar, a barra já mostra **quantas solicitações** e **o valor total** que você está prestes a aprovar de uma vez — a última chance de conferir antes do clique. Depois de confirmar, o resultado vem **item por item**: quem foi aprovado normalmente e quem, por algum motivo (por exemplo, alguém votou primeiro noutra aba), não pôde ser.

> ⚠️ **Atenção · Reprovar continua sendo um de cada vez**
>
> Só a **aprovação** tem seleção em lote. Reprovar exige entrar em cada reembolso, porque **cada reprovação pede um motivo próprio** — motivo genérico aplicado a vários de uma vez não ajuda ninguém a corrigir o que foi apontado. Reserve o lote para o que você já examinou e decidiu aprovar; o que tem ressalva, resolva um a um.

> ⚠️ **Atenção · A seleção vale só para a página aberta**
>
> Marcar itens não atravessa página, aba nem período: trocar qualquer um desses **limpa a seleção**. Selecione, aprove, e só então mude de página ou de filtro.

## Detalhe do reembolso

Clique em qualquer linha para abrir o detalhe completo. A página tem todas as informações necessárias para tomar uma decisão de aprovação consciente — sem precisar perguntar nada para ninguém.

### Rascunho

Abra um reembolso salvo como rascunho para ver os botões **Editar rascunho** e **Excluir rascunho**, lado a lado.

Ao clicar em **Excluir rascunho**, a confirmação mostra qual solicitação será apagada, o valor, quantos anexos vão junto, e avisa que os dados bancários guardados nela também serão removidos. **A exclusão é definitiva** — não tem como recuperar um rascunho depois de excluído. Vale igualmente para pedidos de compra e pagamento (ver [Pedidos de Compra e Pagamento → Rascunho](/modulos/pedidos-pagamento/#rascunho)).

### Aguardando aprovação

[![Reembolso aguardando aprovação](/assets/screenshots/manual-06-reembolso-aguardando.png)](/assets/screenshots/manual-06-reembolso-aguardando.png)
*Detalhe de reembolso aguardando aprovação*

- **Valor, Solicitante e Data da despesa** no topo
- **Status** em destaque no canto superior direito
- **Dados da solicitação**: descrição, categoria (sempre tipo despesa), projeto, centro de custo
- **Dados de pagamento**: método (PIX ou TED) e chave/conta — **visíveis apenas para aprovadores e tesoureiro** (voluntário não-aprovador vê só os próprios)
- **Comprovantes**: nota fiscal, recibo ou foto da despesa anexados pelo solicitante, com pré-visualização inline para imagens e PDFs (não precisa baixar) — visíveis apenas para quem já enxerga esta solicitação, ver [Movimentações → Quem consegue abrir um comprovante](/modulos/movimentacoes/#anexos-e-comprovantes)
- **Histórico de aprovações**: timeline de todos os votos com nome, papel e data, além do **progresso do quórum** (ex.: "1 de 2 aprovações · falta 1") enquanto o reembolso aguarda aprovação
- **Ações**: ✓ Aprovar / ✕ Rejeitar (somente para aprovadores; nunca para o próprio solicitante) · **Retirar solicitação** (somente para quem enviou — ver abaixo)

> 💡 **Por que isso importa**
>
> A timeline de aprovações é mais que registro contábil. É **proteção institucional**: meses depois, se alguém questionar "quem aprovou esse reembolso de R$ 800 do diretor?", a resposta está lá — quem votou, em qual data, com qual comentário. Em OSC com mudança rotativa de diretoria (eleição anual, troca de tesoureiro), esse registro é a diferença entre passagem de bastão tranquila e arenas de acusação.

### Retirar uma solicitação enviada {#retirar-solicitacao}

[![Painel de Ações com o botão Retirar solicitação](/assets/screenshots/reemb-retirar-solicitacao.png)](/assets/screenshots/reemb-retirar-solicitacao.png)
*O botão "Retirar solicitação" aparece junto com "Aprovar" para quem enviou o reembolso*

Antes desta versão, quem enviava um reembolso e mudava de ideia **não tinha saída**: excluir só funcionava em rascunho, e depois de enviado, a única forma de encerrar era pedir para alguém reprovar — o que ficava registrado como **reprovação**, não como desistência, e exigia envolver um aprovador para algo que era só seu de decidir.

Agora, enquanto o reembolso está **Aguardando aprovação**, quem o enviou vê o botão **Retirar solicitação** no painel de Ações. Ao retirar:

- o reembolso passa para **Cancelado**;
- qualquer aprovação que já tinha sido dada é **descartada** — não fica pendurada, como se nunca tivesse existido;
- quem estava na fila de aprovação (e ainda não tinha votado) é **avisado** de que a solicitação saiu da fila.

> 💡 **Por que isso importa**
>
> Nem toda desistência é reprovação. Pedir a alguém que reprove um reembolso que você mesmo já não quer mais é constrangedor para as duas partes, e distorce a estatística de reprovações da OSC — a auditoria vê um reembolso "reprovado" que na verdade nunca teve nada de errado, só deixou de fazer sentido. Retirar é o botão certo para "mudei de ideia"; reprovar é para "isto aqui não pode passar assim".

> ✓ **Dica · Retirado pode ser reenviado sem alterar nada**
>
> Diferente de um reembolso **rejeitado** — que exige corrigir algo de verdade antes de reenviar (ver [Rejeitado](#rejeitado)) —, um reembolso **retirado** por você pode ser reenviado **do jeito que estava**, porque não havia nada de errado nele: você só mudou de ideia sobre o momento, ou percebeu que ainda faltava um comprovante e quer organizar antes de reenviar por conta própria. A trava de "nenhuma alteração detectada" existe para impedir reenvio automático depois de uma **reprovação**, não depois de uma retirada.

> ⚠️ **Atenção · Só você retira a sua solicitação**
>
> Nem o Presidente, nem o Tesoureiro, nem quem tem a permissão de aprovar consegue retirar um reembolso de outra pessoa. Retirar é decisão de quem pediu — se alguém mais precisa encerrar a solicitação de outra pessoa, o caminho continua sendo a reprovação, com o motivo registrado.

### Rejeitado {#rejeitado}

[![Reembolso rejeitado](/assets/screenshots/manual-06b-reembolso-rejeitado.png)](/assets/screenshots/manual-06b-reembolso-rejeitado.png)
*Detalhe de reembolso rejeitado*

O motivo da rejeição aparece em destaque no topo da página, e também fica registrado na timeline do **histórico de aprovações**, com o nome de quem reprovou e a data. O solicitante (e somente o solicitante) vê o botão **Editar e reenviar** — clicando, os campos passam a ser editáveis na própria página, sem precisar criar um reembolso novo. Corrige o que foi apontado (valor errado, comprovante ausente, categoria trocada), reenvia, e o fluxo recomeça.

> ⚠️ **Atenção · Chave PIX/dados bancários já salvos aparecem protegidos**
>
> Se a chave PIX ou os dados bancários já estavam preenchidos, o campo aparece **bloqueado** na edição: mostra só uma parte do valor, a etiqueta **Protegido**, e um botão **Substituir** — salvar sem tocar nele não muda o que está guardado. Esvaziar um campo protegido pede confirmação, porque a remoção é definitiva. O mesmo vale para pedidos de compra e pagamento e para a edição de um lançamento em Movimentações — ver [Movimentações → Editar um lançamento → Dados bancários protegidos](/modulos/movimentacoes/#dados-bancários-protegidos).

> 📖 **Conceito · Quantas reprovações barram o reembolso**
>
> Aprovar e reprovar têm **contas separadas**, ambas configuradas em [Fluxo de Aprovações](/configuracoes/aprovacoes/). O quórum diz quantas aprovações **liberam**; o ajuste de **reprovações necessárias** diz quantas **barram**. Este último vem configurado como **1** — ou seja, no padrão, **uma única reprovação encerra o reembolso na hora**, mesmo que já houvesse uma aprovação registrada, e os demais aprovadores não votam mais. É o comportamento de sempre.
>
> A organização pode **exigir mais de uma reprovação** (até o número de pessoas aptas a aprovar). Nesse caso, enquanto o número exigido não é alcançado, o reembolso **continua Aguardando aprovação** e os demais aprovadores seguem podendo votar; a tela mostra **quantas reprovações já existem e quantas faltam**. O **solicitante só é avisado no desfecho definitivo** — reprovação isolada não gera aviso para ele. Se em algum momento não restarem pessoas suficientes sem voto para reunir as aprovações necessárias, o reembolso é **encerrado como reprovado** em vez de ficar parado. Havendo mais de uma reprovação, o motivo mostrado ao solicitante **reúne os motivos de todos os votos contrários**.
>
> O motivo é sempre **obrigatório** ao reprovar, e **o voto é definitivo** — a tela avisa isso antes de confirmar, tanto para aprovar quanto para reprovar. Mudou de ideia? O caminho é o solicitante corrigir e reenviar.
>
> Válido tanto para **Reembolsos** quanto para **Pedidos de Compra e Pagamento** — os dois fluxos seguem a mesma regra.

> ⚠️ **Atenção · Reenviar exige mudar algo de verdade**
>
> Reenviar sem alterar nada é recusado, com a mensagem **"Nenhuma alteração detectada. Corrija a solicitação antes de reenviar."** — assim o mesmo pedido não volta para a fila de aprovação repetidamente sem que nada tenha sido corrigido. Conta como alteração: valor, descrição, data da despesa, categoria, projeto, centro de custo, dados de pagamento, observações — **e também incluir ou remover um comprovante**. Na prática, esse costuma ser o único ajuste necessário: quando o motivo da rejeição foi "faltou a nota fiscal", basta anexar o comprovante e reenviar — já é alteração suficiente.

> ⚠️ **Atenção · O reenvio reinicia as aprovações**
>
> Ao reenviar, o histórico de votos deste pedido **recomeça do zero** — mesmo quem já tinha aprovado antes da rejeição precisa aprovar de novo. Não é óbvio à primeira vista, mas segue a mesma lógica: cada rodada de aprovação avalia a versão atual do pedido, e a versão mudou.

> ⚠️ **Atenção · Rejeição não é punição**
>
> Os motivos mais comuns de rejeição em OSC bem geridas são **práticos**, não pessoais: comprovante ilegível, valor sem nota, categoria que não bate. Quando rejeitar, **escreva motivo concreto e instrucional** ("anexar nota fiscal", "ajustar categoria para Combustível"), não vago ("revisar"). O solicitante reedita e reenvia em 2 minutos; conflito desnecessário evitado.

### Aprovado, aguardando pagamento

[![Reembolso aprovado](/assets/screenshots/manual-06c-reembolso-aprovado.png)](/assets/screenshots/manual-06c-reembolso-aprovado.png)
*Detalhe de reembolso aprovado, aguardando confirmação de pagamento*

Painel de Ações mostra: **"Aprovado — aguardando confirmação de pagamento pelo tesoureiro."**

> 📖 **Conceito · Aprovado vira movimentação pendente automaticamente**
>
> No momento em que o reembolso é aprovado, o RIT360 Financeiro cria automaticamente uma **movimentação financeira pendente** em Movimentações com origem `reimbursement` (origem reembolso), valor e categoria corretos, ainda sem conta financeira definida. Cabe ao tesoureiro entrar em Movimentações, clicar nessa linha, escolher a conta de onde o dinheiro vai sair e marcar como paga. O ciclo só fecha quando essa confirmação acontece. Os comprovantes anexados ao reembolso **vão junto com o lançamento** — o tesoureiro confere o documento direto ali, na aba Documentos, sem precisar abrir a solicitação original. O lançamento também traz um link **"Ver pedido de reembolso →"**, útil quando o que falta conferir é o histórico de aprovações ou outro dado da solicitação, não o comprovante.

> 📖 **Conceito · Corrigir o centro de custo depois do envio**
>
> Se o reembolso já foi enviado — inclusive aprovado ou pago — e o centro de custo ficou errado, quem faz a gestão financeira da OSC corrige direto no detalhe do reembolso, ao lado do campo **Centro de custo**, botão **Corrigir**. A tela mostra antes o que será alterado (a solicitação e quantos lançamentos gerados por ela) e pede um motivo, que fica na trilha de auditoria. A correção alcança os lançamentos já criados, inclusive os pagos. O mesmo mecanismo vale para pedidos de compra e pagamento — ver [Pedidos de Compra e Pagamento → Corrigir o centro de custo depois do envio](/modulos/pedidos-pagamento/#corrigir-o-centro-de-custo-depois-do-envio).

### Pago

Quando o tesoureiro marca a movimentação financeira correspondente como paga, o reembolso aqui muda automaticamente para **Pago** (💙). O solicitante recebe notificação pelos canais que configurou no perfil. Ciclo encerrado.

Marcar como pago exige a permissão de **pagar**, separada da de criar e editar lançamentos — ver [Cargos e permissões](/configuracoes/cargos/#permissao-pagar).

> ⚠️ **Atenção · Seus dados bancários são apagados depois do pagamento**
>
> Depois que o reembolso é pago, a chave Pix / dados bancários que você informou ficam guardados apenas pelo prazo que a sua OSC definiu (30, 90, 180 ou 365 dias — padrão 90). Passado esse prazo, **CPF do titular, chave Pix, banco, agência e conta são apagados automaticamente**; o reembolso continua no histórico com valor, descrição, datas, comprovantes, aprovações e o seu nome. Por isso, um reembolso antigo pode aparecer sem os dados de pagamento — **não é erro**. Enquanto o reembolso **não** foi pago, os dados são preservados, para que a OSC consiga transferir. Ver [Contas Bancárias → Dados bancários de quem recebe](/configuracoes/contas/#dados-bancarios-de-quem-recebe).
>
> Se você pedir a **exclusão da sua conta**, os dados bancários dos seus reembolsos **já pagos** são apagados junto; os ainda não pagos seguem o prazo normal.

## Nova solicitação de reembolso

[![Nova solicitação de reembolso](/assets/screenshots/manual-06d-novo-reembolso.png)](/assets/screenshots/manual-06d-novo-reembolso.png)
*Formulário de nova solicitação em desktop*

[![Nova solicitação de reembolso no celular](/assets/screenshots/mobile-novo-reembolso.png)](/assets/screenshots/mobile-novo-reembolso.png)
*Formulário no celular — destaque para o botão **Tirar foto** que abre a câmera traseira direto, e a barra de ações fixa no rodapé ("Cancelar / Salvar rascunho / Enviar para aprovação") ao alcance do polegar*

Clique em **+ Nova solicitação** para abrir o formulário.

**Campos obrigatórios:**

- **Data da despesa** — quando você efetivamente gastou
- **Valor** — total a ser reembolsado
- **Descrição** — o que foi comprado e para qual atividade (seja específico: "Combustível para transporte do material do bazar no sábado" vence "gasolina")
- **Forma de pagamento**: **PIX** ou **TED**, com a chave/dados bancários onde quer receber
- **Documentos**: nota fiscal, recibo, comprovante de pagamento ou foto da despesa

**Campos opcionais:**

- **Categoria** — sempre do tipo despesa (o RIT360 Financeiro só lista despesas aqui, não confunde com receita)
- **Projeto** e **Centro de custo** — para OSCs que separam o financeiro por iniciativa ou área. Quem é **Gestor de Centro de Custo** só vê, aqui, os centros que gerencia — ver [Papéis e Permissões → Gestor de Centro de Custo](/papeis/#gestor-de-centro-de-custo)
- **Observações** — contexto adicional para o aprovador

> ✓ **Dica · Configure dados de pagamento no perfil**
>
> Os dados de pagamento (PIX/TED) são pré-preenchidos automaticamente se você configurou o **Método de pagamento padrão** em **Meu Perfil → Dados para Reembolso**. Configura uma vez, todo reembolso futuro já vem com chave correta — você não erra e não precisa redigitar.

**Botões de ação:**

- **Salvar rascunho** — guarda sem enviar; você pode editar e enviar quando estiver pronto (útil quando você está esperando chegar a nota por e-mail, por exemplo)
- **Enviar para aprovação** — envia para os aprovadores elegíveis; status muda para "Aguardando aprovação" e os aprovadores recebem notificação pelos canais configurados

## Boas práticas

> ✓ **Dica · Reembolso curto, comprovante claro**
>
> A diferença entre reembolso aprovado no dia e reembolso que volta para correção: **descrição específica + comprovante legível**. Tire foto do recibo com boa luz, descreva no campo Descrição **o que** foi comprado e **para qual atividade** ("Lanche da reunião de planejamento dia 15"), e o aprovador resolve em 30 segundos sem nenhuma pergunta extra.

> ✓ **Dica · Tire a foto pelo próprio app no celular**
>
> Em mobile, o formulário oferece dois botões na seção **DOCUMENTOS**: **Tirar foto** e **Anexar arquivo**. **Tirar foto** abre a câmera traseira do celular direto, sem passar pela galeria; você enquadra o cupom, captura, vê a foto em tamanho grande e decide entre **Refazer** ou **Confirmar**. Útil para registrar a despesa no momento do gasto (no posto, na loja, na hora). O RIT360 Financeiro reduz automaticamente o tamanho da foto antes do envio — fica leve para subir mesmo em conexão móvel ruim, sem perder a legibilidade do cupom. Tipos aceitos pelo botão **Anexar arquivo**: imagens, PDF, XML (NFe) e ZIP.

> ⚠️ **Atenção · Comprovante é obrigatório, sem exceção**
>
> Reembolso sem comprovante é ponto de risco contábil e jurídico. Mesmo em compra pequena de R$ 10 — anexe o cupom fiscal ou ao menos uma foto da nota com data e estabelecimento. Reembolsos sem comprovação adequada são **a fonte número um de questionamento** em prestação de contas para financiadores e auditorias do terceiro setor.

> ⚠️ **Atenção · Não reembolse despesa de terceiro**
>
> O reembolso é para a pessoa que **pagou de verdade**. Se você levou um voluntário ao posto e ele pagou, o reembolso é dele, não seu. Reembolsar despesa de terceiro vira "doação disfarçada" — confunde a contabilidade, viola dever fiduciário, prejudica auditoria. Quando você não puder reembolsar a pessoa certa diretamente (ela não tem conta bancária, etc.), use um **Pedido de Compra e Pagamento** em nome dela como prestador, com seu CPF.

> ✓ **Dica · Aprovador, leia os comprovantes**
>
> O RIT360 Financeiro mostra os comprovantes em pré-visualização inline justamente para que o aprovador veja antes de votar — sem precisar baixar ou abrir programa externo. Aprovar sem ver o comprovante anula a função do controle. Reserve os 30 segundos para conferir; depois aprove com tranquilidade.

## Notificações dos eventos de reembolso

Cada usuário escolhe em **Meu Perfil → Notificações** quais eventos de reembolso quer receber, e por quais canais (e-mail e push). Eventos cobertos:

- **Reembolso submetido** — aprovadores elegíveis são avisados
- **Aprovação parcial** — em quórum 2, depois do primeiro voto positivo, demais aprovadores elegíveis são lembrados
- **Aprovado** — solicitante e tesoureiro são avisados
- **Rejeitado** — solicitante é avisado com o motivo, **no desfecho definitivo**: quando a organização exige mais de uma reprovação, o aviso só sai depois que o número exigido é alcançado, reunindo os motivos de todos os votos contrários
- **Pago** — solicitante é avisado
- **Retirado** — quem ainda não tinha votado na solicitação é avisado de que ela saiu da fila de aprovação

Padrão é tudo ligado; cada um silencia o que não quer receber.

## Glossário rápido

- **Reembolso** — solicitação para receber de volta dinheiro gasto do próprio bolso em nome da OSC.
- **Quórum** — número mínimo de aprovações necessárias para o reembolso ser aprovado (configurável: 1 ou 2).
- **Reprovações necessárias** — número de votos contrários necessários para barrar o reembolso (configurável: de 1 até o total de pessoas aptas a aprovar; padrão 1).
- **Aprovador elegível** — usuário que pode votar em determinado reembolso pelo papel que ocupa ou por estar individualmente listado na configuração.
- **Auto-aprovação** — situação em que o solicitante é também o único aprovador elegível; permitida mas explicitamente marcada no audit log.
- **PIX/TED** — métodos de pagamento aceitos para crédito do reembolso aprovado.
- **Movimentação correspondente** — lançamento financeiro pendente criado automaticamente na aprovação, vinculado ao reembolso pelo campo origem.
- **Cancelado** — status de uma solicitação retirada pelo próprio solicitante antes da aprovação; diferente de rejeitado, pode ser reenviada sem precisar alterar nada.

## Por onde seguir

- **Pedidos de Compra e Pagamento** — para autorizar despesas que **ainda vão ser pagas** pela OSC (em vez de já ter pagado do bolso).
- **Movimentações** — para o tesoureiro confirmar o pagamento do reembolso aprovado e fechar o ciclo.
- **Meu Perfil → Dados para Reembolso** — para pré-preencher PIX/TED em futuras solicitações.
- **Configurações → Fluxo de Aprovações** — para a OSC ajustar quórum, reprovações necessárias e papéis aprovadores.
- **Meu Perfil → Notificações** — para escolher quais eventos receber e em quais canais.
