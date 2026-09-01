---
title: "Categorias"
nav_order: 5
parent: "Configurações da Organização"
permalink: /configuracoes/categorias/
---

> Disponível para **Presidente (admin)** e **Tesoureiro**.

A página **Categorias** organiza as categorias contábeis e os centros de custo da OSC — o esqueleto da sua contabilidade gerencial.

[![Configurações — Categorias](/assets/screenshots/config-categorias.png)](/assets/screenshots/config-categorias.png)
*Configurações — Categorias e centros de custo*

> 💡 **Por que isso importa**
>
> Categoria é o que **faz o relatório financeiro fazer sentido**. Sem categoria, você tem 200 lançamentos no mês e nenhuma resposta sobre "para onde vai o dinheiro?". Com categoria ruim (inconsistente, duplicada, vaga), o relatório engana mais do que ajuda. Com categoria boa (enxuta, consistente, semântica), o relatório responde sozinho — você vê em 30 segundos quanto a OSC gastou com aluguel, quanto com material, quanto recebeu de doação, quanto de mensalidade. **Tempo investido em organizar categorias é o investimento de melhor retorno** que uma OSC pode fazer no RIT360 Financeiro.

A página tem 3 abas: **Receitas**, **Despesas** e **Centros de custo**.

## Receitas

Categorias para classificar entradas financeiras. Exemplos típicos de OSC:

- Doações
- Mensalidades de associados
- Subvenções e editais
- Arrecadação de eventos
- Venda de produtos (lojinha)
- Patrocínio
- Rendimentos financeiros

## Despesas

Categorias para classificar saídas. Exemplos:

- Aluguel
- Conta de luz, água, internet
- Material didático
- Material de escritório
- Combustível e transporte
- Alimentação
- Salários e encargos
- Manutenção
- Marketing e comunicação

## Centros de custo

> 📖 **Conceito · Categoria vs Centro de custo**
>
> **Categoria** classifica a *natureza* do lançamento (o que foi gasto/recebido): "aluguel", "doação", "combustível". **Centro de custo** classifica a *origem ou destino organizacional*: "Sede", "Filial Norte", "Coordenação de Eventos", "Diretoria de Comunicação". Os dois são independentes — um lançamento pode ter categoria "Combustível" e centro de custo "Filial Norte" simultaneamente. Centro de custo é opcional na maioria dos lançamentos; categoria é (quase sempre) obrigatória.

OSC pequena geralmente não precisa de centros de custo. OSC com **múltiplas frentes operacionais** (sede + filiais; várias coordenações; diretorias com orçamentos separados) ganha muito ao usar.

### Responsáveis pelo centro de custo
{: #responsaveis-pelo-centro-de-custo }

Ao **criar** ou **editar** um centro de custo, o formulário traz a seção **Responsáveis pelo centro de custo** — uma lista dos membros da OSC com uma caixa de seleção para cada. Marque quem responde por aquele centro de custo e salve.

> 📖 **Você já pode designar quem ainda não ativou o acesso**
>
> Um membro recém-cadastrado, que ainda não definiu a senha do primeiro acesso, já aparece nesta lista e pode ser marcado como responsável — sem esperar ele entrar no sistema pela primeira vez. O nome vem com a marca discreta **"· acesso pendente"**. A pessoa só passa a *operar* o centro de custo depois de ativar o acesso.

[![Responsáveis pelo centro de custo](/assets/screenshots/config-cc-responsaveis.png)](/assets/screenshots/config-cc-responsaveis.png)
*Editar centro de custo — seção "Responsáveis pelo centro de custo"*

> ⚠️ **Importante · Atribuir responsável não basta sozinho**
>
> Marcar alguém como responsável por um centro de custo **só concede acesso se a pessoa também tiver o cargo Gestor de Centro de Custo**. São duas coisas complementares: o **cargo** (em Configurações → Usuários → Editar papéis) diz que a pessoa *pode* gerir centros de custo; o **vínculo de responsável** aqui diz *quais* centros de custo. Faltando o cargo, o nome pode até estar marcado aqui, mas a pessoa não enxerga nem opera o centro de custo. Ver [Papéis e Permissões → Gestor de Centro de Custo](/papeis/#gestor-de-centro-de-custo).

Com o cargo e o vínculo em dia, o Gestor de Centro de Custo passa a **criar e editar** lançamentos daquele CC e a **ver** as movimentações e relatórios recortados a ele — sem acesso ao restante do financeiro da OSC. Presidente e Tesoureiro continuam enxergando **todos** os centros de custo, independentemente dessa lista.

### Coluna "Gestor(es)" na lista
{: #coluna-gestores }

A lista da aba **Centros de custo** tem uma coluna **"Gestor(es)"** que mostra, de relance, quem responde por cada centro — sem precisar abrir **Editar**. Centros sem responsável aparecem com **"—"**; quando há mais de um, a lista exibe o **primeiro nome com um "+N"**, e a lista completa aparece ao passar o mouse por cima.

[![Lista de centros de custo com a coluna Gestor(es)](/assets/screenshots/config-cc-lista-gestores.png)](/assets/screenshots/config-cc-lista-gestores.png)
*A coluna "Gestor(es)" mostra o responsável de cada centro de custo (ou "—" quando não há).*
> ✓ **Dica · Confira os responsáveis de relance**
>
> Essa coluna é o jeito rápido de auditar quem está no comando de cada área: um centro de custo importante com "—" na coluna Gestor(es) é sinal de que falta atribuir responsável (ou que quem foi atribuído ainda não tem o cargo Gestor de Centro de Custo).

## Template de categorias

Para começar rapidamente, clique em **Aplicar template**. O RIT360 Financeiro tem modelos prontos por tipo de OSC — há templates para **Grupo Escoteiro, Associação, Instituto, Fundação, ONG, Coletivo e Cooperativa**, cada um com as categorias de receita e despesa típicas daquele perfil. Escolha o modelo mais próximo da sua organização; aplicar o template importa as categorias do modelo para a sua OSC, sem apagar o que você já tinha.

> ✓ **Dica · Comece com template, depois afine**
>
> Você nunca acerta a lista perfeita de categorias na primeira tentativa. Comece com um template próximo ao perfil da sua OSC, opere por 1-2 meses, e ajuste o que **não bater** com sua realidade: renomeie categorias confusas, una categorias que viraram redundantes, crie categoria nova quando 5+ lançamentos foram para "Outros". Lista enxuta vence lista exaustiva — categoria que aparece 2× no ano não vale ter como categoria separada.

> ⚠️ **Atenção · Nome de categoria pode virar informação pública**
>
> Se a sua OSC usa a [Página Pública](/configuracoes/pagina-publica/) de transparência, os **nomes das categorias aparecem lá** — no bloco "De onde vem, para onde vai". Uma categoria chamada *"Acordo trabalhista — Fulano"* ou *"Auxílio jurídico caso X"* vira texto público junto com o valor. Antes de publicar, leia a lista inteira com olhos de quem é de fora e prefira nomes **descritivos e impessoais** ("Despesas jurídicas", "Auxílio a beneficiários"). Categorização inconsistente também fica visível — vale conferir na prévia.

> ⚠️ **Atenção · Cuidado ao renomear categoria em uso**
>
> Renomear uma categoria atinge **retroativamente** todos os lançamentos que já a usavam — eles passam a aparecer com o novo nome em relatórios e listagens. Geralmente isso é o que você quer (ajustou o nome para algo mais claro), mas pense duas vezes antes de renomear uma categoria que já foi referenciada em prestação de contas externa.

## Importar categorias e centros de custo por planilha

> 💡 **Por que isso importa**
>
> Quando você está migrando de outro sistema ou já tem a estrutura contábil inteira numa planilha, cadastrar categoria por categoria na mão é lento e é fácil errar um nome ou esquecer uma sub-categoria. A importação por planilha resolve isso de uma vez: você sobe o arquivo, o RIT360 Financeiro monta a estrutura sozinho e mostra exatamente o que vai mudar **antes** de gravar qualquer coisa.

**Acesso:** botão **Importar por planilha**, ao lado de **Aplicar template**, no topo da página. Exige a permissão **Config. financeira** — ver [Cargos e permissões](/configuracoes/cargos/#permissao-config-financeira).

Categorias e centros de custo têm **modelos separados** (`categorias.csv` e `centros-custo.csv`), em abas distintas da mesma tela — baixe o modelo, preencha e envie de volta.

### Como funciona

1. Clique em **Importar por planilha** e escolha a aba (**Categorias** ou **Centros de custo**).
2. Baixe o modelo e preencha com a sua estrutura.
3. Envie o arquivo. Nada é gravado ainda — a tela mostra uma **prévia**.
4. Confira linha por linha e decida se aplica as atualizações (veja a armadilha abaixo).
5. Confirme.

[![Prévia da importação de categorias](/assets/screenshots/importar-estrutura-previa.png)](/assets/screenshots/importar-estrutura-previa.png)
*Prévia da importação: contadores no topo, a caixa "Aplicar as atualizações" e o desfecho linha a linha*

> 📖 **Conceito · A ordem das linhas não importa**
>
> Você não precisa colocar o grupo antes das categorias dele na planilha. O RIT360 Financeiro lê o arquivo inteiro e monta a hierarquia sozinho, na ordem que fizer sentido — pode escrever as linhas na ordem que for mais prática para você preencher.

**Categorias têm no máximo dois níveis**: um grupo, e categorias dentro dele. Deixe a coluna `grupo` em branco para criar um grupo principal. **Centro de custo não tem grupo nem tipo** — é uma lista simples, com nome e descrição; uma planilha de centro de custo com coluna de grupo é recusada por inteiro.

No exemplo da prévia acima, a organização importou 34 linhas: **27 categorias novas**, **2 atualizações** (nomes que já existiam, com algo mudando), **1 que já estava exatamente igual** e **4 recusadas**. Duas recusas ensinam bem o que a validação verifica:

- **"Doações"** já existia como sub-categoria de outro grupo, e a planilha tentava usá-la como grupo — a mensagem foi **"Categorias têm no máximo dois níveis"**, e as três categorias-filhas dela na planilha foram recusadas em cascata, com **"O grupo Doações foi recusado — veja a linha do grupo"**.
- **"Aluguel"** mudou de grupo — de "Sede e instalações" para "Administrativa" — e apareceu como **atualização**, mostrando o antes e o depois, porque a caixa "Aplicar as atualizações" estava marcada.

> ⚠️ **Atenção · A caixa "Aplicar as atualizações" vem marcada**
>
> Se a sua planilha renomear uma categoria existente ou mudar o grupo dela, isso **muda relatórios e prestação de contas já emitidos** com aquela categoria. Se você quer só acrescentar o que é novo, sem tocar no que já está em uso, **desmarque a caixa** antes de confirmar — as criações entram do mesmo jeito, só as atualizações ficam de fora.

> ✓ **Dica · Nome que já existe não vira duplicata**
>
> A importação **casa por nome**, ignorando maiúsculas/minúsculas e espaços extras. Um nome já cadastrado aparece como "já está igual" (nada muda) ou "atualizar" (mostrando o que mudaria) — nunca cria uma segunda categoria com o mesmo nome. Por isso **reenviar a mesma planilha não duplica nada**: rode de novo sempre que precisar corrigir algo e reimportar.

> ✓ **Dica · Cadastro inativo é reconhecido, mas reativar é sua decisão**
>
> Se a planilha cita uma categoria ou centro de custo que existe mas está **inativo**, a prévia mostra a opção de reativar — vindo **desmarcada**. Você decide, linha a linha, se quer trazer aquele cadastro de volta.

## Hierarquia de categorias

O RIT360 Financeiro suporta **categorias-mãe com sub-categorias** — útil para agrupar afins sem perder granularidade. Exemplo:

- Loja Virtual (categoria-mãe)
  - Camisetas
  - Canecas
  - Doações pelo site

O modo automático de integração com WooCommerce (em Configurações → Organização) usa exatamente esse padrão: cria sub-categorias sob a categoria-mãe escolhida para cada categoria do WC.

## Acompanhar quanto da despesa vai para cada finalidade

Algumas OSCs precisam comprovar que uma **parcela mínima da despesa** foi aplicada em determinada finalidade. É o caso de quem tem CEBAS na área da saúde, que precisa demonstrar que 60% da despesa foi em saúde — mas vale para qualquer certificação, convênio ou estatuto que imponha proporção.

O sistema entrega esse número **sem nenhuma configuração especial**, desde que as categorias estejam organizadas do jeito certo.

### Como organizar

**Coloque a finalidade no primeiro nível das categorias de despesa** e tudo o mais abaixo dela:

- **Saúde**
  - Folha de pagamento
  - Material de enfermagem
  - Manutenção da sala do hospital
- **Assistência**
  - Folha de pagamento
  - Cesta básica
  - Transporte de pacientes
- **Administrativa**
  - Folha de pagamento
  - Aluguel
  - Contabilidade

⚠️ **Use no máximo dois níveis.** O relatório soma cada categoria dentro da **categoria imediatamente acima dela**. Com dois níveis, a soma cai na finalidade, que é o que você quer. Com três — "Saúde → Pessoal → Folha" —, a soma para em "Pessoal" e a finalidade não aparece.

### Onde ler o percentual

Em **Relatórios**, escolha o período e abra a visão de despesa por categoria. Cada linha de primeiro nível traz o **percentual sobre o total** do período, e ainda a variação em relação ao período anterior.

É esse percentual que responde "quanto da minha despesa foi em saúde neste ano". Escolhendo o período do exercício, ele responde a pergunta do órgão certificador; escolhendo o mês, mostra se você está no caminho.

### A despesa que pertence a mais de uma finalidade

Esse é o caso que costuma parecer sem saída: a folha de pagamento de quem trabalha metade do tempo no atendimento em saúde e metade na administração.

**Não é preciso escolher uma finalidade nem "puxar" a folha inteira para um lado.** Ao lançar a despesa, divida o valor entre as categorias correspondentes — uma parte em "Saúde / Folha de pagamento", outra em "Administrativa / Folha de pagamento". O sistema aceita a divisão por valor, e o relatório soma cada parte na finalidade certa.

A proporção pode ser diferente a cada mês: você informa a divisão do mês, e pronto. Nada precisa ser reclassificado depois.

> 💡 **Por que isso importa**
>
> Quem só descobre o percentual no fechamento do exercício descobre tarde: se faltou, já não há o que fazer, e sobra a tentação de reclassificar despesa no fim do ano para fechar a conta — o que um auditor enxerga e questiona. Olhando o percentual a cada mês, a correção é operacional e legítima: dá tempo de priorizar um projeto da finalidade que está atrás.

### E os centros de custo, não serviriam?

Serviriam para o número, mas com dois problemas.

O primeiro é que **um lançamento pertence a um único centro de custo** — então a folha dividida entre duas finalidades não tem como ser representada. Você voltaria a ter que escolher um lado, que é exatamente o problema que a divisão por categoria resolve.

O segundo é que centro de custo responde a outra pergunta: **onde** o dinheiro é gasto — a casa de apoio, o bazar, a unidade no hospital. É por ele que se faz orçamento por unidade, se define quem responde por cada uma e se emite prestação de contas de uma unidade específica. Usando-o para finalidade, você perde a possibilidade de dizer "casa de apoio" **e** "saúde" ao mesmo tempo.

## Por onde seguir

- **Movimentações** — onde as categorias aparecem nos formulários de novo lançamento e nos filtros da lista.
- **Reembolsos** e **Pedidos de Compra e Pagamento** — onde as categorias de despesa são usadas para classificar as solicitações.
- **Configurações → Organização → Integrações** — onde a categoria-mãe do WooCommerce é configurada.
