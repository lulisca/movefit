# Projeto MoveFit — Plano de Go-live

**Referências:** Aula de Implantação e Go-live; Blocos A, C (item 7), D (item 6) e F do handoff
**Dependências:** Roadmap (05); Cronograma (06, C-29 a C-40); Riscos (08); Comunicação (13); Mudanças (14); Qualidade (15)

## 1. Estratégia

O go-live é feito em **piloto na Unidade Centro em 08/03/2027**, depois do pico de janeiro e fevereiro, como pediu o Henrique. A diretoria disse que "não pode parar a recepção" (Bloco A). Por isso:
- a virada acontece no fim de semana;
- existe ensaio de rollback e contingência manual;
- a operação é assistida por 5 dias úteis (Bloco C, item 7).

As demais unidades vêm depois, conforme o plano de expansão (C-38). O que cabe até 25/03 é o ponto 6.1 do Roadmap.

## 2. Linha do tempo

| Data | Etapa | Responsável |
|---|---|---|
| 22/02 a 03/03 | Treinamento (4 sessões de 2 h), checklist, contingência e ensaio de rollback | Paulo, Larissa, Igor |
| 26/02 | Entrega da E3 e início do congelamento de mudanças | Camila |
| 01 a 05/03 | Homologação da E3 | Juliana, Thiago, Carla |
| 05/03 (sexta) | **Go/No-Go** | Juliana, Camila |
| 06 e 07/03 | **Cutover** (carga final e virada) | Diego, Paulo, Igor |
| 08/03 (segunda) | **Go-live do piloto** | Paulo, Larissa, Diego |
| 08 a 12/03 | Operação assistida | Paulo, Larissa, Diego |
| 15 a 19/03 | Aceite do piloto (parcela 4) | Thiago, Juliana |
| 15 a 17/03 | Lições aprendidas | Camila, Lucas |
| 15 a 25/03 | Plano de expansão das demais unidades | Camila, Marina |
| 25/03 (quinta) | **Aceite final** (parcela 5) | Henrique |
| 26/03 a 24/04 | Garantia corretiva de 30 dias corridos (Bloco D, item 6) | Equipe WEBFLOW |
| Depois de 24/04 | Sustentação assistida, por contrato separado (Bloco A) | Fora do projeto |

## 3. Checklist de prontidão

Revisado em 03/03 e apresentado no Go/No-Go.

| # | Item | Prazo | Responsável | Parecer |
|---|---|---|---|---|
| 1 | E1, E2 e E3 homologadas | 05/03 | Juliana | Negócio |
| 2 | Zero defeitos críticos ou altos abertos | 05/03 | Larissa | QA |
| 3 | Carga de validação 2 conferida (alunos, planos e saldos) | 19/02 | Diego, Fernanda | QA |
| 4 | Pagar.me validado | 26/02 | Marina | TI |
| 5 | Catraca do Centro validada no equipamento real, ou acesso manual ensaiado (R-05) | 26/02 | Marina, Marcelo | TI |
| 6 | Janela de rede confirmada com o fornecedor (PR-07) | 12/02 | Marcelo | TI |
| 7 | PRD pronto, com backup e monitoramento | 03/03 | Igor | TI |
| 8 | Treinamento dos usuários-chave concluído | 03/03 | Paulo | Implantação |
| 9 | Ensaio de rollback aprovado | 03/03 | Paulo, Igor | Implantação |
| 10 | Usuários e perfis da equipe do Centro criados | 03/03 | Paulo, Thiago | Implantação |
| 11 | Alunos do Centro avisados da troca e do primeiro acesso ao portal | 03/03 | Juliana | Negócio |
| 12 | Escala da operação assistida confirmada (seção 7) | 03/03 | Camila | Implantação |

## 4. Reunião de Go/No-Go (05/03)

O piloto só é liberado com os **quatro pareceres**: TI (Marcelo), QA (Larissa), implantação (Paulo) e negócio (Juliana). Quem decide é a Juliana, com a Camila (RACI).

| Decisão | Quando | O que acontece |
|---|---|---|
| **Go** | Checklist completo | Cutover em 06 e 07/03 |
| **Go com ressalva** | Só pendências médias ou baixas, com contingência definida (ex.: acesso manual na catraca) | Cutover mantido; a ressalva fica na ata, com dono e prazo |
| **No-Go** | Defeito crítico ou alto aberto, migração sem conferência ou parecer negativo | O Centro segue no legado. Nova data vai para Henrique pelo Fluxo de Mudanças, porque não há folga até 26/03 |

## 5. Cutover (06 e 07/03)

| Quando | Passo | Responsável |
|---|---|---|
| Sábado 06/03, após o fechamento | Extração final do legado (alunos ativos, planos vigentes, saldos) e cópia de segurança | Diego, Marcelo |
| Sábado 06/03, à noite | Carga final no PRD | Diego, Igor |
| Domingo 07/03 | Conferência da carga com os números do legado | Diego, Larissa |
| Domingo 07/03 | Teste de fumaça: login, matrícula, reserva, cobrança e catraca | Larissa, Paulo |
| Domingo 07/03, fim do dia | **Ponto de não retorno:** Juliana e Camila confirmam a virada ou mandam voltar | Juliana, Camila |
| Segunda 08/03, 05h30 | Recepção abre no MoveFit, com suporte presencial | Paulo, Larissa |
| Segunda 08/03 | Lançar no MoveFit o que foi feito no legado no domingo | Carla, Paulo |

O legado fica disponível **só para consulta** durante a operação assistida, como contingência (combinar com o Marcelo).

## 6. Rollback e contingência

**Até o ponto de não retorno (domingo 07/03):** se a conferência ou o teste de fumaça falhar sem correção no fim de semana, o Centro abre segunda no legado, como se nada tivesse mudado. Esse procedimento é o que foi ensaiado em C-31.

**Depois da abertura de segunda:** a regra é contingência e correção, não rollback. Voltar ao legado só com decisão da Juliana e da Camila.

| Falha | Contingência | Quem aciona |
|---|---|---|
| Catraca não integra ou fica instável | Acesso manual: a recepção confere a situação do aluno no MoveFit e libera (R-05) | Thiago; Marina corrige |
| MoveFit fora do ar | Consulta no legado e registro em planilha; lançamento depois | Paulo; Igor corrige |
| Pagar.me fora do ar | Recebimento pelos meios atuais; baixa conferida depois com a Fernanda | Paulo; Diego corrige |
| Dado migrado errado | Correção pontual com conferência; se for em massa, Juliana e Camila decidem | Diego |

## 7. Operação assistida (08 a 12/03)

| Papel | Quem | Como |
|---|---|---|
| Suporte presencial na recepção do Centro | Paulo e Larissa, em revezamento | Na unidade, com foco na abertura e nos horários de mais movimento |
| Correções | Diego e Bruna | Plantão remoto |
| Infraestrutura e monitoramento | Igor | Plantão remoto |
| Catraca e Pagar.me | Marina, com Marcelo | Sob demanda |
| Lado do cliente | Thiago (diário) e Carla | Registram ocorrências para o Paulo |
| Comunicação | Paulo | Boletim diário a Juliana, Thiago e Camila |

O Paulo tem 8 h/semana e a frente de implantação já está em 141% da capacidade (Custos, seção 3). Por isso o revezamento com a Larissa e o pedido de horas extras da semana de 08/03 entram no relatório interno para o Eduardo Viana.

**Critérios para o aceite do piloto** (proposta nossa):
1. Nenhum defeito crítico ou alto aberto.
2. Recepção sem acionar contingência nos dois últimos dias da operação assistida.
3. Movimentações do domingo e correções da migração concluídas.
4. Pendências médias e baixas com dono e data.

## 8. Depois do piloto

1. **Aceite do piloto** por Thiago e Juliana até 19/03 (libera a parcela 4).
2. **Lições aprendidas** (15 a 17/03): o que mudar no treinamento, na carga e na contingência antes das outras unidades.
3. **Plano de expansão** (até 25/03): para cada unidade (Norte, Sul, Cambuí e Taquaral), catraca compatível (PB-31), carga dos dados da unidade, treinamento e data proposta.
4. **Aceite final** por Henrique em 25/03, com a documentação operacional entregue.
5. **Garantia** até 24/04/2027: corrige defeitos do que foi entregue e aceito. Evolução e regra nova vão para mudança ou sustentação.

## 9. Pontos para o grupo decidir

1. **Carga final só do Centro ou das 5 unidades?** A proposta técnica prevê uma carga final. Se for só o Centro, cada unidade precisa de carga própria na expansão, o que vai para o plano de expansão e pode virar mudança.
2. **Testes técnicos da E3.** O Cronograma não tem atividade de testes técnicos da E3 antes da homologação (C-32). Este plano usa 22 a 26/02 com a Larissa.
3. **Horas do Paulo na operação assistida.** Avaliar um risco novo no registro, junto do R-21.

## 10. Rastreabilidade

| Origem | Uso neste plano |
|---|---|
| Bloco A ("não pode parar a recepção") | Cutover no fim de semana, rollback e contingência |
| Bloco C, item 7 | 4 sessões de treinamento e 5 dias úteis de operação assistida |
| Bloco D, item 6 | Garantia de 30 dias corridos |
| Cronograma C-29 a C-40 | Datas do Go/No-Go, cutover, operação assistida e aceites |
| RACI (03) | Go/No-Go com quatro pareceres; decisão da Juliana com a Camila |
| Riscos R-05, R-15, R-16, R-17 | Catraca, falta de folga, recepção na virada e defeitos no Go/No-Go |
