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

> 🎥 **Vídeo tutorial · Conta que já vem com projeto e centro de custo**
>
> Esta tela tem um vídeo curto (sem áudio, com legendas) mostrando como deixar a conta preencher sozinha o que se repete — clique no ícone de vídeo, no canto direito do cabeçalho. Veja todos os vídeos disponíveis em [Vídeos tutoriais dentro do app](/primeiros-passos/#videos-tutoriais).

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
- **Projeto padrão** e **Centro de custo padrão** (opcionais) — ver a seção **Projeto e centro de custo padrão da conta**, abaixo
- **Compõe o saldo disponível da organização** — ligado por padrão, **exceto para o tipo Cartão de crédito, que já nasce desligado**; ver a seção **Compõe o saldo disponível da organização**, abaixo
- **Dados bancários** (opcional, recolhível) — banco, agência e demais dados, quando aplicável
- **Personalização** (opcional, recolhível) — uma **cor** para a conta; ver a seção **Personalização**, abaixo

[![Editar conta — conta padrão e personalização](/assets/screenshots/config-contas-editar.png)](/assets/screenshots/config-contas-editar.png)
*Cadastro/edição de conta — alternar conta padrão e definir a cor*

> 📖 **Conceito · Saldo inicial e data de abertura**
>
> Quando você cadastra uma conta nova no RIT360 Financeiro, ela precisa saber qual era o saldo no momento em que sua OSC começou a usá-la no sistema. **Não é o saldo de hoje** — é o saldo na data de abertura. O RIT360 Financeiro usa esse valor como ponto de partida para calcular saldos futuros somando receitas e subtraindo despesas pagas. Se você está migrando de planilha para o RIT360 Financeiro, **a data de abertura é o dia que você começa a registrar no RIT360 Financeiro**, e o saldo inicial é o que estava na conta naquele dia.

## Ações por conta

- **Definir padrão / Remover padrão** — marca (ou desmarca) a conta como **padrão da organização**; ver abaixo
- **Editar** — alterar nome, banco, tipo e cor (não o saldo — saldo só muda via movimentações)
- **Desativar / Reativar** — uma conta desativada deixa de ser oferecida em novos lançamentos e importações, mas seu histórico permanece preservado e continua aparecendo nos filtros das listas
- **Excluir** — remove o cadastro definitivamente; só para conta sem nenhuma movimentação. Ver [Excluir contas](#excluir-contas), abaixo.

> ⚠️ **Atenção · Só sai do cadastro a conta sem nenhuma movimentação**
>
> Excluir apaga o cadastro **de vez** — por isso só é permitido para uma conta que **nunca teve nenhuma movimentação registrada**. Havendo qualquer lançamento vinculado, mesmo um só, a exclusão é recusada (excluir destruiria a história contábil dessas movimentações — "essa receita foi para qual conta?") e a única saída é **desativar**. Desativar continua funcionando do mesmo jeito de sempre, inclusive para conta com histórico extenso: as movimentações ficam intactas, e a conta desativada só some dos formulários de novo lançamento e das importações.

## Excluir contas {#excluir-contas}

Diferente de desativar, a exclusão **apaga o cadastro da conta**, não só o retira de oferta. É por isso que ela só vale para uma conta que **nunca movimentou nada** — criada por engano, duplicada no cadastro, ou de um teste que não seguiu adiante.

- **Uma de cada vez** — no ícone de lixeira, na linha da conta. O diálogo confere antes: se houver qualquer movimentação vinculada, mostra o que impede e a exclusão fica bloqueada.
- **Várias de uma vez** — marque o checkbox de cada conta (há **selecionar todos**, no cabeçalho da lista) e clique em **Excluir selecionadas**. A recusa de uma não trava as demais: o resultado volta **item por item**, dizendo quem foi excluída e quem foi recusada, com o motivo.

> ⚠️ **Atenção · Não tem como desfazer**
>
> A exclusão é definitiva, e o diálogo sempre avisa quantas contas serão apagadas antes de confirmar. Na dúvida entre excluir e desativar, prefira **desativar** — inclusive porque, tendo qualquer movimentação, excluir não é mesmo uma opção.

> 💡 **Por que isso importa**
>
> Antes desta versão, a única forma de tirar uma conta cadastrada por engano da lista era desativá-la — e ela ficava para sempre no cadastro, mesmo sem nunca ter sido usada para nada. Agora, o que nunca chegou a movimentar dinheiro sai de vez, sem exigir esse "encerramento" permanente de algo que nunca chegou a existir de fato para a contabilidade da OSC.

> 💡 **Antes de confirmar, você sabe o que está desativando**
>
> O diálogo de confirmação mostra quantos lançamentos estão vinculados à conta e, entre eles, quantos ainda estão **pendentes de pagamento**. Enquanto a contagem carrega, o diálogo avisa que está verificando; se a verificação falhar, ele avisa isso também — nunca mostra "nenhum lançamento" por não ter conseguido checar.
>
> **Lançamento pendente numa conta desativada continua podendo ser pago nela normalmente**, inclusive na baixa em lote (marcar vários lançamentos como pagos de uma vez). A única restrição é apontar, na baixa em lote, uma conta inativa **diferente** da que o lançamento já usa — nesse caso o item é recusado, com o motivo explicado, e os demais itens do lote seguem normalmente.

> ✓ **Dica · Conta desativada continua nos filtros**
>
> Uma conta desativada some das listas de escolha em lançamento novo e importação, mas **continua disponível no filtro de conta das listas de consulta** (Movimentações e relatórios), identificada como inativa — desde que tenha algum lançamento vinculado. É assim que você continua conseguindo revisar o histórico de uma conta encerrada sem precisar reativá-la.

## Compõe o saldo disponível da organização

No cadastro da conta, o interruptor **Compõe o saldo disponível da organização** decide se ela entra no total consolidado exibido como saldo disponível — no Painel e em qualquer outro lugar que mostre esse total. Vem **ligado por padrão** para a maioria dos tipos.

- **Cartão de crédito nasce com o interruptor desligado.** Saldo de cartão é dívida a pagar (ou crédito preso, quando a fatura está no seu favor), não dinheiro disponível para gastar — somá-lo ao disponível inflaria o número com um valor que, na verdade, é o oposto de folga. Você pode ligar manualmente se preferir outro critério para a sua OSC, mas o padrão já nasce correto para o caso comum.

  [![Texto de ajuda do interruptor "Compõe o saldo disponível" já desligado para conta tipo Cartão de crédito](/assets/screenshots/config-contas-cartao-nao-compoe-saldo.png)](/assets/screenshots/config-contas-cartao-nao-compoe-saldo.png)
  *Cadastro de conta tipo Cartão de crédito — o interruptor já nasce desligado*
- **Desligado**, a conta **sai apenas desse total**. Quando alguma conta está fora, o total avisa quanto ficou de fora e em quantas contas.
- **Nada mais muda.** O saldo individual da própria conta, os lançamentos, as transferências, a conciliação, os relatórios analíticos, as exportações e a prestação de contas continuam considerando a conta normalmente — é uma marcação de **exibição de disponibilidade**, não de escopo do dado.
- A conta continua **ativa e visível** em todas as listas, formulários e filtros.

> 📖 **Conceito · Recurso carimbado não é dinheiro disponível**
>
> Uma conta que guarda recurso carimbado — um convênio, uma emenda parlamentar, um fundo de uso restrito — tem saldo, mas esse saldo **não pode ser gasto livremente** pela organização; ele só pode ir para o que o convênio autoriza. Somá-lo ao saldo disponível faz o Painel afirmar uma folga que não existe, e isso é justamente o tipo de erro que leva a comprometer dinheiro que já tem destino certo. Desligar o interruptor nessas contas mantém o saldo disponível fiel ao que a OSC pode, de fato, usar.

**Exemplo:** a OSC administra a "Emenda 04/2024" (R$ 120.000, todo destinado à reforma da sede) e o "Caixa Geral" (R$ 18.000, de uso livre). Com a emenda marcada como fora do saldo disponível, o Painel mostra **R$ 18.000 disponíveis** — e um aviso indicando que R$ 120.000 em 1 conta ficaram de fora do total. Sem o interruptor desligado, o Painel mostraria R$ 138.000 disponíveis, dando a impressão de uma folga que não existe.

> ✓ **Dica · É a conta que costuma ser a exclusiva de um financiador**
>
> Uma conta que guarda recurso carimbado de um convênio ou termo de fomento normalmente tem este interruptor desligado — e é justamente esse tipo de conta que costuma ser marcada como **conta exclusiva** de uma fonte, em [Quem paga este projeto](/modulos/projetos/#quem-paga-este-projeto). São dois ajustes independentes, cada um no seu lugar (aqui, o que entra no saldo disponível; lá, se aquele dinheiro sai só por aquela conta), mas costumam andar juntos na prática.

## Conta exclusiva de uma fonte
{: #conta-exclusiva-de-uma-fonte }

Quando uma conta é marcada, num projeto, como **conta exclusiva** de uma fonte de financiamento (ver [Projetos → Acrescentar ou editar uma fonte](/modulos/projetos/#acrescentar-ou-editar-uma-fonte)), a lista de Contas Bancárias passa a mostrar isso na própria linha da conta: **"Conta exclusiva da fonte {nome} · projeto {nome do projeto}"**. Uma conta atendendo mais de uma fonte — uma encerrada e uma nova, por exemplo — mostra todas.

[![Linha da lista de Contas Bancárias mostrando "Conta exclusiva da fonte Fundo Municipal de Cultura · projeto Oficina de Artesanato"](/assets/screenshots/config-contas-conta-exclusiva-fonte-desktop.png)](/assets/screenshots/config-contas-conta-exclusiva-fonte-desktop.png)
*A conta "Banco Exemplo · Poupança" avisando de qual fonte e projeto ela é exclusiva*

[![A mesma lista no celular](/assets/screenshots/config-contas-conta-exclusiva-fonte-mobile.png)](/assets/screenshots/config-contas-conta-exclusiva-fonte-mobile.png)
*A mesma lista, no celular*

Quem tem permissão para emitir a prestação daquela fonte (coordenador do projeto, ou quem tem a permissão de ver relatórios — ver [Projetos → Quem pode emitir](/modulos/projetos/#prestacao-de-contas-por-fonte)) encontra, no menu de ações da própria linha da conta, o atalho **Prestação de contas** — direto para a mesma janela de período que existe na aba Financeiro do projeto. Sem essa permissão, o aviso da fonte continua aparecendo, mas o atalho não.

> ✓ **Dica · Dois caminhos para o mesmo documento**
>
> Se você já sabe qual é o **financiador**, o caminho mais natural é abrir o projeto e usar o botão na fonte (ver [Projetos → Prestação de contas de uma fonte](/modulos/projetos/#prestacao-de-contas-por-fonte)). Se você está olhando para a **conta** — por exemplo, conferindo o extrato de uma conta de convênio — este atalho evita ter que lembrar em qual projeto ela está e abrir o projeto só para achar o botão.

## Conta padrão

Uma das contas pode ser marcada como **conta padrão da organização**. A conta padrão é **pré-selecionada automaticamente ao criar um novo lançamento** — assim, quem registra movimentações não precisa escolher a conta toda vez (é só mudar quando for outra).

- **Apenas uma** conta pode ser a padrão por vez. Ao definir uma nova padrão, a anterior deixa de ser.
- Marque pela ação **Definir padrão** na lista, ou pelo interruptor **Conta padrão da organização** ao criar/editar a conta.
- A conta padrão exibe o selo **Padrão** na lista de contas.
- Se você **desativar** a conta que era a padrão, ela deixa de ser padrão automaticamente — defina outra.

> ✓ **Dica · Aponte para a conta que mais movimenta**
>
> Defina como padrão a conta por onde passa o grosso do dia a dia (geralmente a conta corrente principal). Como ela já vem selecionada no novo lançamento, você economiza um passo na maioria dos registros e reduz o risco de lançar na conta errada por desatenção.

## Projeto e centro de custo padrão da conta
{: #projeto-e-centro-de-custo-padrao-da-conta }

Além da conta padrão da organização (acima), cada conta pode ter, no próprio cadastro, um **Projeto padrão (sugestão)** e um **Centro de custo padrão (sugestão)**.

[![Edição de conta com os campos "Projeto padrão (sugestão)" e "Centro de custo padrão (sugestão)" preenchidos](/assets/screenshots/config-contas-projeto-centro-custo-padrao-desktop.png)](/assets/screenshots/config-contas-projeto-centro-custo-padrao-desktop.png)
*Conta "Caixinha" com projeto e centro de custo padrão configurados*

[![O mesmo formulário no celular](/assets/screenshots/config-contas-projeto-centro-custo-padrao-mobile.png)](/assets/screenshots/config-contas-projeto-centro-custo-padrao-mobile.png)
*O mesmo formulário, no celular*

> 💡 **Por que isso importa**
>
> OSC que mantém uma conta bancária por projeto — comum em quem administra convênio ou emenda com conta segregada — lançava a despesa e depois precisava lembrar de marcar o projeto (e o centro de custo) toda vez, na mesma tela, na planilha de migração e na conciliação do extrato. Com o padrão da conta configurado, os campos **já chegam preenchidos** nos três caminhos — sobra só confirmar ou trocar, quando for o caso.

> 📖 **Conceito · Por que é sugestão, e não trava**
>
> **Exemplo:** o Instituto Exemplo abriu uma conta corrente exclusiva para o Termo de Fomento 12/2026 e configurou o projeto correspondente como padrão dela. No mesmo extrato dessa conta, ao lado dos repasses e das despesas do termo, aparecem também a **tarifa bancária mensal** e o **rendimento da conta remunerada** — nenhum dos dois é despesa ou receita do projeto, e sim custo/rendimento financeiro da própria organização. Se o padrão da conta **travasse** o projeto, esses dois lançamentos entrariam no termo por engano, distorcendo a prestação de contas ao financiador. Sendo sugestão, o projeto vem pré-marcado (poupando o trabalho nas dezenas de lançamentos que são mesmo do termo) e a pessoa troca para "Sem projeto" só nesses dois casos.

- **É sugestão, não trava — nos três caminhos.** Quem está lançando, importando por planilha ou conciliando o extrato pode trocar o projeto e o centro de custo livremente, ou deixar sem projeto; o padrão da conta só preenche o campo quando ele ainda está vazio (planilha) ou ainda não foi trocado na tela (lançamento manual e conciliação) — nunca sobrescreve uma escolha que a pessoa já fez.
- **Onde configurar:** no cadastro ou na edição da conta, em **Configurações → Contas Bancárias**, junto do interruptor de conta padrão.
- **Onde funciona:**
  - no formulário de **[novo lançamento](/modulos/movimentacoes/#registrar-novo-lançamento)**, ao escolher a conta — e, aqui, se você registrar com outro projeto (ou nenhum), a tela pede uma confirmação antes de salvar, para a divergência não passar batida sem ninguém notar;
  - na **[importação por planilha](/modulos/movimentacoes/#importar-lançamentos)**, nas linhas em que as colunas `projeto` e `centro_de_custo` vierem vazias — a planilha, quando traz valor nessas colunas, sempre vence o padrão;
  - na **[conciliação do extrato](/modulos/movimentacoes/#conciliacao-projeto-e-centro-de-custo)**, em toda linha marcada para criar receita ou despesa.
- **Nenhum dos dois é obrigatório.** Conta sem projeto e centro de custo padrão continua funcionando exatamente como antes — nenhum dos três caminhos vem com algo pré-preenchido a partir da conta.

> ✓ **Dica · Uma conta por projeto é o caso que mais aproveita**
>
> Se a sua OSC segrega uma conta bancária por convênio ou por projeto grande, configure o projeto padrão daquela conta uma vez e deixe de repetir a escolha em cada lançamento, em cada linha da planilha de migração e em cada linha da conciliação. Vale o mesmo para um centro de custo que sempre responde pela mesma conta (a filial que só movimenta pela conta local, por exemplo).

## Personalização (cor)

Na seção **Personalização** do cadastro da conta, você pode definir uma **cor** para a conta. A cor vira um **acento visual** nos cartões de saldo — no **Painel**, na lista de movimentações e nos relatórios —, ajudando a distinguir as contas de relance.

> ✓ **Dica · Cores ajudam a bater o olho**
>
> Dar a cada conta uma cor própria (azul para o banco, verde para o caixa, roxo para a poupança) faz o Painel ficar legível num instante — você identifica de qual conta é cada saldo sem precisar ler o nome. É opcional, mas vale o minuto de configuração.

## Saldo em tempo real

Cada conta na lista mostra o **saldo atual**, calculado em tempo real a partir das movimentações pagas. Quando você marca uma receita ou despesa como paga em Movimentações, o saldo aqui atualiza imediatamente.

> ⚠️ **Atenção · Ver o saldo é uma permissão à parte**
>
> Sem a permissão **Ver saldo das contas**, esta página continua acessível para quem tem permissão de configuração financeira, mas o valor de cada conta aparece substituído por um aviso de permissão negada, dizendo a quem pedir. A mesma regra vale no Painel, em Movimentações, no formulário de novo lançamento e na aba Situação. Concede-se e revoga-se em [Cargos e permissões](/configuracoes/cargos/#permissao-ver-saldo) — inclusive para o cargo Presidente.

> ✓ **Dica · Concilie mensalmente contra o extrato bancário**
>
> No final de cada mês, abra o extrato do banco e o saldo da conta correspondente aqui no RIT360 Financeiro. Eles devem bater **centavos por centavos**. Diferenças apontam para lançamento esquecido, valor digitado errado, ou taxa que não foi registrada. Corrigir mensalmente é fácil; descobrir 6 meses depois é pesadelo.

## Dados bancários de quem recebe {#dados-bancarios-de-quem-recebe}

Além das contas da própria OSC, o sistema guarda os **dados bancários de quem recebe** um pagamento — o CPF do titular, a chave Pix, o banco, a agência e a conta que você informa num lançamento de despesa, num pedido de compra e pagamento ou num reembolso. Esses dados têm regras próprias, definidas aqui nesta página.

### Quem vê os dados completos

- **Quem tem permissão de pagar** vê CPF, chave Pix, banco, agência e conta **por inteiro**, como sempre viu — no lançamento, no pedido de compra e pagamento e no reembolso.
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
3. Logo abaixo, a tela mostra **quantos registros já estariam vencidos** com o prazo escolhido, separados por lançamentos, reembolsos e pedidos de compra e pagamento — assim você sabe o efeito imediato da escolha antes de confirmar.
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
- **Saúde 360** — onde os saldos consolidados das contas ativas aparecem.
- **[Cargos e permissões](/configuracoes/cargos/#permissao-pagar)** — onde se define quem pode pagar (e, por consequência, quem vê os dados bancários completos).
- **Configurações → Organização → Integrações → WooCommerce** — onde você define qual conta recebe receitas da loja online.
- **[Projetos → Quem paga este projeto](/modulos/projetos/#quem-paga-este-projeto)** — onde se marca uma conta como exclusiva de uma fonte, e onde a prestação de contas por fonte também pode ser emitida.
