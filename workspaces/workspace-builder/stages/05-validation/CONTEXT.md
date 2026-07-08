# Estágio 05: Validação

Conferir o workspace gerado contra as convenções do ICM e corrigir problemas antes de entregar. Na oficina, este estágio é continuação: faça-o depois, com a IA, quando o workspace estiver montado.

## Entradas

| Fonte | Arquivo/Local | Seção/Escopo | Por quê |
|-------|---------------|--------------|---------|
| Esqueleto | `../03-scaffolding/output/` | Workspace gerado inteiro | O workspace a validar |
| Questionário | `../04-questionnaire-design/output/questionnaire.md` | Arquivo todo | Conferir a cobertura de variáveis |
| Convenções | `/_core/CONVENTIONS.md` | Arquivo todo | As regras a validar |
| Sintaxe | `/_core/placeholder-syntax.md` | Arquivo todo | Regras de seções condicionais |

## Processo

Rode cada verificação abaixo. Registre aprovado/reprovado e os problemas encontrados.

1. **Integridade das referências.** Todo caminho citado em qualquer CONTEXT.md aponta para um arquivo que existe. Liste referências quebradas.
2. **Sem dependências circulares.** Trace o grafo de referências. Se A referencia B, B não referencia A. Confirme que é um grafo sem ciclos.
3. **Cobertura de variáveis.** Varra os arquivos atrás de `{{VARIAVEL}}`. Toda variável tem pergunta no questionário; toda pergunta aponta para pelo menos um arquivo. Liste órfãos.
4. **Seções condicionais válidas.** Todo bloco `{{?SECAO}}...{{/SECAO}}` envolve uma seção inteira (um título e todo o conteúdo abaixo). Sinalize violações.
5. **Cadeia de handoff.** A saída do estágio N bate com o que o estágio N+1 lê. Liste a cadeia e aponte falhas.
6. **Pureza dos CONTEXT.md.** Nenhum CONTEXT.md contém conteúdo de referência (definições, regras extensas, exemplos). Só: título, descrição, Entradas, Processo, Pontos de parada (opcional), Auditoria (opcional), Saídas.
7. **Pontos de parada nos estágios criativos.** Estágios de escrita, design ou ideação têm pelo menos um ponto de parada, com números de passo válidos. Estágios lineares podem pular.
8. **Auditorias nos estágios criativos e de construção.** Esses estágios têm uma auditoria com condições claras, rodada antes de salvar.
9. **Contagem de linhas.** Sinalize CONTEXT.md acima de 80 linhas e arquivos de referência acima de 200.
10. **Convenções de nome.** Pastas e arquivos em minúsculas-com-hífen. Pastas de estágio com números (01-, 02-). Pastas output/ vazias têm .gitkeep.
11. **Qualidade.** Procure travessões longos (troque por hífen), jargão sem explicação e erros de formatação markdown.

Se achar problemas, corrija nos arquivos do workspace e rode de novo as verificações que falharam.

## Saídas

| Artefato | Local | Formato |
|----------|-------|---------|
| Relatório de validação | `output/validation-report.md` | Lista com aprovado/reprovado por verificação, problemas e correções aplicadas |
