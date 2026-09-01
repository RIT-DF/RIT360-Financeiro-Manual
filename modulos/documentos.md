---
title: "Documentos"
nav_order: 9
parent: "Módulos"
permalink: /modulos/documentos/
task: encontrar-documento-ja-gerado
role: [presidente, tesoureiro, comissao-fiscal, coordenador-projetos]
routes: [/documentos]
screenshots: [documentos-lista, documentos-selecao-lote]
source_docs: [changelog v1.79.0, v1.79.1]
last_verified: 2026-08-30
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
- **Arquivo indisponível** — o documento existiu, mas o arquivo não está mais acessível (prazo de guarda vencido, ou falha na geração). Nesse caso não há botão de baixar; se você precisar do conteúdo, gere de novo pelo módulo de origem.

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

> ⚠️ **Atenção · Documento indisponível não entra na entrega**
>
> Se a seleção incluir um documento com status **Arquivo indisponível**, ele fica de fora do lote — o download em lote entrega só o que está **Pronto**, e avisa quantos documentos ficaram fora por esse motivo. Não é falha silenciosa: a contagem do que foi entregue e do que ficou de fora aparece separada.

## Não há exclusão

A área de Documentos é só de consulta e download — **não existe apagar um documento por ali**. É coerente com o papel dela de arquivo permanente: se você pudesse apagar, deixaria de ser um catálogo confiável do que já foi gerado.

Um documento pode, ainda assim, aparecer como **Arquivo indisponível**, e há dois caminhos que levam a isso, ambos fora desta tela: o **prazo de guarda** da organização, que apaga automaticamente os arquivos vencidos, e a ação de **apagar o arquivo** de uma prestação de contas, disponível na tela de Prestações geradas para quem administra a plataforma ou tem permissão de exportar dados — ver [Prestações de contas](/modulos/relatorios/#e-se-for-preciso-apagar-o-arquivo-de-uma-prestacao). Nos dois casos o registro continua na lista; o que some é o arquivo.

## Glossário rápido

- **Em preparo** — geração ainda rodando; a lista atualiza sozinha quando terminar.
- **Arquivo indisponível** — documento que existiu mas cujo arquivo não está mais acessível; gere de novo no módulo de origem se precisar do conteúdo.

## Por onde seguir

- [Movimentações → Prestação de contas](/modulos/movimentacoes/#prestacao-de-contas) — como gerar uma prestação de contas nova.
- [Relatórios](/modulos/relatorios/) — como gerar um PDF ou planilha de relatório financeiro.
- [Projetos](/modulos/projetos/) — relatórios parciais e de encerramento de projeto.
