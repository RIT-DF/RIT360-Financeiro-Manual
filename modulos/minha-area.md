---
title: "Minha área"
nav_order: 11
parent: "Módulos"
permalink: /modulos/minha-area/
task: acompanhar-a-verba-do-centro-de-custo
role: [gestor-centro-custo, presidente, tesoureiro, comissao-fiscal, coordenador-projetos]
routes: [/minha-area]
screenshots: []
source_docs: [changelog v1.155.0, changelog v1.155.2, ADR-011 (revisão de 12/11/2026)]
last_verified: 2026-11-12
status: publicado
---

A **Minha área** é a tela que junta, para um **centro de custo** e um **ano**, tudo o que a sua área tem para gastar: a **verba do ano**, o que já foi **gasto**, o que já está **comprometido** e quanto **sobra**. Ela é só de leitura: mostra os números, mas não altera nada.

> Acesse pelo menu **Minha área**. No celular, ela fica em **Mais**.

> 💡 **Por que isso importa**
>
> Quem responde por uma área — uma filial, uma seção, um núcleo — normalmente não tem como saber, sem perguntar a alguém, quanto ainda pode gastar. Os números estão espalhados: os lançamentos num lugar, o orçamento em outro, os pedidos aprovados em outro. A Minha área reúne tudo na mesma tela, e avisa quando o gasto chega perto do limite, antes de a verba acabar.

## Quem vê a tela

A entrada **Minha área** aparece para duas pessoas:

- quem **responde por pelo menos um centro de custo** da organização (o **Gestor de Centro de Custo**, ver [Papéis e Permissões](/papeis/#gestor-de-centro-de-custo));
- quem tem **permissão de ver o orçamento** — como o Presidente e o Tesoureiro. Essas pessoas escolhem **qualquer centro de custo** da organização.

Quem é Gestor de Centro de Custo vê **só os centros pelos quais responde**. Se você acha que deveria ver um centro e não vê, peça ao administrador da organização para indicá-lo como responsável em **Configurações → Categorias → aba Centros de custo**.

## O que aparece na tela

Ao escolher o **centro de custo** e o **ano**, a tela mostra:

- **Verba do ano** — o valor aprovado para o centro no orçamento do ano.
- **Gasto realizado** — o que já foi pago neste ano pelos lançamentos do centro.
- **Comprometido** — o que já tem destino certo, mas ainda não saiu do caixa: lançamentos a pagar, e pedidos de pagamento e reembolsos já aprovados que ainda não viraram lançamento. Cada compromisso é contado uma vez só.
- **Saldo** — a verba menos o gasto realizado. Fica em vermelho quando passa de zero.

Abaixo dos números há uma **barra de uso** da verba. A parte cheia é o **gasto**; a faixa tracejada, por trás dela, é o **gasto somado ao comprometido**. Quando o gasto chega perto do limite, aparece o aviso **"O gasto está perto do limite da verba"**; quando passa da verba, o aviso **"O gasto já passou da verba do ano"**. Se só o comprometido estoura a verba, a tela avisa que, somando o que já está comprometido, a verba não é suficiente.

> 📖 **Conceito · Os limites são os da organização**
>
> Os avisos seguem os limites de alerta do orçamento configurados pela sua OSC — por padrão, **80%** (perto do limite) e **100%** (passou da verba). Eles são definidos em [Configurações → Fluxo de Aprovações → aba Orçamento](/configuracoes/aprovacoes/#aba-orcamento). A tela não tem limite próprio.

Depois vêm, nesta ordem:

- **Lançamentos do ano neste centro** — a lista das movimentações do centro no ano escolhido, com o status de cada uma. Tocar numa linha abre o lançamento. Quando o custo do lançamento foi repartido entre centros, a linha mostra a parte deste centro e o valor total.
- **Previsto × realizado por categoria** — aparece só quando o centro tem orçamento detalhado por categoria e mês.
- **Projetos com financiador ou receitas próprias neste centro** — aparece só quando há algum. Veja a seção abaixo.

## Passo a passo

1. No menu, abra **Minha área**. Se você responde por mais de um centro, escolha o centro no campo **Centro de custo**.
2. Escolha o **ano** no campo **Ano**. Os números e a lista de lançamentos são sempre do ano escolhido.
3. Leia a verba, o gasto, o comprometido e o saldo. Confira a barra de uso e os avisos.
4. Quer ver de onde veio um número? Toque na linha do lançamento para abrir o detalhe, ou vá em **Movimentações** e filtre pelo centro de custo.

## Como a verba é calculada

A verba que a tela mostra é a que vale no **orçamento aprovado** do ano. Ela pode vir de duas formas, e a tela diz qual delas está valendo:

- **Soma das linhas do orçamento**, quando o centro é detalhado por categoria e mês;
- **Verba do ano em valor único**, quando o centro foi definido com um valor só (ver [Orçamento → Verba do ano em valor único](/modulos/orcamento/#verba-do-ano-valor-unico)).

Se o orçamento do ano ainda **não foi aprovado**, a tela diz que a verba não está valendo ainda e mostra **só o gasto**. O mesmo acontece quando o centro não tem verba definida no orçamento aprovado. Um valor que está só no rascunho não aparece aqui.

## Gasto de projeto: o que entra e o que fica à parte

Os gastos de projeto seguem a mesma regra do orçamento. O que decide é a **fonte escolhida em cada lançamento**, não o projeto como um todo:

- um lançamento de **projeto pago com o caixa geral** da organização conta no **gasto do centro de custo do próprio lançamento** (ou nos centros, se o custo foi repartido), e aparece na lista de lançamentos do ano;
- um lançamento de **projeto pago com financiador ou com receitas do próprio projeto** (como um convênio, ou uma doação destinada) **não entra** no gasto do centro. Ele aparece à parte, em **Projetos com financiador ou receitas próprias neste centro**, com o total gasto nele.

Um projeto misto tem lançamentos dos dois tipos, e cada um segue a sua fonte. Cada lançamento conta em um lugar só. Ver a explicação completa em [Orçamento](/modulos/orcamento/), no conceito "De que centro de custo é o gasto de um projeto".

> 💡 **Dica · Se um gasto de convênio aparecer na sua área**
>
> O que decide é a fonte escolhida no lançamento. Abra o lançamento e confira a fonte: se estiver como caixa geral, o gasto conta aqui; se for o financiador, ele não deveria estar nesta área.

> 💡 **Dica · Entender um número alto**
>
> Se o gasto da sua área parece alto, role a lista de lançamentos do ano. Costuma ser um lançamento grande, ou um lançamento de projeto pago com caixa geral que caiu no centro. Ver cada um ali é mais rápido do que abrir um relatório.

> ✓ **Dica · Tela só de leitura**
>
> A Minha área não grava nada. Para lançar, aprovar ou ajustar o orçamento, use as telas de **Movimentações**, **Reembolsos**, **Pedidos de Pagamento** e **Orçamento**, conforme a permissão de cada um.

## Dicas e armadilhas

> ⚠️ **Atenção · Sem verba aprovada, a tela mostra só o gasto**
>
> Enquanto o orçamento do ano não foi aprovado, ou enquanto o centro não tem verba nele, o campo **Verba do ano** mostra um traço (—) em vez de um valor. Isso não é erro: é a tela dizendo que nenhuma verba está valendo ainda. O gasto continua aparecendo normalmente.

> ⚠️ **Atenção · Comprometido não é gasto**
>
> O comprometido ainda não saiu do caixa, mas já tem destino: uma conta a pagar, um pedido aprovado. Ele entra na barra (faixa tracejada) e no aviso de "não é suficiente", mas não entra no gasto realizado. Quando o pagamento acontece, ele vira gasto e deixa de ser comprometido — sem contar duas vezes.

> ⚠️ **Atenção · Gasto pago com financiador ou receitas próprias não entra na verba da área**
>
> O gasto de um lançamento de projeto pago com financiador ou com receitas do próprio projeto não diminui a verba do centro, mesmo quando o projeto está ligado a esse centro. Ele aparece em **Projetos com financiador ou receitas próprias neste centro**, para você saber que existe, mas tem orçamento próprio.

> ⚠️ **Atenção · A lista mostra os 300 lançamentos mais recentes**
>
> Em centros com muita movimentação, a lista de lançamentos mostra só os 300 mais recentes do ano. Para ver todos, use **Movimentações** com o filtro de centro de custo.

> ⚠️ **Atenção · Centro inativo aparece com "(inativo)"**
>
> Um centro que foi desativado continua na lista do seletor, marcado como inativo, para você consultar o ano em que ele existiu.

## Por onde seguir

- [**Orçamento**](/modulos/orcamento/) — de onde vêm a verba, o previsto e as regras de cada centro.
- [**Movimentações**](/modulos/movimentacoes/) — os lançamentos que formam o gasto e o comprometido.
- [**Projetos**](/modulos/projetos/) — os projetos que podem aparecer à parte nesta tela.
- [**Papéis e Permissões**](/papeis/) — quem vê a Minha área e o que o Gestor de Centro de Custo pode fazer.
