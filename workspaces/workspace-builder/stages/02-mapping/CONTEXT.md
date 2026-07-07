# Estágio 02: Mapeamento

Transformar o mapa do processo em contratos formais de estágio e verificar o grafo de dependências.

## Entradas

| Fonte | Arquivo/Local | Seção/Escopo | Por quê |
|-------|---------------|--------------|---------|
| Estágio anterior | `../01-discovery/output/workflow-map.md` | Arquivo todo | O processo a formalizar |
| Convenções | `/_core/CONVENTIONS.md` | "Pattern 1: Stage Contracts" e "Pattern 3: One-Way Cross-References" | As regras para escrever contratos |

## Processo

1. Leia o mapa do processo, saída da descoberta.
2. Para cada estágio, escreva o contrato formal de Entradas/Processo/Saídas, seguindo o padrão de contrato de estágio.
3. Mapeie as referências cruzadas: quais estágios leem de quais outros?
4. Identifique as fontes canônicas: onde vive cada informação? (uma casa por informação)
5. Verifique referências circulares: desenhe o grafo de dependências e confirme que ele flui em um sentido só.
6. Confirme que a saída de cada estágio é consumida por pelo menos um estágio seguinte (ou é a saída final).
7. **[Ponto de parada]** Apresente o diagrama de dependências e os contratos. Pergunte: o fluxo faz sentido? Falta alguma ligação?
8. Rode a auditoria abaixo. Se algo falhar, ajuste antes de salvar.
9. Produza o documento de contratos com o diagrama de dependências.

## Pontos de parada

| Depois do passo | O agente apresenta | O humano decide |
|-----------------|--------------------|-----------------|
| 6 | Diagrama de dependências e rascunho dos contratos de todos os estágios | Se o fluxo de dependências e os contratos estão corretos |

## Auditoria

| Verificação | Condição de aprovação |
|-------------|-----------------------|
| Sem referências circulares | O grafo de dependências flui em um sentido só |
| Consumo das saídas | A saída de cada estágio é lida por um estágio seguinte ou é a entrega final |
| Contratos completos | Todo estágio tem Entradas, Processo e Saídas, sem campos vazios |
| Fontes canônicas | Nenhuma informação é definida como oficial em mais de um estágio |

## Saídas

| Artefato | Local | Formato |
|----------|-------|---------|
| Contratos de estágio | `output/stage-contracts.md` | Blocos formais de Entradas/Processo/Saídas de cada estágio, mais o diagrama de dependências |
