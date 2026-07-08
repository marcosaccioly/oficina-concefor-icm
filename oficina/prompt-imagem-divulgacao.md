# Prompt: imagem de divulgação (formulário Concefor)

Direção definida em `formulario-concefor.md`: célula/ecossistema digital + frase "IA além do chat". Este arquivo é o dono único do prompt; o formulário só aponta para cá (Pattern 5 das convenções do ICM).

Nenhuma ferramenta de geração de imagem está disponível neste ambiente (Claude Code), então o prompt abaixo precisa ser rodado manualmente em um gerador externo (ChatGPT/DALL-E, Copilot Designer, Gemini, Midjourney etc.).

## Conceito

A "célula" é a metáfora do próprio projeto (ver `plano-da-oficina.md`): o workspace que o participante constrói é a primeira célula de um organismo maior. A imagem deve sugerir organização crescendo a partir de um núcleo simples — não uma IA fria/ameaçadora, e sim algo orgânico, acolhedor, adequado para um público de professores.

## Prompt principal (rodar em inglês costuma dar resultado melhor)

> A single glowing organic cell made of soft circuit-like patterns, positioned at the center of the frame, with delicate branching connections extending outward into a small growing digital ecosystem of nodes and threads. Warm, inviting color palette (amber and teal tones) on a deep navy background. Clean, modern, minimalist digital-art style — professional enough for an academic/educational event, not dystopian or cold. Plenty of negative space around the center-left or top area reserved for a text headline to be added later. No text, no letters, no words in the image. Landscape orientation, high resolution.

Versão em português (caso a ferramenta só aceite PT):

> Uma única célula orgânica brilhante, feita de padrões que lembram circuitos, no centro da imagem, com conexões delicadas se ramificando para fora formando um pequeno ecossistema digital em crescimento (nós e fios conectados). Paleta de cores quente e acolhedora (tons de âmbar e azul-petróleo) sobre um fundo azul-marinho profundo. Estilo de arte digital limpo, moderno e minimalista — profissional o suficiente para um evento acadêmico, sem parecer frio ou distópico. Deixar bastante espaço vazio (canto superior ou centro-esquerda) reservado para um título que será adicionado depois. Sem texto, sem letras, sem palavras na imagem. Orientação paisagem, alta resolução.

## Por que sem texto no prompt

Geradores de imagem costumam errar tipografia. Recomendado: gerar só a arte (sem texto) e depois sobrepor "IA além do chat" em Canva/PowerPoint/Figma, com controle total de fonte e legibilidade.

## Prompt alternativo (mais abstrato)

> Abstract macro photography style of a bioluminescent cell-like structure branching into a neural/network pattern, glowing amber core fading into teal connections, dark background, elegant and warm, shallow depth of field, negative space for text overlay, no text.

## Especificações técnicas

- Limite do formulário: **máx. 10 MB** (único requisito confirmado — não há especificação de dimensão/proporção da Márcia).
- Sugestão (não confirmada): 1920×1080 (paisagem), depois exportar em JPG/PNG comprimido para garantir que fique abaixo de 10 MB.

## Depois de gerar

1. Salvar o arquivo final em `oficina/assets/imagem-divulgacao.png` (ou `.jpg`).
2. Sobrepor o texto "IA além do chat".
3. Conferir tamanho do arquivo (< 10 MB) antes de subir no formulário.
4. Atualizar a linha `[PENDENTE]` em `formulario-concefor.md` apontando para o arquivo final.
