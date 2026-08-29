---
title: "Meu Perfil"
nav_order: 8
permalink: /configuracoes/perfil/
---

A página **Meu Perfil** concentra **seus** dados pessoais e preferências dentro do RIT360 Financeiro — não os dados da organização. Disponível para todos os usuários autenticados, acessada pelo menu do avatar (canto superior direito → **Meu perfil**) ou diretamente pela rota `/perfil`.

[![Página Meu Perfil](/assets/screenshots/config-perfil.png)](/assets/screenshots/config-perfil.png)
*Página Meu Perfil — boxes consolidados de dados e preferências*

> 💡 **Por que isso importa**
>
> Perfil bem configurado tem dois efeitos práticos: (1) **reembolsos mais rápidos** porque a chave PIX/TED já vem pré-preenchida; (2) **menos ruído no dia a dia** porque você só recebe as notificações que importam para você, nos canais que prefere. 5 minutos de configuração inicial economizam horas ao longo dos meses.

A página tem cinco boxes consolidados: **Identificação**, **Dados para Reembolso**, **Notificações**, **Meus dados (LGPD)** e **Ações de Conta**.

## Identificação

- **Foto de perfil** — JPG, PNG ou WebP, até 2 MB. A imagem é redimensionada para 512×512 antes do envio.
- **Nome completo** — como aparece em audit logs, aprovações, registros.
- **Telefone** — o campo tem um **seletor de país** ao lado, com **Brasil já selecionado por padrão**; escolha outro país quando precisar. A máscara é única e uniforme — números brasileiros seguem o formato de sempre `(DDD) 9XXXX-XXXX` — e, ao abrir um cadastro salvo, o país é **reconhecido automaticamente** pelo número.
- **Data de nascimento** — opcional.
- **CPF** e **RG / RNE** — opcionais; o **CPF** é formatado automaticamente (`000.000.000-00`). O campo de documento se chama **"RG / RNE"** porque quem é estrangeiro pode informar o **RNE** (Registro Nacional de Estrangeiro) no mesmo lugar. Armazenados **cifrados em repouso** (chave de criptografia gerenciada separadamente do banco). Usados apenas para emissão de comprovantes quando exigido por lei.

[![Campo Telefone com seletor de país](/assets/screenshots/config-perfil-telefone-pais.png)](/assets/screenshots/config-perfil-telefone-pais.png)
*O campo Telefone com o seletor de país (Brasil por padrão).*
Botão **Salvar alterações** ao final do box salva tudo de uma vez.

> ⚠️ **Atenção · CPF e RG são dados sensíveis pela LGPD**
>
> Você só precisa preencher CPF/RG se a sua OSC vai emitir documento que exija (recibo formal, declaração para imposto de renda, etc.). Se você não tem certeza se precisa, deixe em branco — o RIT360 Financeiro não exige esses dados para operar.

## Dados para Reembolso

Configure aqui sua **chave PIX** ou **dados bancários para TED**. Quando você criar um Reembolso, o RIT360 Financeiro preenche automaticamente esses dados — você não precisa redigitar a cada solicitação, e não corre risco de errar a chave.

> ✓ **Dica · Use chave PIX preferencialmente**
>
> PIX simplifica a vida do tesoureiro: pagamento imediato, sem custo, sem necessidade de TED programada. Se sua conta tem chave PIX configurada, use-a aqui em vez dos dados bancários completos. A OSC paga mais rápido, você recebe mais rápido.

Se você nunca pede reembolso, pode deixar em branco — só preencha quando for fazer a primeira solicitação.

## Notificações

Quatro grupos de configuração:

### Canais de notificação

O RIT360 Financeiro tem três canais de notificação: **E-mail**, **Push** e **Telegram**. E-mail é o canal default — sempre disponível, sem configuração adicional. Push é ativado por dispositivo (veja abaixo). Telegram é vinculado uma vez à sua conta e passa a valer em qualquer dispositivo onde você tenha o Telegram instalado.

### Push (avisos no celular ou no navegador)

A partir da versão **v0.19.0**, **Push** é o segundo canal de notificações, ao lado do E-mail. Funciona como aviso de banco: você recebe um alerta na tela mesmo com o RIT360 Financeiro fechado, toca, e abre direto na tela relevante (reembolso aprovado, pedido pendente de seu voto, etc.).

A ativação é **por dispositivo**, com um interruptor mestre **"Ativar push neste dispositivo"** logo acima da matriz. Pode ativar no celular pessoal e desativar no do trabalho sem afetar a configuração da sua conta — cada dispositivo é independente.

**Como ativar:**

1. Toque (ou clique) no interruptor **"Ativar push neste dispositivo"**.
2. O navegador vai pedir permissão para enviar notificações — autorize.
3. Pelos toggles da matriz logo abaixo, defina quais eventos quer receber por push neste device.

**Requisitos por plataforma:**

- **Android (Chrome / Edge / outro navegador moderno):** funciona direto, sem precisar instalar. Apenas autorize quando perguntar.
- **iOS (Safari):** push só funciona se o RIT360 Financeiro estiver **instalado como app** na sua tela de início. Sem isso, o iOS não permite push e o interruptor fica desabilitado com instrução. Veja **[Instalar como app](/instalar-como-app/)** se ainda não fez.
- **Desktop (Chrome / Firefox / Edge):** funciona como no celular. Útil para receber avisos quando você está com outro aplicativo em primeiro plano.

**Múltiplas OSCs:** se você participa de mais de uma OSC, recebe push de eventos de todas. A OSC aparece no corpo do aviso para identificação da origem.

> 🔒 **Privacidade**
>
> O endpoint do seu dispositivo é armazenado da mesma forma que outros dados de contato. Você pode desativar a qualquer momento no master switch ou pedir exclusão completa pelo fluxo LGPD em **Ações de Conta**.

### Telegram (avisos direto no seu Telegram)

A partir da versão **v1.69.0**, **Telegram** é o terceiro canal de notificações, ao lado do E-mail e do Push. É pensado para quem já usa Telegram no dia a dia e não quer depender de abrir o e-mail ou o navegador para saber que um reembolso foi aprovado ou que um pedido está esperando seu voto.

<!-- CAPTURA PENDENTE: cartão "Telegram" em Meu Perfil → Notificações, estado NÃO vinculado (botão para gerar o link de vínculo). Rota /perfil, viewport desktop e mobile. Sessão de teste (OSC Alpha) caiu para a tela de login no momento desta redação — captura fica para quando o Bruno confirmar sessão autenticada. -->

**Como vincular:**

1. Em **Meu Perfil**, encontre o cartão **Telegram**, dentro de Notificações.
2. Clique para vincular. O RIT360 Financeiro gera um **link com um código de uso único, válido por 15 minutos**.
3. O link abre a conversa com o bot **@rit360financeiro_bot** no Telegram.
4. Toque em **Iniciar** (o botão pode aparecer como **Start**, dependendo do idioma do seu Telegram). O vínculo se completa sozinho, sem mais nenhum passo.
5. A partir daí, os avisos que você já recebia por e-mail passam a valer também no Telegram — e você ajusta evento a evento, em cada canal, na **matriz de preferências** logo abaixo.

Pode **desvincular** quando quiser, pelo mesmo cartão. Desvincular **apaga o contato guardado** — para voltar a receber no Telegram depois, é preciso vincular de novo, com um link novo.

> ⚠️ **Atenção · O código expira em 15 minutos**
>
> Se você demorar para tocar em Iniciar, o bot avisa que o código venceu — não é erro, e a tela de perfil permite gerar quantos links precisar. Cada link vale **uma vez só**: depois de usado (ou vencido), gere outro.

> ⚠️ **Atenção · O bot não responde perguntas**
>
> O **@rit360financeiro_bot** só entrega avisos — ele não é um canal de suporte e não interpreta mensagens que você mandar para ele. Dúvida ou problema se resolve dentro do próprio RIT360 Financeiro, não pelo Telegram.

> 📖 **Conceito · Vincular não liga tudo automaticamente para sempre**
>
> Vincular o Telegram não significa que toda notificação passa a chegar por lá. Você escolhe o que recebe em cada canal, evento por evento, na matriz de preferências — o Telegram entra com a mesma seleção que você já tinha no e-mail, e dali em diante os três canais são independentes.

> 🔒 **Privacidade**
>
> Seu identificador do Telegram é armazenado da mesma forma que outros dados de contato. Desvincular remove esse contato guardado; para exclusão completa dos seus dados, use o fluxo LGPD em **Ações de Conta**.

### Matriz granular de preferências

Tabela que cruza **eventos × 3 canais** (E-mail, Push e Telegram) e permite controle fino sobre quais notificações receber e por onde. Os eventos estão agrupados por área:

- **Reembolsos** (5): submetido, aprovação parcial, aprovado, rejeitado, pago.
- **Pedidos de Compra e Pagamento** (5): submetido, aprovação parcial, aprovado, rejeitado, pago.
- **Feedback** (2): novo feedback enviado, feedback resolvido.
- **Projetos**: comentários no mural, hora de publicar status, marcos atingidos ou perdidos, riscos materializados, tarefas atribuídas ou vencendo, resumo diário, e as aprovações de abertura/alteração e seus resultados.

Para cada par (evento, canal), um switch on/off. **Default é tudo ligado** — você silencia o que não quer receber.

> 📖 **Conceito · Canal desabilitado vs canal não cadastrado**
>
> Se a coluna **Push** aparece **desabilitada** com tooltip ("Ative push neste dispositivo"), é porque você ainda não cumpriu o pré-requisito do canal. Cumpra-o e salve — na próxima abertura da página, a coluna fica habilitada para escolher quais eventos receber por esse canal.

> ✓ **Dica · Calibre por papel**
>
> Se você é aprovador, mantenha "submetido" ligado para ser avisado quando um reembolso/pedido precisa do seu voto. Se você é solicitante e não aprovador, "submetido" não te interessa — pode desligar e manter só "aprovado", "rejeitado" e "pago". Tesoureiro deve manter "aprovado" e "pago" sempre ligados para acompanhar o ciclo de pagamento.

## Meus dados (LGPD)

Você pode **baixar uma cópia dos seus dados pessoais** no RIT360 Financeiro a qualquer momento — é o seu direito de acesso e portabilidade previsto na LGPD.

[![Meus dados (LGPD) e ações de conta](/assets/screenshots/config-perfil-lgpd.png)](/assets/screenshots/config-perfil-lgpd.png)
*Box "Meus dados (LGPD)" para baixar seus dados, e box "Ações de conta"*

- Clique em **Baixar meus dados**. O pacote é um arquivo **JSON** com seu perfil, preferências, consentimentos, vínculos com organizações e as referências dos registros que você criou.
- A geração roda **em segundo plano**. Você recebe um **e-mail com o link de download** (válido por **7 dias**) assim que o pacote fica pronto. O último pedido fica listado na seção, pronto para baixar enquanto o link estiver válido.

## Ações de Conta

Ações administrativas sobre sua própria conta, cada uma com botão independente:

- **Alterar senha** — campos de nova senha e confirmação; clique em "Alterar senha" para confirmar. Senha forte (8+ caracteres, mix de letras, números e símbolos) é exigida.
- **Alterar e-mail de acesso** — troca o e-mail com o qual você entra no sistema (self-service). Veja o passo a passo logo abaixo.
- **Encerrar todas as sessões** — desconecta sua conta de todos os dispositivos onde está logada. Útil se você perdeu acesso a um celular ou suspeita de uso indevido.
- **Excluir minha conta (LGPD)** — exerce o **direito ao esquecimento**. Ao confirmar, sua conta entra em uma **carência de 30 dias**; passado o prazo, seus dados pessoais (nome, e-mail, telefone, CPF, RG, avatar) são **anonimizados de forma irreversível**. Por obrigação legal, **registros financeiros e de auditoria são retidos por 5 anos sem identificação pessoal**.

### Como trocar o e-mail de login

[![Alterar e-mail de acesso — Meu Perfil](/assets/screenshots/config-perfil-alterar-email.png)](/assets/screenshots/config-perfil-alterar-email.png)
*Box "Alterar e-mail de acesso" dentro de Ações de Conta*

É com esse e-mail que você entra no RIT360 Financeiro — diferente do e-mail de contato, do e-mail para reembolso ou de qualquer outro dado do perfil.

1. Em **Ações de Conta**, no bloco **Alterar e-mail de acesso**, digite o **novo e-mail** e **confirme** repetindo no segundo campo.
2. Clique em **Enviar link de confirmação**.
3. Abra a caixa de entrada do **novo endereço** e clique no link recebido. **Só depois desse clique** o e-mail de login realmente muda — até lá, você continua entrando com o e-mail atual normalmente.
4. O **e-mail antigo** recebe um aviso informando que a troca foi solicitada, como camada extra de segurança caso você não tenha sido quem pediu.

Enquanto a confirmação está pendente, é possível **cancelar o pedido** e manter o e-mail atual — não é preciso esperar o link expirar.

> 📖 **Conceito · Por que confirmar no novo e-mail, não no atual**
>
> Se a confirmação fosse no e-mail atual, alguém com acesso à sua sessão (mas não à sua caixa de entrada) poderia trocar seu e-mail de login sem você perceber. Exigir o clique no **novo** endereço garante que só quem realmente tem acesso a essa caixa de entrada consegue efetivar a troca.

> ✓ **Funciona com login pelo Google**
>
> Se você entra no RIT360 Financeiro pela sua conta Google, o fluxo é o mesmo — sem pedir senha atual (você não tem uma senha cadastrada no sistema nesse caso). Depois de confirmar, o login passa a ser feito pelo novo e-mail.

### Como excluir a conta

[![Confirmação de exclusão da conta](/assets/screenshots/config-perfil-excluir.png)](/assets/screenshots/config-perfil-excluir.png)
*Confirmação de exclusão — exige a senha atual e digitar "EXCLUIR"*

Por ser uma ação séria, a confirmação pede duas coisas: **sua senha atual** e digitar a palavra **EXCLUIR**. Ao confirmar, você é **desconectado de todos os dispositivos** e **não consegue mais entrar**. Dentro da janela de 30 dias, a **reativação** só é possível pelo DPO (`dpo@rit.org.br`) — não há autosserviço para reativar.

> ⚠️ **Atenção · Encerrar sessões te desconecta também**
>
> "Encerrar todas as sessões" inclui o navegador atual. Você vai precisar fazer login de novo. Útil principalmente em situação de risco (perdeu celular, suspeita de acesso indevido). Em uso normal, não há motivo para usar.

## Por onde seguir

- **Reembolsos** — onde os dados de reembolso configurados aqui são usados automaticamente.
- **Configurações → Usuários** — para o admin gerenciar acesso de outros membros.
