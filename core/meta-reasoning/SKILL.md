---
name: meta-reasoning
description: Decide como raciocinar diante da tarefa, escolhendo a estratégia cognitiva mais adequada antes de agir.
metadata: {"openclaw":{"emoji":"🧠","homepage":"https://github.com/seu-user/agent-skills/tree/main/meta-reasoning"}}
---

# Meta Reasoning

Use esta skill no início de tarefas relevantes ou quando a melhor abordagem não for óbvia.

## Objetivo

Garantir que o agente:
- escolha a forma certa de pensar para cada tarefa
- adapte profundidade, velocidade e rigor ao contexto
- evite estratégia excessiva para tarefas simples
- evite superficialidade em tarefas complexas

## Regra principal

Antes de agir, decidir como pensar.

## Processo

### 1. Classificar a tarefa
Identificar se a tarefa é:
- simples
- técnica
- investigativa
- ambígua
- multi-etapas
- crítica

### 2. Definir estratégia cognitiva
Escolher entre:
- resposta direta
- decomposição
- pesquisa
- uso de tools
- validação forte
- comparação de opções

### 3. Ajustar profundidade
- tarefa simples → resposta simples
- tarefa complexa → planejamento e validação
- tarefa crítica → evidência, revisão e verificação final

### 4. Reavaliar durante a execução
Se a estratégia não estiver funcionando:
- mudar abordagem
- adicionar skills
- reduzir ou aumentar profundidade

## Perguntas obrigatórias

- Isso precisa de resposta direta ou investigação?
- Isso exige ferramenta externa?
- Isso exige decomposição?
- Isso exige validação forte?
- Estou pensando demais para uma tarefa simples?
- Estou pensando de menos para uma tarefa complexa?

## Regras

1. Não aplicar a mesma estratégia para todas as tarefas.
2. Não usar fluxo pesado quando uma resposta simples basta.
3. Não usar fluxo leve quando o problema exige rigor.
4. Reavaliar a abordagem se não houver progresso.
5. Escolher a menor estratégia suficiente para resolver bem.

## Sinais de estratégia ruim

- passos demais para tarefa trivial
- resposta rasa para tarefa complexa
- uso desnecessário de tools
- falta de validação em tarefa crítica
- pesquisa excessiva sem decisão

## Regra suprema

Não pense sempre do mesmo jeito.

Pense do jeito que a tarefa exige.
