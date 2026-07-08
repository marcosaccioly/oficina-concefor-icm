# Adaptações do repositório para a oficina

Como transformar o ICM na versão que vai para as máquinas dos participantes. A pasta `oficina/` (esta) é só planejamento e fica de fora.

## Status (aplicado em 07/07/2026)

Já aplicado no `workspaces/workspace-builder`:

- `setup/questionnaire.md`, `CLAUDE.md`, `CONTEXT.md` e os cinco `stages/*/CONTEXT.md` reescritos em pt-BR (modo oficina).
- `shared/contexto-oficina.md` criado (evento, público, tom, metáfora da célula, meta do dia, gestão de tempo).
- `meus-materiais/` criado com `LEIA-ME.md`.
- Galeria de exemplos em pt-BR: `references/examples/caso-carlos.md`, `avaliador-de-salas.md`, `devolutivas.md`.
- `references/publicar-no-github.md` criado (bloco opcional final).
- Discovery (01) em modo oficina: mira 3 a 5 estágios, sem busca de skills no GitHub, aponta para `meus-materiais/` e os exemplos.

Ainda falta:

- CLAUDE.md e README da RAIZ do repositório limpo (em pt-BR, sem a pasta `oficina/`): fazer na criação do repo dos participantes.
- Traduzir `references/examples/script-to-animation-summary.md` (opcional; é exemplo avançado, hoje em inglês).
- Decidir com o Elton se os workspaces `script-to-animation` e `course-deck-production` saem da cópia das máquinas.
- Personalização versão 2 (relógio ativo, voz dos facilitadores, transcrição de áudio).

## Estratégia de repositórios

1. Este repositório (`oficina-concefor-icm`) é a bancada de trabalho: o planejamento vive em `oficina/` e as adaptações são aplicadas direto no `workspaces/workspace-builder`.
2. Quando as adaptações estiverem prontas e testadas, criar o repositório limpo dos participantes (novo repo, ex.: `concefor-oficina-ia`), sem a pasta `oficina/` e sem o histórico de rascunho. É esse repo que será clonado em cada máquina.
3. No bloco opcional final, cada participante sobe o próprio workspace para o GitHub dele a partir da máquina.

## Mudanças na raiz (versão das máquinas)

| Arquivo/pasta | Mudança | Por quê |
|---------------|---------|---------|
| `CLAUDE.md` | Reescrever em pt-BR, apontando direto para `workspaces/workspace-builder`. Incluir o contexto da oficina e a instrução: toda conversa em português. | O participante não deve precisar navegar; a IA deve saber onde está. |
| `README.md` | Versão curta em pt-BR com o passo a passo do dia. | Material de consulta do participante. |
| `workspaces/script-to-animation` e `course-deck-production` | Tirar da cópia das máquinas; viram resumos de 1 página na galeria de exemplos do builder. | Menos ruído: os participantes usam apenas o workspace-builder. (Pendência: confirmar com Elton.) |

## Mudanças no workspace-builder

| Item | Mudança |
|------|---------|
| `setup/questionnaire.md` | Traduzir e reescrever as 4 perguntas com exemplos de docência, espelhando a `folha-mapeamento.md` (mesmas perguntas do papel). Acrescentar orientação: começar pela dor e ajudar a transformá-la em processo. |
| `shared/contexto-oficina.md` (novo) | Ficha que a IA lê sempre: o que é o evento, facilitadores (Marcos e Elton), público professor, linguagem simples e sem jargão, hora de início e duração do turno. A IA ajuda a administrar o tempo quando perguntada. |
| `stages/01-discovery/CONTEXT.md` | Traduzir. Modo oficina: mirar processos de 3 a 5 estágios; pular o passo 8 (busca de skills no GitHub: depende de rede e consome tempo); manter um único checkpoint. |
| `stages/02` a `05` | Traduzir os CONTEXT.md. Deixar claro que a meta do dia é chegar ao estágio 03 (scaffolding); 04 e 05 ficam como lição de casa guiada. |
| `references/examples/` | Adicionar 3 resumos de 1 página em pt-BR como inspiração: caso Carlos (PDF para aula interativa), fábrica de courseware inspirada em `alfredang/wsq-courseware-generator-claude-streamlit`, e plano de aula reutilizável inspirado em `AndyJuang/lesson-plan-skill`. Ver `oficina/pesquisa-github-icm-educacao.md`. |
| `meus-materiais/` (novo) | Pasta vazia (com .gitkeep) onde o participante coloca os documentos que trouxe. Referenciada no discovery e no scaffolding. |
| `references/publicar-no-github.md` (novo) | Mini guia do bloco opcional: criar conta, autenticar no VS Code, criar repositório, enviar. |

## Personalização da experiência (versão 2, se der tempo)

- Relógio ativo: o agente sabe a hora de início e avisa marcos de tempo da oficina.
- A IA configurada com a "voz" dos facilitadores, sabendo quem está na sala e o roteiro do dia, para dar uma experiência guiada de criação.
- Transcrição de áudio no lugar de digitação: a dupla grava a conversa do mapeamento e entrega o texto à IA (carta na manga; alguém pode fazer isso espontaneamente).

## Princípios a preservar (não mexer)

- A arquitetura de 5 camadas e os contratos de estágio (`_core/CONVENTIONS.md` continua sendo a fonte).
- O fluxo setup, discovery, mapping, scaffolding: é exatamente a experiência que queremos que eles vivam.
- Agnosticismo de modelo: o repo deve funcionar com Copilot, Claude Code ou outro agente compatível (não depender de skills específicas de um fornecedor).
