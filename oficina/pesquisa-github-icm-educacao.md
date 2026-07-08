# Pesquisa GitHub: ICM e educação

Fonte canônica da pesquisa sobre projetos públicos no GitHub que usam ICM, Model Workspace Protocol ou estruturas próximas para fluxos educacionais.

Pesquisa realizada em 08/07/2026 para apoiar a galeria de exemplos e as adaptações do `workspace-builder` para a oficina do VIII Concefor.

## Pergunta de pesquisa

Quais projetos públicos no GitHub já funcionam como workspaces baseados em ICM, ou se aproximam desse padrão, com foco em educação, produção de materiais didáticos, cursos, planos de aula ou formação?

## Critérios usados

Um projeto foi considerado mais aderente ao ICM quando apresentava:

- `CLAUDE.md` ou equivalente como camada de orientação global.
- `CONTEXT.md` como roteamento de tarefas ou espaços de trabalho.
- Pastas de `stages/` ou etapas numeradas.
- Separação entre instruções, referências e outputs.
- Handoffs editáveis entre etapas.
- Uso de arquivos markdown como superfície de trabalho.

Um projeto foi considerado educacional quando tinha foco em:

- curso, aula, lesson plan, courseware ou curriculum;
- material didático, slides, avaliações ou guias de facilitador;
- formação técnica ou trilhas de aprendizagem;
- sistemas de estudo ou aprendizagem com IA.

## Resultado principal

Há poucos projetos educacionais públicos que declaram usar ICM de forma direta. O padrão ICM ainda aparece mais como método emergente do que como etiqueta consolidada no GitHub.

O que existe em maior volume são projetos educacionais com Claude, skills, agentes ou aplicações web que produzem materiais didáticos, mas que ainda não seguem a estrutura ICM completa de `CLAUDE.md`, `CONTEXT.md`, `stages/`, `references/` e `output/`.

Para a oficina, isso é útil: podemos apresentar o ICM como uma forma simples e transparente de organizar o mesmo tipo de produção educacional que outros projetos resolvem com aplicações, agentes múltiplos ou frameworks.

## Projetos encontrados

| Projeto | Aderência ao ICM | Foco educacional | Uso para a oficina |
|---------|------------------|------------------|--------------------|
| `RinDig/Interpreted-Context-Methdology` | Alta | Média/alta | Referência principal do método e do `course-deck-production` |
| `RinDig/Content-Agent-Routing-Promptbase` | Alta, como precursor | Baixa/média | Base conceitual da arquitetura por contexto roteado |
| `alfredang/wsq-courseware-generator-claude-streamlit` | Média | Alta | Exemplo robusto de fábrica de materiais educacionais |
| `alfredang/courseware_claude_agents` | Média | Alta | Exemplo de geração modular de courseware com agentes e skills |
| `AndyJuang/lesson-plan-skill` | Média/baixa | Alta | Exemplo pequeno e direto para professores |
| `rhpds/claude-code-courseware` | Média | Educação técnica | Modelo de oficina guiada dentro do Claude Code |
| `Matthew-creat3e/hoo-intelligence` | Média | Aprendizagem pessoal | Exemplo de workspace `learning` com contexto roteado |

## Referência principal: ICM oficial

### RinDig/Interpreted-Context-Methdology

Link: https://github.com/RinDig/Interpreted-Context-Methdology

É a referência central do método que estamos usando. Define o ICM como estrutura de pastas funcionando como arquitetura de agente. A lógica central é:

- uma etapa, um trabalho;
- markdown como interface;
- contexto carregado por camadas;
- outputs editáveis entre etapas;
- workspace configurado uma vez e reutilizado várias vezes.

O workspace mais relevante para educação dentro dele é `course-deck-production`, que transforma materiais não estruturados em apresentações de curso.

Relevância para a oficina:

- é o fundamento do nosso repositório;
- deve orientar a adaptação do `workspace-builder`;
- o `course-deck-production` pode virar um resumo de exemplo para os participantes.

### RinDig/Content-Agent-Routing-Promptbase

Link: https://github.com/RinDig/Content-Agent-Routing-Promptbase

É o precursor do ICM. Aplica separação de responsabilidades a janelas de contexto de IA. A contribuição mais importante para nossa oficina é a ideia de que o problema não é apenas "prompt melhor", mas arquitetura de contexto: cada tarefa deve carregar o mínimo necessário e apontar para fontes canônicas.

Relevância para a oficina:

- bom para explicar por que pastas resolvem problemas que o chat isolado não resolve;
- reforça os argumentos de consistência, memória, rastreabilidade e versionamento.

## Projetos educacionais próximos ao ICM

### alfredang/wsq-courseware-generator-claude-streamlit

Link: https://github.com/alfredang/wsq-courseware-generator-claude-streamlit

Projeto voltado para geração de courseware WSQ. Produz materiais como planos de avaliação, guias de facilitador, guias de aprendiz, planos de aula, slides e brochuras. Usa Claude, Streamlit, templates de documento e skills.

Aderência ao ICM:

- não é ICM puro;
- é mais uma aplicação de produção educacional com IA;
- tem modularidade, templates e produção de artefatos;
- falta a estrutura limpa de stages, references e output como contrato de filesystem.

Por que importa:

- mostra uma "fábrica educacional" real;
- ajuda a demonstrar o destino possível de um workspace criado por professores;
- é um bom paralelo para o caso Carlos: transformar materiais antigos em novos materiais didáticos.

### alfredang/courseware_claude_agents

Link: https://github.com/alfredang/courseware_claude_agents

Projeto de geração modular de materiais educacionais com Claude agents. O escopo inclui course proposal, assessment plans, facilitator guide, learner guide, lesson plan, slides e brochuras.

Aderência ao ICM:

- usa agentes, módulos e skills;
- tem boa separação de responsabilidades;
- não parece depender da estrutura ICM canônica;
- pode inspirar estágios educacionais em um workspace ICM.

Possível tradução para ICM:

1. Extrair requisitos do curso.
2. Planejar currículo e avaliação.
3. Gerar plano de aula.
4. Gerar materiais do facilitador e do estudante.
5. Gerar slides.
6. Fazer revisão pedagógica e entrega.

### AndyJuang/lesson-plan-skill

Link: https://github.com/AndyJuang/lesson-plan-skill

Skill pequeno para gerar pacote completo de aula. É diretamente compreensível por professores porque parte de um tema e produz materiais de uso docente.

Aderência ao ICM:

- não é workspace ICM completo;
- funciona mais como skill;
- tem fluxo claro que pode ser transformado em workspace.

Possível tradução para ICM:

1. Intake do tema e contexto da turma.
2. Extração ou organização do conteúdo.
3. Planejamento da aula.
4. Geração dos materiais.
5. Revisão pedagógica.
6. Empacotamento.

Uso na oficina:

- ótimo exemplo simples para a galeria;
- pode inspirar participantes que querem resolver a dor "preparar aulas".

## Projetos de formação e aprendizagem

### rhpds/claude-code-courseware

Link: https://github.com/rhpds/claude-code-courseware

Courseware prático para aprender Claude Code. Organiza módulos com comandos, preflight, passos guiados, verificação final e desafio prático.

Aderência ao ICM:

- não é ICM puro;
- usa comandos e módulos de curso;
- tem uma lógica de aprendizagem guiada, com progresso e verificação;
- é forte como referência de experiência de oficina.

Uso na oficina:

- inspira comandos ou rituais guiados como `/oficina`, `/mapear-dor`, `/gerar-workspace` e `/publicar-github`;
- reforça a importância de preflight e verificação antes da mão na massa.

### Matthew-creat3e/hoo-intelligence

Link: https://github.com/Matthew-creat3e/hoo-intelligence

Projeto de inteligência pessoal/negócio que inclui `workspaces/learning/CONTEXT.md`. O arquivo documenta explicitamente Jake Van Clief, ICM, Content-Agent-Routing-Promptbase, Model Workspace Protocol e princípios de aprendizagem.

Aderência ao ICM:

- usa a ideia de workspaces e contexto roteado;
- possui um workspace de aprendizagem;
- mistura memória pessoal, plano de estudo e referências conceituais;
- não é um pipeline educacional formal por estágios.

Uso na oficina:

- demonstra que ICM também pode organizar aprendizagem pessoal e desenvolvimento profissional;
- é menos adequado para participantes do Concefor do que os exemplos de lesson plan e courseware.

## Interpretação para a oficina Concefor

A pesquisa sugere três mensagens fortes:

1. ICM ainda é raro como padrão público em educação.
2. A demanda educacional existe: há muitos projetos tentando automatizar courseware, lesson plans, slides, avaliações e guias.
3. A contribuição da nossa oficina é mostrar uma forma mais transparente, editável e local de fazer isso, sem transformar tudo em uma aplicação fechada.

## Recomendações

### Para a galeria de exemplos do `workspace-builder`

Criar três resumos de uma página em pt-BR:

| Exemplo | Base | Por que entra |
|---------|------|---------------|
| PDF antigo para aula interativa | Caso Carlos | Exemplo local, emocional e concreto |
| Fábrica de courseware | `alfredang/wsq-courseware-generator-claude-streamlit` | Mostra escala e variedade de materiais |
| Plano de aula reutilizável | `AndyJuang/lesson-plan-skill` | Simples, docente e fácil de entender |

### Para o roteiro da oficina

Usar a pesquisa apenas como bastidor. Para os participantes, não vale abrir muitos repositórios. O foco deve continuar sendo:

- uma dor real;
- um processo de 3 a 5 etapas;
- uma primeira versão de workspace;
- a ideia de configurar a fábrica, não lapidar um produto isolado.

### Para o repositório dos participantes

Não incluir todos os projetos pesquisados. Incluir apenas resumos curtos e traduzidos, sem exigir navegação externa durante a oficina.

## Fontes

- https://github.com/RinDig/Interpreted-Context-Methdology
- https://github.com/RinDig/Content-Agent-Routing-Promptbase
- https://github.com/alfredang/wsq-courseware-generator-claude-streamlit
- https://github.com/alfredang/courseware_claude_agents
- https://github.com/AndyJuang/lesson-plan-skill
- https://github.com/rhpds/claude-code-courseware
- https://github.com/Matthew-creat3e/hoo-intelligence

