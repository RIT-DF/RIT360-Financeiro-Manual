---
title: "Movimentações"
nav_order: 2
parent: "Módulos"
permalink: /modulos/movimentacoes/
---

O módulo de **Movimentações** é onde sua OSC registra cada entrada e saída de dinheiro — doação recebida, conta de luz paga, repasse entre contas, reembolso de combustível do voluntário. É o coração do sistema porque todos os outros módulos (Reembolsos, Pedidos de Pagamento, Relatórios, Conciliação) acabam alimentando ou se apoiando nessa lista.

> 💡 **Por que isso importa**
>
> Uma OSC que registra suas movimentações com disciplina **sabe a qualquer momento quanto tem em caixa, para onde o dinheiro está indo e quais despesas estão por vencer**. Sem esse registro, você descobre que o dinheiro acabou só quando o banco recusa o boleto — geralmente perto do fim do mês, sem tempo para resolver. Movimentações registradas em dia são a base para fluxo de caixa, relatórios para a diretoria, prestação de contas para financiadores e tranquilidade no fechamento contábil anual.

## Conceitos essenciais

Antes de entrar nos botões, vale firmar três conceitos que você vai ver em toda o RIT360 Financeiro.

> 📖 **Conceito · Receita, despesa e transferência**
>
> **Receita** é todo dinheiro que entra na OSC (doação, venda da lojinha, mensalidade de associado, repasse de edital). **Despesa** é todo dinheiro que sai (aluguel, conta de luz, compra de material, reembolso para voluntário). **Transferência** é movimento *interno* entre contas da própria OSC (do banco para a poupança, do dinheiro do caixinha para a conta corrente) — não é nem receita nem despesa, porque o dinheiro continua sendo seu, só muda de lugar. A distinção parece óbvia, mas misturá-las nas categorias é a fonte número um de relatórios financeiros distorcidos.

> 📖 **Conceito · Regime de caixa**
>
> O RIT360 Financeiro opera por **regime de caixa**: o que vale para o seu saldo e seus relatórios é a *data em que o dinheiro entrou ou saiu da conta*, não a data em que você assinou o contrato ou recebeu a fatura. Por isso a movimentação tem dois campos de data: **vencimento** (quando *deveria* acontecer) e **pagamento** (quando *aconteceu de fato*). Enquanto a data de pagamento não estiver preenchida, o dinheiro ainda não mexeu no seu saldo — ele está "previsto", não "realizado". Esse é o jeito mais simples e direto de acompanhar uma OSC e bate com a forma como a maioria das prestações de contas é feita.

> 📖 **Conceito · Status do lançamento**
>
> Cada movimentação tem um status que conta sua história. O ciclo de vida normal é **Pendente → Pago**. Quando o vencimento passa e nada foi pago, vira **Atrasado**. Quando uma movimentação não vai mais acontecer (ex: cancelaram o evento que pagaria o aluguel do salão), você a **Cancela**. Quando ela já estava paga mas precisa ser desfeita (ex: depósito caiu duplicado e o banco devolveu o segundo), você a **Estorna** — o RIT360 Financeiro cria um lançamento contrário automaticamente para preservar a história.

| Status | Significado | Quando aparece |
|---|---|---|
| 🟡 **Pendente** | Lançado, ainda não pago, dentro do prazo | Você registrou a conta de luz que vence dia 15; hoje é dia 10. |
| 🔴 **Atrasado** | Data de vencimento passou sem pagamento | Mesma conta de luz; hoje é dia 18 e ninguém marcou como paga. |
| 🟢 **Pago** | Confirmado como pago | Você marcou a conta como paga, anexou o comprovante. |
| 🟣 **Estornado** | Pagamento desfeito por inversão | Cliente devolveu uma doação; saída espelha a entrada original. |
| ⬛ **Cancelado** | Lançamento foi anulado manualmente | Lançou por engano ou o evento foi cancelado antes do pagamento. |

> O status **Atrasado** é atualizado automaticamente todo dia — você não precisa abrir o lançamento nem fazer nada para ele mudar de "Pendente" para "Atrasado" assim que o vencimento passa.

## O resumo do topo: onde você está e para onde vai

Antes da lista, a tela mostra um bloco de resumo com **dois cartões lado a lado**: **Contas**, à esquerda, e **Resumo do período**, à direita. Eles são compactos de propósito — o protagonista da tela são os lançamentos, e o resumo existe para você se situar em poucos segundos antes de mergulhar neles.

[![Resumo de contas e do período](/assets/screenshots/mov-resumo-contas-periodo.png)](/assets/screenshots/mov-resumo-contas-periodo.png)
*À esquerda, onde o dinheiro está agora; à direita, o que aconteceu (e o que ainda vai acontecer) no período*

### Cartão "Contas" — onde o dinheiro está agora

Cada conta da OSC ocupa **uma linha**: nome e tipo à esquerda, saldo à direita. As contas aparecem separadas por subtítulo entre **Ativos** (o que a organização tem — conta corrente, poupança, caixa) e **Passivos** (o que a organização deve — tipicamente o cartão de crédito). Se sua OSC tem muitas contas, a lista **rola por dentro do próprio cartão**, sem esticar a tela e sem empurrar os lançamentos para baixo.

No rodapé, sempre visível, fica o **Líquido** — a posição consolidada da organização, ou seja, os ativos menos os passivos. É o número que responde "quanto a OSC realmente tem, já descontado o que deve".

Ao fim de cada linha há uma **lupa** 🔎, que abre o **[Caça-diferenças](/modulos/caca-diferencas/)** daquela conta: você informa o saldo que aparece no app do banco e o sistema aponta onde está a diferença.

> 💡 **Por que isso importa**
>
> Somar mentalmente "tenho R$ 7.000 no Sicredi e R$ 86.000 no MercadoPago, mas devo R$ 6.500 no cartão" é exatamente o tipo de conta que se erra com pressa — e errar para mais é o que faz uma organização autorizar um gasto que não cabe. O **Líquido** já entrega essa conta pronta, e sempre à vista.

### Cartão "Resumo do período" — realizado e previsto, separados

O segundo cartão é uma pequena tabela com **Receitas**, **Despesas** e **Resultado**, em **duas colunas**: **Realizado** e **Previsto**.

| Coluna | O que entra ali |
|---|---|
| **Realizado** | O que já foi **efetivamente pago ou recebido** — o dinheiro mexeu na conta. |
| **Previsto** | O que está **pendente ou atrasado** — ainda vai acontecer (ou deveria ter acontecido e não aconteceu). |

O **Resultado** aparece **só na coluna Realizado**, e isso é proposital: resultado previsto seria especulação sobre dinheiro que ainda não existe. Lançamentos **estornados** e **cancelados** ficam fora das duas colunas — não representam dinheiro que circulou.

> 📖 **Conceito · Por que separar realizado de previsto**
>
> Até pouco tempo, o resumo somava os dois num único número chamado "Receitas". O problema é sutil e caro: um valor de R$ 20.000 em "Receitas" podia ser R$ 3.000 que caíram na conta mais R$ 17.000 de um repasse que ainda nem foi liberado. Quem olha rápido lê "temos vinte mil".
>
> **Planejar gasto em cima de receita que ainda não entrou é uma das formas mais comuns de uma organização pequena se enrolar.** O convênio atrasa dois meses, a doação prometida não se confirma, a venda do bazar rende menos que o previsto — e as despesas, essas, já foram assumidas. Separando as colunas, a leitura fica honesta: *isto eu tenho; aquilo eu espero*. Decisão de gasto se toma pela coluna **Realizado**; a coluna **Previsto** serve para você **se preparar** — cobrar quem deve, adiar o que dá para adiar, buscar caixa antes de precisar dele.

> ⚠️ **Atenção · O período segue a data em que o dinheiro se moveu**
>
> O período de **Movimentações** recorta os lançamentos pela **data em que o dinheiro se moveu**: o que já foi **pago ou recebido** entra pelo mês do **pagamento**; o que ainda está **em aberto** (pendente ou atrasado) entra pelo mês do **vencimento**. É o mesmo critério dos **[Relatórios](/modulos/relatorios/)**, que consideram o que foi pago pela data do pagamento — por isso o **Realizado** das duas telas agora **bate** para o mesmo período. (Os Relatórios continuam olhando só o dinheiro que circulou; o que está em aberto aparece aqui, na coluna Previsto.)
>
> Um exemplo concreto: uma conta que **vence em 30 de junho** e é **paga em 2 de julho** aparece em **julho**, tanto aqui quanto nos Relatórios — porque foi em julho que o dinheiro saiu. Enquanto ela estivesse em aberto, apareceria em junho, pelo vencimento.
>
> **O que isso significa na prática:** uma conta paga com atraso aparece no mês do pagamento, não no mês em que venceu. Então um mês que você já conferiu pode mudar depois, se alguma conta dele for paga com atraso. É proposital: o RIT360 Financeiro trabalha em **regime de caixa**, e atribuir a junho um dinheiro que só saiu em julho distorceria o "Realizado" dos dois meses.

### Cores: vermelho é pedido de atenção

O resumo usa cor com parcimônia — **o que fica colorido é o que exige atenção**, e o resto permanece neutro, para que o vermelho realmente salte aos olhos quando aparecer.

- Uma conta de **ativo com saldo negativo** (conta estourada, cheque especial) aparece em **vermelho**. Saldos positivos ficam neutros.
- No **cartão de crédito**, o valor **"a pagar"** é dívida e aparece em **vermelho**; quando o cartão está com **"crédito"** (saldo a seu favor, por exemplo após um estorno da operadora), fica neutro.

O mesmo critério vale no **Painel** e nos **Relatórios** — a leitura é a mesma em todo o sistema.

## Lista de movimentações

[![Lista de movimentações](/assets/screenshots/manual-02-movimentacoes-lista.png)](/assets/screenshots/manual-02-movimentacoes-lista.png)
*A tela de Movimentações: resumo compacto no topo, busca e filtros na mesma linha, e os lançamentos ocupando o espaço principal*

A lista mostra todas as movimentações com as colunas **Vencimento**, **Pagamento**, **Lançamento** (descrição e contraparte), **Conta**, **Categoria**, **Status** e **Valor**.

No **celular** ou em telas estreitas (abaixo de 1024 px de largura), a tabela vira uma **lista de cards** com a mesma informação organizada verticalmente — descrição em destaque, valor colorido, data, contraparte, conta, categoria, status e menu de ações:

[![Lista de movimentações no celular](/assets/screenshots/mobile-movimentacoes-cards.png)](/assets/screenshots/mobile-movimentacoes-cards.png)
*Lista de movimentações no celular — cada lançamento como card*

Para ordenar a lista no celular, use o seletor **"Ordenar por"** logo acima dos cards.

Ao abrir a tela, ela já vem filtrada pelo **mês corrente** — o que você está operando agora. Para ver períodos anteriores ou outros recortes, use o filtro de período.

### Filtros e período contábil

O período segue sendo o recorte principal:

- **Período** — atalhos contábeis prontos (Mês atual, Mês anterior, Trimestre atual, Trimestre anterior, Semestre atual, **Ano até a data atual**, Ano atual, Ano anterior) + opção **Personalizado** para definir intervalo livre + **Todos** para ver tudo

> 💡 **Por que isso importa**
>
> Atalhos contábeis (trimestre, semestre, ano) parecem detalhe, mas eles existem porque **prestação de contas e análise gerencial seguem esses recortes**, não os meses corridos. Quando a diretoria pergunta "como foi o primeiro trimestre?", você seleciona "Trimestre anterior" e o relatório está pronto — sem precisar configurar datas no calendário toda vez.

> 📖 **Conceito · "Ano até a data atual" × "Ano atual"**
>
> São dois recortes parecidos e frequentemente confundidos, disponíveis tanto em **Movimentações** quanto em **[Relatórios](/modulos/relatorios/)**:
>
> - **Ano até a data atual** — de **1º de janeiro até hoje**. Só o que já aconteceu ou já venceu.
> - **Ano atual** — o **ano de calendário inteiro**, de 1º de janeiro a 31 de dezembro, incluindo meses que ainda nem chegaram.
>
> **Quando usar cada um:** escolha **"Ano até a data atual"** quando a pergunta for *"como o exercício está indo até agora?"* — é o recorte para avaliar desempenho, comparar com o ano passado no mesmo ponto ou levar um número à reunião de diretoria. Escolha **"Ano atual"** quando quiser enxergar também **o que já está programado até o fim do ano** — as parcelas que faltam, o aluguel dos próximos meses, a recorrência que continua rodando. O primeiro conta a história até aqui; o segundo mostra o ano inteiro, incluindo o que ainda está por vir.

### Filtros combináveis por marcadores (chips)

No lugar das antigas abas por tipo, a lista agora tem **filtros por marcadores (chips)** que você combina livremente. Pode filtrar ao mesmo tempo por:

- **Tipo** (receita, despesa, transferência)
- **Conta**
- **Categoria**
- **Status**
- **Projeto**
- **Centro de custo**

Em cada um desses filtros você escolhe **vários valores** de uma vez e ainda decide se quer **incluir** apenas os selecionados ou **excluir** ("mostrar tudo, exceto…"). Some-se a isso uma **busca livre** por texto, que procura na descrição, no beneficiário, na conta, na categoria, no valor e na data.

A **busca e os filtros ficam na mesma linha**, logo acima da lista — ocupam uma faixa só da tela, sobrando mais espaço vertical para os lançamentos.

[![Filtros combináveis em Movimentações](/assets/screenshots/mov-filtros-chips.png)](/assets/screenshots/mov-filtros-chips.png)
*Filtre por tipo, conta, categoria, status, projeto e centro de custo — combinando vários ao mesmo tempo.*
> 💡 **Por que isso importa**
>
> Filtro combinável responde perguntas que aba única não alcança: "todas as despesas de material do projeto Feira, exceto as da conta Caixa". Antes você via um tipo de cada vez; agora cruza tipo, categoria, projeto e centro de custo numa consulta só — a conferência e a análise gerencial ficam muito mais rápidas.

Quando há filtros ativos, uma linha "Filtrado por: …" indica o que está sendo aplicado, e o botão **Limpar filtros** remove todos de uma vez. Os totais do **Resumo do período** acompanham o recorte filtrado — o que você vê resumido é sempre o que está na lista.

> 📱 **No celular**
>
> Os filtros abrem em um **painel próprio**, e a tela nunca rola para o lado — você seleciona os marcadores no painel, aplica, e volta para a lista já filtrada.

### Estornados e cancelados ocultos por padrão

Para facilitar a conferência contra o extrato, a lista passa a **esconder automaticamente** os lançamentos **estornados** (o par inteiro — original e contrário) e os **cancelados** — eles não representam dinheiro que entrou ou saiu de fato. Um botão **"Mostrar estornados e cancelados"** traz esses lançamentos de volta quando você precisar vê-los, e a contagem indica quantos estão ocultos no momento. Pelo mesmo motivo, eles também não entram nas colunas **Realizado** e **Previsto** do resumo.

### Identificadores visuais no título

Ao lado do título de cada movimentação, badges contam mais sobre a origem e a história dela:

- **Recorrente** — lançamento gerado por uma série recorrente (ex: aluguel mensal)
- **Parcela X de N** — uma parcela de um lançamento parcelado (ex: 3/6 de uma compra parcelada)
- **Estornado** — aparece tanto no lançamento original quanto no contrário gerado pelo estorno
- **WooCommerce** (roxo) — pedido importado automaticamente da sua loja online; clique no badge abre o pedido no admin do WooCommerce em nova aba

### Ordenação

Clique no cabeçalho de qualquer coluna para ordenar. Um segundo clique inverte a ordem; um terceiro remove a ordenação.

### Ações por linha

Cada linha tem ícones de ação que mudam conforme o status:

- ✏️ **Editar** — disponível para movimentações pendentes ou atrasadas (ver **Editar um lançamento**, abaixo)
- 💲 **Marcar como pago** — disponível para pendentes e atrasadas (atalho rápido sem entrar no detalhe), **para quem tem permissão de pagar**
- ✕ **Cancelar** — disponível para pendentes e atrasadas
- ↩ **Estornar** — disponível para pagas
- 🗑 **Excluir** — disponível apenas para canceladas (estornos são preservados e **não** podem ser excluídos)

> ⚠️ **Atenção · Cancelar não é a mesma coisa que excluir**
>
> **Cancelar** marca o lançamento como anulado mas mantém o histórico — útil quando algo registrado não vai mais acontecer (evento desmarcado, fornecedor desistiu) e você quer rastreabilidade. **Excluir** apaga o lançamento de vez. O RIT360 Financeiro só permite excluir lançamentos já **cancelados**, justamente para evitar perda acidental; **estornos são preservados** (não podem ser excluídos) para manter a prestação de contas íntegra. Para auditoria limpa, prefira sempre **cancelar** a excluir.

> 📖 **Conceito · Registrar não é o mesmo que pagar**
>
> **Marcar como pago** exige a permissão de **pagar**, que é separada da de criar e editar. Quem registra lançamentos mas não tem essa permissão simplesmente **não vê** a ação de marcar como pago — nem na linha, nem no detalhe, nem na seleção em lote, nem na conciliação de extrato. Isso permite que uma pessoa organize as contas a pagar e outra confirme a saída do dinheiro. Quem ajusta isso é o Presidente, em [Cargos e permissões](/configuracoes/cargos/#permissao-pagar); por padrão, quem já podia pagar continua podendo.

### Seleção em lote

Marque o checkbox no início das linhas para selecionar várias movimentações. A barra de ações em lote aparece no rodapé com as opções **Marcar como pago** (para quem tem permissão de pagar) e **Excluir**.

### Exportação

As exportações são **fiéis ao que está na tela**: refletem exatamente os filtros ativos (chips, busca e período) — o que você vê é o que exporta. O botão **Exportar** oferece três saídas:

- **PDF** — relatório formatado com cabeçalho, filtros ativos e totais (bom para imprimir / enviar para diretoria)
- **Excel** — planilha para análises customizadas
- **Prestação de contas** — o documento contábil completo do período, em regime de caixa, com os comprovantes anexados (ver a seção **Prestação de contas** abaixo)

Ao escolher **PDF** ou **Excel**, antes de gerar o arquivo o RIT360 Financeiro abre um **seletor de colunas**: marque ou desmarque o que deve aparecer no relatório. Vêm marcadas por padrão oito colunas — Vencimento, Pagamento, Pagador/Beneficiário, Lançamento, Conta, Categoria, Status e Valor — e você pode acrescentar **Tipo**, **Forma de pagamento**, **Observações** e **Nº de anexos**. A seleção é **lembrada para a próxima exportação**, separada por organização (cada OSC mantém o formato que prefere). É preciso deixar pelo menos uma coluna marcada.

O **Excel** baixa na hora. Já o **PDF** é montado **em segundo plano**: ao clicar em gerar, abre uma página de acompanhamento que mostra "Gerando…" e, assim que o documento fica pronto, **o download começa sozinho**. Você não precisa esperar parado — pode fechar a aba e continuar trabalhando, porque **o link do PDF também chega no seu e-mail**. É o mesmo comportamento da prestação de contas.

[![Página de acompanhamento do PDF](/assets/screenshots/mov-exportar-pdf-acompanhamento.png)](/assets/screenshots/mov-exportar-pdf-acompanhamento.png)
*A página de acompanhamento: quando o PDF fica pronto, o download começa sozinho (e o link também chega por e-mail).*

## Detalhe de uma movimentação

[![Detalhe de movimentação](/assets/screenshots/manual-03-movimentacao-detalhe.png)](/assets/screenshots/manual-03-movimentacao-detalhe.png)
*Detalhe de uma despesa*

Clique em qualquer linha da lista para abrir o detalhe completo, organizado em duas colunas no desktop:

**Coluna principal:**

- Tipo e status (chips coloridos no topo)
- Título e valor em destaque
- Dados do lançamento: vencimento, pagamento, conta, categoria, beneficiário/fornecedor, forma de pagamento, projeto, centro de custo
- **Dados de pagamento** — quando o lançamento tem chave PIX ou dados bancários do destinatário, um card mostra esses dados para efetivar o pagamento sem abrir a solicitação de origem. Vale tanto para lançamentos vindos de **reembolso/pedido de pagamento** quanto para **despesas lançadas à mão** (ver "Forma de pagamento" no formulário). **Quem tem permissão de pagar vê os dados por inteiro; os demais veem apenas os últimos dígitos** — o nome de quem recebe fica visível para todos. Passado o prazo de descarte definido pela OSC, o card informa que os dados foram removidos por já terem cumprido sua finalidade. Detalhes em [Contas Bancárias → Dados bancários de quem recebe](/configuracoes/contas/#dados-bancarios-de-quem-recebe)
- Distribuição entre categorias (se o valor foi dividido)
- Observações
- Documentos: comprovantes e notas fiscais anexados, com pré-visualização inline para imagens e PDFs
- Quando o lançamento veio de outro módulo, links cruzados aparecem aqui:
  - **Ver pedido de pagamento** — para movimentações geradas a partir de uma solicitação de pagamento aprovada
  - **Ver pedido de reembolso** — para movimentações que pagaram um reembolso

**Coluna de auditoria (à direita no desktop, abaixo no mobile):**

Linha do tempo com todas as ações sobre o lançamento — quem criou, quem marcou como pago, quem estornou, quando, em qual ordem. Cada evento mostra ícone, nome do responsável e data/hora.

> 💡 **Por que isso importa**
>
> A timeline de auditoria não é firula. Em OSC, é comum a função financeira ser rotativa (passa de um voluntário para outro a cada ano) e questões surgem meses ou anos depois — *"essa despesa foi paga ou não?", "quem autorizou esse estorno?"*. A linha do tempo responde sem ambiguidade e protege todo mundo: o tesoureiro atual, o anterior, a diretoria que vai prestar contas.

## Registrar novo lançamento

[![Formulário de novo lançamento](/assets/screenshots/manual-04-novo-lancamento.png)](/assets/screenshots/manual-04-novo-lancamento.png)
*Formulário de novo lançamento*

Clique em **+ Novo lançamento** no topo da lista. O formulário abre em **página própria**, com um resumo e um checklist do lado direito que vão se preenchendo conforme você digita.

**Campos obrigatórios:**

- **Tipo** — Receita, Despesa ou Transferência (define o resto do formulário)
- **Descrição** — descrição breve do lançamento (ex: "Conta de luz - março", "Doação Família Silva")
- **Data de vencimento**
- **Valor total**
- **Conta** — qual conta financeira movimenta. Já vem **pré-selecionada com a [conta padrão](/configuracoes/contas/#conta-padrão)** da OSC; troque se for outra
- **Categoria** — não pedida para Transferências (porque transferência é só mudança de lugar)

**Campos opcionais:**

- **Beneficiário / Pagador** — quem recebeu o pagamento (em Despesa, "Beneficiário") ou de quem veio o dinheiro (em Receita, "Pagador"). Fica no topo do formulário, logo após o tipo
- **Tipo de documento fiscal** e **Número do documento** — para registrar a nota/recibo que originou o lançamento
- **Data de pagamento** — se preenchida no momento da criação, o lançamento já entra como **Pago**; se vazia, entra como **Pendente** e você confirma o pagamento depois
- **Projeto** e **Centro de custo** — para OSCs que dividem o financeiro por projeto/área
- **Forma de pagamento** (em Despesa) — como o pagamento será feito. Ao escolher **PIX**, o formulário abre os campos da **chave PIX** (tipo e chave); ao escolher **Transferência bancária**, abre os **dados bancários** do destinatário (banco, agência, conta e titular); **Boleto** e as demais formas não pedem campos extras. Esses dados são opcionais e ficam guardados no lançamento — úteis para quem for efetivar o pagamento depois
- **Distribuir valor entre categorias** — divide um único valor por várias categorias (ex: uma compra de R$ 500 que vai 60% para "Material didático" e 40% para "Manutenção")

> 📖 **Conceito · O formulário se adapta ao tipo**
>
> Ao escolher **Transferência**, o RIT360 Financeiro **oculta os campos que não fazem sentido** para um movimento interno entre contas — Beneficiário, Categoria e os campos de documento fiscal somem, e aparece o campo de **conta de destino**. Você só vê o que precisa preencher para cada tipo de lançamento. Da mesma forma, os campos de destinatário (chave PIX / dados bancários) só aparecem em **Despesa**, conforme a forma de pagamento escolhida.

No **celular**, o mesmo formulário se organiza em uma coluna única, na ordem em que você preenche — desenhado para registrar um lançamento de pé, em campo, sem zoom nem rolagem horizontal:

[![Novo lançamento no celular](/assets/screenshots/mobile-novo-lancamento.png)](/assets/screenshots/mobile-novo-lancamento.png)
*Novo lançamento no celular — coluna única, campos na ordem de preenchimento*

> ✓ **Dica · Categorias consistentes valem ouro nos relatórios**
>
> Categoria é o que faz seus relatórios mensais e anuais terem sentido. Se metade dos lançamentos de combustível foi para "Transporte" e a outra metade para "Combustível", o relatório vai mostrar dois grupos pequenos em vez de um grupo real. Defina as categorias da sua OSC com cuidado em **Configurações → Categorias**, deixe a lista enxuta, e treine quem registra para usar sempre a mesma.

### Tipo de repetição

A barra lateral direita também controla a repetição do lançamento:

- **Único** — lançamento avulso (default para a maioria dos casos)
- **Parcelado** — divide um valor único em N parcelas com datas distintas (ex: compra de equipamento em 6×). A aprovação cria as parcelas todas de uma vez; cada uma tem sua data e pode ser paga individualmente.
- **Recorrente** — cria uma série que se repete automaticamente em intervalo regular (semanal, quinzenal, mensal, bimestral, trimestral, semestral, anual). A duração pode ser **por data final**, **por quantidade de ocorrências** ou **indefinida até cancelar**.

> 📖 **Conceito · Parcelado × Recorrente — qual usar?**
>
> Use **Parcelado** quando você sabe o valor total e quantas vezes vai pagar (compra de notebook em 6×, contrato fechado em 12 prestações). Use **Recorrente** quando o lançamento se repete por tempo indeterminado ou até segunda ordem (aluguel mensal, mensalidade de internet, doação fixa do mantenedor). A diferença é mais que cosmética: parcelas dividem **um valor único**, enquanto recorrências são **lançamentos independentes que repetem**. Cancelar uma recorrência para no mês escolhido; cancelar uma parcela cria uma pendência no plano de pagamento.

### Anexos e comprovantes

Você pode anexar arquivos (comprovantes, notas fiscais, contratos) ao lançamento. Anexo é **opcional** — lançamento sem comprovante continua válido — mas é fortemente recomendado para qualquer movimentação que tenha origem em compra, serviço contratado ou pagamento de terceiro. PDFs e imagens ganham pré-visualização inline na página de detalhe.

**Em mobile**, a seção **DOCUMENTOS** exibe dois botões: **Tirar foto** (abre a câmera traseira do celular direto, com preview **Refazer** ou **Confirmar** antes de subir) e **Anexar arquivo**. O RIT360 Financeiro reduz a foto automaticamente antes do upload — fica leve mesmo em conexão móvel ruim, sem perder a legibilidade do cupom para auditoria humana ou para extração automática futura via IA.

**Em desktop**, a seção mostra uma área para arrastar arquivos ou clicar para selecionar — o botão "Tirar foto" não aparece nesse contexto (webcam de laptop não serve para fotografar comprovante apoiado na mesa).

> 📖 **Conceito · Quais arquivos você pode anexar como comprovante**
>
> Além de **imagens** e **PDF**, o RIT360 Financeiro aceita **XML de NFe**, **ZIP** e agora também **documentos de escritório**: Word (`.docx`), Excel (`.xlsx`), PowerPoint (`.pptx`) e os formatos equivalentes do OpenDocument (`.odt`, `.ods`, `.odp`) — úteis para anexar, por exemplo, uma planilha de prestação de contas de um fornecedor ou um recibo em Word. Vale tanto para o anexo manual quanto para o comprovante que chega por **link** na importação de lançamentos (ver "Importar lançamentos" abaixo). Por segurança, **arquivos executáveis continuam bloqueados** e não podem ser anexados.

**Anexou um arquivo ZIP?** O RIT360 Financeiro **descompacta o pacote automaticamente** e anexa cada documento de dentro como um anexo individual do lançamento — o ZIP some da lista, dando lugar aos arquivos. Assim, cada comprovante que estava no pacote ganha pré-visualização (quando é imagem ou PDF) e **entra na prestação de contas**. A expansão roda em segundo plano, em segundos, e vale também quando o comprovante chega por **link** na importação por CSV.

> 💡 **Documentos de escritório na prestação de contas**
>
> PDFs e imagens aparecem embutidos no corpo da prestação de contas — dá para ver o comprovante sem sair do documento. Já Word, Excel, PowerPoint, OpenDocument e ZIP não têm como ser exibidos embutidos num PDF; nesses casos, a prestação de contas mostra uma linha **"📎 nome-do-arquivo — disponível no lançamento"**, avisando que o comprovante está anexado e pode ser aberto no detalhe do lançamento dentro do sistema (ver a seção **Prestação de contas** abaixo).

**Em Novo Lançamento nos modos Recorrente e Parcelado**, a seção de anexo é ocultada na criação da série — não há um lançamento único ao qual associar o documento. Uma nota explicativa orienta a anexar individualmente em cada lançamento depois que a série for criada. Em **Editar Lançamento**, a seção funciona normalmente, pois você sempre edita um movimento individual.

> ✓ **Dica · Anexe sempre, anexe na hora**
>
> Comprovante anexado na criação do lançamento custa 10 segundos. Procurar um comprovante de 8 meses atrás na pasta de e-mails do diretor anterior custa horas e às vezes não dá certo. **Adote como regra: nenhum lançamento sem comprovante.** Sua diretoria, sua auditoria contábil e seu eu do futuro vão agradecer.

> ✓ **Dica · Tesoureiro em campo, câmera direto no app**
>
> Tesoureiro voluntário em viagem com o grupo, pagou combustível no posto: abre o RIT360 Financeiro instalado no celular, **Novo Lançamento → Tirar foto**, fotografa o cupom fiscal, confirma. Quatro toques contra os oito tradicionais de tirar foto pelo app de câmera, salvar na galeria, abrir o RIT360 Financeiro, navegar, selecionar.

## Editar um lançamento

Lançamentos **pendentes** ou **atrasados** podem ser editados por completo. Clique no ícone ✏️ **Editar** na linha da lista, ou no botão **Editar** no detalhe do lançamento. (Para corrigir um lançamento que já está **pago**, veja **Corrigir os dados de um lançamento pago**, mais abaixo — é uma janela mais restrita, que não mexe no valor nem no status.)

> 📖 **Conceito · Editar um lançamento de série recorrente**
>
> Ao editar um lançamento que faz parte de uma série recorrente, o RIT360 Financeiro pergunta primeiro o alcance da mudança: **Apenas este lançamento**, **Este e os próximos** ou **Toda a série**. Escolha com atenção — o alcance vale para tudo que você mudar em seguida (data, valor, categoria etc.), exceto os dados bancários, que têm regra própria (ver abaixo).

[![Escolha do alcance ao editar um lançamento recorrente](/assets/screenshots/mov-editar-serie-escopo.png)](/assets/screenshots/mov-editar-serie-escopo.png)
*Editar um lançamento de série recorrente: escolha entre alterar só este, este e os futuros, ou toda a série*

O formulário de edição tem os mesmos campos do lançamento novo (descrição, datas, conta, categoria, projeto, centro de custo, forma de pagamento, anexos — ver **Registrar novo lançamento**, acima).

### Dados bancários protegidos

Quando o lançamento já tem chave PIX ou dados bancários do destinatário guardados, esses campos aparecem **bloqueados** na tela de edição: mostram só uma parte do valor (por exemplo, `e2···@example.com`), a etiqueta **Protegido**, e um botão **Substituir** no lugar do campo aberto para digitar.

[![Campo de chave PIX protegido na edição de um lançamento](/assets/screenshots/mov-editar-dado-protegido.png)](/assets/screenshots/mov-editar-dado-protegido.png)
*Chave PIX protegida: valor parcial, etiqueta "Protegido" e botão "Substituir"*

- **Salvar sem tocar no campo protegido não altera o que está guardado.** Você pode ajustar qualquer outro dado do lançamento — data, conta, categoria, valor — sem risco de mexer sem querer nos dados bancários.
- **Clique em Substituir** para digitar um valor novo; o dado só é trocado de fato quando você salvar. Um botão **Desfazer** aparece para voltar ao estado protegido, caso mude de ideia antes de salvar.
- **Esvaziar um campo protegido pede confirmação**, porque a remoção é definitiva — não tem como recuperar o dado depois de apagado.
- **Em lançamento de série recorrente, os dados de pagamento nunca são propagados**, mesmo quando você escolhe editar "Este e os próximos" ou "Toda a série": cada lançamento da série guarda os seus próprios dados bancários, e uma edição em lote não mexe neles — cada um continua como estava.

> 💡 **Por que isso importa**
>
> Chave PIX e dados bancários são informação sensível: depois que a pessoa (voluntário, fornecedor) confirmou o dado certo, ele não deve mudar sozinho só porque alguém salvou o lançamento para corrigir a categoria ou a data. O campo protegido evita erro de transferência por edição acidental, e o aviso ao esvaziar evita perder o dado à toa.

## Estornar um lançamento

[![Dialog de estorno](/assets/screenshots/manual-04c-estornar-dialog.png)](/assets/screenshots/manual-04c-estornar-dialog.png)
*Dialog de estorno — informe a razão antes de confirmar*

Estornar é diferente de cancelar. Estorno é a forma contábil correta de reverter um lançamento **que já foi pago**.

> 📖 **Conceito · O que acontece quando você estorna**
>
> O RIT360 Financeiro não apaga o lançamento original. Em vez disso, cria automaticamente um **lançamento contrário** com a mesma data, o mesmo valor e a categoria/conta espelhadas — uma receita estornada vira uma despesa de igual valor, e vice-versa. Os dois ficam vinculados na timeline e ambos exibem o badge "Estornado". O resultado no saldo é o mesmo que se nada tivesse acontecido, mas **a história fica preservada**: você consegue mostrar, anos depois, que aquele depósito chegou, foi estornado, e por quê.

Para estornar: vá no detalhe do lançamento → botão **Estornar** → informe a razão. O lançamento contrário é criado e ambos ficam marcados na lista.

> ⚠️ **Atenção · Estorno preserva, exclusão apaga**
>
> Estornos podem ser feitos por motivos legítimos — devolução bancária, depósito duplicado, doação devolvida. Em todos esses casos, **estornar é o caminho correto, não excluir**. Excluir um lançamento pago não é nem permitido pelo RIT360 Financeiro justamente para preservar a integridade da prestação de contas.

## Corrigir os dados de um lançamento pago

Às vezes o que ficou registrado num lançamento pago sai diferente do que aconteceu — você pagou num dia e lançou no outro, marcou a conta errada, ou a despesa entrou na categoria/centro de custo errado. Antes era preciso estornar e refazer; agora dá para **corrigir direto**, sem desfazer o lançamento, pela mesma janela **Editar dados de pagamento**.

[![Editar dados de pagamento de um lançamento pago](/assets/screenshots/mov-editar-cc-categoria-01.png)](/assets/screenshots/mov-editar-cc-categoria-01.png)
*Editar dados de pagamento — ajuste data, conta, categoria e/ou centro de custo e informe o motivo*

**Quem pode:** **Presidente** e **Tesoureiro** (o mesmo perfil que marca lançamentos como pagos e faz estornos).

Para corrigir:

1. Abra o **detalhe** do lançamento (ele precisa estar com status **Pago**) e clique em **Editar dados de pagamento** — ou use **Editar** na linha da tabela de Movimentações.
2. Ajuste o que precisar: **data de pagamento**, **conta financeira**, **categoria** e/ou **centro de custo**.
3. Escreva um **motivo** (obrigatório) — ele fica guardado na **trilha de auditoria** do lançamento.
4. Salve. Se você trocou a conta, os **saldos das contas envolvidas são recalculados** automaticamente.

> ⚠️ **Atenção · O que esta janela NÃO muda**
>
> Por aqui você corrige **data, conta, categoria e centro de custo**. Para corrigir o **valor**, o caminho continua sendo o **Estorno**. A correção **não altera o valor nem o status** do lançamento — ele continua pago, pelo mesmo valor. Transferências não usam essas correções.

> 📖 **Conceito · Reclassificar não é remexer o dinheiro**
>
> Mudar a **categoria** ou o **centro de custo** de um lançamento pago muda só a **classificação gerencial** (para qual área e sob qual categoria a despesa/receita conta) — os saldos das contas não mudam. Por isso pode ser feito depois de pago sem estorno. Como qualquer correção sobre lançamento pago, o **motivo** fica guardado na trilha de auditoria — quem prestar contas depois vê o que foi reclassificado e por quê.

## Importar lançamentos

[![Importar Lançamentos com 2 fontes](/assets/screenshots/manual-04b-importar-lancamentos.png)](/assets/screenshots/manual-04b-importar-lancamentos.png)
*Importar Lançamentos — duas fontes disponíveis: CSV e WooCommerce*

Em vez de digitar lançamento por lançamento, você pode importar de duas fontes:

**Acesso:** botão **Importar Lançamentos** no topo da lista de movimentações — a tela tem três abas: **CSV**, **WooCommerce** e **Histórico**.

> 📖 **Conceito · A importação roda em segundo plano**
>
> Depois de confirmar, você não precisa ficar com a tela aberta esperando. O RIT360 Financeiro recebe as linhas, responde em segundos confirmando que elas **entraram na fila**, e processa tudo por trás — você pode navegar para outra tela ou fechar o navegador. Uma planilha de **800 linhas leva cerca de 9 minutos** para ser processada por completo; acompanhe o andamento pela aba **[Histórico](#aba-historico)** e receba um aviso quando terminar. Antes, a tela ficava travada até o fim e uma planilha grande podia **falhar no meio** por demora — hoje isso não acontece mais.

### Importação por CSV

Útil para migrar histórico de planilhas (a base mais comum quando uma OSC começa a usar o RIT360 Financeiro). Faça download do template, preencha as linhas com seus lançamentos antigos, faça upload. O RIT360 Financeiro mostra um **preview** com erros por linha antes de enviar qualquer coisa para a fila; você confirma e as linhas entram na fila de processamento (ver caixa acima).

> ⚠️ **Atenção · Limite de 5.000 linhas por arquivo**
>
> Planilhas com mais de 5.000 linhas são recusadas já no upload — divida o arquivo em partes menores e importe uma de cada vez. Mesmo dentro do limite, uma planilha perto do teto pode levar **cerca de uma hora** para terminar de processar; isso é esperado, não é travamento. Deixe rodando e volte para conferir pelo Histórico.

**Formato:** separador ponto-e-vírgula (`;`); valor em reais com vírgula decimal (`1500,00`); data `DD/MM/AAAA`.

**Colunas aceitas:**

| Coluna | Obrigatória? | Conteúdo |
|---|---|---|
| `data` | Sim | Data do lançamento. |
| `valor` | Sim | Valor em reais, vírgula decimal. Sempre positivo; o tipo define entrada/saída. |
| `descricao` | Sim | Descrição curta. |
| `tipo` | Sim | `receita`, `despesa` ou `transferencia`. |
| `conta` | Sim | Conta de origem (deve existir na OSC). |
| `categoria` | Sim (exceto transferência) | Categoria compatível com o tipo. Transferência não tem categoria. |
| `conta_destino` | Só em transferência | Conta que recebe; obrigatória e diferente da origem. |
| `projeto` | Não | Projeto **aberto** para vincular (qualquer tipo). |
| `centro_de_custo` | Não | Centro de custo para vincular (qualquer tipo). |
| `data_pagamento` | Não | Data de efetivação. Em branco = pendente. |
| `beneficiario` | Não | Quem recebeu/pagou. |
| `forma_pagamento` | Não | `pix`, `cartão`, `dinheiro`, etc. |
| `observacoes` | Não | Texto livre. |

- **Transferência** entre contas da OSC é **uma linha** (`tipo=transferencia`, `conta` + `conta_destino`, sem categoria) — preserva o saldo total.
- **Projeto** não encontrado (fechado/inexistente) → o lançamento entra **sem o vínculo**, com aviso; nunca bloqueia.
- **Conta ou categoria que ainda não existe** na OSC vira uma **pendência resolvida na própria tela de resumo**: criar a categoria que falta, mapear para uma existente, ou deixar as linhas daquela conta de fora para reimportar depois. O casamento de nomes ignora acentos, maiúsculas/minúsculas e espaços.
- **Centro de custo que ainda não existe** também vira **pendência na tela de resumo**, com três opções por nome: **criar** o centro de custo, **mapear** para um existente, ou **importar aquelas linhas sem** centro de custo. Centro de custo em branco (ou coluna ausente) → o lançamento entra sem centro de custo, sem aviso.

> 💡 **Migrando de uma planilha ou de outro sistema?**
>
> O **[Guia de Migração](/migracao/)** cobre o caminho completo — ponto de corte, ordem de montar a base, formato da planilha coluna a coluna, reconciliação e como virar a chave com segurança.

O **template baixável** já vem com todas essas colunas e linhas de exemplo — inclusive uma transferência, uma com projeto vinculado e uma com centro de custo. Baixe, apague os exemplos e preencha com os seus lançamentos.

Parcelas e recorrências não entram por CSV — crie pelo formulário. **Comprovantes, sim:** a planilha tem uma coluna `comprovante` onde você informa o **link** do arquivo (vários links na mesma célula, separados por vírgula, barra vertical ou espaço). Cada linha é criada pela fila e, na sequência, os comprovantes são **baixados** e anexados — também em segundo plano; qualquer link que não baixar fica registrado na **observação** do lançamento. Use o **link direto** do arquivo; links de compartilhamento de nuvem que abrem uma página (em vez de baixar o arquivo) não funcionam.

> ⚠️ **Atenção · Deu erro no meio da importação? Reenvie o mesmo arquivo**
>
> Se a importação for **interrompida** — queda de conexão, fechamento acidental do navegador, falha do lado do servidor — a solução é simples: **envie o mesmo arquivo de novo**. O RIT360 Financeiro reconhece o que já foi processado e **continua de onde parou**, sem criar lançamentos duplicados. Ao escolher um arquivo que já foi importado antes, a tela **avisa** antes de você confirmar, para você saber exatamente o que está prestes a acontecer.
>
> Esta é a mudança mais importante desta versão: **antes**, reimportar depois de um erro duplicava os lançamentos que já tinham entrado, e a única forma segura de corrigir era caçar e apagar as duplicatas na mão. **Hoje não existe mais esse risco** — reenviar é sempre seguro.

Quando a importação termina — com sucesso, com linhas recusadas, ou com falha — quem importou recebe uma **notificação**. Não é preciso ficar de olho na tela esperando. Ela traz um **resumo** (quantos lançamentos foram criados, quantos ficaram de fora por erro, quantos comprovantes foram anexados e quantos não puderam ser baixados) e, quando há falha em comprovante, a **lista dos lançamentos com comprovante não baixado** (título, data e motivo) — facilitando anexar manualmente depois.

### Importação do WooCommerce

Se sua OSC tem loja online em WooCommerce (venda de produtos, doações online, ingressos), pode conectar a loja ao RIT360 Financeiro em **Configurações → Organização → WooCommerce**. Uma vez configurada, pedidos pagos viram receitas automaticamente — diariamente via sincronização programada ou sob demanda pelo botão **Importar agora** desta tela. A sincronização roda **em segundo plano**: a tela responde na hora, você acompanha o andamento pela aba **Histórico** e recebe uma notificação ao concluir; importações grandes se completam sozinhas, em um único disparo.

Mais detalhes na seção de configurações.

### Aba Histórico {#aba-historico}

A terceira aba da tela de importação lista **todas as importações já feitas** na sua OSC — de CSV e de WooCommerce juntas — com:

- o **arquivo** (ou a origem, no caso do WooCommerce);
- a **situação** (na fila, processando, concluída, concluída com linhas recusadas, ou falhou);
- o **andamento** — quantas linhas já foram processadas do total (ex.: *"340 de 800"*), enquanto a importação está rodando;
- o **resultado** final, quando termina;
- um botão para **baixar o relatório das linhas recusadas**, quando houve alguma.

Enquanto há importação em andamento, a aba **se atualiza sozinha**; há também um botão para **atualizar manualmente** a qualquer momento.

> ✓ **Dica · Uma importação interrompida aparece aqui como pista, não como mistério**
>
> Se você fechou a tela sem querer ou a conexão caiu no meio de uma planilha grande, volte à aba Histórico: ela mostra em que ponto a importação parou. A partir daí, o caminho é sempre o mesmo — reenviar o mesmo arquivo (ver caixa acima).

## Conciliação bancária (extrato OFX)

Se você baixa o **extrato do banco em formato OFX** (a maioria dos bancos oferece), pode conciliá-lo com seus lançamentos no RIT360 Financeiro — em vez de marcar conta por conta como paga.

**Acesso:** tela de **Conciliação**, a partir das movimentações.

**Como funciona:**

1. Escolha a **conta** e suba o arquivo `.ofx`.
2. O RIT360 Financeiro lê cada transação do extrato e **procura o lançamento correspondente** (por valor e proximidade de data), organizando tudo em quatro grupos:
   - **Conciliados** — alta confiança no casamento; já vêm pré-marcados.
   - **Em revisão** — casamento provável, mas com alguns dias de diferença; você confirma ou recusa.
   - **Novos** — transações sem lançamento correspondente; você pode **criar** o lançamento (escolhendo a categoria) ou ignorar.
   - **Já conciliados** — transações que você já processou antes (apenas informativo).
3. Ao **confirmar**, os lançamentos conciliados/aceitos são marcados como **pagos** com a data do extrato e ficam vinculados à conciliação; os "novos" que você escolher viram lançamentos.

**Reimportar o mesmo extrato não duplica nada** — cada transação é reconhecida pelo identificador único do banco.

**Quem pode confirmar:** subir e conferir o extrato é uma coisa; **confirmar** — que marca lançamentos como pagos — exige a **permissão de pagar**, a mesma de marcar como pago em Movimentações. Ver [Cargos e permissões](/configuracoes/cargos/#permissao-pagar).

> 💡 **Por que isso importa**
> Conciliar pelo extrato substitui a conferência manual lançamento a lançamento, reduz erro e dá confiança de que o que está registrado no RIT360 Financeiro bate com o banco.

> 🔎 **Não tem o arquivo OFX?** Se você só tem o **saldo final** que aparece na tela do banco, use o **[Caça-diferenças](/modulos/caca-diferencas/)**: informe o saldo e ele aponta na hora onde está a diferença, com correção em um clique. É a conferência rápida "pelo número", complementar a esta conciliação por extrato.

## Prestação de contas {#prestacao-de-contas}

[![Diálogo de prestação de contas](/assets/screenshots/manual-mov-prestacao-contas.png)](/assets/screenshots/manual-mov-prestacao-contas.png)
*Em Exportar → Prestação de contas: escolha o período e, opcionalmente, anexe documentos complementares*

A **prestação de contas** é um documento em PDF, no padrão visual do RIT360 Financeiro, que reúne **tudo o que a organização precisa apresentar de um período** — para a diretoria, o conselho fiscal, a assembleia de associados, um financiador ou um órgão público. Diferente do *Exportar PDF* (que é a lista de lançamentos), a prestação de contas é um **relatório contábil completo, em regime de caixa**, pronto para entregar. Está disponível para a **diretoria/tesouraria** e a **comissão fiscal** da organização.

### O que o documento traz

- **Capa e termo de abertura** — identidade da OSC (razão social, CNPJ), período e regime.
- **Demonstração de receitas e despesas** — totais por categoria, com **gráficos** por grupo e o resultado do período (superávit ou déficit).
- **Posição de caixa por conta** — saldo inicial, créditos, débitos e saldo final de cada conta, com o total geral que reconcilia.
- **Demonstrativo analítico** — lançamento a lançamento, **separado em Receitas, Despesas e Transferências** e agrupado por categoria, com os valores sinalizados e coloridos (entradas em verde com `+`, saídas em vermelho com `−`), no mesmo padrão do extrato. As transferências aparecem com a conta de origem e a de destino.
- **Extrato por conta** — a movimentação cronológica de cada conta, com saldo corrente.
- **Comprovantes** — as imagens e PDFs anexados aos lançamentos, **mesclados ao final** do documento e organizados em três grupos (**Despesas, Receitas e Transferências**), na ordem dos lançamentos. Quando o comprovante é um **documento de escritório** (Word, Excel, PowerPoint, OpenDocument) ou outro arquivo que não dá para exibir embutido, o PDF mostra em seu lugar uma observação **"📎 nome-do-arquivo — disponível no lançamento"** — o comprovante está anexado e continua acessível, só não aparece embutido no relatório. Os lançamentos sem nenhum comprovante ficam listados à parte.
- **Documentos complementares** (opcional) — outros documentos que você anexar na hora de gerar (extrato bancário, parecer da comissão fiscal, notas explicativas), incluídos **no fim do PDF**, cada um precedido de uma folha com título e descrição.
- **Termo de encerramento** — com os nomes do **Presidente** e do **Tesoureiro** e um bloco de **autenticação eletrônica** (data/hora de geração e um código de verificação único do documento).

### Documentos complementares (opcional)

Além dos comprovantes dos lançamentos, você pode **anexar outros documentos** ao relatório no momento de gerar — por exemplo, o **extrato bancário** do período, o **parecer da comissão fiscal** ou **notas explicativas**. O objetivo é entregar a prestação de contas **completa em um único PDF**, sem precisar mandar anexos soltos por e-mail depois.

Os documentos ficam **vinculados àquele período**: se você gerar o mesmo período de novo, eles **reaparecem já anexados**, prontos para complementar ou remover. No PDF, entram **no fim, depois dos comprovantes**, cada um precedido de uma folha com o título e a descrição que você informou.

Para anexar, na seção **Documentos complementares** do diálogo: escolha o arquivo (PDF ou imagem), preencha o **título** (obrigatório) e uma **descrição** opcional, e clique em **Anexar este documento**. Repita para quantos documentos quiser.

> ⚠️ Escolher o arquivo **não basta** — é o botão **Anexar este documento** que efetiva o anexo. Se você clicar em *Gerar PDF* com um arquivo escolhido mas ainda não anexado, o RIT360 Financeiro anexa automaticamente (quando há título) ou avisa para você concluir antes.

### Como gerar

1. Em **Movimentações**, clique em **Exportar → Prestação de contas**.
2. Escolha o período:
   - **Mês** — um mês específico já **fechado** (o mês corrente, ainda em andamento, não fica disponível);
   - **Ano (acumulado)** — de janeiro até o último mês fechado daquele ano (ou o ano inteiro, se for um ano anterior).
3. Clique em **Gerar PDF**. A geração roda **em segundo plano**: você pode continuar trabalhando, e **o link do PDF chega no seu e-mail** assim que ficar pronto (a montagem com gráficos e comprovantes pode levar de alguns segundos a poucos minutos). Se algo falhar, você é avisado por e-mail e por notificação no app.

### Onde encontrar os documentos já gerados

Você **não depende do e-mail** para chegar a uma prestação de contas: todo documento gerado fica listado na página **[Prestações de contas](/modulos/relatorios/#prestacoes-de-contas)**, dentro de **Relatórios** — acessível pela pílula de mesmo nome, ao final da fileira de filtros. Lá você vê período, data e hora da geração, quem gerou e o intervalo coberto, e pode **baixar**, **gerar de novo** ou **apagar o arquivo**. A organização também pode definir, em **Configurações → Relatórios**, um **prazo de guarda** para esses PDFs — que por padrão é "sem descarte".

> 💡 **Por que isso importa · Transparência e governança não são burocracia**
>
> Em uma OSC, **prestar contas é o que sustenta a confiança** — de quem doa, de quem fiscaliza, de quem assina junto. Um relatório completo, com os comprovantes anexados e a posição de caixa que reconcilia, responde de uma vez às perguntas que sempre voltam: *"para onde foi o dinheiro?", "esse gasto tem nota?", "o saldo bate?"*. Gerar a prestação de contas a cada mês fechado — e o acumulado para a assembleia anual — cria um **histórico íntegro e fácil de auditar**, protege a diretoria atual e a futura, e transforma a prestação de contas de uma correria de fim de ano em um clique.

> ⚠️ **Atenção · O PDF reflete o que está registrado**
>
> A prestação de contas só é tão boa quanto os dados que a alimentam. Lançamentos sem categoria, despesas sem comprovante anexado ou contas desatualizadas aparecem assim no relatório. Use a rotina semanal e a conferência mensal contra o extrato para chegar ao fim do período com a prestação pronta — e **anexe os comprovantes na hora de lançar**.

## Boas práticas

> ✓ **Dica · Adote uma rotina semanal de 15 minutos**
>
> A maior dor de OSCs amadoras na função financeira é deixar tudo acumular para o fim do mês. Aí cada lançamento exige resgatar comprovante, lembrar contexto, perguntar para gente que já esqueceu. **Reserve 15 minutos uma vez por semana** (toda terça de manhã, por exemplo) para registrar a movimentação da semana. É a diferença entre ter a contabilidade da OSC sempre pronta e viver apagando incêndio no dia 25.

> ✓ **Dica · Confira a lista contra o extrato bancário todo mês**
>
> No final do mês, abra o extrato do banco e a lista de movimentações do RIT360 Financeiro filtrada pelo mês. Cada linha do extrato deve ter um lançamento correspondente. Diferenças vão aparecer (taxa que você esqueceu, transferência que veio sem aviso) — corrigir essas diferenças mensalmente é mil vezes mais fácil do que descobrir 6 meses depois.

> ⚠️ **Atenção · Cuidado com transferências entre contas**
>
> Quando você move R$ 5.000 do banco para a poupança, **não é despesa nem receita** — é transferência. Se você lançar errado como despesa em "Banco" e como receita em "Poupança", o relatório vai mostrar que sua OSC gastou R$ 5.000 e ganhou R$ 5.000 do nada. Sempre use o tipo **Transferência** nesses casos; ele preserva o saldo geral e mantém os relatórios limpos.

## Glossário rápido

- **Receita** — dinheiro entrando na OSC.
- **Despesa** — dinheiro saindo da OSC.
- **Transferência** — movimento interno entre contas da própria OSC; não afeta o saldo total.
- **Vencimento** — data prevista para o pagamento (campo planejado).
- **Pagamento** — data em que o pagamento foi efetivamente realizado (campo realizado).
- **Categoria** — classificação contábil do lançamento (ex: Aluguel, Material didático, Doações).
- **Centro de custo** — agrupamento gerencial paralelo à categoria (ex: Sede, Filial-Norte).
- **Projeto** — agrupamento por iniciativa (ex: Acampamento 2026, Campanha do Agasalho).
- **Estorno** — reversão de um lançamento já pago, com criação automática de lançamento contrário.
- **Recorrente** — lançamento que se repete automaticamente em intervalo fixo.
- **Parcelado** — valor único dividido em parcelas com datas distintas.
- **Regime de caixa** — modelo contábil em que o que vale é a data de entrada/saída do dinheiro, não a data do contrato.
- **Realizado** — o que já foi efetivamente pago ou recebido; o dinheiro mexeu na conta.
- **Previsto** — o que está pendente ou atrasado; ainda vai acontecer.
- **Líquido** — a posição consolidada da OSC: tudo o que ela tem (ativos) menos tudo o que ela deve (passivos).

## Por onde seguir

- **Reembolsos** — para registrar despesas pagas com dinheiro próprio por voluntários ou diretores.
- **Pedidos de Pagamento** — para pedir aprovação antes de uma despesa ser paga.
- **Relatórios** — para visualizar fluxo de caixa, comparativos por categoria, evolução do saldo.
- **Configurações → Categorias** — para deixar suas categorias enxutas e consistentes.
