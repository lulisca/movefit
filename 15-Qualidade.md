# Projeto MoveFit — Plano de Qualidade

**Referências:** Aula de Gestão da Qualidade; Bloco C do handoff (itens 4, 5 e 6); Bloco D (item 5, Aceite e Homologação)
**Dependências:** Backlog; Roadmap (05); Cronograma (06); Custos (07); Riscos (08)

## 1. Objetivo

Definir como cada entrega é testada e aceita, para que nenhum defeito crítico chegue ao piloto de 08/03/2027. Os critérios vêm da proposta técnica e do contrato; o que é proposta nossa está marcado.

## 2. Critérios de aceite do contrato

| Critério (Bloco C, item 5) | Como verificamos | Responsável |
|---|---|---|
| Funcionalidades conforme a especificação aprovada e os cenários de aceite | Cenários de aceite escritos para cada item do Backlog | Lucas escreve, Larissa revisa, Juliana aprova |
| Sem defeito bloqueador nos fluxos críticos do marco | Testes técnicos antes de cada envio para homologação | Larissa |
| Integrações validadas no ambiente e nos equipamentos do cliente | Pagar.me no sandbox (P-02); catraca no Centro (P-01) | Marina, Diego |
| Cenários de homologação executados pelos usuários-chave | Homologação de cada entrega (seção 5) | Juliana e usuários-chave |
| Defeitos críticos e altos corrigidos antes da produção | Regra de classificação (seção 4) | Larissa, Camila |
| Documentação operacional mínima e treinamento concluídos | Manual de uso da recepção e 4 sessões de 2 h (C-30) | Paulo |

## 3. Tipos de teste

| Tipo | O que cobre | Quem faz | Quando |
|---|---|---|---|
| Testes do desenvolvedor | Cada item antes de ser dado como pronto | Diego, Bruna, Caio | Durante o desenvolvimento |
| Testes técnicos da entrega | Fluxos da entrega e regressão dos fluxos críticos | Larissa | C-13 (18 a 21/01), C-22a (01 a 05/02), C-22b (15 a 19/02), E3 (22 a 26/02) |
| Testes de integração | Pagar.me (boleto, Pix, situação de pagamento) e catraca (libera e bloqueia conforme a situação do aluno) | Diego, Marina, Larissa | C-20 e C-27 |
| Testes de migração | Cargas de validação 1 e 2, com conferência (seção 7) | Diego, Larissa, Fernanda | C-24 (25 a 29/01) e C-25 (15 a 17/02) |
| Homologação | Cenários de aceite com os usuários-chave | Juliana e usuários-chave | C-14, C-23a, C-23b, C-32 |
| Ensaio de rollback | Voltar ao legado sem parar a recepção | Paulo, Larissa, Igor | C-31 (até 03/03) |
| Teste de fumaça do cutover | Login, matrícula, reserva, cobrança e catraca no PRD | Larissa, Paulo | 07/03 |

**Fluxos críticos** (sem eles a recepção para): situação do aluno na recepção e liberação na catraca; matrícula e cobrança; reserva de aula; login do aluno no portal.

## 4. Classificação de defeitos

| Severidade | Definição | Regra |
|---|---|---|
| **Crítico** | Para um fluxo crítico, sem alternativa (ex.: catraca bloqueia aluno em dia) | Corrigir antes da produção; bloqueia o Go/No-Go |
| **Alto** | Fluxo funciona com erro relevante ou só com alternativa manual (ex.: saldo errado) | Corrigir antes da produção (Bloco C) |
| **Médio** | Erro com alternativa simples, sem impacto em dinheiro ou acesso | Corrigir na entrega seguinte ou na operação assistida |
| **Baixo** | Texto, visual ou ajuste cosmético | Corrigir conforme a capacidade |

Na homologação, a rejeição precisa de evidência e referência ao requisito ou critério de aceite (Bloco D, item 5). Rejeição sem isso volta para esclarecimento.

## 5. Homologação por entrega

| Entrega | Período | Homologadores | Foco |
|---|---|---|---|
| E1 | 25 a 29/01 | Juliana e usuários-chave | Cadastros, planos, matrícula, cobranças, auditoria |
| E2 parte 1 | 08 a 16/02 (Carnaval em 08 e 09/02) | Juliana, Patrícia | Agenda, reservas e avaliação física |
| E2 parte 2 | 22 a 26/02 | Juliana, Fernanda | Portal, Pagar.me e inadimplência |
| E3 | 01 a 05/03 | Juliana, Thiago, Carla | Migração, situação na recepção, catraca, painel |

Regras: envio formal por e-mail com os cenários; lembrete no 3º dia útil (R-03); sem manifestação em 5 dias úteis, a WEBFLOW pode considerar o marco aceito (Bloco D).

## 6. Requisitos não funcionais

| Requisito (Bloco C, item 4) | Como verificamos |
|---|---|
| Web responsiva: Chrome, Edge e Safari atuais | Testes técnicos nos três navegadores, em computador e celular |
| HTTPS, acesso por perfil e proteção de credenciais | Teste de perfis por função e unidade (PB-02); revisão de segurança da Marina com o Marcelo |
| Trilhas de auditoria de eventos críticos | Teste do PB-27 na E1 |
| LGPD: retenção e perfis de acesso | Definidos na especificação e aprovados por Juliana e Marcelo |
| Disponibilidade de 99,5% ao mês após a estabilização | Monitoramento pelo Igor a partir do go-live; medido depois da operação assistida |
| Segregação por unidade e visão consolidada | Teste com usuários de unidades diferentes |

## 7. Qualidade da migração

A WEBFLOW não faz saneamento manual da base (exclusão do Bloco B). Por isso a migração é conferida, e os erros voltam ao cliente para correção.

| Conferência | Como | Quem aprova |
|---|---|---|
| Layout de importação | Aprovado até 22/01 | Juliana |
| Alunos ativos e planos vigentes | Quantidade carregada igual ao relatório do legado, por unidade | Juliana |
| Saldos em aberto | Soma dos saldos igual ao legado, por unidade | Fernanda |
| Registros rejeitados | Lista de erros enviada ao cliente para correção antes da carga seguinte | Lucas |

## 8. Pronto para homologação

Um item só vai para homologação quando:
1. Tem cenários de aceite aprovados pela Juliana.
2. Passou nos testes do desenvolvedor e nos testes técnicos da Larissa.
3. Não tem defeito crítico ou alto aberto.
4. Está instalado no HML com dados de teste.

## 9. Indicadores

| Indicador | Meta | Fonte da meta |
|---|---|---|
| Defeitos críticos e altos abertos no Go/No-Go | Zero | Bloco C, item 5 |
| Prazo de homologação | Até 5 dias úteis | Bloco D, item 5 |
| Disponibilidade após a estabilização | 99,5% ao mês | Bloco C, item 4 |
| Diferença na conferência da migração | Zero sem explicação | Proposta nossa |
| Cenários aprovados na primeira rodada | Acompanhar (sem meta no kit) | — |
| Defeitos achados na homologação × nos testes técnicos | Acompanhar (sem meta no kit) | — |

Os indicadores entram no status semanal com a Juliana.

## 10. Capacidade de QA

A frente de QA tem 260 h de referência e a Larissa tem 256 h em 16 semanas (102%, Custos seção 3). Para fechar a conta sem contratar:
- Os desenvolvedores testam o próprio item antes de passar para a Larissa.
- O Lucas escreve os cenários de aceite; a Larissa só revisa.
- Os usuários-chave executam a homologação; a Larissa apoia.
- A Larissa concentra o tempo em testes técnicos, regressão dos fluxos críticos e migração.

## 11. Rastreabilidade

| Origem | Uso neste plano |
|---|---|
| Bloco C, item 5 | Critérios de aceite (seção 2) |
| Bloco C, item 4 | Requisitos não funcionais (seção 6) |
| Bloco C, item 6; Bloco B (exclusões) | Migração conferida, sem saneamento pela WEBFLOW |
| Bloco D, item 5 | Prazo e regra de homologação |
| Cronograma C-13, C-14, C-22a a C-25, C-31, C-32 | Datas dos testes e homologações |
| Riscos R-03, R-06, R-16, R-17 | Homologação, migração, recepção na virada e defeitos no Go/No-Go |
