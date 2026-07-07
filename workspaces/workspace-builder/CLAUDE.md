# Construtor de Workspace (versão Oficina Concefor)

Este workspace guia a construção de um novo workspace ICM para qualquer domínio, desde entender o fluxo de trabalho até gerar um esqueleto completo e validado.

Nesta oficina, você (o agente) conduz um professor a transformar uma dor real do trabalho dele em um workspace reutilizável. Fale sempre em português do Brasil, com linguagem simples. Antes de começar, leia `shared/contexto-oficina.md` para se situar.

## Mapa de pastas

```
workspace-builder/
├── CLAUDE.md              (você está aqui)
├── CONTEXT.md             (comece por aqui para o roteamento de tarefas)
├── setup/
│   └── questionnaire.md   (onboarding: as 4 perguntas iniciais)
├── shared/
│   └── contexto-oficina.md (o evento, o público, o tom, a meta do dia)
├── meus-materiais/        (onde o participante coloca os documentos dele)
├── stages/
│   ├── 01-discovery/      (entender o processo do participante)
│   ├── 02-mapping/        (formalizar os contratos de estágio)
│   ├── 03-scaffolding/    (gerar a estrutura de pastas: meta do dia)
│   ├── 04-questionnaire-design/  (montar o questionário do novo workspace)
│   └── 05-validation/     (validar contra as convenções do ICM)
└── references/
    ├── conventions-reference.md   (ponteiro para as convenções do ICM)
    ├── publicar-no-github.md      (guia do bloco opcional final)
    └── examples/
        ├── caso-carlos.md         (PDF de aula vira aula interativa)
        ├── avaliador-de-salas.md  (avaliar sala virtual no seu estilo)
        ├── devolutivas.md         (devolutivas escritas para atividades)
        └── script-to-animation-summary.md  (exemplo de workspace completo)
```

## Gatilhos

| Palavra | Ação |
|---------|------|
| `setup` | Roda o onboarding: as 4 perguntas iniciais sobre a dor e o processo |
| `status` | Mostra o andamento dos cinco estágios |

### Como o `status` funciona

Verifique as pastas `stages/*/output/`. Para cada estágio, se a pasta `output/` tem arquivos além do `.gitkeep`, o estágio está COMPLETO. Senão, PENDENTE. Mostre:

```
Andamento: workspace-builder

  [01-discovery]  -->  [02-mapping]  -->  [03-scaffolding]  -->  [04-questionnaire]  -->  [05-validation]
      STATUS              STATUS              STATUS                 STATUS                  STATUS
```

## Roteamento

| Tarefa | Vá para |
|--------|---------|
| Começar a construir um novo workspace | `stages/01-discovery/CONTEXT.md` |
| Formalizar os contratos de estágio | `stages/02-mapping/CONTEXT.md` |
| Gerar os arquivos do workspace | `stages/03-scaffolding/CONTEXT.md` |
| Desenhar o questionário de onboarding | `stages/04-questionnaire-design/CONTEXT.md` |
| Validar o workspace | `stages/05-validation/CONTEXT.md` |

## O que carregar

| Tarefa | Carregue | NÃO carregue |
|--------|----------|--------------|
| Descobrir o processo | `shared/contexto-oficina.md`, `references/conventions-reference.md`, os exemplos em `references/examples/` | `stages/02-mapping/` até `stages/05-validation/` |
| Formalizar contratos | `stages/01-discovery/output/`, `references/conventions-reference.md` | `references/examples/`, `stages/03-scaffolding/` até `stages/05-validation/` |
| Gerar esqueleto | `stages/02-mapping/output/`, `references/conventions-reference.md`, `/_core/templates/*`, `/_core/placeholder-syntax.md` | `stages/01-discovery/`, `references/examples/` |
| Desenhar questionário | `stages/01-discovery/output/`, esqueleto do estágio 03, `/_core/templates/questionnaire-template.md` | `stages/02-mapping/`, `references/examples/` |
| Validar workspace | esqueleto do estágio 03, `stages/04-questionnaire-design/output/`, `/_core/CONVENTIONS.md` | `stages/01-discovery/`, `stages/02-mapping/`, `references/examples/` |

## Meta da oficina

A meta do dia é chegar ao Estágio 03 (scaffolding) com o esqueleto do workspace gerado. Os estágios 04 e 05 ficam como continuação depois da oficina. Detalhes em `shared/contexto-oficina.md`.

## Handoffs entre estágios

Cada estágio escreve seu resultado na própria pasta `output/`. O estágio seguinte lê de lá. Se você editar um arquivo de saída entre os estágios, o próximo estágio usa a sua versão editada.
