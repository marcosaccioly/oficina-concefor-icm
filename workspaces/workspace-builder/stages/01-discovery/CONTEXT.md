# Estágio 01: Descoberta

Entender o processo do participante através de uma conversa. Modo oficina: em português, começando pela dor e conduzindo para o processo.

## Entradas

| Fonte | Arquivo/Local | Seção/Escopo | Por quê |
|-------|---------------|--------------|---------|
| Contexto | `../../shared/contexto-oficina.md` | Arquivo todo | Tom, público e meta da oficina |
| Participante | (conversa) e respostas do setup | Descrição do processo | O domínio a mapear |
| Materiais | `../../meus-materiais/` | Arquivos que a pessoa trouxe | Entender o processo real dela |
| Exemplos | `../../references/examples/` | O caso mais parecido | Inspiração concreta |
| Referência | `../../references/conventions-reference.md` | Arquivo todo | Padrões do ICM a mirar |

## Processo

1. Peça à pessoa que descreva o processo de ponta a ponta. Com o que ela começa? Com o que termina? Use as respostas do setup como ponto de partida.
2. Identifique os estágios distintos. Mire de 3 a 5. Onde uma tarefa termina e outra começa? Procure pontos naturais onde um humano vai querer revisar antes de continuar.
3. Para cada estágio, pergunte:
   - O que entra? (arquivos, decisões da pessoa, saída do estágio anterior)
   - O que sai? (o material que aquele estágio produz)
   - O que a IA precisa saber? (regras, exemplos, modelos, restrições)
4. Identifique o contexto compartilhado. Que informação é usada em vários estágios? (o tom, um padrão de correção, um design)
5. Identifique o que varia a cada uso. O que muda de um trabalho para outro? (o PDF da vez, a turma, a disciplina). Isso vira variável.
6. Identifique estágios opcionais. Algum estágio que a pessoa às vezes pula?
7. Se a pessoa colocou documentos em `meus-materiais/`, leia-os para entender o processo real dela. Se precisar de inspiração, mostre um dos exemplos de docência.
8. **[Ponto de parada]** Apresente o rascunho do mapa do processo. Pergunte: todos os estágios estão capturados? Falta alguma entrada ou saída? Algum estágio para juntar ou separar?
9. Rode a auditoria abaixo. Se algo falhar, ajuste antes de salvar.
10. Escreva o mapa do processo resumindo o que foi descoberto.

## Pontos de parada

| Depois do passo | O agente apresenta | O humano decide |
|-----------------|--------------------|-----------------|
| 7 | Rascunho do mapa: estágios com entradas/saídas, contexto compartilhado, variáveis, estágios opcionais | Se a divisão de estágios, os pontos de handoff e o contexto compartilhado estão corretos |

## Auditoria

| Verificação | Condição de aprovação |
|-------------|-----------------------|
| Clareza dos estágios | Cada estágio tem uma responsabilidade única e um resultado nomeado |
| Cadeia de entrada/saída | A entrada de cada estágio vem da pessoa ou de um estágio anterior |
| Contexto compartilhado | Os recursos usados em vários estágios estão listados à parte |
| Cobertura de variáveis | Todo detalhe que varia a cada uso está registrado como variável |

## Saídas

| Artefato | Local | Formato |
|----------|-------|---------|
| Mapa do processo | `output/workflow-map.md` | Documento estruturado: estágios com entradas/saídas, contexto compartilhado, variáveis, estágios opcionais |
