---
title: "Comissão Fiscal"
nav_order: 6
parent: "Configurações da Organização"
permalink: /configuracoes/comissao-fiscal/
---

> Disponível exclusivamente para **Presidente (admin)**.

A página **Comissão Fiscal** define os parâmetros estatutários, a vigência dos mandatos e as regras de votação do Conselho Fiscal da OSC.

[![Configurações — Comissão Fiscal](/assets/screenshots/config-comissao-fiscal.png)](/assets/screenshots/config-comissao-fiscal.png)
*Configurações da Organização — Parâmetros, quórum e mandatos da Comissão Fiscal*

> 💡 **Por que isso importa**
>
> Em Organizações da Sociedade Civil (OSCs), a Comissão Fiscal (ou Conselho Fiscal) é a principal instância de controle independente da governança. Ela não administra o dinheiro no dia a dia, mas responde perante a Assembleia Geral, os associados, o Ministério Público e os financiadores sobre a regularidade das contas. 
>
> Cada OSC possui regras próprias em seu Estatuto Social: periodicidade das contas (anual, semestral ou mensal), número de conselheiros, critérios de quórum e forma de desempate. **Configurar essa tela corretamente é o que garante que a fiscalização eletrônica no RIT360 tenha pleno respaldo estatutário e jurídico.**

> 🔒 **Segregação de funções e prevenção de conflito de interesses**
>
> Esta tela de configuração é **bloqueada para Tesoureiros e Gestores Financeiros**. Apenas o Presidente da OSC tem permissão para cadastrar ou alterar as regras da comissão fiscal. Quem executa a despesa e elabora as contas não pode definir as regras que regem sua própria fiscalização.

---

## 1. Parâmetros Gerais e Periodicidade

A seção superior da página define como os períodos de fiscalização são estruturados:

| Campo | O que define | Opções disponíveis |
|---|---|---|
| **Periodicidade** | A frequência oficial com que as contas devem ser submetidas ao parecer do Conselho Fiscal, conforme o estatuto. | **Anual** (padrão na maioria das OSCs), **Semestral**, **Quadrimestral**, **Trimestral** ou **Mensal**. |
| **Abertura de Períodos** | Como os ciclos de fiscalização são iniciados no sistema. | • **Manual**: O Presidente ou a Comissão abre o período quando a escrituração contábil e a conciliação estiverem prontas.<br>• **Automática**: O sistema abre o período automaticamente ao final de cada exercício/mês. |
| **Antecedência para Alerta** | Quantos dias antes da data limite da assembleia o sistema começa a alertar os conselheiros sobre pendências. | 15, 30, 45 ou 60 dias. |

> ⚠️ **Armadilha · Abrir período com lançamentos pendentes de conciliação**
>
> Se a sua OSC optar por abertura **Manual**, nunca abra o período fiscal enquanto o tesoureiro ainda estiver importando extratos ou caçando diferenças. Uma vez aberto para análise, os conselheiros começam a emitir atestes. Se lançamentos forem alterados no meio da fiscalização, atestes já concedidos podem perder a validade ou gerar inconsistências no relatório final.

---

## 2. Quórum e Regras de Deliberação

O Estatuto Social da sua organização estabelece como o colegiado fiscal decide e o que acontece quando há discordância. O RIT360 permite refletir com precisão essas normas:

### Tipo de Quórum
- **Maioria Simples dos Votantes**: Aprova se o número de votos favoráveis for superior aos votos contrários entre os conselheiros que participaram da votação.
- **Maioria Absoluta do Conselho**: Exige que mais da metade da totalidade dos membros titulares vote favoravelmente (ex.: em um conselho de 3 membros, exige ao menos 2 votos favoráveis, mesmo que um membro esteja ausente).
- **Unanimidade**: Exige concordância de 100% dos membros votantes para emissão de parecer favorável.

### Critério de Desempate
Quando a votação empata (comum em conselhos com número par de votantes ou em caso de abstenções):
1. **Restritivo (Recomendado / Prudência)**: Em caso de empate, a deliberação é considerada **desfavorável** (ou favorável com ressalvas, se as divergências forem saneáveis). O princípio da prudência orçamentária estabelece que dúvida relevante não autoriza aprovação tácita.
2. **Voto de Minerva (Voto de Qualidade)**: O Presidente da Comissão Fiscal detém o voto decisivo para desempatar o julgamento.

### Modalidade de Voto
- **Voto Nominal (Identificado)**: Cada voto, justificativa e ressalva é associado nominalmente ao conselheiro no parecer final e no caderno de fiscalização. Altamente recomendado para transparência perante doadores e órgãos de auditoria.
- **Voto Colegiado (Consolidado)**: O sistema registra os votos individuais internamente para cômputo do quórum, mas o documento emitido apresenta a decisão como deliberação única do órgão colegiado.

---

## 3. Prazos do Rito e Diligências

Durante o processo de fiscalização, os conselheiros podem identificar documentos ausentes, notas com descrição genérica ou lançamentos não conciliados. O sistema permite estruturar esse diálogo formal por meio de **Diligências**:

- **Prazo para Solicitação de Diligências**: Quantidade de dias úteis que a comissão tem para formular pedidos de esclarecimento após a abertura do período.
- **Prazo de Resposta da Diretoria / Tesouraria**: Prazo (em dias úteis) para que o tesoureiro responda ao questionamento, anexe novos documentos ou regularize a pendência.
- **Prazo Final para Deliberação**: Prazo para emissão do parecer conclusivo após o encerramento do prazo de diligências.

> 💡 **Prazos em dias úteis**
>
> Todos os prazos de diligências no RIT360 Financeiro são computados em **dias úteis**, excluindo finais de semana e feriados nacionais, garantindo tempo hábil para que voluntários e dirigentes possam responder sem prejuízo de prazos estatutários.

---

## 4. Cadastro de Mandatos e Membros da Comissão

No bloco inferior da tela, você cadastra a composição oficial da comissão fiscal conforme a **Ata de Eleição e Posse**:

[![Cadastro de Mandato da Comissão](/assets/screenshots/config-comissao-fiscal.png)](/assets/screenshots/config-comissao-fiscal.png)

### Campos do Mandato
1. **Membro / Usuário**: Selecione o usuário cadastrado na OSC. Se o conselheiro ainda não estiver na lista, convide-o primeiro em [Configurações → Usuários](/configuracoes/usuarios/).
2. **Cargo no Colegiado**:
   - **Presidente da Comissão**: Conduz os trabalhos, distribui relatorias, formaliza diligências em nome do colegiado e assina o parecer conclusivo.
   - **Membro Titular**: Participa de todas as análises, atesta comprovantes e tem direito a voto na deliberação final.
   - **Membro Suplente**: Acompanha a fiscalização em modo consulta e pode ser convocado a votar em caso de vacância, ausência justificada ou impedimento de titular.
3. **Direito a Voto**: Define se o membro entra no cômputo do quórum deliberativo.
4. **Vigência do Mandato**: Data de início e data de término do mandato (conforme registrado no cartório de títulos e documentos).
5. **Número / Registro da Ata de Posse**: Identificação do livro e folha da ata de posse registrada em cartório, vinculando a legitimidade do conselheiro ao documento público.

---

## Armadilhas Comuns e Como Evitar

> ⚠️ **Mandato vencido no dia da deliberação**
>
> **O que acontece:** Se o mandato cadastrado estiver com data de término ultrapassada, o sistema bloqueia a assinatura do parecer pelo conselheiro para proteger a OSC contra vícios de representação jurídica.
>
> **Como evitar:** Mantenha os mandatos atualizados assim que a nova assembleia geral eleger a comissão. Se a assembleia prorrogou o mandato anterior até a posse dos novos membros, atualize a data de vigência nesta tela.

> ⚠️ **Conselheiro com papel incompatível na mesma OSC**
>
> **O que acontece:** O sistema impede que a mesma pessoa acumule o papel de **Comissão Fiscal** com **Presidente** ou **Tesoureiro**. 
>
> **Por quê:** O artigo 54 do Código Civil e os princípios de governança do terceiro setor vedam expressamente que quem ordena ou executa despesas fiscalize a si mesmo. Se um membro assumir a tesouraria, seu mandato na comissão fiscal deve ser finalizado imediatamente.

---

## Glossário de Termos Estatutários

- **Conselho Fiscal / Comissão Fiscal**: Órgão de assessoramento e controle interno da OSC, encarregado de examinar livros contábeis, extratos e comprovantes e emitir parecer anual à Assembleia Geral.
- **Mandato**: Período de investidura oficial no cargo eletivo, delimitado por datas de início e fim averbadas em cartório.
- **Quórum de Instalação**: Número mínimo de conselheiros necessários para iniciar os trabalhos de conferência.
- **Quórum de Deliberação**: Número de votos concordantes necessários para aprovar ou rejeitar a prestação de contas.
- **Voto de Minerva**: Prerrogativa do Presidente do conselho para desatar empates em votações colegiadas.
- **Diligência**: Procedimento oficial pelo qual a comissão solicita esclarecimentos, notas explicativas ou segundas vias de comprovantes antes de concluir seu julgamento.
