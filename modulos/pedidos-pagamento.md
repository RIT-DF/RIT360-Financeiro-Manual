---
title: "Pedidos de Compra e Pagamento"
nav_order: 5
parent: "Módulos"
permalink: /modulos/pedidos-pagamento/
---

O módulo de **Pedidos de Compra e Pagamento** é onde alguém da OSC **pede autorização** para pagar uma despesa **antes que o pagamento aconteça** — pagar o aluguel do salão, contratar o fornecedor do som do evento, quitar o boleto da energia. O fluxo tem aprovação por aprovadores elegíveis e termina com o tesoureiro confirmando o pagamento.

> Acesse pelo menu **Pagamentos e Reembolsos → aba Pedidos de Compra e Pagamento**.

> 💡 **Por que isso importa**
>
> Em OSC sem disciplina de pedido de compra e pagamento, **acontece de gente sair pagando contas sem combinar com a diretoria** — desconfiando do saldo, criando despesas que nem todos sabiam, gerando o famoso "como? alguém pagou isso?". O pedido de compra e pagamento resolve com fluxo simples: **antes de a OSC tirar dinheiro do caixa, alguém autoriza**. O autor da solicitação demonstra a despesa (descrição, fornecedor, comprovante), os aprovadores decidem com base em informação concreta, e o tesoureiro executa só o que foi autorizado. Resultado: controle sobre saídas, transparência, prevenção de despesas surpresa.

> 📖 **Conceito · Por que o nome mudou**
>
> O módulo se chamava só "Pedido de Pagamento" e servia bem a um caso: você já tem o boleto ou a nota em mãos e só precisa de autorização para pagar. Mas há um segundo caso comum em OSC — a organização **precisa comprar algo e ainda não sabe o preço final**: levanta orçamentos, pede autorização com base numa estimativa, e só depois negocia o valor efetivo com o fornecedor. O nome novo, **Pedido de Compra e Pagamento**, cobre os dois: a compra que ainda vai ser fechada e o pagamento já certo. O endereço da tela não mudou.

## Conceitos essenciais

> 📖 **Conceito · Pedido de Compra e Pagamento ≠ Reembolso**
>
> **Pedido de Compra e Pagamento** é para despesa que **ainda vai acontecer**: o dinheiro está na OSC e a aprovação autoriza que saia. **Reembolso** é para despesa que **já aconteceu**: alguém pagou do bolso e quer receber de volta. Use Pedido de Compra e Pagamento quando você tem a conta a pagar (boleto, fatura, nota de fornecedor) e o pagamento ainda não foi feito; o destinatário do dinheiro é o fornecedor/prestador, não você. Use Reembolso quando você já desembolsou e a conta está paga pelo seu CPF.

> 📖 **Conceito · Pedido único, recorrente ou parcelado**
>
> O RIT360 Financeiro permite três tipos de pedido de compra e pagamento, escolhidos no momento da solicitação:
>
> - **Único** — pedido avulso, uma vez (o caso mais comum: pagar uma fatura, contratar um serviço pontual)
> - **Recorrente** — gera uma série que se repete em intervalo regular (mensal, trimestral, anual, etc.). Útil para aluguel, mensalidade de internet, contrato de manutenção. A aprovação cria a série inteira; cada ocorrência é paga individualmente pelo tesoureiro.
> - **Parcelado** — divide um valor único em N parcelas com datas e valores ajustáveis. Útil para compras parceladas (equipamento em 6×, contrato fechado em prestações). A aprovação cria as parcelas todas de uma vez.
>
> A duração de uma série recorrente pode ser **por data final**, **por quantidade de ocorrências** ou **indefinida até cancelar**.

> 📖 **Conceito · Valor fechado ou valor estimado**
>
> Ao criar o pedido, você declara a **condição do valor** — o sistema nunca deduz isso pelo anexo:
>
> - **Valor fechado** — é o que vai ser pago. Use quando já tem o boleto, a nota ou o recibo em mãos. É a opção pré-selecionada, porque é o caso mais comum.
> - **Valor estimado** — a confirmar na compra. Use quando a OSC ainda vai negociar o preço final: você levanta orçamentos, **anexa os orçamentos ao pedido**, e pede autorização com base na estimativa. O financeiro negocia depois e registra o valor efetivo.
>
> A escolha muda o que a tela sugere anexar (orçamentos, no caso estimado; boleto ou nota, no fechado) e mostra um selo **"Valor estimado"** para quem aprova. Ver **Quando o valor pago diverge do autorizado**, abaixo, para o que acontece quando o valor negociado difere do que foi aprovado.

> 📖 **Conceito · Quórum e fluxo de aprovação**
>
> A OSC configura em **Configurações → Fluxo de Aprovações** quantos votos são necessários (1 ou 2), **quantas reprovações barram o pedido** (padrão: 1) e quais papéis podem aprovar. O solicitante nunca aprova o próprio pedido quando há outros aprovadores elegíveis — o RIT360 Financeiro bloqueia automaticamente. Quando o solicitante é o único aprovador (caso de OSCs muito pequenas), a auto-aprovação é permitida mas explicitamente registrada no audit log como `self_approved`.

> 📖 **Conceito · Status do pedido**
>
> O ciclo normal é **Rascunho → Aguardando aprovação → Aprovado → Pago**. **Rejeitado** é desvio do caminho aprovado — solicitante pode editar e reenviar. **Cancelado** é o encerramento do pedido por outro caminho: o solicitante o retirou antes da aprovação, ou o pedido aprovado foi [cancelado](#cancelar-pedido) — por quem cuida dos pagamentos ou automaticamente, quando um pagamento estornado deixou o pedido sem nada a pagar.

| Status | Significado |
|---|---|
| ⬜ **Rascunho** | Salvo mas não enviado — só o solicitante vê |
| 🟡 **Aguardando aprovação** | Esperando voto dos aprovadores elegíveis |
| 🟢 **Aprovado** | Aprovado; movimentação financeira pendente criada automaticamente |
| 🔴 **Rejeitado** | Reprovado com motivo registrado — pode ser editado e reenviado |
| 💙 **Pago** | Tesoureiro confirmou o pagamento na movimentação correspondente |
| ⬛ **Cancelado** | Encerrado sem pagamento. Aparece como **Retirado pelo solicitante** quando foi o próprio solicitante que o retirou antes da aprovação (pode ser enviado de novo, mesmo sem alterar nada); nos demais casos — cancelamento do pedido aprovado, ou pagamento estornado sem nada mais a pagar — aparece só como **Cancelado**, sem apontar ninguém |

## Lista de pedidos de compra e pagamento

[![Lista de pedidos](/assets/screenshots/manual-07-pedidos-lista.png)](/assets/screenshots/manual-07-pedidos-lista.png)
*Lista de pedidos de compra e pagamento em desktop*

A lista exibe todos os pedidos com colunas Descrição, Destinatário, Valor, Data da despesa, Solicitante e Status. Quando o pedido já tem um lançamento vinculado (aprovado ou pago), o código curto desse lançamento aparece abaixo da descrição — útil para localizá-lo rapidamente em Movimentações.

> ℹ️ **Se você é aprovador, abrir Pagamentos e Reembolsos já leva direto à fila** — inclusive quando as solicitações que esperam por você estão na aba Reembolsos, não nesta. Detalhe completo, com o porquê e o que fazer se a tela não conseguir confirmar que você pode aprovar, em [Reembolsos → Ao abrir Pagamentos e Reembolsos, você já cai na fila certa](/modulos/reembolsos/#aterrissagem-na-fila) — o mecanismo é idêntico para os dois módulos.

> 💡 **A lista carrega por página.** Em organizações com muitos pedidos, a tela não traz o histórico inteiro de uma vez — ela carrega aos poucos, conforme você navega. Os **filtros continuam valendo sobre o conjunto inteiro**, não só sobre a página aberta.

Nas abas **Aprovado** e **Pago** há um filtro de período (mês atual, mês anterior, trimestre, ano etc.), igual ao de Movimentações, sempre aberto no **mês atual** por padrão. As abas **Aguardando aprovação**, **Rascunho** e **Rejeitado** não usam esse filtro — mostram sempre tudo, para nada que precise da sua atenção ficar escondido fora do período selecionado.

### Pagar pedido aprovado pela lista {#pagar-pela-lista}

Pedido aprovado pode ser marcado como pago **direto na aba "Aprovado"**, sem precisar abrir o detalhe nem ir até Movimentações procurar o lançamento correspondente. A ação pede a **data do pagamento** e a **conta** de onde o dinheiro saiu, do mesmo jeito que já funciona [para reembolsos](/modulos/reembolsos/#pagar-pela-fila). Só vê o botão de pagar quem tem a [permissão de pagar](/configuracoes/cargos/#permissao-pagar) — a mesma já exigida no detalhe do pedido, que **continua funcionando** igual.

[![Aba Aprovado da lista de pedidos, com o ícone de pagar na coluna Ações de cada linha](/assets/screenshots/ped-pagar-pela-lista-desktop.png)](/assets/screenshots/ped-pagar-pela-lista-desktop.png)
*Aba "Aprovado" — o ícone de pagar aparece na coluna Ações de cada pedido, sem precisar abrir o detalhe*

No **celular**, os cards de resumo ficam em grade de 2 colunas e a lista de pedidos vira cards verticais otimizados para toque, com o mesmo botão de pagar:

[![Cards de pedidos aprovados no celular, cada um com o botão de pagar](/assets/screenshots/ped-pagar-pela-lista-mobile.png)](/assets/screenshots/ped-pagar-pela-lista-mobile.png)
*Aba "Aprovado" no celular — cada card traz o botão de pagar, sem precisar entrar no detalhe do pedido*

[![Pedidos de pagamento no celular](/assets/screenshots/mobile-pedidos-pagamento.png)](/assets/screenshots/mobile-pedidos-pagamento.png)
*Pedidos de compra e pagamento no celular — KPIs em grade 2×N e abas roláveis horizontalmente*

### Pagar vários pedidos de uma vez {#pagar-varios-de-uma-vez}

Na aba **Aprovado**, marque o checkbox de cada pedido que você já conferiu e vai pagar. No rodapé, o botão **"Marcar como pago (N)"** abre um diálogo em que você informa **a conta** e **a data do pagamento** uma única vez — em vez de repetir os dois campos pedido por pedido.

Cada pedido é pago **separadamente**: se um falhar no meio do lote, os que já foram pagos **continuam pagos**, e você pode interromper a qualquer momento sem perder o que já foi feito. Ao final, o resultado vem **item por item** — pago, recusado por regra (sem permissão de pagar, ou conta inativa diferente da do lançamento), com o motivo, ou falhou, também com o motivo. Pedido de projeto com financiador pode ainda sair pago com aviso de fonte ou item do plano de trabalho pendentes de escolha — ver [Projetos → De qual fonte e de qual item sai cada despesa](/modulos/projetos/#de-qual-fonte-e-item).

Funciona do mesmo jeito que já funciona para reembolsos — ver [Reembolsos → Pagar reembolso aprovado pela fila](/modulos/reembolsos/#pagar-pela-fila).

> ⚠️ **Atenção · Lote tem limite de itens**
>
> Selecionar um número muito grande de pedidos de uma vez trava o botão de pagar, com o aviso de quantos são permitidos por vez. Nesse caso, pague em duas levas: selecione uma parte, pague, e repita com o restante.

### Cards de resumo no topo

De acordo com seu papel, você vê cards que viram atalhos para as listas filtradas:

- **Aguardando aprovação** — para aprovadores (Presidente, Tesoureiro): pedidos na fila de aprovação da OSC (não só os que dependem de você)
- **Aprovados aguardando pagamento** — para o Tesoureiro
- **Solicitado por mim** — para todos os papéis

### Tipos visíveis na linha

Ao lado da descrição, badges discretos indicam o tipo do pedido:

- **Recorrente** — pedido que gerou série recorrente
- **Parcela X de N** — uma parcela específica de um pedido parcelado

Pedidos únicos aparecem sem badge adicional.

### Aprovar vários de uma vez

Marque o checkbox das linhas que você já examinou e decidiu aprovar para ver, no rodapé, quantas solicitações e qual o valor total antes de confirmar — o resultado sai item por item. Funciona exatamente como em Reembolsos; **reprovar continua sendo um de cada vez**, porque cada reprovação exige um motivo próprio. Detalhe completo em [Reembolsos → Aprovar vários de uma vez](/modulos/reembolsos/#selecao-em-lote).

## Detalhe do pedido

### Rascunho

Abra um pedido salvo como rascunho para ver os botões **Editar rascunho** e **Excluir rascunho**, lado a lado.

Ao clicar em **Excluir rascunho**, a confirmação mostra qual solicitação será apagada, o valor, quantos anexos vão junto, e avisa que os dados bancários guardados nela também serão removidos. **A exclusão é definitiva** — não tem como recuperar um rascunho depois de excluído. Use quando o pedido não faz mais sentido (por exemplo, a compra foi cancelada antes mesmo de pedir aprovação); se ainda faz sentido, prefira **Editar rascunho** e enviar quando estiver pronto.

### Aguardando aprovação

[![Pedido aguardando aprovação](/assets/screenshots/manual-08-pedido-aguardando.png)](/assets/screenshots/manual-08-pedido-aguardando.png)
*Detalhe de pedido aguardando aprovação*

[![Pedido de valor estimado aguardando aprovação, com o selo Valor estimado](/assets/screenshots/pedido-aprovacao-valor-estimado.png)](/assets/screenshots/pedido-aprovacao-valor-estimado.png)
*Pedido de valor estimado: o selo "Valor estimado" aparece junto ao valor, para quem vai aprovar decidir com essa informação em mãos*

- **Valor, Destinatário, Solicitante e Data da despesa** no topo
- **Tipo do pedido** (único / recorrente / parcelado) com configuração da série/parcelas, quando aplicável
- **Dados do pedido**: descrição, categoria, projeto, centro de custo
- **Dados de pagamento do destinatário** (PIX, TED ou Boleto) — visíveis apenas para aprovadores e tesoureiro
- **Documentos**: orçamento, nota fiscal, contrato ou outros anexos — visíveis apenas para quem já enxerga esta solicitação, ver [Movimentações → Quem consegue abrir um comprovante](/modulos/movimentacoes/#anexos-e-comprovantes)
- **Histórico de aprovações**: timeline de todos os votos, com o **progresso do quórum** (ex.: "1 de 2 aprovações · falta 1") enquanto o pedido aguarda aprovação
- **Ações**: ✓ Aprovar / ✕ Reprovar (somente para aprovadores; nunca para o próprio solicitante) · **Retirar solicitação** (somente para quem enviou — ver abaixo)

Pedidos recorrentes mostram aqui uma seção **Ocorrências** com a lista de cada ocorrência prevista, seu status individual e ações específicas (marcar como pago, cancelar essa ocorrência, ver movimento gerado).

### Retirar uma solicitação enviada

Enquanto o pedido está **Aguardando aprovação**, quem o enviou pode clicar em **Retirar solicitação** para encerrá-lo sem depender de ninguém reprovar. O pedido passa para **Cancelado**, qualquer aprovação já dada é descartada, e quem ainda não tinha votado é avisado de que ele saiu da fila. **Só quem solicitou retira** — nem administrador nem tesoureiro retiram pedido de outra pessoa. Diferente de um pedido **rejeitado**, um pedido **retirado** pode ser reenviado sem precisar alterar nada, porque não havia nada de errado nele. Detalhe completo, com o porquê e as armadilhas, em [Reembolsos → Retirar uma solicitação enviada](/modulos/reembolsos/#retirar-solicitacao) — o mecanismo é idêntico para os dois módulos.

### Rejeitado

[![Pedido rejeitado](/assets/screenshots/manual-08b-pedido-rejeitado.png)](/assets/screenshots/manual-08b-pedido-rejeitado.png)
*Detalhe de pedido rejeitado*

O motivo da rejeição aparece em destaque no topo, e também fica registrado na timeline do **histórico de aprovações**, com o nome de quem reprovou e a data. O solicitante pode editar os campos e reenviar para nova rodada de aprovação.

> ⚠️ **Atenção · Dados de pagamento do destinatário já salvos aparecem protegidos**
>
> Se a chave PIX ou os dados bancários do destinatário já estavam preenchidos, o campo aparece **bloqueado** na edição: mostra só uma parte do valor, a etiqueta **Protegido**, e um botão **Substituir** — salvar sem tocar nele não muda o que está guardado. Esvaziar um campo protegido pede confirmação, porque a remoção é definitiva. Detalhe completo, válido igualmente para reembolsos e para a edição de um lançamento em Movimentações, em [Movimentações → Editar um lançamento → Dados bancários protegidos](/modulos/movimentacoes/#dados-bancários-protegidos).

> 📖 **Conceito · Quantas reprovações barram o pedido**
>
> Aprovar e reprovar têm **contas separadas**, ambas em [Fluxo de Aprovações](/configuracoes/aprovacoes/): o quórum diz quantas aprovações **liberam**, e o ajuste de **reprovações necessárias** diz quantas **barram**. O padrão de reprovações é **1** — uma pessoa encerra o pedido na hora, mesmo que já houvesse uma aprovação registrada. Se a organização exigir **mais de uma**, o pedido **continua Aguardando aprovação** até o número ser alcançado, a tela mostra quantas faltam, e o solicitante só é avisado no desfecho definitivo. **O voto é definitivo** nos dois sentidos, e a tela avisa antes de confirmar. O reenvio, além disso, **exige uma alteração real** (trocar o comprovante já conta) e **reinicia as aprovações já dadas**. O detalhe completo, válido igualmente para pedidos de compra e pagamento e reembolsos, está em [Reembolsos → Rejeitado](/modulos/reembolsos/#rejeitado).

### Aprovado, aguardando pagamento

[![Pedido aprovado](/assets/screenshots/manual-08c-pedido-aprovado.png)](/assets/screenshots/manual-08c-pedido-aprovado.png)
*Detalhe de pedido aprovado, aguardando pagamento*

Painel de Ações mostra: **"Aprovado — aguardando confirmação de pagamento pelo tesoureiro."**, e quem tem a [permissão de pagar](/configuracoes/cargos/#permissao-pagar) vê aqui os mesmos campos de **data do pagamento** e **conta** que a lista pede — sem precisar sair do detalhe.

Há três caminhos para confirmar o pagamento, e todos levam ao mesmo lugar: pagar **direto aqui no detalhe**, [pagar pela lista](#pagar-pela-lista) na aba "Aprovado", ou pelo caminho mais antigo, abaixo, via Movimentações.

Se o pedido não vai mais ser pago — a compra foi desfeita, o fornecedor desistiu, o pedido foi aprovado por engano —, o botão **Cancelar pedido**, no alto da tela, encerra tudo de uma vez. Ver [Cancelar o pedido](#cancelar-pedido).

> 📖 **Conceito · Aprovado vira movimentação automaticamente**
>
> No momento da aprovação, o RIT360 Financeiro cria automaticamente a **movimentação financeira pendente** (ou várias, no caso de parcelado e recorrente) com origem `purchase_order` (pedido de compra e pagamento). O tesoureiro entra em Movimentações, escolhe a conta de saída e marca como paga — ou faz a mesma coisa em um passo só, [pagando pela lista](#pagar-pela-lista) ou aqui no detalhe. Cada ocorrência de uma série recorrente gera um movimento individual no momento programado, pago separadamente. Os comprovantes anexados ao pedido **vão junto com o lançamento** — aparecem direto na aba Documentos, sem precisar abrir o pedido original para conferir. O lançamento em Movimentações também tem o link **"Ver pedido de compra e pagamento →"**, útil para consultar o histórico de aprovações ou outros dados da solicitação.

> 📖 **Conceito · Confirmar o pagamento exige permissão própria**
>
> Marcar uma **parcela do pedido como paga** — assim como marcar um lançamento como pago — depende da permissão de **pagar**, separada da de criar e editar lançamentos. Quem não a tem acompanha o pedido normalmente, mas não dá baixa no pagamento. Ver [Cargos e permissões](/configuracoes/cargos/#permissao-pagar).

> ⚠️ **Atenção · Os dados bancários do destinatário têm prazo**
>
> No detalhe do pedido, **quem tem permissão de pagar vê os dados bancários por inteiro**; os demais veem apenas os últimos dígitos (o nome do destinatário fica visível para todos). E, passado o prazo que a OSC definiu, **esses dados são apagados automaticamente** depois que o pagamento é concluído — o pedido continua no histórico com valor, descrição, datas, anexos e o nome de quem recebeu. Ver [Contas Bancárias → Dados bancários de quem recebe](/configuracoes/contas/#dados-bancarios-de-quem-recebe).

### Quando o valor pago diverge do autorizado
{: #valor-diverge-do-autorizado }

O valor **autorizado** na aprovação fica guardado separado do valor **efetivamente lançado**. Isso importa sobretudo em pedido de **valor estimado**, mas vale para qualquer pedido cujo valor final saia diferente do que foi aprovado.

> 📖 **Conceito · Como o valor efetivo é registrado**
>
> Não existe tela própria para isso: o valor efetivo é registrado **editando o lançamento** gerado pelo pedido, como já era antes. Ao salvar um valor diferente do autorizado, o pedido mostra os dois lado a lado: **"Autorizado R$ X · lançado R$ Y — R$ Z acima (N%)"**.

**Exemplo:** a diretoria autoriza R$ 1.000 para reformar o telhado da sede, com base num orçamento estimado. O fornecedor fecha o serviço por R$ 1.500 — R$ 500 a mais, **50% acima** do autorizado. Se o limiar da OSC for o padrão de 10%, essa diferença passa longe do limite e o pagamento fica retido até alguém autorizar.

[![Pedido aprovado com o card Valor acima do autorizado](/assets/screenshots/pedido-valor-acima-do-autorizado.png)](/assets/screenshots/pedido-valor-acima-do-autorizado.png)
*"Autorizado R$ 1.000,00 · lançado R$ 1.500,00 — R$ 500,00 acima (50,0%)": o pedido continua aprovado, só o pagamento fica retido, e quem aprova decide entre autorizar a diferença, pedir outro aprovador ou recusar*

- **Dentro do limiar configurado pela OSC** (ver [Configurações → Fluxo de Aprovações → Limiar de reaprovação](/configuracoes/aprovacoes/#limiar-de-reaprovacao)): o lançamento é gravado normalmente, a diferença passa a aparecer no pedido, e **nada trava**.
- **Acima do limiar: o pagamento fica retido.** O pedido continua **aprovado** — o que trava é só o pagamento daquele lançamento.
  - Quem tem permissão de **aprovar** vê três botões: **Autorizar a diferença**, **Pedir autorização a outro aprovador** e **Recusar a diferença**.
  - Quem tem permissão de **pagar** mas não é aprovador vê **Pedir autorização do valor excedente** — os aprovadores são avisados, e o pagamento segue retido até alguém decidir.
  - Em qualquer um dos caminhos, **o motivo é obrigatório**.
- **Lançamento que já estava pago** quando o valor foi ajustado: não há pagamento a reter — fica só o registro da diferença.
- **Em pedido parcelado, o limiar vale sobre o total**, não parcela a parcela: o valor efetivo é a soma das parcelas lançadas.

> ⚠️ **Atenção · Recusar a diferença não paga o valor antigo automaticamente**
>
> Recusar mantém o pagamento retido — não volta o lançamento para o valor autorizado sozinho. Se o fornecedor não aceitar renegociar, ajuste o lançamento para o valor que de fato será pago (ou cancele e refaça o pedido) antes de tentar de novo.

> 💡 **Por que isso importa**
>
> O valor estimado dá agilidade para autorizar uma compra antes do preço fechado — mas sem limite, a aprovação original perderia o sentido: qualquer coisa poderia ser aprovada por um valor e paga por outro bem maior, sem ninguém revisar. O limiar é o equilíbrio: pequena variação (frete, arredondamento) passa direto; diferença grande volta para quem autorizou decidir se topa.

### Pedido vinculado a um financiador com plano de trabalho

Quando o pedido está vinculado a um projeto que tem um financiador com **plano de trabalho** (ver [Projetos → Plano de trabalho](/modulos/projetos/#plano-de-trabalho)), o pagamento continua acontecendo normalmente, mesmo que o valor passe do que foi aprovado para aquele item. O que aparece é um **aviso**, independente do cartão de valor acima do autorizado (seção anterior):

- **Acima do plano** — o valor deste pagamento faz o item do plano de trabalho passar do aprovado. O pedido mostra o aviso de risco de glosa, com o atalho para [registrar um remanejamento](/modulos/projetos/#plano-de-trabalho). Nada trava.
- **Fora do plano de trabalho** — a categoria da despesa não está associada a nenhum item do plano vigente daquela fonte. O pedido é pago e marcado como tal, com o atalho para incluir a categoria num item.

> ✓ **Dica · Estes dois avisos nunca retêm o pagamento**
>
> Diferente do aviso de **valor acima do autorizado** (seção anterior — esse sim pode reter, por decisão da própria OSC), acima do plano e fora do plano de trabalho são só avisos: o pagamento acontece, e a decisão de corrigir, remanejar ou aceitar o risco de glosa é sua, sem prazo.

Os cartões de valor acima do autorizado (seção anterior) e de plano de trabalho do financiador são **independentes**: um pedido pode ter mais de um aviso ao mesmo tempo.

### Corrigir o centro de custo depois do envio

Se o pedido já foi enviado — inclusive **aprovado** ou até **pago** — e o centro de custo ficou errado, quem faz a gestão financeira da OSC pode corrigir sem precisar reabrir ou cancelar nada. No detalhe do pedido, ao lado do campo **Centro de custo**, clique em **Corrigir**.

[![Corrigir centro de custo de um pedido já enviado](/assets/screenshots/ped-corrigir-centro-custo.png)](/assets/screenshots/ped-corrigir-centro-custo.png)
*Corrigir centro de custo: escolha o novo, informe o motivo, e a tela mostra antes o que vai mudar*

Escolha o **novo centro de custo** e escreva o **motivo da correção** (obrigatório) — ele fica guardado na trilha de auditoria, junto com o valor anterior e o novo. Antes de confirmar, a tela mostra o que será alterado: a própria solicitação e quantos lançamentos financeiros gerados por ela também vão mudar. A correção alcança os lançamentos já criados a partir deste pedido, **inclusive os que já foram pagos**.

### Cancelar o pedido {#cancelar-pedido}

[![Detalhe de um pedido aprovado com o botão Cancelar pedido desabilitado e a explicação logo abaixo](/assets/screenshots/ped-cancelar-pedido-desabilitado.png)](/assets/screenshots/ped-cancelar-pedido-desabilitado.png)
*Pedido aprovado em que não há mais nada a cancelar: o botão fica desabilitado e a tela diz por quê*

> 💡 **Por que isso importa**
>
> Um pedido aprovado cria lançamentos pendentes que ficam esperando pagamento — e continuam aparecendo na previsão e nas filas de quem paga. Se o pedido deixou de fazer sentido e você só apaga lançamento por lançamento, o pedido continua **Aprovado** (e a tela continua oferecendo pagar algo que não existe mais). **Cancelar o pedido** resolve tudo de uma vez e deixa o pedido no histórico como **Cancelado**, com o motivo guardado.

O botão **Cancelar pedido** fica no alto do detalhe, ao lado do status, e serve para qualquer tipo de pedido — **único**, **parcelado** ou **recorrente**. Ele **substituiu o antigo "Cancelar série"**: antes, um pedido de pagamento único não tinha como ser cancelado pela tela.

> 📖 **Conceito · Quem vê o botão e quando ele aparece**
>
> O botão aparece enquanto o pedido está **Aprovado**, para quem tem a [permissão de pagar](/configuracoes/cargos/#permissao-pagar) — quem decide pagar é quem pode decidir não pagar. Pedido que ainda aguarda aprovação não usa este botão: o solicitante o [retira](#retirar-uma-solicitação-enviada), ou os aprovadores o rejeitam.

**Para cancelar:**

1. Abra o pedido aprovado e clique em **Cancelar pedido**.
2. A confirmação diz **quantas ocorrências serão canceladas e quanto elas somam** — por exemplo, "Serão canceladas 12 ocorrências, somando R$ 1.800,00". Confira se é isso mesmo que você quer encerrar.
3. Escreva o **Motivo** (obrigatório) e clique em **Cancelar 12 ocorrências** (o número muda conforme o pedido). O motivo fica na trilha de auditoria.

[![Confirmação do cancelamento: 12 ocorrências somando R$ 1.800,00, aviso de que o pedido será encerrado e campo Motivo](/assets/screenshots/ped-cancelar-pedido-confirmacao.png)](/assets/screenshots/ped-cancelar-pedido-confirmacao.png)
*Confirmação única: quantas ocorrências, quanto somam, e o aviso de que não há volta*

> ⚠️ **Atenção · Não há como desfazer**
>
> A confirmação traz, em um quadro laranja, o aviso de que o **pedido inteiro será encerrado como cancelado, junto com a trilha de aprovação**, e de que não há como desfazer. Se você cancelou o pedido errado, a saída é **abrir um novo pedido e passar de novo pela aprovação** — o cancelado não volta. Por isso o motivo é obrigatório e a confirmação mostra o total antes: leia antes de confirmar.

**Só cancela o que ainda não foi pago.** Ocorrências já pagas ficam preservadas (auditoria). Por isso, quando o pedido **já tem pagamento registrado**, o botão fica **desabilitado** e a tela explica o caminho: *estorne o pagamento na tela de movimentações e depois cancele o pedido*. O botão também fica desabilitado quando **não há ocorrências canceláveis** (por exemplo, todas já foram canceladas).

#### Paguei por engano, e agora? {#paguei-por-engano}

Este é o caso que mais gera dúvida: o pedido foi aprovado, o pagamento foi confirmado — e não deveria ter sido. A ordem é sempre a mesma:

1. **Estorne o pagamento** em **Movimentações**, no lançamento que foi pago — ver [Estornar um lançamento](/modulos/movimentacoes/#estornar-um-lançamento). O estorno cria o lançamento contrário e preserva a história do que aconteceu.
2. **Se não sobrou nada a pagar no pedido, ele se encerra sozinho**, como **Cancelado**. É o caso típico de um pedido de pagamento único: pagou, estornou, acabou. Você não precisa fazer mais nada.
3. **Se ainda restam ocorrências pendentes** (um pedido parcelado ou recorrente em que só uma parcela foi paga por engano), o pedido continua **Aprovado** e o botão **Cancelar pedido** passa a funcionar — use-o para encerrar as parcelas restantes, ou deixe-as seguir se o resto do pedido continua valendo.

> ⚠️ **Atenção · Estornar não é cancelar, e não adianta tentar cancelar antes**
>
> Com pagamento registrado, o botão **Cancelar pedido** fica desabilitado de propósito. Excluir ou "apagar" o pagamento também não é o caminho: pagamento já feito só se reverte por **estorno**. Antes dessa mudança, o pedido ficava **Aprovado** (ou **Pago**, no caso do pagamento único) para sempre depois do estorno, oferecendo uma ação de pagamento que não funcionava — hoje ele se encerra sozinho quando não resta nada a pagar.

> ✓ **Dica · Pagou e vai pagar de novo?**
>
> Se o estorno foi para refazer o pagamento com outro valor, outra conta ou outro destinatário, abra um **novo pedido**: o cancelado não é reaproveitado, e o novo passa pela aprovação com as informações corretas.

#### Quando dá errado

| O que aparece | O que significa | O que fazer |
|---|---|---|
| Botão **Cancelar pedido** desabilitado: *"Há pagamento registrado neste pedido. Estorne o pagamento na tela de movimentações e depois cancele o pedido."* | Há pelo menos uma ocorrência paga e não estornada | [Estorne o pagamento](/modulos/movimentacoes/#estornar-um-lançamento) e volte ao pedido |
| Botão desabilitado: *"Não há ocorrências canceláveis."* | Todas as ocorrências já foram canceladas ou estornadas | Nada a cancelar. Se o pedido segue como **Aprovado** e você precisa pagar o fornecedor, abra um novo pedido |
| *"Este pedido não tem ocorrência a pagar: as ocorrências foram canceladas ou estornadas. Para pagar este fornecedor, abra um novo pedido."* (no painel **Ações**) | Mesmo caso acima, visto do lado de quem paga | Abra um novo pedido |
| *"Não foi possível conferir as ocorrências deste pedido. Recarregue a página."* | A tela não conseguiu consultar as ocorrências | Recarregue a página; se persistir, envie um [feedback](/enviar-feedback/) |
| *"O pedido não foi encerrado: N cancelada(s), N recusada(s) por regra, N com falha…"* (dentro da confirmação) | O cancelamento rodou **parcialmente**: algumas ocorrências foram canceladas e outras não, por regra do sistema ou por falha | Leia a mensagem que acompanha cada recusa, resolva o impedimento e clique em cancelar de novo — o pedido só se encerra quando não resta nenhuma ocorrência |

### Cancelar só uma ocorrência (recorrente / parcelado) {#cancelar-ocorrencia}

Para encerrar **apenas parte** de um pedido recorrente ou parcelado, use a lista de **Ocorrências** do detalhe: no menu **⋯** da linha, a opção **Cancelar esta ocorrência**. A janela pergunta o alcance:

- **Apenas este lançamento** — cancela só a parcela/ocorrência escolhida
- **Este e os próximos** — encerra a série a partir dali
- **Toda a série** — cancela tudo o que ainda está pendente

Ocorrências já pagas não podem ser canceladas (preservação de auditoria) — apenas estornadas via Movimentações. Cancelar **a última** ocorrência viva encerra o pedido inteiro, como se você tivesse usado **Cancelar pedido** — a janela avisa antes.

## Novo pedido de compra e pagamento

[![Novo pedido](/assets/screenshots/manual-08d-novo-pedido.png)](/assets/screenshots/manual-08d-novo-pedido.png)
*Formulário de novo pedido*

Clique em **+ Nova solicitação** para abrir o formulário.

### Condição do valor

[![Condição do valor no formulário de novo pedido](/assets/screenshots/pedido-condicao-do-valor.png)](/assets/screenshots/pedido-condicao-do-valor.png)
*Condição do valor: "Valor fechado" vem pré-selecionada; "Valor estimado" pede para anexar os orçamentos*

O primeiro campo do formulário pede para você escolher:

- **"Valor fechado — é o que vai ser pago"** — pré-selecionada. Você já tem o boleto, a nota ou o recibo em mãos.
- **"Valor estimado — a confirmar na compra"** — o preço final ainda vai ser negociado.

A escolha muda a dica de anexo (orçamentos, no estimado; boleto, nota ou recibo, no fechado) e aparece como selo **"Valor estimado"** para quem aprova, e no aviso de aprovação pendente. Ver **Quando o valor pago diverge do autorizado**, acima, para o que acontece depois — quando o valor negociado sai diferente do autorizado.

**Campos obrigatórios:**

- **Data da despesa** — a data da despesa em si (por exemplo, a data da nota fiscal)
- **Valor**
- **Destinatário** — nome do fornecedor ou prestador de serviços
- **Descrição** — o que está sendo pago e para qual finalidade
- **Dados de pagamento do destinatário**: PIX, TED ou Boleto (chave/conta/código de barras)

**Campos opcionais:** Categoria, Projeto, **Centro de custo**, Observações, Documentos (orçamento, nota fiscal, contrato) e, **apenas no tipo Único**, a **Data de pagamento solicitada**.

> 💡 **Centro de custo no pedido** (opcional): a lista traz **apenas os centros de custo ativos** da OSC — ou, para quem é **Gestor de Centro de Custo**, apenas os que a pessoa gerencia (ver [Papéis e Permissões → Gestor de Centro de Custo](/papeis/#gestor-de-centro-de-custo)). Escolher um vincula o pedido àquela área desde a origem — quando ele for aprovado e virar movimentação, o lançamento já nasce com o centro de custo certo, sem precisar corrigir depois. Deixar em branco é normal para quem não usa centros de custo. Os centros de custo são cadastrados em [Configurações → Categorias → Centros de custo](/configuracoes/categorias/#centros-de-custo).

> 💡 **Data de pagamento solicitada** (opcional, só no tipo Único): o prazo em que o fornecedor espera receber. Serve de **referência para o tesoureiro** na hora de pagar e aparece no detalhe do pedido. Deixá-la em branco não impede enviar o pedido.

> ⚠️ **Atenção · Dados são do destinatário, não do solicitante**
>
> No reembolso, a chave PIX é a sua. No Pedido de Compra e Pagamento, é a do **fornecedor**. Mesmo quando a descrição parece com a de um pedido anterior, **os dados de pagamento nunca vêm preenchidos automaticamente** — chave PIX, banco, agência, conta e CPF do destinatário precisam ser conferidos e informados a cada solicitação (ou cadastre o fornecedor nos seus contatos e copie). Erro nesses dados significa transferência para destino errado.

### Tipo do pedido (Único / Recorrente / Parcelado)

Toggle no formulário escolhe entre os três tipos. Para **Recorrente** ou **Parcelado**, campos adicionais aparecem:

- Recorrente: frequência (semanal, quinzenal, mensal, bimestral, trimestral, semestral, anual) + duração (data final / quantidade de ocorrências / indefinido até cancelar)
- Parcelado: tabela editável com data e valor de cada parcela; valor total = soma das parcelas

> ⚠️ **Atenção · Anexo é obrigatório no envio**
>
> Salvar como rascunho não exige anexo, mas **enviar para aprovação exige pelo menos 1 documento anexado**. O RIT360 Financeiro bloqueia o envio se faltar comprovante. Motivo: aprovação sem documento é aprovação no escuro — vira ponto de risco contábil. Sempre anexe a nota, contrato ou orçamento antes de enviar.

> ✓ **Dica · Foto direto pelo celular no momento do pedido**
>
> Em mobile, a seção **DOCUMENTOS** do formulário exibe dois botões: **Tirar foto** (abre a câmera traseira do celular direto, com preview **Refazer** ou **Confirmar** antes de subir) e **Anexar arquivo** (PDF, imagem, XML de NFe ou ZIP). O RIT360 Financeiro reduz a foto automaticamente antes do upload — fica leve mesmo em conexão ruim. Combina bem com o caso de uso de coordenador de projeto registrando o pedido de compra e pagamento ainda no fornecedor, com o orçamento na mão.

**Botões de ação:**

- **Salvar rascunho** — guarda sem enviar
- **Enviar para aprovação** — envia para aprovadores elegíveis (status muda para "Aguardando aprovação")

## Boas práticas

> ✓ **Dica · Pedido com 1 mês de antecedência poupa noite mal dormida**
>
> Aluguel vence dia 5? Crie o Pedido de Compra e Pagamento no dia 20 do mês anterior. Aprovadores votam com calma, tesoureiro programa o pagamento, ninguém entra em pânico no último dia. **Recorrência é seu aliado** — cria pedido de aluguel mensal recorrente uma vez, todo mês cai pra aprovação automaticamente.

> ✓ **Dica · Descrição clara economiza ida e volta**
>
> "Fornecedor X — Y" é vago. "Aluguel da quadra para treino dos novatos, mensal, contrato firmado em janeiro/2026" responde tudo. Aprovadores votam mais rápido quando a história está completa.

> ⚠️ **Atenção · Pagou sem aprovar? Volta no fluxo**
>
> Se a urgência levou alguém a pagar antes de ter aprovação, **registre como reembolso retroativo** (a pessoa pagou do bolso) e justifique a urgência. Não tente "burlar" criando um pedido de compra e pagamento de despesa que já foi paga em nome da pessoa. A confusão contábil que sai disso é maior que o ganho.

## Notificações dos eventos de pedidos

Cada usuário escolhe em **Meu Perfil → Notificações** quais eventos receber e por quais canais:

- **Pedido submetido** — aprovadores elegíveis são avisados
- **Aprovação parcial** — em quórum 2, após primeiro voto, demais aprovadores são lembrados
- **Aprovado** — solicitante e tesoureiro são avisados
- **Rejeitado** — solicitante é avisado com o motivo, **no desfecho definitivo**: quando a organização exige mais de uma reprovação, o aviso só sai depois que o número exigido é alcançado, reunindo os motivos de todos os votos contrários
- **Pago** — solicitante é avisado
- **Retirado** — quem ainda não tinha votado na solicitação é avisado de que ela saiu da fila de aprovação

## Glossário rápido

- **Pedido de Compra e Pagamento** — solicitação para a OSC pagar uma despesa que ainda vai acontecer.
- **Destinatário** — quem recebe o dinheiro (fornecedor, prestador, locador).
- **Tipo do pedido** — único, recorrente ou parcelado.
- **Ocorrência** — uma das execuções programadas de um pedido recorrente.
- **Parcela** — uma das partes de um pedido parcelado.
- **Cancelar pedido** — botão do detalhe de um pedido aprovado que encerra, de uma vez, todas as ocorrências ainda não pagas e leva o pedido ao status **Cancelado**. Substituiu o antigo "Cancelar série" e vale também para pedido único. Sem volta.
- **Cancelar esta ocorrência** — cancela só uma parcela ou ocorrência de um pedido recorrente/parcelado (apenas ela, ela e as próximas, ou toda a série pendente).
- **Cancelado** — status de um pedido encerrado sem pagamento: retirado pelo solicitante antes da aprovação (aparece como **Retirado pelo solicitante** e pode ser reenviado sem alterar nada), cancelado depois de aprovado, ou encerrado sozinho porque o pagamento foi estornado e não restou nada a pagar. Diferente de rejeitado.
- **Estorno** — a forma de reverter um pagamento já feito: cria um lançamento contrário em Movimentações e preserva a história. Não se cancela pagamento já realizado.
- **Reprovações necessárias** — número de votos contrários necessários para barrar o pedido (configurável: de 1 até o total de pessoas aptas a aprovar; padrão 1).
- **Valor fechado** — condição do pedido em que o valor declarado é o que vai ser pago (o boleto, a nota ou o recibo já existem).
- **Valor estimado** — condição do pedido em que o preço final ainda vai ser negociado; a aprovação autoriza com base numa estimativa.
- **Valor autorizado** — o valor aprovado no pedido, guardado separado do que acaba sendo lançado.
- **Valor lançado (efetivo)** — o valor registrado de fato no lançamento gerado pelo pedido; pode divergir do autorizado.
- **Limiar de reaprovação** — percentual, definido pela OSC, acima do qual a diferença entre autorizado e lançado exige nova autorização antes de o pagamento ser liberado (padrão: 10%).

## Por onde seguir

- **Reembolsos** — para despesas que **já foram pagas** do bolso e querem ressarcimento.
- **Movimentações** — para o tesoureiro confirmar o pagamento do pedido aprovado, registrar o valor efetivo de um pedido de valor estimado, ou [estornar um pagamento feito por engano](#paguei-por-engano).
- **Configurações → Fluxo de Aprovações** — para a OSC ajustar quórum, reprovações necessárias, papéis aprovadores e o limiar de reaprovação.
- **Cargos e permissões** — para saber quem pode alterar o valor de um lançamento vindo de pedido (exige a permissão **Pagar**).
- **Meu Perfil → Notificações** — para configurar canais e eventos das notificações de pedido.
