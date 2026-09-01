---
title: "Documentos"
nav_order: 9
parent: "Módulos"
permalink: /modulos/documentos/
task: encontrar-documento-ja-gerado
role: [presidente, tesoureiro, comissao-fiscal, coordenador-projetos]
routes: [/documentos]
screenshots: [documentos-lista, documentos-selecao-lote]
source_docs: [changelog v1.79.0, v1.79.1, v1.97.1, v1.98.0]
last_verified: 2026-09-01
status: publicado
---

O RIT360 Financeiro gera bastante documento ao longo do trabalho — relatório em PDF, prestação de contas, planilha de lançamentos, relatório de encerramento de projeto. Antes da área de **Documentos**, cada um desses arquivos vivia só no momento em que foi criado: fechou a aba sem baixar, ou perdeu o e-mail com o link, tinha que gerar tudo de novo. A área de Documentos é o **catálogo permanente** de tudo isso — o que já ficou pronto e o que ainda está sendo preparado, num só lugar.

> 💡 **Por que isso importa**
>
> Prestação de contas do ano passado, aquele relatório que você mandou para o financiador em março, o PDF de encerramento de um projeto antigo — nenhum desses documentos precisa mais ser gerado de novo só porque ninguém guardou o link. A área de Documentos poupa esse retrabalho e, ao juntar tudo num único lugar filtrável, também facilita auditoria: dá para conferir rápido quantas prestações de contas já saíram este ano, ou quem pediu qual relatório.

## Onde acessar

No menu principal, **Documentos**, ao lado de Relatórios.

## O que aparece na lista

Cada linha é um documento gerado (ou em preparo), com o tipo, um resumo do período ou escopo que ele cobre, quem pediu e quando, o nome do arquivo, e o status:

- **Pronto** — o arquivo existe e pode ser baixado agora, pelo botão **Baixar**.
- **Em preparo** — a geração ainda está rodando em segundo plano; a lista se atualiza sozinha, sem precisar recarregar a página.
- **Falhou** — a geração não terminou com sucesso. Não há arquivo para baixar nem para apagar; o link **Gerar de novo na origem** leva de volta ao módulo onde o documento nasce (Movimentações, Relatórios, Projetos ou Orçamento), para tentar de novo.

> ⚠️ **Atenção · Documento sem arquivo não aparece mais aqui**
>
> Até a v1.97.0, um documento cujo arquivo tinha sumido (prazo de guarda vencido, ou falha na geração) continuava na lista com o status "Arquivo indisponível" — ocupando espaço sem que houvesse nada a fazer com ele ali. Desde a v1.97.1, esse documento **some da tela de Documentos**. O registro não foi apagado: para a **prestação de contas**, ele continua visível na tela de **Prestações geradas** (em Movimentações), mostrando quando o arquivo foi removido e por quem — ver [Guarda dos documentos de prestação de contas](/modulos/relatorios/#guarda-dos-documentos). Se precisar do conteúdo de novo, gere o documento outra vez pelo módulo de origem.

### Tipos de documento cobertos

PDF de lançamentos, planilha de lançamentos, PDF e planilha do relatório financeiro, PDF de encerramento de projeto, relatório parcial de projeto, planilha do orçamento anual, planilha de execução orçamentária, e PDF ou planilha de [prestação de contas](/modulos/movimentacoes/#prestacao-de-contas). Cada um é gerado no módulo a que pertence (Movimentações, Relatórios, Projetos, Orçamento) — a área de Documentos não gera nada por conta própria, só reúne e guarda o que os outros módulos já produziram.

## Filtros

- **Tipo de documento** — restringe a um dos tipos acima.
- **Gerado de / até** — período em que o documento foi pedido (não o período que o documento cobre).
- **Quem pediu** — só aparece, e só lista, quem tem permissão para ver o que os outros pediram; um voluntário comum não vê essa opção com nome de terceiros.

> 📖 **Conceito · Você só vê o que já alcançava**
>
> A área de Documentos **não abre acesso novo a ninguém**. Cada pessoa continua vendo exatamente os documentos que já conseguiria gerar ou consultar pelo caminho de origem — um coordenador de projeto vê os relatórios do projeto que coordena, não os de todos; quem não acessa Relatórios não vê PDFs de relatório financeiro aqui. Documentos é um catálogo do que você já alcançava, organizado num lugar só, não uma porta nova.

## Selecionar vários e baixar em lote

[![Barra de seleção em lote na área de Documentos, com dois documentos selecionados e o botão Baixar em lote](/assets/screenshots/documentos-selecao-lote.png)](/assets/screenshots/documentos-selecao-lote.png)
*Ao marcar mais de um documento, aparece a contagem e o botão "Baixar em lote"*

Marque a caixa de cada documento, ou use **Selecionar os N documentos exibidos** para marcar tudo o que está na tela (respeitando os filtros ativos). Com um ou mais marcados, aparece a barra de seleção com o total marcado e o botão **Baixar em lote**.

> ⚠️ **Atenção · Só documento Pronto entra na entrega**
>
> Se a seleção incluir um documento **Em preparo** ou que **Falhou**, ele fica de fora do lote — o download em lote entrega só o que está **Pronto**, e avisa quantos documentos ficaram fora por esse motivo. Não é falha silenciosa: a contagem do que foi entregue e do que ficou de fora aparece separada.

## Excluir o arquivo de um documento {#excluir-arquivo}

Desde a v1.98.0, quem tem permissão pode apagar o **arquivo** de um documento direto na área de Documentos — por linha, ou em lote pela mesma seleção usada para baixar.

> 💡 **Por que isso importa**
>
> Nem todo documento gerado precisa continuar ocupando espaço de armazenamento para sempre. Um relatório de teste, um PDF gerado com o filtro errado, ou um documento que já foi substituído por uma versão mais recente do mesmo período — antes disso só se resolvia esperando o prazo de guarda vencer sozinho (quando existia um configurado) ou, para prestação de contas, indo até a tela de Prestações geradas. Agora dá para limpar isso na hora, no mesmo lugar em que o documento é encontrado.

### O que exatamente é apagado

**Só o arquivo — nunca o registro.** O documento continua listado no histórico da organização (a menos que, sem arquivo, ele deixe de aparecer nesta lista — ver o aviso acima), com quem pediu, quando e o que ele cobria. O que some é o PDF ou a planilha em si; não há como recuperá-lo depois, a não ser gerando o documento de novo pelo módulo de origem — e, se os dados mudaram desde então, o resultado não será uma cópia idêntica.

> ⚠️ **Atenção · Não existe "desfazer"**
>
> Apagar o arquivo é uma ação **irreversível**: não existe lixeira nem restauração. Antes de confirmar, especialmente em lote, confira se a seleção é mesmo a que você quer apagar.

### Por linha

Em cada documento com arquivo disponível, aparece o botão **Excluir arquivo**, ao lado de Baixar. Ele pede confirmação, informando qual documento será afetado, antes de apagar.

### Em lote

Marque um ou mais documentos (do mesmo jeito que para baixar em lote) e use o botão **Excluir selecionados**, na barra de seleção. A confirmação diz **quantos documentos** terão o arquivo apagado antes de você confirmar — e, se algum item da seleção já não tiver arquivo para apagar, ela avisa que esse ficará de fora.

O resultado, depois de confirmar, mostra **item a item** o que aconteceu: apagado, recusado (documento sem arquivo, ou fora do seu acesso) ou falhou. Não é um "pronto" genérico que esconde falha parcial — se cinco documentos forem selecionados e um falhar, você vê exatamente qual.

### Quem pode

A mesma permissão que já existia para apagar o arquivo de uma prestação de contas pela tela de Prestações geradas: quem administra a plataforma ou tem a permissão de **exportar dados** da organização. Quem não tem essa permissão **não vê o botão**, nem por linha nem em lote — em nenhum documento.

## Não há exclusão do registro

O que **continua** impossível é apagar a **linha** — o registro de que aquele documento foi gerado, por quem e quando. Isso é coerente com o papel de Documentos como arquivo permanente da organização: mesmo sem o PDF, fica a prova de que ele existiu, para quando conselho, financiador ou auditoria perguntarem "vocês geraram esse relatório?".

Além de apagar pela tela, há um caminho automático que também remove só o arquivo, nunca o registro: o **prazo de guarda** configurado pela organização para prestações de contas, em Configurações → Relatórios — ver [Guarda dos documentos de prestação de contas](/modulos/relatorios/#guarda-dos-documentos).

## Glossário rápido

- **Em preparo** — geração ainda rodando; a lista atualiza sozinha quando terminar.
- **Excluir arquivo** — remove o PDF ou a planilha, mantendo o registro do documento no histórico; ação irreversível.

## Por onde seguir

- [Movimentações → Prestação de contas](/modulos/movimentacoes/#prestacao-de-contas) — como gerar uma prestação de contas nova.
- [Relatórios](/modulos/relatorios/) — como gerar um PDF ou planilha de relatório financeiro.
- [Projetos](/modulos/projetos/) — relatórios parciais e de encerramento de projeto.
