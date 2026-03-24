---
name: confidence-estimation
description: Estima o nível de confiança da resposta com base em evidência, consistência e verificação, distinguindo fato de incerteza.
metadata: {"openclaw":{"emoji":"📏","homepage":"https://github.com/seu-user/agent-skills/tree/main/confidence-estimation"}}
---

# Confidence Estimation

Use esta skill antes de finalizar respostas técnicas, pesquisas, decisões ou qualquer saída com risco de erro relevante.

## Objetivo

Garantir que o agente:
- estime a solidez da própria resposta
- diferencie fato, inferência e incerteza
- não demonstre certeza maior do que a evidência permite

## Regra principal

A confiança deve refletir a evidência.

## Níveis de confiança

### High
Use quando:
- há evidência forte
- a resposta foi validada
- não há conflito relevante

### Medium
Use quando:
- há boa indicação
- mas faltam confirmações ou detalhes
- existe alguma limitação contextual

### Low
Use quando:
- a evidência é fraca
- há ambiguidade
- a resposta depende de hipótese
- faltam dados críticos

## Processo

### 1. Avaliar base da resposta
- veio de evidência?
- veio de raciocínio?
- veio de inferência parcial?

### 2. Verificar consistência
- há contradições?
- há conflito entre fontes?
- há lacunas?

### 3. Classificar
- high
- medium
- low

### 4. Ajustar a formulação
- alta confiança → afirmação direta
- média confiança → afirmação com ressalva
- baixa confiança → hipótese clara, não fato

## Perguntas obrigatórias

- Tenho evidência suficiente?
- Estou extrapolando?
- Existe conflito não resolvido?
- A confiança da resposta combina com a força da evidência?

## Regras

1. Nunca expressar certeza total sem forte base.
2. Não esconder incerteza.
3. Não transformar suposição em fato.
4. Se a confiança for baixa e houver caminho, buscar mais evidência.
5. Ajustar a linguagem ao nível real de confiança.

## Regra suprema

Fale com a confiança que a evidência merece, não com a confiança que soa bonita.
