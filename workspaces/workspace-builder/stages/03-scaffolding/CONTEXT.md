# Estágio 03: Geração do esqueleto

Gerar a estrutura completa de pastas, os arquivos CONTEXT.md e os arquivos de referência com variáveis. Esta é a meta do dia na oficina: sair com o esqueleto do workspace gerado.

## Entradas

| Fonte | Arquivo/Local | Seção/Escopo | Por quê |
|-------|---------------|--------------|---------|
| Estágio anterior | `../02-mapping/output/stage-contracts.md` | Arquivo todo | Os contratos a virar pastas e arquivos |
| Descoberta | `../01-discovery/output/workflow-map.md` | Seções de estágios opcionais e materiais | Estágios que podem ser removidos, documentos do participante |
| Template | `/_core/templates/stage-context-template.md` | Arquivo todo | Modelo dos CONTEXT.md de estágio |
| Template | `/_core/templates/workspace-claude-template.md` | Arquivo todo | Modelo do CLAUDE.md do workspace |
| Template | `/_core/templates/workspace-context-template.md` | Arquivo todo | Modelo do CONTEXT.md do workspace |
| Sintaxe | `/_core/placeholder-syntax.md` | Arquivo todo | Como escrever as variáveis |

## Processo

1. Leia os contratos de estágio, saída do mapeamento.
2. Crie a estrutura de pastas do workspace:
   - Raiz: CLAUDE.md, CONTEXT.md, setup/
   - Pasta de contexto (equivalente ao brand-vault do domínio) com o próprio CONTEXT.md
   - stages/ com uma subpasta numerada por estágio, cada uma com CONTEXT.md, output/ e references/
   - shared/ para arquivos de referência usados em vários estágios
3. Preencha cada CONTEXT.md de estágio usando o template, com as entradas, o processo e as saídas do contrato. Para cada estágio, decida:
   - **Pontos de parada:** o estágio se beneficia de o humano conduzir entre os passos? Estágios criativos (escrever, desenhar, idealizar) devem ter pelo menos um. Estágios lineares (extrair, gerar, validar) podem pular.
   - **Auditoria:** o estágio precisa de conferência de qualidade antes de salvar? Estágios criativos e de construção devem ter. Apague as seções que o estágio não precisa.
4. Crie o CLAUDE.md do workspace: mapa de pastas, gatilhos, tabela de roteamento e a seção "o que carregar".
5. Crie o CONTEXT.md do workspace: tabela de roteamento e recursos compartilhados.
6. Crie os arquivos de referência de cada estágio, com variáveis `{{VARIAVEL}}` para o conteúdo que muda de pessoa para pessoa.
7. Para workspaces que produzem conteúdo, crie um arquivo de referência com o framework de valor.
8. Para workspaces que produzem código, crie um arquivo de constantes compartilhadas.
9. Crie a pasta de contexto (equivalente ao brand-vault) com arquivos de variáveis. Se o workspace produz textos com voz/estilo, estruture as regras de tom com exemplos concretos, não uma descrição só.
10. Adicione arquivos .gitkeep em todas as pastas output/.
11. Rode a auditoria abaixo. Se algo falhar, corrija antes de salvar.
12. Escreva tudo em output/.

Observação para a oficina: as máquinas já vêm prontas, então não há passos de instalação de ferramentas nem busca de skills. Se o mapa do processo não trouxer essas seções, siga sem elas.

## Auditoria

| Verificação | Condição de aprovação |
|-------------|-----------------------|
| Estrutura de pastas | Todo estágio tem CONTEXT.md, output/ e references/ |
| Fidelidade ao contrato | Cada CONTEXT.md bate com os contratos do Estágio 02 |
| Sintaxe das variáveis | Todas as variáveis usam o formato `{{MAIUSCULAS_COM_UNDERSCORE}}` |
| Cobertura de .gitkeep | Toda pasta output/ tem um .gitkeep |
| Tamanho dos CONTEXT.md | Nenhum CONTEXT.md passa de 80 linhas |
| Convenções de nome | Todas as pastas e arquivos usam minúsculas-com-hífen |

## Saídas

| Artefato | Local | Formato |
|----------|-------|---------|
| Workspace gerado | `output/` | Estrutura completa de pastas e arquivos, pronta para o desenho do questionário |
