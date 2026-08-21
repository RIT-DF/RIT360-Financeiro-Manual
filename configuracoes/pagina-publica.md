---
title: "Página Pública"
nav_order: 7
parent: "Configurações da Organização"
permalink: /configuracoes/pagina-publica/
---

> Disponível para quem administra a configuração da organização — na prática, **Presidente (admin)**.

A **Página pública** é um endereço aberto, **sem login**, em que a sua OSC mostra ao mundo o que arrecadou e no que aplicou. Quem tem o link — doador, financiador, conselho, associado, jornalista, qualquer pessoa — abre e vê os números do período, direto do sistema, sem precisar pedir nada a ninguém.

Ela fica em **Configurações → Página pública** e o endereço é sempre no formato:

```
financeiro.rit360.org.br/transparencia/sua-organizacao
```

[![Configurações — Página pública](/assets/screenshots/config-pagina-publica.png)](/assets/screenshots/config-pagina-publica.png)
*Configurações → Página pública — chave de publicar/despublicar, endereço, link, QR Code e missão*

> 💡 **Por que isso importa**
>
> Existe uma diferença enorme entre uma OSC que **é cobrada** por prestação de contas e uma que **presta contas por iniciativa própria**. A primeira responde a pedidos, um a um, sempre atrasada e sempre montando planilha de última hora. A segunda publica, aponta o link e segue trabalhando. Isso se chama **transparência ativa**, e ela resolve quatro coisas ao mesmo tempo: (1) **prestação de contas à sociedade**, que é a razão de ser de uma organização sem fins lucrativos; (2) **exigência de editais e financiadores**, que cada vez mais pedem endereço público de transparência como critério de habilitação; (3) **obrigação de publicidade** para quem recebe recurso público — parcerias, convênios, termos de fomento e colaboração costumam trazer essa cláusula; (4) **credibilidade para captar** — doador confia em quem mostra número, e desconfia de quem só mostra foto. Some a isso um detalhe que vale mais do que parece: **o número vem do sistema, não de uma planilha montada à mão**. Uma OSC que consegue publicar um panorama financeiro atualizado sem retrabalho está, implicitamente, provando que tem controle interno. Isso é um sinal de organização que financiador experiente lê na hora.

## Nasce fechada — e isso é de propósito

A página **começa despublicada**, e **todos os blocos começam desligados**. Nada da sua OSC vai para a internet por acidente ou por padrão de fábrica: cada informação que aparece lá é uma decisão consciente que alguém da organização tomou.

O interruptor **Publicar / Despublicar página pública**, no topo da tela, é a chave geral:

- **Despublicada** — quem abrir o endereço vê apenas um aviso de que a página não está disponível.
- **Publicada** — a página passa a responder para qualquer visitante.

**Despublicar é imediato e não apaga nada.** Se você precisar tirar a página do ar para revisar alguma coisa, desligue a chave: as escolhas de blocos, período e missão continuam salvas, e religar devolve tudo exatamente como estava.

> ✓ **Dica · Comece pequeno e amplie depois**
>
> Não tente publicar tudo na primeira semana. Um bom começo é ligar só **Quem somos** (identidade) e **Panorama do período** (receitas, despesas, resultado). Isso já entrega o essencial e é seguro. Depois de rodar um mês, com as categorias revisadas (ver abaixo), ligue **De onde vem, para onde vai**. **Projetos** entra quando a OSC quiser mostrar as iniciativas em andamento. Transparência é caminho, não interruptor único.

## Endereço da página

O endereço nasce a partir do **identificador que a organização já tem** no sistema e pode ser trocado. Aceita letras minúsculas, números e hífen, a partir de 3 caracteres — por exemplo `grupo-escoteiro-arara`. Ele é **único na plataforma**: se outra organização já usa aquele texto, o sistema avisa e você escolhe outro.

> ⚠️ **Atenção · Trocar o endereço quebra os links já divulgados**
>
> Assim que você muda o endereço, **o antigo deixa de funcionar**. Todo lugar em que o link já foi divulgado — relatório enviado a financiador, post em rede social, rodapé do site, QR Code impresso no mural, prestação de contas do ano passado — passa a apontar para o nada. Escolha o endereço **uma vez, com calma, antes de divulgar**, e só troque se houver um motivo forte (mudança de nome da organização, por exemplo). Se trocar, gere de novo o QR Code e atualize os lugares onde o link antigo aparece.

Três botões acompanham o campo:

- **Copiar link** — coloca o endereço completo na área de transferência, pronto para colar em e-mail, ofício ou rede social.
- **QR Code** — baixa a imagem do código para usar em material impresso: cartaz no mural da sede, última página do relatório anual, banner de evento, slide de assembleia.
- **Abrir página** — abre a página pública numa nova aba, do jeito que o visitante vê.

## Missão da organização

O campo **Missão da organização** é o texto que aparece no bloco "Quem somos". Ele **não é uma cópia**: é o mesmo dado do cadastro da organização, usado também nos relatórios. Editar aqui é editar lá — e vice-versa. Uma missão só, coerente em todos os lugares.

## O que aparece na página: os quatro blocos

A seção **O que aparece na página** traz os quatro blocos que a OSC pode mostrar. Cada um tem um interruptor (ligado/desligado) e uma única escolha de profundidade: **Resumido** ou **Detalhado**.

[![Os quatro blocos da página pública](/assets/screenshots/config-pagina-publica-blocos.png)](/assets/screenshots/config-pagina-publica-blocos.png)
*Cada bloco tem interruptor próprio e a escolha entre Resumido e Detalhado*

| Bloco | O que mostra | No modo Detalhado, acrescenta |
|---|---|---|
| **Quem somos** | A missão da organização | CNPJ, cidade, site e e-mail de contato |
| **Panorama do período** | Receitas, despesas e resultado do período | Comparação com o período anterior equivalente |
| **De onde vem, para onde vai** | Composição das receitas e das despesas por categoria | A lista completa de categorias (no Resumido, só as 5 maiores, com o restante agrupado em "Outras") |
| **Projetos** | Nome, objetivo e situação de cada projeto | Período do projeto e orçado × executado |

> 📖 **Conceito · Resumido não é só um jeito mais bonito de mostrar**
>
> A diferença entre Resumido e Detalhado não é estética: no modo **Resumido, o detalhe nem sai do servidor**. Não é uma informação que está lá escondida atrás de um clique ou de um "ver mais" — ela simplesmente não é enviada para o navegador do visitante. Quem escolhe mostrar menos, mostra menos de verdade. Isso importa para a OSC que quer publicar o panorama sem abrir a lista inteira de categorias, por exemplo.

## Contato de proteção de dados (se estiver preenchido)

Além dos quatro blocos, a página pode exibir o **contato de proteção de dados** da organização — o endereço para quem teve dados cadastrados pela OSC (fornecedor, prestador, participante de projeto, beneficiário, doador) pedir acesso, correção ou exclusão.

Ele **não tem interruptor próprio aqui**: aparece quando o campo está preenchido em **[Configurações → Organização](/configuracoes/organizacao/#contato-de-proteção-de-dados)** e a página está publicada. Se o campo estiver em branco, **nada aparece** — e a página segue exatamente como antes.

> ⚠️ **Atenção · É um dado público, como todo o resto da página**
>
> Como a página é aberta a qualquer pessoa, o e-mail e o nome do responsável preenchidos lá ficam **visíveis para todo mundo**. Prefira um **e-mail institucional da OSC**, não o e-mail pessoal de um voluntário. O aviso também aparece na própria tela de configuração, antes de salvar.

## Período mostrado

O campo **Período mostrado por padrão** define o recorte que o visitante vê ao abrir a página. Ele pode trocar depois, escolhendo entre **opções fixas**: exercício corrente, últimos 12 meses e os exercícios anteriores.

**Não existe intervalo personalizado.** O visitante não escolhe "de 3 de março a 17 de abril" — só recortes inteiros e comparáveis. É uma limitação de propósito: recorte solto convida a leitura enviesada e a comparação injusta.

[![Período padrão, buscadores e código de incorporação](/assets/screenshots/config-pagina-publica-periodo-incorporar.png)](/assets/screenshots/config-pagina-publica-periodo-incorporar.png)
*Período mostrado por padrão, permissão para buscadores e o código para colar no site da organização*

> ⚠️ **Importante · A página nunca mostra o mês em andamento**
>
> O recorte para **sempre no último mês encerrado**. Se hoje é 3 de agosto, a página mostra dados até julho. Isso não é atraso nem falha de atualização — é proteção. O mês em curso é um mês de rascunho: tem lançamento pela metade, comprovante que ainda não chegou, erro de digitação que ninguém percebeu, pagamento que vai ser estornado na semana que vem. **Número público é número conferido.** Publicar o mês corrente seria pedir para explicar depois por que o valor mudou — e, para quem está de fora, número que muda parece número maquiado. E o melhor: isso é automático. Ninguém na OSC precisa lembrar de "fechar o mês na página".

## Permitir que buscadores encontrem a página

Esta opção nasce **desligada**. Com ela desligada, a página continua **totalmente acessível por link direto** — quem tem o endereço abre normalmente —, mas o sistema pede aos buscadores que não a listem. Ou seja: ela não aparece quando alguém procura o nome da sua OSC no Google.

Ligue quando a OSC **quiser ser encontrada** — por exemplo, quando a transparência faz parte da estratégia de captação e você quer que um doador em potencial ache a página sozinho. É uma decisão consciente, e por isso o padrão é o mais discreto.

## Colocar no site da organização

A seção **Colocar no site da organização** entrega um trecho de código pronto para colar no site da OSC. Você clica em **Copiar código** e cola numa página do seu site — no WordPress, por exemplo, dentro de um bloco de **HTML personalizado**.

O conteúdo aparece embutido na página, **com a altura se ajustando sozinha** (sem barra de rolagem dentro do quadro) e acompanhando a largura da coluna do site. Se a sua entidade reúne mais de uma organização no sistema, dá para incorporar várias na mesma página.

> 💡 **Por que vale a pena incorporar**
>
> Duas razões práticas. A primeira: **a pessoa não sai do site da sua OSC** — a transparência vira parte do site institucional, e não um link externo que leva o visitante embora no meio da visita. A segunda, e a mais importante no dia a dia: **o conteúdo se atualiza sozinho**. Ninguém precisa copiar número à mão todo mês, montar tabela, subir PDF, lembrar de trocar. A página de transparência do site fica correta por construção, inclusive nos meses em que a equipe está sobrecarregada — que são justamente os meses em que a atualização manual não aconteceria.

## Prévia

No fim da tela, o bloco **Prévia** mostra **exatamente o que o público vê** — inclusive com a página despublicada. É a forma de conferir tudo antes de ligar a chave geral, e depois, de tempos em tempos, revisar como a OSC está aparecendo.

[![Prévia da página pública](/assets/screenshots/config-pagina-publica-previa.png)](/assets/screenshots/config-pagina-publica-previa.png)
*A prévia reproduz a página do visitante, mesmo antes de publicar*

## O que o visitante vê

A página pública é enxuta e legível em celular. No topo, a logo da OSC, o nome, o período carregado e o seletor de período. Há também um botão **Imprimir / salvar PDF**, que gera um documento do recorte visível — útil para anexar a uma prestação de contas ou levar impresso a uma assembleia.

[![Topo da página pública](/assets/screenshots/transparencia-publica-topo.png)](/assets/screenshots/transparencia-publica-topo.png)
*Topo da página pública: identidade, período, botão de impressão e o bloco "Quem somos"*

O bloco **Panorama do período** traz receitas, despesas e resultado em destaque, com o comparativo ao lado quando o modo Detalhado está ativo.

[![Panorama do período](/assets/screenshots/transparencia-publica-panorama.png)](/assets/screenshots/transparencia-publica-panorama.png)
*Panorama do período — receitas, despesas, resultado e comparação com o período anterior equivalente*

O bloco **De onde vem, para onde vai** mostra a composição por categoria, em gráfico de rosca e tabela.

[![De onde vem, para onde vai](/assets/screenshots/transparencia-publica-composicao.png)](/assets/screenshots/transparencia-publica-composicao.png)
*Composição das receitas e das despesas por categoria*

E o bloco **Projetos** lista as iniciativas com objetivo e situação — e, no modo Detalhado, período e orçado × executado.

[![Projetos na página pública](/assets/screenshots/transparencia-publica-projetos.png)](/assets/screenshots/transparencia-publica-projetos.png)
*Projetos, e no rodapé o critério de apuração informado ao visitante*

## O que o sistema nunca publica

Esta é, talvez, a parte mais importante desta página do manual. **Existe uma lista de coisas que a página pública nunca mostra — mesmo que a OSC queira mostrar.** Não há interruptor para liberar:

- **Lançamento individual.** A página trabalha com totais somados por período e por categoria. Nunca com a linha "pagamento de R$ 1.200 para fulano em 12/03".
- **Nome de qualquer pessoa física** — solicitante de reembolso, beneficiário, fornecedor pessoa física, membro da equipe, aprovador. Nenhum.
- **Comprovantes e anexos.** Nota fiscal, recibo, foto de cupom: nada disso é publicado.
- **O relatório de prestação de contas** gerado dentro do sistema.
- **Dados bancários e saldo das contas.**
- **CPF, RG, e-mail e telefone** de pessoas.
- **As telas internas de gestão** — aprovações, reembolsos, pedidos de compra e pagamento, movimentações, orçamento.

> ℹ️ **A única exceção é o contato de proteção de dados — e ela é escolha da OSC**
>
> Se a organização preencher o **contato de proteção de dados** em Configurações → Organização, o e-mail e o nome do responsável informados **aparecem na página**. É a única informação de contato que sai daqui, ela **só existe se alguém digitar** e serve justamente para dar endereço a quem precisa falar com a OSC sobre os próprios dados. É por isso que a recomendação é usar um **e-mail institucional**, e não o de uma pessoa.

> 💡 **Por que isso é proteção, e não limitação**
>
> Poderia ser diferente: o sistema poderia oferecer tudo e deixar cada OSC decidir. Só que essa liberdade transferiria para o gestor voluntário — muitas vezes sem formação em finanças, em proteção de dados ou em governança — a responsabilidade de **avaliar risco item a item**, num assunto em que errar uma vez já é caro. Com a lista acima fechada no produto, **a OSC não precisa fazer essa avaliação**. Ela decide *quanto* mostrar (blocos, resumido ou detalhado), não *se pode* mostrar algo sensível. A pergunta difícil já foi respondida.

> ⚠️ **Atenção · Por que o saldo bancário nunca é publicado**
>
> Esse cuidado merece parágrafo próprio porque quase nenhuma OSC pensa nele sozinha. A página pública fala de **fluxo do período** — quanto entrou, quanto saiu, no que foi aplicado. Ela **nunca** fala de **quanto há em caixa hoje**. Divulgar posição de caixa expõe a organização a dois riscos concretos: **engenharia social** (golpista que sabe que a conta tem R$ 80 mil monta uma abordagem muito mais convincente contra tesoureiro ou fornecedor) e **pressão indevida sobre a diretoria** (basta o saldo aparecer para começarem os pedidos: "vi que vocês têm dinheiro sobrando"). Nenhum dos dois tem a ver com má-fé de quem publica — tem a ver com informação que, uma vez pública, você não controla mais.

## Antes de publicar: revise as categorias

Este é o cuidado mais fácil de esquecer e o de consequência mais direta.

**Os nomes das categorias aparecem na página.** O bloco "De onde vem, para onde vai" mostra exatamente o texto que está cadastrado em **Configurações → Categorias**. Se em algum momento alguém criou uma categoria com nome revelador — algo como *"Acordo trabalhista — Fulano"*, *"Auxílio jurídico caso X"* ou *"Ajuda ao voluntário da Maria"* —, esse nome vai para a internet junto com o valor.

> ⚠️ **Antes de ligar o bloco "De onde vem, para onde vai", faça isto**
>
> 1. Abra **Configurações → [Categorias](/configuracoes/categorias/)** e leia a lista inteira **com olhos de quem é de fora**.
> 2. Renomeie qualquer categoria que traga **nome de pessoa**, referência a **processo, litígio ou caso individual**, ou apelido interno que não faça sentido fora da OSC.
> 3. Prefira nomes **descritivos e impessoais**: "Despesas jurídicas", "Auxílio a beneficiários", "Encargos trabalhistas".
> 4. Volte à **Prévia** e confira o resultado antes de publicar.
>
> Lembre que renomear categoria vale **retroativamente** para todos os lançamentos que já a usavam — o que, aqui, é exatamente o que você quer.

**Categorização inconsistente também fica visível.** Uma categoria de despesa usada por engano num lançamento de receita, duas categorias que significam a mesma coisa, uma categoria "Outros" que virou o maior valor do gráfico: tudo isso aparece na página e passa uma impressão de descontrole que nem sempre corresponde à realidade. A prévia é o lugar de descobrir isso — antes do público.

## De onde vêm os números

O critério de apuração é simples e está escrito no rodapé da própria página pública, para o visitante saber o que está lendo:

- **Só entram lançamentos efetivamente pagos ou recebidos** no período, pela **data de pagamento**.
- **Contas a pagar e a receber em aberto não entram.** O que está previsto, agendado ou pendente fica de fora.
- **Estornos não são contados.**
- **Transferências entre contas da própria organização** não são receita nem despesa — dinheiro que sai da conta A e entra na conta B da mesma OSC não movimentou nada de verdade.

> 📖 **Conceito · Por que a página pode mostrar valor diferente de Movimentações**
>
> Quem trabalha no dia a dia da OSC olha a tela de [Movimentações](/modulos/movimentacoes/), que lista **tudo** — pago, pendente, atrasado, cancelado. A página pública lista **só o que aconteceu de fato**. Por isso é normal e esperado que os dois números não batam: não é erro de sistema nem inconsistência, são perguntas diferentes. Movimentações responde "o que temos para acompanhar?"; a página pública responde "quanto de dinheiro entrou e saiu, de verdade, neste período?". Esse mesmo critério — chamado **regime de caixa** — é o que os [Relatórios](/modulos/relatorios/) usam. É também o critério que financiador e contador esperam encontrar numa prestação de contas de OSC.

## Boas práticas

> ✓ **Dica · Divulgue o link nos quatro lugares que importam**
>
> (1) Na **prestação de contas anual** enviada ao conselho, à assembleia e aos financiadores — o link vale mais que um anexo, porque continua correto depois. (2) Nas **propostas para editais**, no campo de transparência ou governança. (3) No **rodapé do site** da organização e na página "Quem somos". (4) Nas **redes sociais**, ao menos uma vez por semestre — publicar o link junto de um resultado do período costuma render mais engajamento que post genérico de agradecimento.

> ✓ **Dica · QR Code para o que é físico**
>
> Imprima o QR Code no **mural da sede**, no **verso do material de campanha**, no **slide de abertura da assembleia** e na **última página do relatório impresso**. Quem estiver na sala aponta a câmera e vê os números na hora — inclusive durante a própria prestação de contas, o que muda completamente o tom da conversa.

> ✓ **Dica · Revise com olhos de quem é de fora**
>
> Depois de publicar, abra a página **num navegador em que você não está logado** (ou peça a alguém de fora da OSC) e leia de cima a baixo, devagar. Pergunte: os nomes de categoria fazem sentido para quem não conhece a organização? A missão está atualizada? Tem alguma categoria com valor estranho? Faça isso a cada fechamento de exercício, no mínimo.

> ✓ **Dica · Despublicar é imediato — use sem medo**
>
> Se você notou algo errado (uma categoria mal nomeada, um lançamento classificado no lugar errado que distorceu o gráfico), **desligue a chave geral, corrija com calma e religue**. Não há penalidade, não há perda de configuração, e é infinitamente melhor do que deixar no ar um número que você sabe que está errado.

## Por onde seguir

- **[Configurações → Categorias](/configuracoes/categorias/)** — revise os nomes antes de ligar o bloco de composição.
- **[Configurações → Organização](/configuracoes/organizacao/)** — logo, CNPJ, cidade, site, e-mail de contato e missão, que alimentam a página pública.
- **[Módulos → Relatórios](/modulos/relatorios/)** — a visão interna e completa dos mesmos números, com filtros, comparativos e exportação.
- **[Módulos → Projetos](/modulos/projetos/)** — de onde vêm os projetos listados no bloco Projetos.
