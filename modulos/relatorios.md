---
title: "Relatórios"
nav_order: 7
parent: "Módulos"
permalink: /modulos/relatorios/
---

O módulo de **Relatórios** consolida o que entra e o que sai da sua OSC em **análises gerenciais prontas para uso** — sem precisar exportar planilha, montar gráfico, copiar e colar. É onde a diretoria descobre quanto há em caixa, para onde o dinheiro está indo, o que merece atenção este mês e o que esperar dos próximos meses.

> 💡 **Por que isso importa**
>
> O dado que entra no sistema todo dia (lançamentos, reembolsos, pedidos) **só vale se vira informação para decidir**. OSC sem relatórios financeiros bem feitos toma decisões no escuro: contratar ou não contratar, gastar ou poupar, captar ou esperar. Relatório bom não é firula visual — é base para a diretoria escolher caminho com segurança e para a OSC prestar contas com transparência para conselho, financiadores e assembleia.

## Conceitos essenciais

Antes de entrar nos botões, vale firmar dois conceitos que aparecem em toda a página.

> 📖 **Conceito · Regime de caixa**
>
> Toda análise dos Relatórios olha o **dinheiro que de fato entrou ou saiu** — não o que estava contratado ou previsto. Receita só conta quando a doação **caiu na conta**; despesa só conta quando o pagamento **saiu da conta**. Por isso o bloco "Resultado do período" usa apenas movimentações com status **Pago**. Esse é o padrão usado por OSC para prestação de contas e bate com a forma como tesoureiros amadores enxergam o dinheiro: "quanto tem na conta hoje?".

> 📖 **Conceito · O mesmo critério vale na página pública**
>
> A [Página Pública](/configuracoes/pagina-publica/) de transparência da OSC usa **exatamente este critério**: só entram lançamentos efetivamente pagos ou recebidos no período, pela data de pagamento; estornos não contam; transferências entre contas da própria organização não são receita nem despesa. É por isso que os valores da página pública podem **não bater com o que você vê em [Movimentações](/modulos/movimentacoes/)**, que lista também pendentes e atrasados — não é inconsistência, são perguntas diferentes. A página pública ainda para sempre no **último mês encerrado**, para nunca publicar número de mês em rascunho.

> 📖 **Conceito · Período anterior equivalente**
>
> O toggle **Comparar com período anterior** no cabeçalho compara o período carregado com o **mesmo tamanho de janela imediatamente anterior**. Se você está olhando Abril/2026 completo, a comparação é com Março/2026 completo. Se você selecionou um intervalo personalizado de 12 dias, a comparação é com os 12 dias anteriores ao início. Quando o período é um **mês em andamento** (ex: Maio até hoje), a comparação é com o mesmo número de dias do mês anterior — não com o mês anterior inteiro. Isso evita que uma comparação "honesta" mostre o mês em curso "menor" só porque ainda não terminou.

## Quem acessa

Acesso a Relatórios é restrito a três papéis:

- **Presidente** — visão completa
- **Tesoureiro** — visão completa
- **Comissão Fiscal** — visão completa (consulta; sem operação)

Voluntários e Coordenadores de Projeto têm acesso restrito a Relatórios no momento.

> 💡 **Novidade · Filtro por projeto**
>
> Com o módulo de [Projetos](/modulos/projetos/), os Relatórios ganharam um **filtro por projeto** no cabeçalho: selecione uma iniciativa e a página passa a mostrar apenas receitas, despesas e gráficos daquele projeto — pronto para a prestação de contas específica de um financiador. Cada projeto também tem uma aba **Relatório** própria, com os mesmos números recortados.

## Uma página só, de cima a baixo

[![Página de Relatórios com resultado do período, evolução do saldo, saldo por conta e receitas/despesas por categoria](/assets/screenshots/manual-relatorios-01-visao-geral.png)](/assets/screenshots/manual-relatorios-01-visao-geral.png)
*Relatórios — resultado do período, evolução do saldo, saldo por conta na data final, e receitas/despesas lado a lado*

Relatórios deixou de ter abas: é hoje **uma página única**, que você rola de cima a baixo, com os filtros e o período do cabeçalho valendo para tudo. **A URL reflete o estado completo** (período, filtros, comparativo ligado/desligado): copiar e enviar o link leva outra pessoa exatamente ao mesmo recorte.

> 💡 **Por que isso importa**
>
> Antes, cada pergunta ficava numa aba separada — trocar de "Visão geral" para "Receitas" perdia o fio da leitura. Numa página só, o resultado do mês, a curva do saldo, o saldo por conta e a composição por categoria aparecem juntos, na ordem em que a diretoria costuma perguntar: quanto sobrou, como o caixa andou, quanto tem em cada conta, e onde foi o dinheiro.

### Resultado do período

Receitas menos despesas pagas, em destaque com cor semântica (verde se positivo, vermelho se negativo). Com comparativo ligado, mostra também variação em R$, em % e seta de tendência.

### Evolução do saldo

Gráfico de linha mostrando a trajetória do saldo da OSC ao longo do período. Quando o comparativo está ligado, uma linha pontilhada sobrepõe a evolução do período anterior.

### Saldo por conta na data final

Cards com o saldo de cada conta financeira na **data final do período** (não "hoje"). Isso garante coerência com prestação de contas histórica: o saldo mostrado é o que de fato existia no fechamento daquele mês. Contas de **uso restrito** aparecem à parte, fora do total líquido consolidado — mesma separação que já existe no Painel.

### Receitas e despesas por categoria

Receitas e despesas aparecem **lado a lado**, não mais em abas separadas — dá para comparar entrada e saída sem trocar de tela:

- **Gráfico** por categoria (barras horizontais com as principais categorias do período).
- **Tabela detalhada** com valor absoluto e % do total, ordenada da maior categoria para a menor.
- Com **comparativo ligado**: colunas extras com valor do período anterior, variação em R$, variação em % e seta de tendência.
- **Drilldown** — clique em uma linha de categoria e o RIT360 Financeiro abre `/movimentacoes` já filtrado por essa categoria + o mesmo período. Você passa do agregado para o detalhe em um clique.

## Onde foram parar Atenção e Previsão

Duas seções que antes eram abas desta tela **mudaram de casa**, e continuam existindo — só que na tela inicial, não aqui:

- **Pontos de atenção** — as anomalias detectadas nos seus lançamentos (despesa concentrada, categoria com pico, fornecedor novo, categoria que voltou, queda de receita) agora moram só no **[Painel](/modulos/painel/#bloco-4-pontos-de-atencao)**, considerando os últimos 30 dias. Os limites de cada regra continuam configuráveis em **Configurações → Relatórios**, no mesmo lugar de sempre.
- **Previsão** — a projeção de saldo mês a mês virou a terceira aba da tela inicial, ao lado do Painel e da Saúde 360: veja **[Painel → Previsão](/modulos/painel/#previsao)**. Os mesmos filtros (Tipo, Projeto, Conta, Categoria, Centro de custo) e o mesmo horizonte de 3, 6 ou 12 meses continuam lá.

> ⚠️ **Atenção · Se você procurar aqui, não vai achar**
>
> Se você está acostumado a abrir Relatórios para ver os avisos ou a projeção, essa é a mudança que mais pega quem já usava o sistema. Não é bug: **Atenção e Previsão saíram desta tela de propósito**, para responder à pergunta "para onde vamos" no mesmo lugar onde já se responde "o que urge hoje" e "como estamos" — a tela inicial.

## Filtros e período compartilhados

Filtros disponíveis na barra do cabeçalho:

- **Período** — presets (mês corrente, mês anterior, trimestre, semestre, **Ano até a data atual**, Ano atual, ano anterior) + intervalo customizado. Default: último mês fechado.
- **Tipo** (receita / despesa)
- **Projeto** (multi-select)
- **Conta** (multi-select)
- **Categoria** (multi-select)
- **Centro de custo** (multi-select)

> 📖 **Conceito · "Ano até a data atual" × "Ano atual"**
>
> **Ano até a data atual** vai de 1º de janeiro **até hoje** — é o recorte para responder *"como o exercício está indo?"*, seja para avaliar desempenho ou levar um número à diretoria. **Ano atual** cobre o **ano de calendário inteiro**, até 31 de dezembro, incluindo meses que ainda nem chegaram — útil quando você quer enxergar também o que já está programado até o fim do ano. Os dois atalhos existem igualmente em [Movimentações](/modulos/movimentacoes/).

> 📖 **Conceito · Por que status não aparece como filtro**
>
> Relatórios usam **regime de caixa** (ver início desta página): consideram apenas movimentações com status `pago`, agregadas pela data de pagamento. Pendentes e cancelados não entram no cálculo.

## Comparativo com período anterior

Toggle no cabeçalho. Quando ligado, cada bloco/gráfico/tabela da página mostra também a variação contra o período anterior equivalente.

## Exportação

Botão **Exportar** no cabeçalho. Três opções:

- **Exportar visão atual (PDF)** — a página com o recorte atual de filtros e período
- **Exportar relatório completo (PDF)** — o relatório completo, com sumário no topo
- **Exportar dados (Excel)** — planilha com uma worksheet por seção

O **Excel** baixa na hora, como sempre. Já o **PDF** — nas duas variantes — é montado **em segundo plano**: ao clicar em exportar, abre uma página de acompanhamento com "Gerando…" e, assim que o documento fica pronto, **o download começa sozinho**. Você não precisa esperar parado — pode fechar a aba e continuar trabalhando, porque **o link do PDF também chega no seu e-mail**. É o mesmo comportamento já usado na exportação de Movimentações e na prestação de contas.

[![Página de acompanhamento do PDF de Relatórios](/assets/screenshots/manual-relatorios-pdf-acompanhamento.png)](/assets/screenshots/manual-relatorios-pdf-acompanhamento.png)
*A página de acompanhamento: quando o PDF fica pronto, o download começa sozinho (e o link também chega por e-mail).*

> ⚠️ **Atenção · Quem quer o número agora usa Excel; quem quer o documento para apresentar usa PDF**
>
> A espera do PDF é curta (segundos, raramente mais que isso), mas existe — porque agora ele é **montado como documento de apresentação**, não só exportado. Precisa de um número na hora, para conferir algo rápido? Peça o **Excel**, que continua imediato. Precisa de um documento pronto para enviar à diretoria, ao conselho ou a um financiador? Peça o **PDF** e deixe a aba de acompanhamento (ou o e-mail) avisar quando estiver pronto.

Todos os PDFs trazem, agora, uma **capa** com o logo e a identidade visual da organização, seguida de um bloco de destaque com **receitas, despesas e o resultado do período** — rotulado como **Superávit** ou **Déficit**, em vez de uma linha solta de texto — e **numeração de páginas**. O relatório completo também ganhou **gráficos de verdade**: a evolução do saldo e a composição por categorias de receitas e despesas saem impressas como gráfico, não só como tabela de números.

> 💡 **Dica · No gráfico de evolução do saldo, repare na base do eixo**
>
> Nos gráficos de composição por categoria, o eixo começa em zero, que é a referência certa para comparar valores. Já no gráfico **Evolução do saldo**, o eixo vertical **não começa em zero** — ele se ajusta à faixa de valores do período, e o próprio documento avisa isso logo abaixo do gráfico. É proposital: se o saldo da OSC variou, por exemplo, entre R$ 149 mil e R$ 155 mil, um eixo começando em zero faria essa variação de R$ 6 mil parecer uma linha reta, escondendo o movimento. Ajustando a base à faixa dos valores, a variação real fica visível — mas isso também significa que **a inclinação da linha não deve ser lida como se o eixo partisse de zero**: confira sempre os valores nas extremidades antes de concluir que o saldo subiu ou caiu muito.

> 📖 **Novo · A série diária de saldo virou anexo**
>
> Num relatório de um mês inteiro, a tabela dia a dia do saldo ocupava uma página só de números quase repetidos, enquanto o gráfico de evolução mostra a mesma informação de relance. Por isso essa tabela **saiu do corpo do PDF e passou para um anexo no final do documento** — quem só quer entender a tendência lê o gráfico; quem precisa conferir dia a dia encontra a tabela no anexo, sem que ela atrapalhe a leitura do relatório.

Fora a capa, os gráficos e essa reorganização, **o conteúdo é o mesmo de sempre**: cabeçalho identificador (nome da OSC, escopo, período, filtros aplicados, estado do comparativo e data/hora de geração), Receitas/Despesas com **todas** as categorias (não só o top 10), Atenção com a lista completa de anomalias (mensagem, severidade textual e regra) e Previsão com a tabela mês a mês e a coluna "Origem". **Os números e os cálculos não mudaram** — só a forma como o documento se apresenta.

> 📖 **Novo · Seção "Execução por Centro de Custo" na prestação de contas**
>
> Quando a OSC usa o módulo de [Orçamento](/modulos/orcamento/), a prestação de contas ganha uma seção **"Execução por Centro de Custo"**: para cada área da OSC, ela mostra o **previsto**, o **realizado** e o quanto do previsto já foi consumido no ano. É a forma de mostrar a financiadores e à diretoria não só quanto foi gasto, mas quanto foi gasto **em relação ao que se planejou** — o mesmo previsto × realizado do orçamento, agora dentro do relatório oficial.

## Prestações de contas geradas {#prestacoes-de-contas}

Toda vez que alguém gera uma [prestação de contas](/modulos/movimentacoes/#prestacao-de-contas), o documento fica **guardado na organização** — e é na área **[Documentos](/modulos/documentos/)** que você encontra todas as que já foram geradas, filtrando por tipo "Prestação de contas". A antiga página de prestações dentro de Relatórios não existe mais; o catálogo de Documentos é o novo lugar único para isso.

> 💡 **Por que isso importa · O documento deixou de depender do e-mail**
>
> Antes da área de Documentos, o único caminho para chegar a uma prestação de contas já gerada era **o link enviado por e-mail** na hora da geração. Quem gerou trocou de e-mail, apagou a mensagem sem querer ou simplesmente não estava na organização na época? O documento existia, mas ninguém alcançava. Agora ele está **na plataforma, à vista de toda a diretoria** — e a prestação de contas do ano passado continua a um clique quando o conselho, o financiador ou a auditoria pedirem.

Em Documentos, cada linha traz quem pediu e quando, e o **Baixar** quando o arquivo ainda está disponível. Gerar de novo é feito voltando ao diálogo em [Movimentações → Prestação de contas](/modulos/movimentacoes/#prestacao-de-contas), escolhendo o mesmo período — cada geração entra como um registro novo, não substitui a anterior.

### Como quem recebe confere a autenticidade {#conferir-autenticidade}

Toda prestação de contas em **PDF** sai com um **código de verificação e um QR Code**, impressos duas vezes no documento: na capa e no Termo de Encerramento, ao lado das assinaturas. Qualquer pessoa que receber esse PDF — inclusive alguém **de fora da OSC, sem login no sistema** — pode conferir, numa página pública, que aquele arquivo específico foi mesmo emitido pela organização e não foi alterado depois de gerado.

> 💡 **Por que isso importa**
>
> Um financiador, um conselheiro ou um auditor não tem como saber, só olhando um PDF, se ele é o documento original ou uma versão editada. O selo resolve isso sem exigir confiança cega: em vez de acreditar na palavra de quem entregou o arquivo, quem recebe confere direto com o sistema que o emitiu. É também uma forma de a OSC se proteger — um documento falsificado em nome dela não passa pela conferência.

**Como conferir**, sem precisar de conta nem senha:

1. Acesse **financeiro.rit360.org.br/verificar** (o mesmo endereço impresso no PDF), ou aponte a câmera do celular para o **QR Code** do documento.
2. Digite o **código de verificação** que aparece no rodapé do PDF — pode digitar com ou sem espaços e hífens, o sistema entende do mesmo jeito. Quem chegou pelo QR Code não precisa digitar nada: a conferência já roda sozinha.
3. Clique em **Conferir**.

[![Página pública de conferência de autenticidade, com o campo para digitar o código de verificação](/assets/screenshots/manual-verificar-documento.png)](/assets/screenshots/manual-verificar-documento.png)
*A página de conferência — sem login, sem menu, só o campo do código*

A página devolve um destes resultados:

- **Documento reconhecido** — é a versão vigente, emitida pela organização indicada, com o tipo, o período e a data de emissão.
- **Documento reconhecido, mas substituído** — a organização gerou de novo o mesmo período depois; o código ainda é autêntico, mas não é mais a versão atual. Quem recebeu deve pedir a versão nova.
- **Documento reconhecido, arquivo removido** — o documento foi emitido de fato, mas o PDF já não está guardado no sistema (por prazo de guarda vencido, ou porque alguém apagou o arquivo). O registro da emissão continua válido; o que não existe mais é o arquivo.
- **Código não reconhecido** — nenhum documento deste sistema corresponde ao código digitado. Confira a digitação; se o código veio impresso, o problema pode ser leitura errada de um caractere parecido (zero e letra O, por exemplo — o campo já corrige essas trocas comuns sozinho).

> 📖 **Conceito · A página confirma, não mostra**
>
> A conferência **nunca exibe o conteúdo financeiro do documento** — nem valores, nem nomes, nem anexos. Ela só responde "este código corresponde a um documento real, emitido por esta organização, nesta data, para este período?". Quem quer ver o conteúdo precisa do próprio PDF, entregue por quem gerou.

> ⚠️ **Atenção · Só o PDF tem selo**
>
> A versão em **planilha** da prestação de contas **não leva** código nem QR Code — ela é editável, então não serviria como prova de autenticidade mesmo que tivesse um. Quem precisa comprovar o documento perante terceiros deve gerar em PDF, não em planilha. Ver [Movimentações → Formato de saída](/modulos/movimentacoes/#formato-de-saida-prestacao).

> ✓ **Dica · Avise quem recebe que o documento pode ser conferido**
>
> Quase ninguém sabe, de cara, que o PDF se verifica sozinho — e essa informação sozinha já aumenta a confiança de quem recebe. Ver [Usar os relatórios para captar recurso](/gestao/relatorios-para-captacao/#5-use-o-selo-de-autenticidade).

### E se for preciso apagar o arquivo de uma prestação?

Dá, por dois caminhos: direto na área **[Documentos](/modulos/documentos/#excluir-arquivo)** (por linha ou em lote, junto com qualquer outro tipo de documento), ou na tela de **Prestações geradas**, alcançável pelo botão de mesmo nome em Movimentações, ao lado de "Prestação de contas" — que continua existindo e mostrando o histórico completo de cada prestação, inclusive as que já perderam o arquivo.

Em qualquer um dos dois lugares, cada linha que ainda tem arquivo oferece **Apagar o arquivo** (ou **Excluir arquivo**, em Documentos), e também dá para apagar vários de uma vez pela seleção em lote. A ação pede confirmação antes, dizendo quantos documentos serão afetados.

> ⚠️ **Quem pode, e o que exatamente some**
>
> Apagar o arquivo é ação destrutiva e está restrita a quem administra a plataforma ou tem a permissão de **exportar dados** da organização. Quem não tem simplesmente não vê o botão, em nenhuma das duas telas.
>
> O que some é **o PDF**, não o registro. Em **Prestações geradas**, o período continua listado, com quem pediu e quando, e a marca de quando o arquivo foi removido e por quem. Em **Documentos**, porém, um documento sem arquivo **deixa de aparecer na lista** (desde a v1.97.1) — o registro não some, só a tela que o mostra é outra. Se precisar do conteúdo de novo, gere a prestação outra vez pelo mesmo período.

Há ainda o caminho automático: o **prazo de guarda** configurado pela organização (abaixo), que apaga os arquivos vencidos sem ninguém precisar agir.

## Guarda dos documentos de prestação de contas {#guarda-dos-documentos}

[![Guarda dos documentos de prestação de contas](/assets/screenshots/manual-prestacoes-guarda-config.png)](/assets/screenshots/manual-prestacoes-guarda-config.png)
*Configurações → Relatórios — o bloco de guarda fica acima das regras de pontos de atenção*

**Por padrão, nada é descartado: os PDFs ficam guardados para sempre.** Se a sua organização não fizer nada, é assim que continua funcionando — este ajuste só entra em ação quando alguém escolhe um prazo.

Em **Configurações → Relatórios**, no bloco **Guarda dos documentos de prestação de contas**, a organização define por quantos anos os PDFs são mantidos:

- **Sem descarte (guardar para sempre)** — o padrão
- **1 ano**, **2 anos**, **3 anos**, **5 anos** ou **10 anos**

A contagem começa no **fim do período coberto** pelo documento, não na data em que ele foi gerado. Uma prestação de Março/2026 com prazo de 5 anos vence em março de 2031, mesmo que tenha sido gerada de novo em 2027.

Ao escolher um prazo, **antes de salvar** a tela informa quantos documentos **já estariam vencidos** por aquela regra e quantos **vencem nos próximos 30 dias** — você vê o efeito da decisão antes de tomá-la.

> 📖 **Conceito · Ninguém é pego de surpresa**
>
> Com um prazo configurado, o RIT360 Financeiro **avisa por e-mail 30 dias antes** de qualquer descarte, listando os documentos que vão sair e permitindo baixá-los enquanto dá tempo. Se o prazo for **alterado**, o aviso anterior perde a validade e **a contagem recomeça** — nenhum documento é descartado antes do que foi comunicado.

> ⚠️ **Atenção · O registro nunca é apagado**
>
> O descarte automático remove **apenas o arquivo**. A prestação continua listada em [Documentos](/modulos/documentos/), com status **Arquivo indisponível** — lembrando que gerar de novo reflete os dados atuais, não o original.

> ✓ **Dica · Só configure prazo se houver política que peça isso**
>
> Prazo de guarda existe para organizações com política de retenção definida (por estatuto, por exigência de financiador ou por decisão de conselho). Se a sua não tem uma, **deixe em "sem descarte"** — PDF ocupa pouco espaço, e prestação de contas é justamente o tipo de documento que se lamenta ter perdido. Quando houver política, configure o prazo mais **longo** que ela permitir.

## Configuração das regras de atenção

[![Configuração de regras](/assets/screenshots/manual-config-relatorios-regras.png)](/assets/screenshots/manual-config-relatorios-regras.png)
*Configurações → Relatórios → Regras de pontos de atenção — cards editáveis, um por regra*

Acessível em **Configurações → Relatórios → Regras de pontos de atenção** (só Presidente). Um card por regra — as cinco regras que aparecem no bloco de [Pontos de atenção do Painel](/modulos/painel/#bloco-4-pontos-de-atencao) **e** a regra de **Déficit projetado no fluxo de caixa**, exclusiva de lá. Cada card tem:

- **Toggle on/off** — ligar ou desligar a regra
- **Limite (threshold)** em campo numérico editável com unidade clara (%, ×, R$ ou meses)
- **Link "Restaurar padrão"** — volta ao valor default daquela regra

No rodapé: **Salvar alterações** (só habilita se houver mudança) e **Restaurar todas as regras ao padrão** (com confirmação modal).

> 📖 **Card · Déficit projetado no fluxo de caixa**
>
> Vem **ligado por padrão**. O limite, aqui, é a **antecedência**: com quantos meses de folga o RIT360 Financeiro deve avisar sobre um déficit projetado — **3, 6 ou 12 meses** (padrão: 6). Quanto maior a antecedência, mais cedo o aviso aparece, mas também mais sujeito a mudar conforme novos lançamentos entram no sistema.

### Calibrar pelo histórico

Quando a OSC tem **6 ou mais meses de movimentação registrada**, o botão **Calibrar pelo histórico** dispara uma análise estatística: para cada regra, o RIT360 Financeiro calcula um limite sugerido baseado no padrão real da sua OSC. Útil porque tesoureiros raramente sabem chutar bons valores ("20% é muito? 30%?") — calibração entrega valores ancorados no histórico real.

Cada sugestão vem com **nível de confiança** (alta / média / baixa, dependendo do volume de histórico) e **justificativa em linguagem natural** (ex: *"Sua maior despesa única costuma ser 27% do total — sugerimos alertar a partir de 30%"*).

Três opções na hora de revisar:

- **Aceitar todas as sugestões** — aplica em transação única (tudo ou nada; se uma falha, nenhuma é salva)
- **Editar individualmente** — fecha o diálogo deixando os valores propostos pré-preenchidos nos cards; admin ajusta e clica Salvar
- **Cancelar** — descarta sem aplicar

> ✓ **Dica · Comece pelos defaults e calibre só depois de 6 meses**
>
> Os limites default (20% / 2× / R$ 5.000 / 3 meses / 70%) foram escolhidos para serem **conservadores** — disparam pouco em OSC saudável, mas mostram sinais claros quando algo sai do padrão. Use os defaults nos primeiros 6 meses. Quando atingir o histórico mínimo, rode a calibração — os limites passam a ser **personalizados para a sua OSC**, não para uma OSC genérica.

## Boas práticas

> ✓ **Dica · Olhe Relatórios uma vez por mês, no dia 5**
>
> Reserve 30 minutos no dia 5 de cada mês para abrir Relatórios filtrado no mês anterior fechado e dar uma volta pela página — resultado, evolução do saldo, receitas e despesas por categoria. Passe também pelo [Painel](/modulos/painel/) para conferir os pontos de atenção do período. Em 5 minutos você sabe se houve algo fora do esperado. Em outros 25, você manda o PDF do "relatório completo" para a diretoria com filtros do mês fechado — virou prestação de contas mensal sem esforço.

> ✓ **Dica · Previsão antes de decisão grande**
>
> Antes de aprovar contratação, compra grande ou novo projeto, abra a [aba Previsão](/modulos/painel/#previsao) da tela inicial, com horizonte de 6 ou 12 meses. Veja se o gasto extra mantém o saldo positivo. Se o gráfico mostra vermelho aparecendo em algum mês, a decisão precisa de mais conversa antes — não menos.

> ⚠️ **Atenção · Comparativo só faz sentido se o período faz sentido**
>
> Comparar Abril/2026 (mês fechado) com Março/2026 é direto. Comparar "Maio até hoje" (10 dias) com "10 dias antes de maio" também — mesma janela. Mas comparar "Ano até hoje" com algo... não tem comparação intuitiva. Em períodos não-canônicos, leia a variação com cautela.

## Glossário rápido

- **Regime de caixa** — modelo em que o que vale é a data em que o dinheiro entrou/saiu da conta, não a data do contrato ou da fatura.
- **Período anterior equivalente** — janela imediatamente anterior, com a mesma duração do período carregado.
- **Comparativo** — toggle que adiciona variação versus período anterior em cada bloco.
- **Anomalia** — evento detectado por uma das 5 regras determinísticas de [Pontos de atenção, no Painel](/modulos/painel/#bloco-4-pontos-de-atencao); ranqueado por severidade.
- **Déficit projetado no fluxo de caixa** — regra exclusiva do Painel que avisa quando o caixa tende a ficar negativo em um mês futuro, considerando agendados e, quando necessário, a média histórica.
- **Severidade** — leve / moderada / alta, derivada do quanto o evento ultrapassa o limite da regra.
- **Calibração** — análise estatística que sugere limites de regras personalizados ao padrão da sua OSC.
- **Forecast (projeção)** — estimativa do comportamento financeiro futuro, combinando agendados (já cadastrados) com estimados (média histórica); veja [Painel → Previsão](/modulos/painel/#previsao).
- **Prestação de contas (documento)** — o relatório contábil completo de um período, gerado em PDF ou planilha em Movimentações e listado na área de [Documentos](/modulos/documentos/).
- **Selo de autenticidade** — o código de verificação e o QR Code impressos no PDF da prestação de contas, que permitem a qualquer pessoa conferir a emissão numa página pública, sem login.
- **Código de verificação** — a sequência impressa no PDF que se digita em [financeiro.rit360.org.br/verificar](https://financeiro.rit360.org.br/verificar) para conferir a autenticidade — ver [Como quem recebe confere a autenticidade](#conferir-autenticidade).
- **Prazo de guarda** — por quantos anos os PDFs de prestação de contas são mantidos, contados do fim do período coberto. Padrão: sem descarte.
- **Descarte** — remoção apenas do arquivo PDF; o registro da prestação permanece listado, marcado como indisponível.

## Por onde seguir

- **Movimentações** — onde estão os lançamentos que alimentam todas as análises, e onde a [prestação de contas](/modulos/movimentacoes/#prestacao-de-contas) é gerada.
- **[Painel](/modulos/painel/)** — pontos de atenção e previsão de caixa, que saíram de Relatórios e viraram abas da tela inicial.
- **[Documentos](/modulos/documentos/)** — onde ficam as prestações de contas e os PDFs já gerados.
- **Configurações → Categorias** — relatório bom depende de categorização consistente.
- **Configurações → Relatórios** (Presidente) — ajustar limites de pontos de atenção, calibrar pelo histórico e definir o prazo de guarda dos documentos de prestação de contas.
