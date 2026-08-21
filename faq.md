---
title: "Perguntas Frequentes"
nav_order: 10
permalink: /faq/
---

Respostas para dúvidas comuns. Se a sua pergunta não está aqui, use o botão **💬 Feedback** dentro do RIT360 Financeiro — sua dúvida ajuda este manual a melhorar.

## Acesso e conta

### Não recebi o e-mail para acessar. O que faço?

Quando o administrador da sua organização adiciona você, **sua conta já é criada** — não existe uma etapa de "aceitar convite". Você recebe um e-mail para **definir sua senha** (o link vale por 7 dias) e, a partir daí, entra normalmente. Se preferir, pode entrar direto com **Continuar com Google**, desde que use o mesmo e-mail com que foi cadastrado.

Se o e-mail não chegou, confira a caixa de spam/lixo eletrônico primeiro — ele sai de um domínio institucional e às vezes cai lá.

Você não depende de ninguém para se desbloquear: na tela de login, clique em **Esqueci a senha** e informe o e-mail com que foi cadastrado. Como você ainda não concluiu o primeiro acesso, o sistema envia um **novo link de primeiro acesso** (não um link de redefinição de senha). Se preferir, o administrador também pode reenviá-lo em **Configurações → Usuários → ações da sua linha → Reenviar e-mail**.

Outra saída, se você tem conta Google no mesmo e-mail: clique em **Continuar com Google** na tela de login. O acesso à organização é concluído na hora, sem precisar do link.

Se mesmo assim você deixar para depois, o sistema **lembra sozinho**: chegam lembretes automáticos **2, 7 e 14 dias** após o cadastro (três no total, sendo o último anunciado como tal), cada um com um **link novo** — use sempre o mais recente.

### Esqueci minha senha (ou nunca cheguei a criar uma). Como faço?

Na tela de login, clique em **Esqueci a senha**, informe o e-mail da sua conta e clique em **Enviar link para entrar**.

[![Tela de recuperação de senha](/assets/screenshots/manual-recuperar-senha.png)](/assets/screenshots/manual-recuperar-senha.png)

Essa opção resolve os **dois** casos, e o sistema identifica sozinho qual é o seu:

- **Você já usa o sistema e esqueceu a senha** → chega um link para definir uma nova senha. Ele **vale por 1 hora e só pode ser usado uma vez**. Ao definir a nova senha, você volta para a tela de login e entra com ela.
- **Você foi cadastrado por um administrador e nunca criou senha** → chega um **novo link de primeiro acesso** (vale por 7 dias), para concluir o cadastro.

Por segurança, a confirmação na tela é sempre a mesma, exista ou não uma conta para aquele e-mail (não revelamos quais e-mails têm cadastro). Por isso o e-mail que chega pode ser de um tipo ou de outro — basta seguir o que ele pede. Se não receber, confira a caixa de spam; há um limite de **3 pedidos por hora** para o mesmo e-mail, então evite clicar várias vezes seguidas.

Se você cadastrou via Google no primeiro acesso, use **Continuar com Google** em vez de senha — contas só-Google não têm senha para redefinir.

### Não consigo concluir meu cadastro. A senha é sempre recusada.

A tela agora mostra o motivo direto embaixo do campo de senha, mas o caso mais comum confunde: você digita uma senha longa, com letras, números e símbolos — e mesmo assim ela é recusada. Isso não é bug nem exagero do sistema: essa senha provavelmente **já apareceu em vazamentos de dados conhecidos** de outros serviços, e por segurança o RIT360 Financeiro não aceita senhas nessa situação, por mais "fortes" que pareçam.

A saída é simples: escolha uma senha que você **não usa em nenhum outro site ou aplicativo**. Se preferir não decorar uma nova, considere um gerenciador de senhas.

Se em vez disso a tela mostrar que o **link expirou** ou que ele **já foi usado**, veja a pergunta anterior — nenhum dos dois casos exige ajuda de terceiros.

### Cliquei em "Continuar com Google" e voltei para a tela de login, sem entender por quê.

Quando o login com Google não completa (por exemplo, você cancelou no meio ou a sessão do Google expirou), a tela mostra uma mensagem curta explicando o motivo — ela não te devolve mais ao login em silêncio. Se aparecer essa mensagem, tente de novo; se persistir, entre com **e-mail e senha**, ou use **Esqueci a senha** se ainda não tiver uma senha definida.

### Posso usar o mesmo e-mail em mais de uma organização?

Sim. Sua conta no RIT360 Financeiro é única, atrelada ao seu e-mail, mas você pode ser membro de várias OSCs simultaneamente. Use o **seletor de organização** no topo da tela para alternar entre elas — toda a interface reage à organização ativa.

### Posso encerrar minhas sessões em outros dispositivos?

Sim. Em **Meu Perfil → Ações de Conta → Encerrar todas as sessões**. Útil se você perdeu um dispositivo ou suspeita de uso indevido. Atenção: isso te desconecta também do navegador atual; você precisa fazer login de novo.

## Navegação e papéis

### Onde encontro Configurações? Não vejo nenhum item no menu.

Configurações da organização está no **ícone de engrenagem** no canto superior direito da TopNav (entre o Feedback e o menu do avatar). O ícone só aparece para usuários com papel **Admin (Presidente)** ou **Tesoureiro** — voluntários e coordenadores não veem porque não têm acesso às configurações da OSC.

### Onde está "Meu Perfil"?

No **menu do avatar** (canto superior direito da tela) → **Meu perfil**. A rota é `/perfil`, separada das Configurações da organização porque o perfil é pessoal (não da OSC).

### Sou voluntário. Por que não vejo o módulo "Movimentações"?

Voluntários não têm acesso a Movimentações (lançamentos detalhados da OSC). Eles veem o Painel (com saldo geral), e a aba Reembolsos em Pagamentos e Reembolsos (para registrar os próprios reembolsos). Para ver Movimentações, é necessário papel Coordenador, Tesoureiro ou Presidente — fale com o administrador da OSC.

### O que significa "auto-aprovação"?

Quando você é o único aprovador elegível para o seu próprio reembolso ou pedido (caso comum em OSC pequena onde o presidente é o único aprovador e também é o solicitante), o RIT360 Financeiro **permite a auto-aprovação** para não travar o fluxo, mas marca explicitamente no audit log. Conforme a OSC ganha mais aprovadores cadastrados, auto-aprovações naturalmente diminuem.

### Apareceu um ponto ao lado do meu nome (ou perto do número da versão). O que é isso?

É o aviso discreto de que o sistema foi atualizado desde a última vez que você olhou as [Novidades](/changelog/). Não interrompe nada: basta abrir a página de Novidades — pelo número da versão no rodapé ou pelo menu do avatar (no celular, menu **Mais**) — e o ponto some. Ele só volta a aparecer quando sair uma versão mais nova.

### Vi um aviso de novidades e fechei sem ler. Como recupero?

Sem problema. A página de **Novidades** fica sempre acessível, a qualquer momento: pelo número da versão no rodapé de qualquer tela, ou pelo menu do avatar (no celular, menu **Mais**). Ela reúne o histórico completo, não só o que apareceu na janela de aviso.

## Movimentações

### O sistema registrou minha despesa com data errada. Posso corrigir?

Depende do status. Se o lançamento está **Pendente** ou **Atrasado**, clique em **Editar** no detalhe da movimentação e ajuste o que precisar. Se já está **Pago**, os responsáveis financeiros podem corrigir a **data de pagamento** e a **conta** em **detalhe do lançamento → Editar dados de pagamento** (é pedido um motivo, que fica no histórico). Para corrigir o **valor** de um lançamento já pago, o caminho continua sendo **Estornar** e criar um novo lançamento correto.

### Qual a diferença entre Cancelar e Excluir uma movimentação?

**Cancelar** mantém o lançamento no histórico com status "Cancelado" — útil para rastreabilidade ("essa despesa estava prevista mas não aconteceu"). **Excluir** apaga o lançamento de vez. O RIT360 Financeiro só permite excluir movimentações que já foram canceladas ou estornadas, justamente para evitar perda acidental. Para auditoria limpa, prefira sempre **cancelar** a excluir.

### Sumiu o botão "Marcar como pago". Por quê?

Porque **pagar virou uma permissão separada** de criar e editar. Se o seu cargo não tem a permissão de pagar, você continua registrando e editando lançamentos, mas não confirma pagamentos — o botão não aparece na linha, no detalhe, na seleção em lote nem na conciliação de extrato. Quem administra a OSC pode ligar essa permissão no seu cargo em [Configurações → Cargos e permissões](/configuracoes/cargos/#permissao-pagar). Se ninguém mexeu nos cargos, nada mudou: quem já podia pagar continua podendo.

### Estou vendo só os últimos dígitos do CPF / da chave Pix. Está com defeito?

Não. **Os dados bancários de quem recebe só aparecem por inteiro para quem tem permissão de pagar** — os demais veem apenas os dígitos finais, o suficiente para conferir de qual conta se trata. O nome de quem recebe continua visível para todo mundo. E fique tranquilo: **editar o lançamento sem mexer no bloco de pagamento não apaga nada** — os dados originais continuam lá. Ver [Dados bancários de quem recebe](/configuracoes/contas/#dados-bancarios-de-quem-recebe).

### Posso exportar os lançamentos?

Sim. Na lista de **Movimentações**, clique em **Exportar** e escolha PDF (formatado) ou Excel (planilha). A exportação inclui os filtros ativos no momento da exportação. O Excel baixa na hora; o **PDF** é montado em segundo plano — o download começa sozinho quando fica pronto e o link também chega no seu e-mail, então você pode fechar a aba.

### Como funcionam as recorrências?

Ao criar uma movimentação, você pode escolher tipo **Recorrente**: define frequência (mensal, trimestral, etc.) e duração (data final, quantidade de ocorrências ou indefinido até cancelar). O RIT360 Financeiro cria as ocorrências automaticamente; cada uma é paga individualmente. Para encerrar uma série em andamento, abra o detalhe e use o cancelamento em 3 escopos (apenas esta / esta e futuras / série inteira).

### Posso informar o centro de custo ao importar lançamentos por planilha?

Sim. A planilha de importação tem a coluna `centro_de_custo` (opcional). Se o nome informado ainda não existir na OSC, ele aparece como **pendência** na tela de resumo, onde você escolhe **criar** o centro de custo, **mapear** para um existente ou **importar aquelas linhas sem** centro de custo — antes de confirmar. Em branco, o lançamento entra sem centro de custo.

### Anexei um arquivo ZIP a um lançamento. Os documentos de dentro aparecem na prestação de contas?

Sim. O RIT360 Financeiro **descompacta o ZIP automaticamente** e anexa cada arquivo de dentro como um anexo individual do lançamento — o pacote dá lugar aos arquivos, que passam a aparecer na pré-visualização e a entrar na prestação de contas. Vale também quando o comprovante chega por **link** na importação por CSV. Arquivos que não dá para exibir num PDF (planilhas, textos) ficam anexados, mas não aparecem no corpo do relatório.

### Em que mês cada lançamento entra, em Movimentações e nos Relatórios?

Pela **data em que o dinheiro se moveu**. As duas telas usam o mesmo critério: o que já foi **pago ou recebido** entra pelo mês do **pagamento**; o que ainda está **em aberto** (pendente ou atrasado) entra pelo mês do **vencimento**. Por isso o **Realizado** de Movimentações e os totais dos Relatórios **batem** para o mesmo período. (Os Relatórios continuam olhando só o dinheiro que circulou; o que está em aberto aparece em Movimentações, na coluna Previsto.)

Exemplo: uma conta que **vence em 30 de junho** e é **paga em 2 de julho** aparece em **julho**, nas duas telas — foi em julho que o dinheiro saiu. Enquanto estivesse em aberto, apareceria em junho, pelo vencimento.

Consequência prática: uma conta paga **com atraso** aparece no mês do pagamento, não no mês em que venceu — então um mês já conferido pode mudar depois, se alguma conta dele for quitada em atraso. É proposital: o RIT360 Financeiro trabalha em **regime de caixa**, e somar a junho um dinheiro que só saiu em julho distorceria o "Realizado" dos dois meses. A própria tela de Movimentações traz um aviso sobre o critério logo abaixo do resumo.

### O que significa "Previsto" no resumo de Movimentações?

**Previsto** é o que **ainda vai acontecer**: lançamentos com status **Pendente** ou **Atrasado**, que não foram pagos nem recebidos. **Realizado** é o que já **mexeu na conta** de verdade. Estornados e cancelados não entram em nenhuma das duas colunas.

Antes esses valores vinham somados num número só, o que dava a impressão de dinheiro em caixa que ainda não entrou. Separados, a leitura fica honesta: **decida gasto pela coluna Realizado**; use a coluna **Previsto** para se preparar — cobrar quem deve, adiar o que dá para adiar, buscar caixa antes de precisar. O **Resultado** aparece só no Realizado, de propósito: resultado previsto seria especulação.

### Por que uma conta aparece em vermelho?

Porque a cor sinaliza **o que exige atenção** — por isso nem tudo é colorido. Uma conta de ativo (corrente, poupança, caixa) fica **vermelha** quando o saldo está **negativo**, ou seja, a conta estourou ou entrou no cheque especial. Saldos positivos ficam neutros.

No **cartão de crédito** a lógica é a mesma vista pelo avesso: o valor **"a pagar"** é dívida, e aparece em vermelho; quando o cartão está com **"crédito"** (saldo a seu favor, por exemplo depois de um estorno da operadora), fica neutro. O mesmo critério vale no Painel e nos Relatórios.

### Se eu sair da tela enquanto preencho, perco o que já digitei?

Não. Ao preencher um **novo lançamento**, **reembolso** ou **pedido de compra e pagamento**, o que você digita é salvo automaticamente no seu dispositivo. Se você sair da tela — por exemplo, para escolher um arquivo para anexar — ou o navegador recarregar a página, ao voltar os campos continuam preenchidos e aparece um aviso de **"rascunho recuperado"**. O rascunho é apagado assim que você envia o formulário (ou clica em descartar), e some ao sair da sua conta. Observação: **arquivos ainda não enviados** não são guardados — só os campos digitados.

## Painel e pontos de atenção

### Um aviso que eu via no Painel sumiu. O que aconteceu?

Pode ser uma entre três coisas: (1) o problema foi resolvido — o lançamento que gerou o aviso mudou de status ou foi corrigido; (2) o aviso saiu da **janela de 30 dias** que o Painel considera (ele é sobre o que aconteceu recentemente, não sobre o histórico inteiro); ou (3) alguém com acesso a Configurações **desligou aquele tipo de regra** para a organização. Para conferir o histórico completo sem o recorte de 30 dias, use [Relatórios → aba Atenção](/modulos/relatorios/#atencao) com o período que quiser.

### Por que o Painel mostra avisos diferentes dos Relatórios?

Porque as duas telas recortam o tempo de forma diferente, de propósito. O **Painel** olha sempre os **últimos 30 dias** — é o "o que aconteceu recentemente". Os **Relatórios** (aba Atenção) olham o **período que você escolher** no filtro do cabeçalho — pode ser o mês fechado, o trimestre, o ano. Um aviso pode aparecer só em um dos dois: algo de 45 dias atrás some do Painel mas continua em Relatórios se o período escolhido incluir aquela data. Além disso, o Painel tem uma regra própria — **Déficit projetado no fluxo de caixa** — que não existe na aba Atenção dos Relatórios, porque olha para meses futuros, não para o período analisado.

### Quem pode desligar um aviso, e para quem vale?

Só quem tem permissão de administrar as configurações financeiras da OSC (tipicamente o Presidente) vê a opção de desligar um tipo de aviso, direto no próprio card do aviso no Painel ou em **Configurações → Relatórios → Regras de pontos de atenção**. O desligamento **vale para toda a organização** — não é uma preferência pessoal de quem clicou, é uma regra da OSC. O texto do aviso deixa isso explícito antes de confirmar, exatamente para evitar que alguém desligue "só para mim" sem perceber o alcance.

## Caça-diferenças (conciliação pelo saldo)

### O saldo do sistema não bate com o do meu banco. Como descubro por quê?

Use o **Caça-diferenças**. Na tela de **Movimentações**, no cartão **Contas**, cada conta tem um ícone de **lupa** 🔎 ao fim da linha. Clique nele, informe o **saldo final do extrato do banco** e a **data**, e o RIT360 Financeiro calcula a diferença e lista **hipóteses ranqueadas** do que pode tê-la causado — um lançamento duplicado, um lançamento que explica exatamente a diferença, algo lançado na conta errada, uma combinação de dois, ou um lançamento que ainda falta registrar. Veja o passo a passo em [Caça-diferenças](/modulos/caca-diferencas/).

### Qual a diferença entre o Caça-diferenças e "Conciliar extrato"?

**Conciliar extrato** parte de um **arquivo OFX** do banco e casa cada linha do extrato com os lançamentos do sistema. O **Caça-diferenças** parte só do **saldo final** que você lê no app do banco ou no caixa eletrônico — sem precisar de arquivo. Use o Conciliar extrato quando tiver o OFX; use o Caça-diferenças para uma conferência rápida "pelo número", ou para caçar aquela diferença que sobrou.

### É seguro clicar em "Excluir lançamento"?

A exclusão é **permanente** — por isso o botão só aparece para quem tem permissão de excluir movimentações, e sempre pede uma confirmação. Já **"Mover para esta conta"** apenas troca a conta do lançamento (reversível). Nas duas ações, depois de aplicar, a diferença é recalculada na hora para você ver o efeito. Na dúvida, use **"Abrir lançamento"** e confira antes de decidir.

### Minha conta está no cheque especial (saldo negativo). Consigo usar?

Sim. No campo de saldo do banco, use o sinal de **"−"** para informar um valor negativo (ex.: `−1.500,00`). O cálculo da diferença considera o sinal corretamente. Vale também para conciliar a **fatura de um cartão de crédito**.

## Reembolsos e Pedidos de Compra e Pagamento

### Meu pedido foi reprovado. E agora?

Não é o fim: abra o detalhe do reembolso ou pedido de compra e pagamento rejeitado (o motivo aparece em destaque no topo, com quem reprovou e quando) e clique em **Editar e reenviar** — só o solicitante vê esse botão. Os campos passam a ser editáveis na própria página; corrija o que foi apontado (comprovante ilegível, valor errado, categoria trocada) e envie de novo. Não é preciso criar uma solicitação nova, e o fluxo de aprovação recomeça a partir do reenvio. Veja o detalhe completo em [Reembolsos → Rejeitado](/modulos/reembolsos/#rejeitado).

### Enviei um reembolso (ou pedido) por engano, ou mudei de ideia. Como desisto?

Enquanto a solicitação está **Aguardando aprovação**, você mesmo pode retirá-la: abra o detalhe e clique em **Retirar solicitação**, no painel de Ações. Ela passa para **Cancelado**, qualquer aprovação que já tinha sido dada é descartada, e quem ainda não tinha votado é avisado de que ela saiu da fila. Antes desta versão, a única forma de encerrar uma solicitação já enviada era pedir para alguém reprovar — o que ficava registrado como reprovação, não como desistência. **Só você retira a sua própria solicitação**; nem administrador nem tesoureiro retiram a de outra pessoa. Detalhes em [Reembolsos → Retirar uma solicitação enviada](/modulos/reembolsos/#retirar-solicitacao).

### Por que uma solicitação retirada posso reenviar sem mudar nada, e uma reprovada não?

Porque são situações diferentes. Uma solicitação **reprovada** tem algo que um aprovador apontou como problema — por isso reenviar exige corrigir de verdade algo (valor, comprovante, categoria...), e reenviar sem alterar nada é recusado. Uma solicitação **retirada** por você não tinha nada de errado: você só mudou de ideia sobre o momento, ou decidiu reorganizar antes de mandar de novo. Por isso ela pode voltar para a fila de aprovação exatamente como estava, sem exigir alteração nenhuma.

### Por que uma única reprovação encerra meu pedido, se a OSC exige duas aprovações?

Porque aprovar e reprovar têm contas separadas, e a de reprovação **vem configurada como 1**. O quórum diz quantas aprovações **liberam** o pagamento; um ajuste próprio, em [Fluxo de Aprovações](/configuracoes/aprovacoes/), diz quantas reprovações **barram**. No padrão — uma —, assim que alguém reprova o pedido vira **Rejeitado** e os demais aprovadores não podem mais votar. É a escolha conservadora: soltar dinheiro da OSC exige acordo de mais de uma pessoa, mas qualquer aprovador elegível pode barrar sozinho, porque é esse o papel de quem fiscaliza.

Se a sua organização preferir, ela pode **exigir mais de uma reprovação** (até o número de pessoas aptas a aprovar). Nesse caso o pedido continua **Aguardando aprovação** até o número ser alcançado, a tela mostra quantas reprovações já existem e quantas faltam, e você só é avisado quando houver decisão definitiva.

### Por que não dá para reprovar vários reembolsos ou pedidos de uma vez, se dá para aprovar?

Porque **cada reprovação exige um motivo próprio**. Aprovar em lote faz sentido porque um "sim" vale igual para todos os itens marcados; um "não" não — cada reprovação precisa dizer especificamente o que está errado naquela solicitação (comprovante ilegível, valor incorreto, categoria trocada), para que quem pediu saiba o que corrigir. Um motivo genérico aplicado a vários de uma vez não ajudaria ninguém. Por isso a seleção em lote em [Reembolsos](/modulos/reembolsos/#selecao-em-lote) e Pedidos de Compra e Pagamento só tem o botão **Aprovar selecionados** — reprovar continua sendo um de cada vez.

### Quem pode escrever a nota explicativa da prestação de contas?

Por padrão, **Presidente** e **Tesoureiro** — a mesma permissão de sempre. A organização pode conceder essa permissão a outros cargos, inclusive cargos que ela mesma criou, em [Cargos e permissões](/configuracoes/cargos/#permissao-nota-explicativa). A **Comissão Fiscal** não escreve a nota: ela **emite o relatório e lê o que foi escrito**, mas redigir é ato de quem presta contas, não de quem fiscaliza. Detalhes em [Movimentações → Nota explicativa](/modulos/movimentacoes/#nota-explicativa).

### Onde encontro uma prestação de contas que já foi gerada?

Em **Relatórios**, clique na pílula **Prestações de contas**, ao final da fileira de filtros: ali está a lista de todos os documentos já gerados pela organização, com período, data e hora da geração, quem gerou e o intervalo coberto. Você pode **baixar** o PDF, **gerar de novo** ou **apagar o arquivo**. Antes, o único acesso era o link enviado por e-mail na hora da geração — agora o documento fica na plataforma. As três ações exigem a mesma permissão de exportar dados que já é necessária para ver a lista. Detalhes em [Relatórios → Prestações de contas](/modulos/relatorios/#prestacoes-de-contas).

### "Gerar de novo" me devolve o mesmo PDF de antes?

Não. O documento é montado com **os dados de hoje** — não é uma cópia do que foi entregue na época. Se algum lançamento daquele período foi editado, estornado ou cancelado desde então, o resultado vai ser diferente do original. O arquivo que já existe também **não é substituído**: cada geração cria um **registro novo** na lista, por isso é normal ver várias prestações do mesmo mês.

### Apagar o arquivo apaga a prestação de contas?

Não. Sai **apenas o PDF**. A linha continua na lista de [Prestações de contas](/modulos/relatorios/#prestacoes-de-contas), marcada com a data em que o arquivo foi removido e por quem, e com a opção de gerar de novo. Antes de apagar, a confirmação mostra exatamente qual documento você escolheu (período, data e hora da geração, autor) — vale conferir, porque é comum haver várias prestações do mesmo mês.

### Por quanto tempo os PDFs de prestação de contas ficam guardados?

**Para sempre, por padrão — nada é descartado.** Se a sua organização tiver política de retenção, o Presidente pode definir um prazo em **Configurações → Relatórios**: 1, 2, 3, 5 ou 10 anos, contados do fim do período coberto pelo documento. Com prazo configurado, o sistema **avisa por e-mail 30 dias antes** de qualquer descarte, listando o que vai sair e permitindo baixar antes; se o prazo mudar, o aviso perde a validade e a contagem recomeça. O registro da prestação nunca é apagado.

### Por que não consigo reenviar meu pedido rejeitado?

Porque reenviar **exige corrigir algo de verdade**. Se você clicar em reenviar sem alterar nenhum campo, o RIT360 Financeiro recusa com a mensagem "Nenhuma alteração detectada. Corrija a solicitação antes de reenviar." — isso evita que o mesmo pedido volte para a fila de aprovação sem que nada tenha sido corrigido. Contam como alteração: valor, descrição, data da despesa, categoria, projeto, centro de custo, dados de pagamento, observações, e também **incluir ou remover um comprovante**. Se o motivo da rejeição foi "faltou a nota fiscal", basta anexar o comprovante — já é alteração suficiente para reenviar.

### Eu já tinha aprovado esse pedido antes. Por que preciso aprovar de novo?

Porque o reenvio **reinicia a contagem de aprovações**. Quando alguém reprova e o solicitante corrige e reenvia, o histórico de votos daquele pedido recomeça do zero — mesmo quem já tinha aprovado a versão anterior precisa votar de novo na versão corrigida. Não é intuitivo, mas a lógica é consistente: cada rodada de aprovação avalia a versão atual do pedido, e o pedido mudou.

### O que acontece quando um reembolso é aprovado?

O RIT360 Financeiro cria automaticamente uma **movimentação financeira pendente** em Movimentações com origem `reimbursement`, vinculada ao reembolso. O tesoureiro entra em Movimentações, escolhe a conta de onde vai sair o dinheiro e marca como paga. O ciclo só fecha quando essa confirmação acontece.

### Posso anexar mais de um comprovante em um reembolso?

Sim. O formulário aceita múltiplos arquivos. Anexe nota fiscal, recibo, foto da despesa, comprovante de pagamento — quanto mais clareza, mais rápida a aprovação.

### Onde configuro minha chave PIX para receber reembolsos?

Em **Meu Perfil → Dados para Reembolso**. Configure uma vez; o formulário de nova solicitação preenche automaticamente em todas as próximas vezes.

### Abri um reembolso (ou pedido) antigo e os dados bancários sumiram. Perdi alguma coisa?

Não. Depois que o pagamento é concluído, os dados bancários de quem recebeu ficam guardados apenas pelo prazo que a sua OSC definiu (padrão: **90 dias**) e então são **apagados automaticamente** — a tela explica isso quando você abre o registro. **Continuam ali** valor, descrição, datas, categoria, centro de custo, projeto, anexos, situação e o **nome de quem recebeu**: a prestação de contas fica completa. Se precisar pagar de novo para a mesma pessoa, peça os dados outra vez. Registros **ainda não pagos nunca são tocados**. Ver [Dados bancários de quem recebe](/configuracoes/contas/#dados-bancarios-de-quem-recebe).

### Qual a diferença entre Reembolso e Pedido de Compra e Pagamento?

**Reembolso** é para despesa que **já aconteceu**: você pagou do bolso e quer receber de volta. **Pedido de Compra e Pagamento** é para despesa que **ainda vai acontecer**: a OSC vai pagar (boleto, fornecedor, contrato) e a aprovação autoriza a saída de dinheiro.

### Posso criar um Pedido de Compra e Pagamento recorrente para o aluguel?

Sim. Ao criar um pedido, escolha tipo **Recorrente** e configure a frequência (mensal) e a duração (data final, quantidade de ocorrências ou indefinida até cancelar). A aprovação cria a série inteira; cada ocorrência é paga separadamente pelo tesoureiro. Veja a [seção de Pedidos de Compra e Pagamento](/modulos/pedidos-pagamento/) para detalhes.

### Ainda não sei o preço final da compra. Posso pedir aprovação mesmo assim?

Sim — escolha **"Valor estimado — a confirmar na compra"** ao criar o pedido, e anexe os orçamentos que embasam a estimativa. A aprovação libera com base nesse valor; depois, quando o preço fecha com o fornecedor, alguém com permissão de pagar registra o valor efetivo editando o lançamento. Se a diferença passar do limiar definido pela sua OSC (padrão 10%), o pagamento fica retido até um aprovador autorizar. Ver [Pedidos de Compra e Pagamento → Quando o valor pago diverge do autorizado](/modulos/pedidos-pagamento/#valor-diverge-do-autorizado).

### Registrei o valor final da compra e o pagamento sumiu do fluxo normal. O que aconteceu?

Provavelmente o valor final passou do valor autorizado além do limiar de reaprovação da sua OSC — o pedido continua **aprovado**, só o pagamento ficou retido até alguém autorizar a diferença. Abra o pedido: se você aprova, verá os botões **Autorizar a diferença**, **Pedir autorização a outro aprovador** e **Recusar a diferença**; se só paga, verá **Pedir autorização do valor excedente**. Ver [Pedidos de Compra e Pagamento → Quando o valor pago diverge do autorizado](/modulos/pedidos-pagamento/#valor-diverge-do-autorizado).

## Projetos

### Como crio um projeto?

Em **Projetos → Novo projeto**. Um assistente de 4 passos (tipo e identidade, período, financeiro essencial, coordenador e equipe) conduz a criação, com textos de ajuda em cada etapa. O projeto nasce como rascunho "Em planejamento"; quando estiver pronto, você solicita a aprovação de abertura.

### Quem pode criar projetos?

Presidente, Tesoureiro e Coordenador podem criar diretamente. O **Voluntário** pode **propor** um projeto — ao ser aprovado, ele é promovido a coordenador daquele projeto. Veja o [Guia do Coordenador de Projetos](/guias/coordenador-projetos/).

### Como vinculo uma despesa (ou receita) a um projeto?

No formulário de lançamento, use o campo **Projeto** (opcional). O dinheiro continua sendo da OSC, nas mesmas contas — o projeto apenas **rotula** a movimentação, para você ver o recorte dele sem perder o todo. O mesmo vale para reembolsos e pedidos de compra e pagamento.

### O que é a "saúde" do projeto (o semáforo)?

Um indicador (🟢 Saudável, 🟡 Atenção, 🔴 Crítico, com pontuação de 0 a 100) que combina **prazo**, **orçamento** e **riscos**. Ele aparece na lista de projetos e no Painel, para a diretoria ver de relance o que pede atenção.

### Onde vejo as lições de projetos anteriores?

Em **Projetos → Lições aprendidas** — um acervo da OSC com as lições e boas práticas registradas no encerramento de todos os projetos, com busca e filtros. Ao criar um novo projeto, o sistema ainda indica quantas lições existem para aquele tipo.

### Como encerro um projeto?

Na aba **Encerramento** do projeto, um assistente de avaliação conduz por perguntas (objetivos, critérios, engajamento, pontos altos, lições...). O RIT360 Financeiro monta o **relatório de encerramento** consolidado, exportável em PDF para a prestação de contas. Cada campo traz orientação e um exemplo de preenchimento.

### Qual a diferença entre meu papel na OSC e meu papel no projeto?

São independentes. Seu **papel na OSC** (Presidente, Tesoureiro, Voluntário...) define o acesso geral. Seu **papel no projeto** (Coordenador, integrante, observador) define o que você faz **dentro daquele projeto** — um voluntário pode ser coordenador de um projeto específico, e um tesoureiro pode ser só integrante de outro.

## Estornos

### Quando devo estornar e quando cancelar?

**Cancele** quando a movimentação **ainda não foi paga** e não vai mais acontecer (evento desmarcado, fornecedor desistiu). **Estorne** quando a movimentação **já foi paga** e precisa ser desfeita (depósito duplicado, doação devolvida pelo banco, refund). Estornar preserva o histórico e cria automaticamente um lançamento contrário; cancelar simplesmente marca como anulada.

### Estornei um lançamento por engano. Como desfazer?

Estorno não tem "desfazer estorno" automático no RIT360 Financeiro. Para reverter, você precisa **criar manualmente uma movimentação nova** com os mesmos dados do estornado, com data atual. Por isso a operação de estorno tem dialog de confirmação com campo de razão — para evitar engano no clique.

## Contas, categorias e configuração

### Minha conta bancária sumiu da lista. O que aconteceu?

Contas podem ser **desativadas** por um administrador (em Configurações → Contas Bancárias). Contas desativadas não aparecem em filtros e formulários, mas as movimentações históricas associadas a elas são preservadas. Verifique com o admin.

### Por quanto tempo ficam guardados os dados bancários de quem a OSC paga? Dá para mudar?

Dá. Em **Configurações → Contas Bancárias**, no cartão **Descarte de dados bancários**, a organização escolhe entre **30, 90, 180 ou 365 dias** contados a partir da conclusão do pagamento — o padrão é **90**. Antes de salvar, a tela mostra **quantos registros já estariam vencidos** com o prazo escolhido. **Não existe a opção de guardar para sempre**: esses dados servem para fazer a transferência e, cumprida a finalidade, não precisam continuar guardados — ainda mais porque quem recebe muitas vezes nem tem conta no sistema para pedir a remoção. Ver [Dados bancários de quem recebe](/configuracoes/contas/#dados-bancarios-de-quem-recebe).

### Quero que quem lança as despesas não possa dar baixa nos pagamentos. É possível?

Sim. Em **Configurações → Cargos e permissões**, abra o cargo e **desligue "Pagar (marcar como pago)"** em Movimentações. A pessoa continua registrando e editando lançamentos normalmente, mas não confirma pagamentos — nem pelo lançamento, nem pela parcela de pedido de compra e pagamento, nem pela conciliação de extrato. É a mesma lógica de segregação de funções que já protege a Comissão Fiscal. Ver [Cargos e permissões](/configuracoes/cargos/#permissao-pagar).

### Como começo do zero com as categorias? Não sei o que cadastrar.

Em **Configurações → Categorias**, clique em **Aplicar template** e escolha um modelo próximo ao perfil da sua OSC (ex: "Padrão Grupo Escoteiro 2026"). O template traz categorias típicas pré-configuradas. Depois você ajusta o que não bater com sua realidade — renomeia, exclui, adiciona.

### Tenho a lista inteira de categorias e centros de custo pronta. Preciso cadastrar um por um?

Não, se estiver numa planilha. Em **Configurações → Categorias**, clique em **Importar por planilha** (ao lado de "Aplicar template"), baixe o modelo, preencha e envie — a ordem das linhas não importa, o sistema monta a hierarquia sozinho. Antes de gravar, você vê uma **prévia** com o que vai ser criado, atualizado ou recusado (e por quê), e escolhe se quer aplicar as atualizações a categorias já existentes ou só acrescentar o que é novo. Ver [Configurações → Categorias → Importar por planilha](/configuracoes/categorias/#importar-categorias-e-centros-de-custo-por-planilha).

### Cadastrei várias pessoas e metade nunca entrou. Como descubro quem são?

Em **Configurações → Usuários**, quem ainda não concluiu o primeiro acesso aparece com o tempo de espera ("Aguardando há N dias"). Passados **14 dias** — quando os lembretes automáticos do sistema já se esgotaram — a pessoa ganha o selo **"Sem resposta"**, e um **resumo no topo da tela** mostra a contagem e filtra a lista só para essas pessoas com um clique. A partir daí você decide: reenviar o acesso, corrigir um e-mail digitado errado ou cancelar o acesso pendente. Ver [Configurações → Usuários](/configuracoes/usuarios/).

### Preciso desativar (ou reenviar o acesso de) 30 pessoas. Tenho que fazer uma por uma?

Não. Em **Configurações → Usuários** você marca várias pessoas na lista — ou usa **"Selecionar os N filtrados"** — e aplica a ação em lote. Como a seleção pode misturar situações diferentes, cada botão avisa a quantas pessoas a ação realmente se aplica, e ao final você vê o resultado **pessoa a pessoa**. Detalhe importante: se você interromper no meio, **quem já foi processado continua processado**. Ver [Configurações → Usuários](/configuracoes/usuarios/).

## Página pública (transparência)

### Publicar a página expõe dados das pessoas?

Não. A [Página Pública](/configuracoes/pagina-publica/) trabalha apenas com **totais somados por período e por categoria**. O sistema **nunca publica** — mesmo que a OSC queira — lançamento individual, nome de pessoa física (solicitante, beneficiário, fornecedor pessoa física, membro da equipe), comprovantes e anexos, o relatório de prestação de contas, dados bancários, **saldo das contas**, CPF, RG, e-mail ou telefone de pessoas, nem as telas internas de gestão. Isso é decisão de produto: a OSC escolhe *quanto* mostrar (quais blocos, resumido ou detalhado), não precisa avaliar risco item a item.

O único cuidado que fica com você: **os nomes das categorias aparecem na página**. Antes de ligar o bloco "De onde vem, para onde vai", revise a lista em Configurações → Categorias e renomeie qualquer categoria com nome de pessoa ou referência a caso individual.

### Por que a página não mostra o mês atual?

Porque o recorte para sempre no **último mês encerrado**. O mês em curso é um mês de rascunho — tem lançamento pela metade, comprovante que ainda não chegou, erro de digitação não corrigido. Publicar isso obrigaria a explicar depois por que o número mudou, e número que muda parece número maquiado para quem está de fora. **Número público é número conferido.** E é automático: ninguém na OSC precisa lembrar de "fechar o mês na página".

### Posso colocar a página no site da minha organização?

Sim. Em **Configurações → Página pública → Colocar no site da organização**, clique em **Copiar código** e cole o trecho numa página do seu site — no WordPress, dentro de um bloco de **HTML personalizado**. O conteúdo aparece embutido, com a altura se ajustando sozinha e acompanhando a largura da coluna do site. A grande vantagem é que **ele se atualiza sozinho**: ninguém precisa copiar número à mão todo mês.

### A página mostra algum e-mail de contato da minha organização?

Só se você quiser. Em **Configurações → Organização** existe um bloco **opcional** chamado **[Contato de proteção de dados](/configuracoes/organizacao/#contato-de-proteção-de-dados)**, com um e-mail e, se você quiser, o nome da pessoa responsável. **Em branco, nada aparece.** Preenchido, o contato passa a aparecer na página pública quando ela está publicada — por isso a recomendação é usar um **e-mail institucional da OSC**, e não o e-mail pessoal de um voluntário. A tela avisa isso antes de salvar.

### Como tiro a página do ar se precisar corrigir algo?

Desligue a chave **Publicar / Despublicar página pública**, no topo de Configurações → Página pública. O efeito é **imediato** e **nenhuma configuração é perdida** — blocos, período e missão continuam salvos, e religar devolve tudo como estava. Enquanto despublicada, você ainda consegue conferir tudo pela **Prévia**, que mostra exatamente o que o público veria.

## Integração com WooCommerce

### Posso conectar minha loja online ao RIT360 Financeiro?

Se sua loja usa **WooCommerce**, sim. Em **Configurações → Organização → seção WooCommerce**, configure URL da loja, Consumer Key e Consumer Secret. O RIT360 Financeiro sincroniza pedidos pagos como receitas automaticamente. A seção tem instruções passo a passo de como gerar as credenciais no admin do WooCommerce.

### Quando a sincronização com WooCommerce acontece?

**Automaticamente todo dia às 6h da manhã** (horário de Brasília), respeitando a frequência configurada por OSC: diária, semanal (segundas), mensal (dia 1) ou desligada. Você também pode disparar manualmente a qualquer momento em **Movimentações → Importar Lançamentos → aba WooCommerce → Importar agora**.

### Um pedido foi reembolsado no WooCommerce. O que acontece no RIT360 Financeiro?

A próxima sincronização detecta a mudança de status e **estorna automaticamente** a movimentação correspondente no RIT360 Financeiro — cria um lançamento contrário (despesa de igual valor que cancela a receita anterior) e ambos passam a exibir o badge "Estornado". Sem intervenção manual.

## Notificações

### Não quero receber tantos e-mails. Como reduzir?

Em **Meu Perfil → Notificações → Matriz**, você escolhe **por evento e por canal** quais notificações quer receber. Default é tudo ligado — desligue o que não interessa. Cuidado para não silenciar eventos críticos do seu papel (ex: aprovador deve manter "submetido" ligado para saber quando algo precisa do voto).

### Como ativo notificações push no celular?

Em **Meu Perfil → Notificações**, toque no interruptor **"Ativar push neste dispositivo"** (acima da matriz). O navegador vai pedir permissão; autorize. A coluna **Push** na matriz fica habilitada para você escolher quais eventos receber por esse canal — funciona como aviso de banco, chega na tela mesmo com o RIT360 Financeiro fechado e abre direto na tela relevante ao tocar.

**Importante:** no **iPhone (Safari)**, push só funciona se você **instalou o RIT360 Financeiro como app** na tela de início — sem instalar, o interruptor fica desabilitado com instrução. Veja [Instalar como aplicativo](/instalar-como-app/). No **Android (Chrome / Edge)** e em **desktop (Chrome / Firefox / Edge)**, funciona direto sem precisar instalar como app.

A ativação é **por dispositivo**: pode ativar no celular pessoal e deixar desativado no celular do trabalho, sem afetar a configuração da sua conta.

## Guias por papel

### Existe um guia de como atuar no meu papel na OSC?

Sim. Além de explicar as telas, o manual traz **cartilhas de atuação** por papel — o que se espera de você, pontos de atenção e boas práticas, com exemplos de como o RIT360 Financeiro ajuda em cada aspecto:

- [Guia do Coordenador de Projetos](/guias/coordenador-projetos/) — escopo, prazo, recursos e pessoas.
- [Guia do Tesoureiro](/guias/tesoureiro/) — registrar, organizar, aprovar e prestar contas.
- [Guia da Comissão Fiscal](/guias/comissao-fiscal/) — fiscalização independente.
- [Guia do Presidente](/guias/presidente/) — responsabilidade com visão, delegação e acompanhamento tranquilo.

## Geral

### Tenho uma sugestão ou encontrei um erro. Como informo?

Use o botão **💬 Feedback** no menu superior. Está disponível para todos os usuários e envia sua mensagem direto para a equipe da RIT, com a versão do app e o seu contexto.

### Onde acompanho as novidades do RIT360 Financeiro?

Nas [Novidades](/changelog/) deste manual. Toda nova versão lançada é registrada lá com a lista de adições, correções e mudanças. As entregas significativas aparecem em destaque.

### Quero entender melhor um conceito que aparece no RIT360 Financeiro (fluxo de caixa, regime de caixa, estorno...). Onde leio?

Cada módulo deste manual tem uma seção **Conceitos essenciais** que cobre os termos relevantes em linguagem simples. Movimentações cobre regime de caixa e estorno; Reembolsos cobre quórum e auto-aprovação; Pedidos cobre recorrente vs parcelado.

### Um fornecedor (ou participante de projeto) quer ver, corrigir ou apagar os dados dele. Quem responde?

Depende de **quem decide sobre aquele dado**. Se foi a **sua organização** que cadastrou — cadastro de fornecedor, dados de um participante, um anexo —, quem responde é a **organização**, porque é ela quem pode corrigir, incluir ou remover. Se o assunto é **conta e acesso** — e-mail de login, senha, registros de acesso —, quem responde é a **RIT** (`dpo@rit.org.br`). Para que essas pessoas saibam onde procurar a sua OSC, preencha o **[contato de proteção de dados](/configuracoes/organizacao/#contato-de-proteção-de-dados)** em Configurações → Organização — ele aparece na página pública de transparência. O roteamento completo está na Política de Privacidade, em [Com quem falar sobre seus dados](/privacidade/#10-com-quem-falar-sobre-seus-dados).

### Posso integrar o RIT360 Financeiro com outro sistema?

Sim. Em [Configurações → Integrações](/configuracoes/integracoes/), gere uma credencial e libere para um sistema parceiro (site institucional, painel do conselho, ferramenta interna) consultar o **resumo financeiro** da sua OSC por API — só totais, sem dado individual e sem dar acesso à plataforma. É diferente da [Página Pública](/configuracoes/pagina-publica/): ali é leitura humana e aberta a qualquer visitante; aqui é um canal técnico, autenticado, para outro sistema.

### Posso usar o RIT360 Financeiro se não sou de OSC?

O RIT360 Financeiro é desenhado para OSCs (Organizações da Sociedade Civil) — terceiro setor. O fluxo de aprovação, os papéis e a linguagem refletem esse contexto. Outros tipos de organização (empresa, autônomo) podem usar tecnicamente, mas vão encontrar funcionalidades que não fazem sentido no contexto deles.
