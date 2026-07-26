---
title: "Usuários"
nav_order: 2
parent: "Configurações da Organização"
permalink: /configuracoes/usuarios/
---

> Disponível para **Presidente (admin)**.

A página **Usuários** é onde você gerencia quem tem acesso à sua OSC dentro do RIT360 Financeiro — convidar novos membros, alterar papéis, suspender acessos.

[![Configurações — Usuários](/assets/screenshots/manual-09b-config-usuarios.png)](/assets/screenshots/manual-09b-config-usuarios.png)
*Configurações — Gerenciamento de usuários*

> 💡 **Por que isso importa**
>
> A pessoa errada com permissão errada é o caminho mais curto para um problema sério em OSC. Acesso administrativo dado para alguém que não devia, papel de aprovador para quem não tem mandato, voluntário recém-saído que ainda tem acesso meses depois — todos os casos derivam de gestão de usuários frouxa. Esta página é o ponto onde você mantém **quem entra, quem sai e quem pode o quê**.

Listagem traz todos os membros da OSC com nome, e-mail, papel, status (ativo/pendente/inativo) e foto de perfil.

## Adicionar usuário

Clique em **+ Adicionar usuário**. Informe o **e-mail** e o **papel** desejado. A tela **responde na hora**, assim que o cadastro é salvo — o e-mail de convite com o link de primeiro acesso é enviado em segundo plano. O status do usuário fica como "Pendente" até ele aceitar. Se o envio do e-mail falhar, o registro da falha fica guardado e o convite pode ser **reenviado** normalmente (ver Ações por membro).

> 📖 **Conceito · Convite vs acesso direto**
>
> O RIT360 Financeiro usa **convite por e-mail** como mecanismo de entrada, não cadastro aberto. Isso protege a OSC de spam, garante que a pessoa convidada confirma o acesso pelo próprio e-mail, e permite mensagem personalizada no convite. O convite tem prazo de validade — se expirar, o admin pode reenviar pelo mesmo fluxo.

> 📖 **Conceito · Já dá para designar quem ainda não ativou o acesso**
>
> Um membro recém-cadastrado, que ainda não concluiu o primeiro acesso (não definiu a senha), **já pode ser escolhido** como **gestor de centro de custo**, **coordenador ou integrante de projeto** e **aprovador** (de reembolso, pedido de pagamento, orçamento e projeto) — sem esperar ele entrar no sistema pela primeira vez. Nessas listas o nome aparece com a marca discreta **"· acesso pendente"**. A permissão para *agir* (aprovar, coordenar, operar) continua valendo **só depois** que a pessoa ativa o acesso.

## Importar usuários em lote (planilha CSV)

[![Importar usuários — tela de upload](/assets/screenshots/manual-config-usuarios-importar.png)](/assets/screenshots/manual-config-usuarios-importar.png)
*Importar usuários — instruções, download do template e área de upload*

Para OSCs que estão migrando de outro sistema ou que precisam cadastrar muitos membros de uma vez, há a opção **Importar usuários** ao lado de "Adicionar usuário". O fluxo é o mesmo padrão do importador de movimentações.

1. Clique em **Importar usuários** → abre uma tela dedicada.
2. **Baixe o template** CSV. O arquivo já vem com o cabeçalho correto e algumas linhas de exemplo.
3. Preencha sua planilha. Campos **obrigatórios**: nome completo, e-mail e papel. **Opcionais**: telefone, data de nascimento, CPF, RG.
4. Faça **upload** do arquivo. O RIT360 Financeiro mostra uma **pré-visualização** com cada linha classificada por status:
   - **Novo** — vai receber e-mail para definir a senha de acesso
   - **Já cadastrado** — usuário existente em outra OSC; cria vínculo direto sem novo acesso
   - **Vínculo ativo na OSC** — usuário que já é membro; perfil pode ser atualizado (campos vazios apenas)
   - **Com erro** — linha que será pulada (motivo explícito ao lado)

   [![Importar usuários — pré-visualização com linhas classificadas](/assets/screenshots/manual-config-usuarios-importar-preview.png)](/assets/screenshots/manual-config-usuarios-importar-preview.png)
   *Pré-visualização — cada linha classificada por status (novo, já cadastrado, vínculo ativo, com erro)*

5. Clique em **Importar**. A importação **começa a rodar em segundo plano** e a tela é liberada na hora — você não precisa esperar com o navegador aberto. Aparece a mensagem **"Importação iniciada — avisaremos quando concluir"** e você pode seguir usando o app normalmente.

   [![Importação iniciada — processando em segundo plano](/assets/screenshots/manual-config-usuarios-importacao-iniciada.png)](/assets/screenshots/manual-config-usuarios-importacao-iniciada.png)
   *Ao confirmar, a importação começa em segundo plano e a tela é liberada*

> 📖 **Conceito · Por que a importação roda em segundo plano**
>
> Cadastrar muitos membros de uma vez (dezenas ou centenas) envolve criar cada acesso e disparar cada e-mail — o que leva tempo. Fazer tudo "na frente" travava a tela e, em planilhas grandes, chegava a **falhar por demora**. Agora o sistema recebe sua planilha, confirma na hora e faz o trabalho pesado por trás; ao terminar, ele te avisa. Você importa 5 ou 500 membros sem diferença na sua espera.

### Aviso de conclusão

Quando a importação termina, quem importou recebe um **e-mail e uma notificação** com o resumo: quantos foram convidados, quantos ficaram com **e-mail pendente**, quantos foram **vinculados**, quantos **perfis foram atualizados** e quantas linhas tiveram **erro**.

[![E-mail de conclusão da importação com o resumo](/assets/screenshots/manual-config-usuarios-importacao-email.png)](/assets/screenshots/manual-config-usuarios-importacao-email.png)
*E-mail de conclusão — resumo do que foi processado, criado, vinculado, atualizado e pulado*

Se alguma linha deu erro, o aviso é **acionável**: ele lista o **número da linha**, o **nome ou e-mail** e o **motivo** (ex.: *"Linha 5 (joao@exemplo.org): CPF deve ter 11 dígitos"*), para você corrigir na planilha e reimportar **apenas as linhas que faltaram**. Por segurança, o aviso nunca traz CPF nem RG no corpo — esses dados ficam só no arquivo completo, protegido por login (ver Histórico abaixo).

### Histórico de importações

A tela de importação tem uma aba **Histórico** que lista todas as importações já feitas na sua OSC, com **data**, **quem importou**, **progresso**, **totais** e **status**:

- **Na fila** — recebida, aguardando processamento
- **Processando** — rodando em segundo plano
- **Concluída** — terminou (com ou sem linhas puladas)
- **Falhou** — foi interrompida (o aviso explica o que aconteceu)

Em cada importação com erros, você pode **baixar a planilha completa das linhas que falharam** — com todos os motivos — para corrigir e reimportar só o que faltou. Esse arquivo fica disponível apenas aqui, atrás de login, porque pode conter CPF/RG.

[![Importar usuários — aba Histórico com uma importação concluída](/assets/screenshots/manual-config-usuarios-importar-historico.png)](/assets/screenshots/manual-config-usuarios-importar-historico.png)
*Aba Histórico — importações da OSC com data, solicitante, totais, status e download da planilha de erros*

> 💡 **Se a planilha tiver um problema de formato**
>
> Se faltar uma coluna obrigatória (por exemplo, "papel") ou o arquivo passar do tamanho máximo, o sistema mostra **exatamente o que está errado** já no upload — não uma mensagem técnica genérica. Ajuste a planilha conforme a indicação e tente de novo.

> 📖 **Conceito · Upsert seletivo**
>
> Quando o e-mail da planilha já existe na sua OSC, o RIT360 Financeiro **só preenche os campos que estão vazios** no perfil atual. Nenhum dado existente é substituído. Útil para migrações onde você importa dados de uma planilha mestre sem o risco de sobrescrever informações que o membro já cadastrou no próprio perfil.

> ⚠️ **Atenção · Multi-papel não entra via planilha**
>
> Cada linha do CSV atribui exatamente um papel. Se o membro precisar acumular papéis (ex: Coordenador de Projeto + Comissão Fiscal), use o botão **Editar papéis** no menu de ações depois da importação. Isso é decisão pra evitar erros de digitação em CSV grande.

> ⚠️ **Atenção · Dados de pagamento (PIX/conta) não vêm no CSV**
>
> Por segurança e simplicidade, a planilha não importa dados de PIX, banco ou conta. Cada membro preenche isso depois no próprio perfil, em **Configurações → Perfil** (acessível por qualquer usuário). Mantém esse dado fora da planilha que circula entre administradores.

> ⚠️ **Atenção · Senha não vem no CSV**
>
> O fluxo é igual ao convite individual: para cada e-mail novo, o RIT360 Financeiro envia link de setup por e-mail. O usuário define a própria senha ao clicar no link. Admin nunca digita nem vê a senha de outro membro.

## Ações por membro

Cada linha tem menu de ações que muda conforme o status:

- **Editar papéis** — abre painel lateral com checkboxes para os papéis disponíveis (Presidente, Tesoureiro, Diretor, Coordenador de Projeto, Comissão Fiscal e Voluntário). Um usuário pode ter mais de um papel ao mesmo tempo — ver [Papéis e Permissões](/papeis/) para a regra de combinações.

  [![Editar papéis — painel multi-select](/assets/screenshots/manual-config-usuarios-editar-papeis.png)](/assets/screenshots/manual-config-usuarios-editar-papeis.png)
  *Editor de papéis — marque os papéis desejados; combinações proibidas ficam visualmente desabilitadas*

- **Desativar acesso** — bloqueia entrada sem excluir histórico
- **Reativar acesso** — restaura entrada de quem estava desativado
- **Cancelar convite pendente** — remove convite que ainda não foi aceito
- **Reenviar convite** — re-dispara o e-mail de convite (útil quando o destinatário não recebeu ou o link expirou)

> ⚠️ **Atenção · Mudança de papel deve ser deliberada**
>
> Promover alguém para Tesoureiro dá acesso à aprovação de despesas. Conversão entre papéis com poder financeiro deve passar pela diretoria, não ser ação unilateral do presidente. Em OSC com estatuto formal, pode até exigir ata de assembleia ou eleição. O sistema não bloqueia a mudança, mas registra tudo no audit log com data, autor e papéis anterior/novo.

> ⚠️ **Atenção · Desativar ≠ excluir**
>
> Desativar bloqueia entrada mas **preserva todo o histórico** (lançamentos criados, aprovações dadas, comentários escritos). Para auditoria e prestação de contas, isso é essencial — você consegue mostrar quem fez o quê mesmo depois que a pessoa saiu. O RIT360 Financeiro não tem opção de "excluir usuário"; só "desativar" + histórico preservado. Quem deixou a OSC: desative.

## Solicitações pendentes

Em OSCs com **acesso público ao link de vínculo** ativado (em Configurações → Organização), pessoas externas podem pedir entrada espontaneamente. As solicitações pendentes aparecem em uma seção separada, com botão **Aprovar** ou **Rejeitar**. Aprovar gera o convite formal; rejeitar nega o acesso sem criar conta.

## Foto de perfil dos membros

A lista mostra a foto de cada membro (configurada por cada um no Meu Perfil). Caso a pessoa não tenha foto, aparece um avatar com as iniciais do nome.

## Por onde seguir

- **Papéis e Permissões** — para entender o que cada papel pode fazer antes de atribuir.
- **Configurações → Fluxo de Aprovações** — para definir quais papéis aprovam e quem é aprovador individual.
- **Configurações → Organização** — para controlar o acesso público de vínculo.
