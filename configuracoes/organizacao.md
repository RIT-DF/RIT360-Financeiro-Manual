---
title: "Organização"
nav_order: 1
parent: "Configurações da Organização"
permalink: /configuracoes/organizacao/
---

> Disponível para **Presidente (admin)**.

A página **Organização** centraliza os dados da sua OSC e as **integrações** com sistemas externos. Acessada pelo **ícone de engrenagem** no canto superior direito (a engrenagem só aparece para admin e tesoureiro) → Configurações → seção Organização.

[![Configurações — Organização](/assets/screenshots/config-organizacao.png)](/assets/screenshots/config-organizacao.png)
*Configurações — Dados da organização*

> 💡 **Por que isso importa**
>
> Os dados da OSC aqui aparecem em **todos os documentos gerados pelo RIT360 Financeiro** (recibos, declarações, relatórios para financiadores, exportações em PDF). Manter atualizado é o que faz a marca da sua OSC aparecer profissional na prestação de contas. As **integrações** abrem porta para automação: WooCommerce sincroniza vendas, Google Drive armazena documentos.

## Identidade da OSC

[![Identidade da OSC — Nome, CNPJ, Inscrição Estadual e Municipal](/assets/screenshots/config-organizacao-identidade.png)](/assets/screenshots/config-organizacao-identidade.png)
*Identidade da OSC — Inscrição Estadual e Inscrição Municipal ficam ao lado do CNPJ*

- **Nome** — a razão social. É este nome que aparece em documentos, e-mails e na página pública
- **Nome curto** (opcional) — nome fantasia ou sigla pela qual a organização é conhecida (ex.: "RFCC Brasília"). Aparece só na **navegação do sistema** — cabeçalho, seletor de organização e menu do celular —, para caber e ser lido de relance. **Não substitui a razão social**: documentos, e-mails e a página pública continuam usando o Nome. Em branco, a navegação também mostra a razão social — nada muda.
- **CNPJ** — formatado automaticamente conforme você digita. Aceita tanto o CNPJ numérico tradicional quanto o novo **CNPJ alfanumérico** (que passa a valer a partir de julho/2026)
- **Inscrição Estadual** — campo opcional, de preenchimento livre. Se a OSC não tem inscrição estadual, digite **"ISENTO"**
- **Inscrição Municipal** — campo opcional, de preenchimento livre
- **E-mail institucional**
- **Telefone** — com **seletor de país** (Brasil já selecionado por padrão) e a mesma máscara única usada em todo o sistema; ao abrir o cadastro salvo, o país é reconhecido automaticamente pelo número
- **Site** — endereço completo (`https://...`)
- **Identificador único** — slug não editável usado em URLs e identificações internas (gerado a partir do nome no cadastro)

> 💡 **Por que isso importa**
>
> Razão social costuma ser longa — "Associação Beneficente de Apoio à Família e à Criança", por exemplo — e não cabe no cabeçalho nem no seletor de organização, sobretudo em quem participa de mais de uma OSC. O nome curto resolve isso sem mexer no que é oficial: você continua vendo a razão social completa em qualquer documento, e-mail ou relatório, e ganha uma identificação enxuta só para navegar no dia a dia.

## Endereço e redes sociais

Endereço completo (CEP, logradouro, número, complemento, bairro, cidade, UF) e perfis em redes sociais (Instagram, Facebook, LinkedIn, YouTube).

> ✓ **Dica · Preencha endereço completo para documentos formais**
>
> Recibos e declarações geradas pelo RIT360 Financeiro usam o endereço daqui. OSC com endereço incompleto no sistema pode acabar com documentos que não passam em conferência de financiador ou contador.

## Logo da organização

Upload da logo da OSC (JPG, PNG, WebP ou **SVG**, até 2 MB). A imagem é aceita em **qualquer proporção** e ajustada automaticamente, preservando o formato original — não é mais recortada em quadrado. A logo aparece na **barra superior** (no lugar do nome da OSC), no **cabeçalho dos e-mails** de notificação e nos **relatórios em PDF** (movimentações e prestação de contas). Ao **trocar a logo**, a nova imagem passa a valer na hora.

## Configurações operacionais

- **Moeda** — padrão Real (BRL); pode ser alterada se a OSC opera em outra moeda
- **Fuso horário** — todas as datas/horas no sistema seguem esse fuso
- **Início do ano fiscal** — define os recortes de "Ano YTD" e "Ano anterior" nos filtros (default Janeiro)

## Acesso público

- **Aceitar solicitações públicas de vínculo** — quando ativado, qualquer pessoa com o link público da OSC pode pedir vínculo (a OSC ainda precisa aprovar). Desligado por default.

> ⚠️ **Atenção · Acesso público é compartilhamento controlado**
>
> "Aceitar solicitações públicas de vínculo" não dá acesso automático — ainda passa pelo admin. Mas com o link público, qualquer pessoa pode pedir entrada na sua OSC. Use quando você quiser receber inscrições espontâneas (ex: novos voluntários, novos associados); desligue quando preferir só convidar manualmente.

## Regras padrão para projetos

Valores iniciais que o módulo de [Projetos](/modulos/projetos/) usa ao planejar — em especial na **calculadora de taxa de eventos**. São apenas o **ponto de partida**: cada projeto pode ajustar conforme o caso.

- **Fundo de reserva padrão (%)** — uma folga de segurança sobre os custos previstos ao planejar o orçamento de um evento (default 10%). Entra como reserva no cálculo da taxa de inscrição.
- **Regra padrão de pagamento de voluntários** — como os voluntários entram na conta da taxa: **rateados** (não pagam; o custo deles é dividido entre os pagantes), **pagam taxa cheia**, **OSC paga** pelos voluntários, ou **com desconto** (quando aplicável, com o percentual de desconto).
- **Permitir que cada projeto sobrescreva esta regra** — se ligado, um projeto específico pode escolher uma regra de pagamento de voluntários diferente da padrão da OSC.

> 💡 **Por que isso importa**
>
> Definir essas regras uma vez, no nível da OSC, evita reconfigurar a calculadora de taxa a cada evento — e mantém coerência entre os projetos (todos partem do mesmo fundo de reserva e da mesma política de voluntários). Quando um evento for exceção, o projeto sobrescreve pontualmente, sem mudar o padrão da organização.

## Integrações

Integração permite que sistemas externos conversem com o RIT360 Financeiro — economizando trabalho manual de transferir dados de um sistema para outro.

### WooCommerce

[Saiba mais no manual de Movimentações → seção Importar lançamentos](/modulos/movimentacoes/#importar-lançamentos)

Sincroniza pedidos pagos da sua loja online (WooCommerce) como receitas no RIT360 Financeiro. Cron diário automático + botão para importar sob demanda. Refunds no WooCommerce viram estornos automáticos no RIT360 Financeiro. Cada pedido importado tem badge "WooCommerce" clicável na lista de movimentações que abre o pedido original no admin do WC.

Configure URL da loja, Consumer Key e Consumer Secret (com instruções passo a passo de como gerar no admin do WooCommerce), frequência da sincronização, modo de mapeamento de categorias (automático com categoria-mãe ou manual explícito), conta financeira destino, data de corte para backfill.

#### Mapeamento manual de categorias tem ordem
{: #mapeamento-manual-de-categorias-tem-ordem }

[![Mapeamento manual do WooCommerce, com setas de subir e descer em cada linha](/assets/screenshots/config-organizacao-woocommerce-mapeamento.png)](/assets/screenshots/config-organizacao-woocommerce-mapeamento.png)
*Configurações → Organização → WooCommerce — mapeamento manual de categorias, com as setas de reordenar em cada linha*

No **modo manual**, a tela de mapeamento lista uma linha por categoria da loja, cada uma apontando para uma categoria financeira do RIT360 Financeiro. Cada linha tem setas para **subir** e **descer** — e a ordem não é só visual: ela decide o desempate quando um produto da loja está em **mais de uma** categoria mapeada ao mesmo tempo.

> 📖 **Conceito · Por que precisa de desempate**
>
> Um produto do WooCommerce pode estar em mais de uma categoria da loja ao mesmo tempo (ex.: "Camisetas" e "Promoção de aniversário"). Se as duas estiverem mapeadas para categorias financeiras diferentes, o RIT360 Financeiro precisa escolher uma só para lançar o valor daquele item — não existe rateio dentro do mesmo produto, só entre produtos diferentes do mesmo pedido (veja o rateio por produto no [manual de Movimentações](/modulos/movimentacoes/#importar-lançamentos)). A ordem da lista de mapeamento é esse critério de desempate: **vale a primeira linha que casar com alguma categoria do produto.**

*Exemplo:* a "Camiseta Institucional" está nas categorias de loja "Camisetas" e "Promoção de aniversário". Se "Promoção de aniversário → Doações" estiver **acima** de "Camisetas → Venda de produtos" na lista, todo pedido dessa camiseta lança em **Doações** — enquanto o produto continuar marcado nas duas categorias na loja.

> ✓ **Dica · Deixe o mapeamento mais específico no topo**
>
> Categoria de promoção, campanha ou evento — algo que um produto ganha temporariamente — costuma ser mais específica que a categoria "de prateleira" (Camisetas, Acessórios). Deixá-la no topo garante que ela vença o desempate enquanto durar.

> ⚠️ **Atenção · Reordenar afeta só as próximas sincronizações**
>
> Mudar a ordem do mapeamento não reprocessa nada sozinho — vale para os pedidos que **ainda vão** ser importados. Para aplicar a nova ordem a lançamentos que já entraram no RIT360 Financeiro, use o [reprocessamento de categorias](/modulos/movimentacoes/#reprocessar-categorias-woocommerce), na tela de importação.

No **modo automático** (categoria-mãe) não existe essa tela de mapeamento manual — e por isso não há ordem para configurar. O desempate, quando acontece, segue um critério fixo do sistema, não editável. Quem precisa decidir explicitamente qual categoria vence usa o **modo manual**.

### Google Drive *(em implantação)*

Armazenamento de documentos da OSC no Google Drive da organização. Anexos de movimentações, reembolsos e pedidos serão sincronizados automaticamente.

## Contato de proteção de dados

O bloco **Contato de proteção de dados** informa **para onde escrever quem quer tratar de dados pessoais que a sua organização cadastrou** — um fornecedor, um prestador de serviço, um participante de projeto, um beneficiário, um doador. Em geral são pessoas que **não têm conta** no RIT360 Financeiro e que precisam de um endereço para pedir acesso, correção ou exclusão dos próprios dados.

[![Contato de proteção de dados](/assets/screenshots/manual-contato-protecao-de-dados.png)](/assets/screenshots/manual-contato-protecao-de-dados.png)
*Configurações → Organização — o bloco Contato de proteção de dados, com o aviso de que o dado fica visível na página pública*

São dois campos:

- **E-mail de contato** — o endereço para onde essas solicitações devem ir.
- **Pessoa responsável** — opcional; o nome (ou o cargo) de quem responde por esses pedidos na organização.

**Preencher é opcional.** Se você deixar em branco, **nada muda e nada aparece em lugar nenhum** — nem na página pública, nem para os usuários. O bloco existe para a OSC que quer oferecer esse canal, não como uma exigência do sistema.

> ⚠️ **Atenção · Preenchido, o contato fica visível para qualquer pessoa**
>
> Quando você preenche esses campos e a **[página pública de transparência](/configuracoes/pagina-publica/)** da sua organização está no ar, o contato **aparece nela** — e a página é aberta, sem login. Por isso: use um **e-mail institucional da OSC** (por exemplo, `contato@suaosc.org.br` ou um endereço criado para esse fim), e evite o e-mail pessoal de um voluntário. A própria tela avisa isso antes de salvar. Se a página pública não está publicada, o contato não aparece — mas vale preencher já pensando em quando ela for ao ar.

> 📖 **Conceito · Não é o mesmo que o e-mail institucional**
>
> São campos diferentes, com finalidades diferentes, e um **não vira o outro automaticamente**. O **e-mail institucional** (lá em cima, na identidade da OSC) é o contato geral da organização, usado em documentos e relatórios. O **e-mail de proteção de dados** é o canal específico para pedidos sobre dados pessoais. Nada impede que sejam o mesmo endereço — mas isso é uma escolha sua, feita preenchendo os dois campos.

> 💡 **Por que isso existe**
>
> Quando alguém quer tratar de dados pessoais, o caminho depende de **quem decide sobre aquele dado**. Dado que a **sua organização** cadastrou — o cadastro de um fornecedor, os dados de um participante de projeto, um anexo — se resolve **com a organização**, porque é ela quem pode corrigir, incluir ou remover. Já dado de **conta e acesso** — e-mail de login, senha, registros de acesso — é com a **RIT**. Este campo é o que dá endereço à primeira dessas duas portas: sem ele, quem procura a sua OSC não sabe para onde escrever. O roteamento completo está na Política de Privacidade, em **[Com quem falar sobre seus dados](/privacidade/#10-com-quem-falar-sobre-seus-dados)**.

Quem edita esse bloco é quem já administra a organização — **não há permissão nova** nem papel novo envolvido.

## Exportar dados da organização (LGPD)

No fim da página, a seção **Exportação de dados da organização (LGPD)** permite ao admin **baixar todos os dados da OSC** em um único pacote — útil para guardar um backup, levar para outro sistema ou atender a uma solicitação de transparência.

[![Exportação e encerramento da organização](/assets/screenshots/config-organizacao-lgpd.png)](/assets/screenshots/config-organizacao-lgpd.png)
*Exportação de dados (LGPD) e zona de perigo para encerramento da organização*

- Clique em **Exportar dados da organização**. O pacote é um **ZIP** com uma planilha **Excel** (movimentações, reembolsos, pedidos de compra e pagamento, membros, categorias, centros de custo e configurações) mais **todos os anexos e comprovantes**.
- A geração roda **em segundo plano**. Você recebe um **e-mail com o link de download** (válido por **7 dias**) assim que o pacote fica pronto. O link só pode ser baixado por administradores da OSC.
- O último pacote gerado fica listado na própria seção, com a data e um botão para baixar enquanto o link estiver válido.

> 💡 **Por que isso importa**
>
> Poder exportar a base inteira a qualquer momento é uma garantia de **autonomia e transparência**: os dados são da sua OSC, não ficam reféns da plataforma. Serve de backup, ajuda numa eventual migração e responde de imediato a um pedido de prestação de contas ou auditoria.

## Encerrar organização

Ainda no fim da página, a **Zona de perigo · Encerrar organização** inicia o encerramento definitivo da OSC no RIT360 Financeiro. É uma ação séria e foi desenhada com calma para que ninguém perca dados por engano.

- O encerramento **bloqueia novas escritas imediatamente** — a partir dali ninguém lança, edita ou aprova nada na OSC.
- Você tem uma **janela de 30 dias** para exportar tudo o que precisar antes da eliminação (use a exportação acima).
- Após o prazo, **identificadores e anexos são apagados** e os **dados pessoais dos membros são anonimizados**. Por **obrigação legal**, os **registros financeiros e a trilha de auditoria são mantidos sem identificação pessoal**, e o **CNPJ é retido**.

> ⚠️ **Atenção · Encerrar é irreversível pelo autosserviço**
>
> Não há botão para "desfazer" um encerramento pela própria interface. Só recorra a essa opção quando a OSC realmente vai deixar de operar no RIT360 Financeiro. Em dúvida, **exporte os dados primeiro** e procure o suporte/DPO antes de confirmar.

## Por onde seguir

- **Configurações → Usuários** — para gerenciar membros da OSC.
- **Configurações → Contas Bancárias** — para cadastrar as contas que aparecem em Movimentações.
- **Movimentações → Importar Lançamentos** — onde a integração WooCommerce aparece como fonte ao lado do CSV.
- **[Configurações → Página pública](/configuracoes/pagina-publica/)** — onde o contato de proteção de dados aparece para o visitante, se estiver preenchido.
