# Projeto MoveFit — Fluxo de Mudanças

**Referências:** Aula de Gestão de Mudanças; Bloco D do handoff (item 7, Mudanças de Escopo)
**Dependências:** Escopo (02); RACI (03); Backlog; Roadmap (05); Cronograma (06); Custos (07); Riscos (08)

## 1. Objetivo

Garantir que nenhum pedido mude escopo, prazo ou custo sem registro, análise de impacto e aprovação de quem tem alçada. O contrato (Bloco D, item 7) diz que qualquer alteração que impacte escopo, esforço, prazo, custo, arquitetura ou premissas deve ser registrada e analisada, e que a execução depende de aprovação formal quando houver impacto comercial.

## 2. O que é e o que não é mudança

| É mudança (segue este fluxo) | Não é mudança |
|---|---|
| Funcionalidade fora do Escopo (ex.: QR Code, app nativo) | Correção de defeito: vai para o Plano de Qualidade (15) |
| Item condicional cuja condição não foi atendida (catracas de outras unidades, histórico, SMS, SSO) | Detalhar um requisito que já está no Escopo |
| Alteração de regra já aprovada na especificação | Trocar a ordem de itens dentro da mesma entrega (Juliana aprova a prioridade) |
| Mudança de data de marco ou do prazo final | |
| Atraso de dependência do cliente que afeta marco (OS permite prorrogar) | |

## 3. Fluxo

| Passo | O que acontece | Responsável | Prazo |
|---|---|---|---|
| 1. Registro | O pedido entra no registro de mudanças (seção 7), com quem pediu e por quê. Pedido verbal é registrado, mas não altera nada | Lucas | No mesmo dia |
| 2. Triagem | Decide se é mudança, defeito ou detalhamento | Camila, Lucas | 2 dias úteis (proposta nossa) |
| 3. Análise de impacto | Impacto em escopo, prazo, custo, arquitetura, qualidade e premissas | Camila, consultando Lucas, Marina, Larissa e Marcelo | 5 dias úteis (proposta nossa) |
| 4. Decisão | Conforme a alçada (seção 4) | Ver seção 4 | Na reunião seguinte do aprovador |
| 5. Comunicação e atualização | Resultado comunicado a Juliana. Se aprovado, entra no Backlog e no Roadmap, e Cronograma, Custos e Riscos são revistos | Camila, Lucas | 2 dias úteis após a decisão |

## 4. Alçadas

| Impacto da mudança | Quem aprova | Quem é informado |
|---|---|---|
| Não afeta escopo contratado, prazo final nem custo | Camila | Juliana |
| Só muda a prioridade dentro do Backlog | Juliana | Camila |
| Afeta escopo contratado, prazo final ou custo | Henrique e a autoridade comercial da WEBFLOW (Rafael Prado, proposto no kick-off) | Juliana, Eduardo Viana |
| Afeta arquitetura, segurança ou integração | Parecer obrigatório de Marina antes da decisão | Marcelo |
| Afeta dados, acessos ou equipamentos do cliente | Parecer obrigatório de Marcelo antes da decisão | Juliana |

Mudança com custo para o cliente é paga por aditivo ou trocada por item de mesmo tamanho, com aprovação do Henrique.

*Nota interna (não mostrar ao cliente): a reserva gerencial não paga pedido novo do cliente (Custos, seção 6).*

## 5. Congelamento antes do piloto (ajuste)

De **26/02/2027** (entrega da E3) a **12/03/2027** (fim da operação assistida) nenhuma mudança entra na versão do piloto. Só entram correções de defeito crítico ou alto. Mudanças aprovadas nesse período vão para depois do piloto.

**Motivo:** a folga entre a homologação da E3 (05/03) e a carga final (06/03) é zero. Qualquer novidade nessa janela coloca o piloto de 08/03 em risco (R-15, R-17).

## 6. Exemplo: pedido de entrada por QR Code

O cliente perguntou se o aluno poderia "entrar pelo celular" (Bloco A, 08/09). O comercial disse que o QR Code "poderia ser avaliado", mas ele não está na proposta aprovada.

| Passo | Resultado |
|---|---|
| 1. Registro | SM-01, pedido do cliente na negociação (08/09), registrado por Lucas no kick-off |
| 2. Triagem | É mudança: QR Code está fora do Escopo |
| 3. Análise de impacto | **Escopo:** nova funcionalidade no portal e no controle de acesso. **Arquitetura:** depende de a catraca Control iD do Centro aceitar leitura de QR Code (Marina e Marcelo). **Equipamento:** se precisar de leitor novo, a compra é do cliente (exclusão do Bloco B). **Prazo:** a integração da catraca (PB-21) já está no caminho crítico, sem folga até o piloto. **Custo:** o kit não traz horas para estimar; é preciso orçar antes da decisão |
| 4. Decisão | Afeta escopo e prazo: Henrique e Rafael Prado decidem |
| Recomendação | Não incluir antes do piloto. Avaliar depois do encerramento, como aditivo ou sustentação |
| 5. Comunicação | Juliana recebe a decisão; se aprovada, vira item novo no Backlog, fora da E3 |

## 7. Registro de mudanças

| ID | Pedido | Quem pediu | Data | Tipo | Situação | Decisão |
|---|---|---|---|---|---|---|
| SM-01 | Entrada por QR Code | Cliente, na negociação (08/09) | 26/11/2026 | Fora do escopo | Em análise | Recomendação: depois do encerramento |

**Pedidos já esperados** (ainda não registrados, mas devem seguir este fluxo se aparecerem):

| Pedido provável | Risco | Tratamento |
|---|---|---|
| SSO Microsoft 365 | R-14 | Usuário e senha na baseline; SSO só por mudança |
| Histórico completo de avaliações | R-12 | Só entra o histórico no layout e compatível; saneamento é do cliente |
| Recorrência em cartão no Pagar.me | R-23 | Confirmar com Fernanda na descoberta; se for pedida, é mudança |
| Catracas das demais unidades sem compatibilidade | R-11 | Troca de equipamento pelo cliente ou mudança |
| Adiar o PB-26 (e-mails) | R-15 | Não é mudança de escopo: Juliana aprova a nova prioridade |

## 8. Rastreabilidade

| Origem | Uso neste fluxo |
|---|---|
| Bloco D, item 7 | Base contratual do fluxo |
| RACI (03), regra 7 | Alçadas: Camila, Juliana, Henrique e a autoridade comercial |
| Escopo (02) | O que está dentro, fora e condicional |
| Custos (07), seção 6 | A reserva não paga mudança |
| Cronograma (06), seção 7 | Ordem de resposta quando o trabalho não cabe |
| Riscos R-11, R-12, R-14, R-19, R-23 | Pedidos esperados e pedidos informais |
