# Estágio 04: Desenho do questionário

Montar o questionário de onboarding que preenche as variáveis do novo workspace. Na oficina, este estágio é continuação: você pode fazê-lo depois, com a IA, a partir do esqueleto gerado no Estágio 03.

## Entradas

| Fonte | Arquivo/Local | Seção/Escopo | Por quê |
|-------|---------------|--------------|---------|
| Descoberta | `../01-discovery/output/workflow-map.md` | Seção de variáveis | As variáveis que precisam de perguntas |
| Esqueleto | `../03-scaffolding/output/` | Todos os arquivos com `{{VARIAVEL}}` | Saber onde cada variável aparece |
| Template | `/_core/templates/questionnaire-template.md` | Arquivo todo | Formato e regras de desenho a seguir |
| Sintaxe | `/_core/placeholder-syntax.md` | Arquivo todo | Regras de variáveis e seções condicionais |

## Processo

1. Leia a seção de variáveis do mapa do processo.
2. Varra todos os arquivos do esqueleto atrás de padrões `{{VARIAVEL}}`. Monte a lista completa.
3. Separe as variáveis em dois grupos:
   - **De sistema:** o que fica igual a cada uso (identidade, tom, design, preferências). Viram perguntas de setup.
   - **De cada uso:** o que muda a cada trabalho (nome do projeto, tema, turma). NÃO viram perguntas de setup; o estágio de entrada coleta na conversa, no início de cada uso.
4. Para cada variável de sistema, escreva uma pergunta: texto que uma pessoa não técnica entende, a variável que ela preenche, os arquivos onde aparece, o tipo de resposta e um exemplo ou padrão para quem quiser pular.
5. Para perguntas de voz/estilo, peça exemplos concretos, não descrições. "Me dê 2 ou 3 frases que soam como você" extrai um padrão; "descreva seu tom" extrai uma abstração.
6. Se um campo pode ser deduzido de outra resposta, liste-o como derivado. O agente preenche sem perguntar.
7. Escreva TODAS as perguntas como uma lista numerada única, sem agrupamentos. A pessoa deve responder tudo em uma mensagem.
8. Adicione lógica condicional para estágios opcionais: perguntas sim/não que removem pastas ou blocos `{{?SECAO}}`.
9. Se houver regras de voz/estilo com campos derivados, adicione um segundo passo: depois de preencher as regras, apresente-as para a pessoa revisar antes de finalizar.
10. Confira que toda variável de sistema tem uma pergunta.
11. Confira que as variáveis de cada uso são tratadas pelos CONTEXT.md de estágio, não pelo questionário.
12. Rode a auditoria abaixo. Se algo falhar, ajuste antes de salvar.
13. Escreva o questionnaire.md.

## Auditoria

| Verificação | Condição de aprovação |
|-------------|-----------------------|
| Cobertura de variáveis | Toda variável de sistema tem uma pergunta correspondente |
| Separação por uso | Nenhuma variável de cada uso aparece no questionário |
| Estrutura plana | Todas as perguntas em uma lista numerada única, sem agrupamentos |
| Exemplos presentes | Toda pergunta tem um padrão ou exemplo |

## Saídas

| Artefato | Local | Formato |
|----------|-------|---------|
| Questionário | `output/questionnaire.md` | Questionário plano, tudo de uma vez, para a pasta setup/ do novo workspace |
