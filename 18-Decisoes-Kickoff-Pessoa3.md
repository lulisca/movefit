# Decisões da Pessoa 3 — para defender no kick-off

Cada item tem a decisão, o motivo, a fonte e uma resposta curta caso alguém pergunte. Cobre os arquivos 13 a 16 (Comunicação, Mudanças, Qualidade e Go-live), que correspondem ao bloco **"Controle e entrega"** da apresentação (Aula 15).

**Regra de ouro para responder:** prazos de homologação, critérios de aceite, treinamento, operação assistida e garantia vêm do kit (Blocos C e D). Datas internas e prazos de análise são **propostas nossas**, marcadas nos documentos.

## 1. Comunicação: custo interno fora do status do cliente

**Decisão:** o status para o Henrique fala de marcos, riscos, decisões e mudanças. Horas e custo vão só para a gestão de operações da WEBFLOW (Eduardo Viana), a cada 15 dias.
**Motivo:** o teto, a meta e o valor-hora são "uso interno e confidencial" (Bloco E). É a mesma lógica do ajuste no RE-03 do Escopo (arquivo 12).
**Se perguntarem:** "O cliente não acompanha o custo?" → O cliente pagou preço fechado (R$ 286.000). Ele acompanha o que afeta ele: prazo, escopo e mudanças com custo.

## 2. Envio formal de cada homologação

**Decisão:** cada entrega vai por e-mail formal, com os cenários e o prazo de 5 dias úteis, e há lembrete no 3º dia.
**Motivo:** o contrato (Bloco D, item 5) permite considerar o marco aceito se o cliente não se manifestar em 5 dias úteis, mas só se o envio for formal. O lembrete atende ao R-03.
**Se perguntarem:** "Vocês vão forçar aceite?" → Não. A regra existe para o projeto não travar; o lembrete serve para ela nunca precisar ser usada.

## 3. Alçadas de mudança iguais às da RACI

**Decisão:** Camila aprova o que não afeta escopo contratado, prazo final nem custo. Juliana aprova prioridade. Henrique e a autoridade comercial da WEBFLOW aprovam o que afeta escopo, prazo ou custo.
**Motivo:** é a regra 7 da RACI e o item 7 do Bloco D.
**Ponto em aberto:** a RACI ainda não tem a autoridade comercial. O Rafael Prado é o candidato (arquivo 12, ponto 6). Confirmar no kick-off.

## 4. Congelamento de mudanças de 26/02 a 12/03

**Decisão:** da entrega da E3 até o fim da operação assistida, só entram correções de defeito crítico ou alto.
**Motivo:** a folga entre a homologação da E3 (05/03) e a carga final (06/03) é zero (Cronograma, seção 5).
**Se perguntarem:** "E se o cliente precisar de algo urgente?" → Registra agora e entra logo depois do piloto. O piloto não pode correr risco por uma novidade de última hora.

## 5. QR Code: não entra antes do piloto

**Decisão:** o pedido é registrado (SM-01) e a recomendação é avaliar depois do encerramento, como aditivo ou sustentação.
**Motivo:** está fora do Escopo, depende de a catraca aceitar QR Code (talvez com leitor novo, comprado pelo cliente) e mexeria na integração da catraca, que está no caminho crítico.
**Se perguntarem:** "Mas o comercial disse que seria avaliado." → E foi avaliado, pelo fluxo. Avaliar não é prometer; a decisão final é do Henrique.

## 6. Defeitos em quatro níveis

**Decisão:** crítico e alto bloqueiam a produção; médio e baixo seguem com plano.
**Motivo:** o Bloco C (item 5) exige que críticas e altas sejam tratadas antes da produção e que não haja defeito bloqueador nos fluxos críticos.
**Se perguntarem:** "Qual é o fluxo crítico?" → Situação do aluno e catraca na recepção, matrícula e cobrança, reserva e login no portal.

## 7. QA a 102% da capacidade

**Decisão:** os desenvolvedores testam o próprio item, o Lucas escreve os cenários de aceite e os usuários-chave executam a homologação. A Larissa foca em testes técnicos, regressão e migração.
**Motivo:** a frente de QA tem 260 h e a Larissa tem 256 h em 16 semanas (Custos, seção 3).
**Se perguntarem:** "Por que não contratar outro QA?" → O custo já passa do teto (R-20). Redistribuir o teste é a saída sem custo novo.

## 8. Migração conferida por números

**Decisão:** cada carga é conferida pela quantidade de alunos ativos e planos e pela soma dos saldos, por unidade. A Fernanda aprova os saldos. Registros com erro voltam ao cliente.
**Motivo:** a WEBFLOW não faz saneamento manual (exclusão do Bloco B) e as bases têm campos não padronizados (Bloco G, R-06).

## 9. Go/No-Go com quatro pareceres e três resultados

**Decisão:** TI, QA, implantação e negócio dão parecer. O resultado pode ser Go, Go com ressalva (só pendências médias ou baixas, com contingência) ou No-Go.
**Motivo:** regra da RACI; o "Go com ressalva" evita que uma pendência pequena adie o piloto.
**Se perguntarem:** "E se der No-Go?" → O Centro segue no legado e a nova data vai para o Henrique pelo fluxo de mudanças, porque não há folga até 26/03.

## 10. Cutover no fim de semana, com ponto de não retorno

**Decisão:** extração e carga no sábado 06/03, conferência e teste de fumaça no domingo, e decisão final no domingo à noite. O que a recepção fizer no domingo é lançado na segunda.
**Motivo:** "não pode parar a recepção" (Bloco A). Até domingo, voltar é simples, porque o legado nem foi desligado.
**Se perguntarem:** "E se der problema na segunda?" → Aí a regra é contingência e correção, não rollback: acesso manual na catraca e legado só para consulta.

## 11. Operação assistida com revezamento

**Decisão:** Paulo e Larissa se revezam no Centro; Diego e Bruna em plantão de correção; Igor na infraestrutura; boletim diário para a Juliana.
**Motivo:** o Paulo tem 8 h/semana e a frente de implantação está em 141% (Custos, seção 3). O pedido de horas extras da semana de 08/03 vai para o Eduardo Viana.

## 12. Garantia até 24/04/2027

**Decisão:** 30 dias corridos após o aceite final de 25/03 (Bloco D, item 6). Depois disso, a sustentação é outro contrato (Bloco A).
**Se perguntarem:** "Uma regra nova na garantia é corrigida?" → Não. Garantia corrige defeito do que foi entregue e aceito; regra nova é mudança ou sustentação.

## 13. Ajustes sugeridos nos documentos dos colegas

| Documento | Ajuste | Motivo |
|---|---|---|
| 06 Cronograma | Incluir uma atividade de testes técnicos da E3 (22 a 26/02, Larissa) antes da C-32 | As outras entregas têm testes técnicos (C-13, C-22a, C-22b); a E3 não |
| 06 Cronograma | Registrar o congelamento de mudanças de 26/02 a 12/03 | Decisão 4 |
| 07 Custos, seção 10 | Trocar "junto com o status para Henrique" por "no relatório interno para a gestão de operações" | O custo interno é confidencial (decisão 1) |
| 08 Riscos | Avaliar um risco novo: horas do Paulo (8 h/semana) na operação assistida | Implantação a 141% da capacidade |
| Grupo | Decidir se a carga final é só do Centro ou das 5 unidades | Muda o plano de expansão (Go-live, seção 9) |

## 14. Perguntas prováveis, em uma linha

| Pergunta | Resposta |
|---|---|
| Como vocês garantem que a recepção não para? | Virada no fim de semana, ensaio de rollback, ponto de não retorno no domingo e acesso manual como contingência |
| Quem decide se o piloto entra? | A Juliana, com a Camila, depois dos pareceres de TI, QA, implantação e negócio |
| O que acontece se o cliente pedir algo novo? | Vai para o registro, passa por análise de impacto e a alçada decide. Nenhum pedido verbal muda a baseline |
| E se o cliente não homologar? | Lembrete no 3º dia; depois de 5 dias úteis sem manifestação, o contrato permite considerar o marco aceito |
| Quantas pessoas testam? | Uma QA (Larissa), com apoio dos desenvolvedores, do Lucas e dos usuários-chave |
| O que é preciso para o aceite do piloto? | Nenhum defeito crítico ou alto aberto e a recepção sem contingência nos dois últimos dias da operação assistida |
| Quando acaba a responsabilidade da WEBFLOW? | Garantia até 24/04/2027; depois, sustentação por contrato separado |

## 15. Roteiro da sua fala (cerca de 4 minutos)

1. **Ponte** (15 s): "Já vimos o que vamos entregar e quando. Agora, como a gente controla o projeto e garante que o piloto entra sem parar a recepção."
2. **Comunicação** (45 s): dois pontos focais, Juliana e Camila; status semanal e status executivo quinzenal com o Henrique; envio formal de cada homologação. Toda decisão vira ata.
3. **Mudanças** (1 min): nenhum pedido verbal muda a baseline. Cinco passos: registro, triagem, impacto, decisão pela alçada e comunicação. Exemplo do QR Code. Congelamento de 26/02 a 12/03.
4. **Qualidade** (1 min): escada de testes até a homologação; crítico e alto bloqueiam a produção; migração conferida por números; meta de zero defeitos críticos ou altos no Go/No-Go.
5. **Go-live** (1 min): Go/No-Go em 05/03 com quatro pareceres; cutover no fim de semana; ponto de não retorno no domingo; go-live em 08/03; operação assistida até 12/03; aceite final em 25/03; garantia até 24/04.
6. **Próximos passos** (15 s): até 04/12, formalizar o ponto focal, os usuários-chave e o calendário de indisponibilidade; cobrar as pendências P-01 a P-08; especificação aprovada em 18/12.
