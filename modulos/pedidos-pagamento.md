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
> O ciclo normal é **Rascunho → Aguardando aprovação → Aprovado → Pago**. **Rejeitado** é desvio do caminho aprovado — solicitante pode editar e reenviar.

| Status | Significado |
|---|---|
| ⬜ **Rascunho** | Salvo mas não enviado — só o solicitante vê |
| 🟡 **Aguardando aprovação** | Esperando voto dos aprovadores elegíveis |
| 🟢 **Aprovado** | Aprovado; movimentação financeira pendente criada automaticamente |
| 🔴 **Rejeitado** | Reprovado com motivo registrado — pode ser editado e reenviado |
| 💙 **Pago** | Tesoureiro confirmou o pagamento na movimentação correspondente |
| ⬛ **Cancelado** | Retirado pelo próprio solicitante antes de ser aprovado — pode ser enviado de novo, mesmo sem alterar nada |

## Lista de pedidos de compra e pagamento

[![Lista de pedidos](/assets/screenshots/manual-07-pedidos-lista.png)](/assets/screenshots/manual-07-pedidos-lista.png)
*Lista de pedidos de compra e pagamento em desktop*

A lista exibe todos os pedidos com colunas Descrição, Destinatário, Valor, Data da despesa, Solicitante e Status. Quando o pedido já tem um lançamento vinculado (aprovado ou pago), o código curto desse lançamento aparece abaixo da descrição — útil para localizá-lo rapidamente em Movimentações.

> 💡 **A lista carrega por página.** Em organizações com muitos pedidos, a tela não traz o histórico inteiro de uma vez — ela carrega aos poucos, conforme você navega. Os **filtros continuam valendo sobre o conjunto inteiro**, não só sobre a página aberta.

Nas abas **Aprovado** e **Pago** há um filtro de período (mês atual, mês anterior, trimestre, ano etc.), igual ao de Movimentações, sempre aberto no **mês atual** por padrão. As abas **Aguardando aprovação**, **Rascunho** e **Rejeitado** não usam esse filtro — mostram sempre tudo, para nada que precise da sua atenção ficar escondido fora do período selecionado.

No **celular**, os cards de resumo ficam em grade de 2 colunas e a lista de pedidos vira cards verticais otimizados para toque:

[![Pedidos de pagamento no celular](/assets/screenshots/mobile-pedidos-pagamento.png)](/assets/screenshots/mobile-pedidos-pagamento.png)
*Pedidos de compra e pagamento no celular — KPIs em grade 2×N e abas roláveis horizontalmente*

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
- **Documentos**: orçamento, nota fiscal, contrato ou outros anexos
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

Painel de Ações mostra: **"Aprovado — aguardando confirmação de pagamento pelo tesoureiro."**

> 📖 **Conceito · Aprovado vira movimentação automaticamente**
>
> No momento da aprovação, o RIT360 Financeiro cria automaticamente a **movimentação financeira pendente** (ou várias, no caso de parcelado e recorrente) com origem `purchase_order` (pedido de compra e pagamento). O tesoureiro entra em Movimentações, escolhe a conta de saída e marca como paga. Cada ocorrência de uma série recorrente gera um movimento individual no momento programado, pago separadamente. Os comprovantes anexados ao pedido **vão junto com o lançamento** — aparecem direto na aba Documentos, sem precisar abrir o pedido original para conferir. O lançamento em Movimentações também tem o link **"Ver pedido de compra e pagamento →"**, útil para consultar o histórico de aprovações ou outros dados da solicitação.

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

### Corrigir o centro de custo depois do envio

Se o pedido já foi enviado — inclusive **aprovado** ou até **pago** — e o centro de custo ficou errado, quem faz a gestão financeira da OSC pode corrigir sem precisar reabrir ou cancelar nada. No detalhe do pedido, ao lado do campo **Centro de custo**, clique em **Corrigir**.

[![Corrigir centro de custo de um pedido já enviado](/assets/screenshots/ped-corrigir-centro-custo.png)](/assets/screenshots/ped-corrigir-centro-custo.png)
*Corrigir centro de custo: escolha o novo, informe o motivo, e a tela mostra antes o que vai mudar*

Escolha o **novo centro de custo** e escreva o **motivo da correção** (obrigatório) — ele fica guardado na trilha de auditoria, junto com o valor anterior e o novo. Antes de confirmar, a tela mostra o que será alterado: a própria solicitação e quantos lançamentos financeiros gerados por ela também vão mudar. A correção alcança os lançamentos já criados a partir deste pedido, **inclusive os que já foram pagos**.

### Cancelar série (recorrente / parcelado)

Para séries (recorrentes ou parceladas), o detalhe permite **cancelar com 3 escopos diferentes**, escolhidos no momento do cancelamento:

- **Apenas esta ocorrência** — cancela só a parcela/ocorrência específica
- **Esta e todas as futuras** — encerra a série a partir de uma data
- **Série inteira** — cancela tudo (apenas ocorrências ainda não pagas)

Ocorrências já pagas não podem ser canceladas (preservação de auditoria) — apenas estornadas via Movimentações.

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

> 💡 **Centro de custo no pedido** (opcional): a lista traz **apenas os centros de custo ativos** da OSC. Escolher um vincula o pedido àquela área desde a origem — quando ele for aprovado e virar movimentação, o lançamento já nasce com o centro de custo certo, sem precisar corrigir depois. Deixar em branco é normal para quem não usa centros de custo. Os centros de custo são cadastrados em [Configurações → Categorias → Centros de custo](/configuracoes/categorias/#centros-de-custo).

> 💡 **Data de pagamento solicitada** (opcional, só no tipo Único): o prazo em que o fornecedor espera receber. Serve de **referência para o tesoureiro** na hora de pagar e aparece no detalhe do pedido. Deixá-la em branco não impede enviar o pedido.

> ⚠️ **Atenção · Dados são do destinatário, não do solicitante**
>
> No reembolso, a chave PIX é a sua. No Pedido de Compra e Pagamento, é a do **fornecedor**. Não há pré-preenchimento automático — informe corretamente os dados do destinatário a cada solicitação (ou cadastre o fornecedor nos seus contatos e copie). Erro nesses dados significa transferência para destino errado.

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
- **Cancelar série** — encerrar pedido recorrente/parcelado em um dos 3 escopos (apenas uma / esta e futuras / série inteira). Não confundir com o status **Cancelado**, abaixo — são mecanismos diferentes.
- **Cancelado** — status de uma solicitação retirada pelo próprio solicitante antes da aprovação; diferente de rejeitado, pode ser reenviada sem precisar alterar nada.
- **Reprovações necessárias** — número de votos contrários necessários para barrar o pedido (configurável: de 1 até o total de pessoas aptas a aprovar; padrão 1).
- **Valor fechado** — condição do pedido em que o valor declarado é o que vai ser pago (o boleto, a nota ou o recibo já existem).
- **Valor estimado** — condição do pedido em que o preço final ainda vai ser negociado; a aprovação autoriza com base numa estimativa.
- **Valor autorizado** — o valor aprovado no pedido, guardado separado do que acaba sendo lançado.
- **Valor lançado (efetivo)** — o valor registrado de fato no lançamento gerado pelo pedido; pode divergir do autorizado.
- **Limiar de reaprovação** — percentual, definido pela OSC, acima do qual a diferença entre autorizado e lançado exige nova autorização antes de o pagamento ser liberado (padrão: 10%).

## Por onde seguir

- **Reembolsos** — para despesas que **já foram pagas** do bolso e querem ressarcimento.
- **Movimentações** — para o tesoureiro confirmar o pagamento do pedido aprovado, ou registrar o valor efetivo de um pedido de valor estimado.
- **Configurações → Fluxo de Aprovações** — para a OSC ajustar quórum, reprovações necessárias, papéis aprovadores e o limiar de reaprovação.
- **Cargos e permissões** — para saber quem pode alterar o valor de um lançamento vindo de pedido (exige a permissão **Pagar**).
- **Meu Perfil → Notificações** — para configurar canais e eventos das notificações de pedido.
