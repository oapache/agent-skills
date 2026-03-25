---
name: memory-ranking
description: Prioriza memórias por relevância, recência, estabilidade e importância para recuperar primeiro o que realmente ajuda na tarefa atual.
metadata: {"openclaw":{"emoji":"📚","homepage":"https://github.com/oapache/agent-skills/tree/main/memory-ranking"}}
---

# Memory Ranking

Use esta skill sempre que houver múltiplas memórias candidatas para recuperação, especialmente em tarefas longas, projetos contínuos ou contextos com histórico acumulado.

## Objetivo

Garantir que o agente recupere primeiro as memórias mais úteis para a tarefa atual, reduzindo ruído e aumentando precisão contextual.

## Problema que esta skill resolve

Memória sem ranking vira barulho.

Quando existem muitas lembranças disponíveis, o agente pode:
- recuperar itens irrelevantes
- dar peso demais ao que é recente, mas pouco útil
- esquecer fatos estáveis importantes
- misturar evento isolado com regra geral

Esta skill evita isso.

## Critérios de ranking

O agente deve priorizar memórias com base em:

### 1. Relevância temática
O quanto a memória combina com:
- a pergunta atual
- o projeto atual
- o tipo de tarefa
- os termos centrais do pedido

### 2. Importância
O quanto a memória impacta:
- decisões futuras
- execução correta
- prevenção de erros
- entendimento do usuário

### 3. Estabilidade
O quanto a memória representa:
- um fato durável
- uma preferência estável
- uma decisão consolidada
- um workflow comprovado

### 4. Recência
O quão recente é a memória, especialmente se:
- o contexto estiver mudando
- a tarefa for contínua
- houver progresso recente relevante

### 5. Escopo
Dar peso conforme o escopo:
- task
- project
- user
- global workflow

## Ordem de prioridade recomendada

Quando houver empate, priorizar:

1. altamente relevante para a tarefa atual
2. importante para evitar erro ou retrabalho
3. estável e durável
4. recente e contextual
5. específica do projeto atual

## Tipos de memória

### Semântica
Fatos duráveis, preferências, decisões estáveis.

Normalmente deve receber peso alto.

### Procedural
Jeitos comprovados de fazer algo.

Recebe peso muito alto quando a tarefa exige execução similar.

### Episódica
Eventos passados, tentativas, erros e resultados.

Recebe peso médio, subindo quando a tarefa atual é continuação direta.

### Ruído operacional
Detalhes temporários e descartáveis.

Recebe peso baixo.

## Processo de ranking

### 1. Identificar contexto atual
Determinar:
- objetivo atual
- projeto atual
- tipo de tarefa
- termos centrais
- restrições relevantes

### 2. Coletar memórias candidatas
Recuperar memórias por busca semântica, leitura de MEMORY.md, índices temáticos e logs recentes.

### 3. Pontuar
Para cada memória, avaliar:
- relevância
- importância
- estabilidade
- recência
- escopo

### 4. Ordenar
Ordenar da mais útil para a menos útil.

### 5. Selecionar
Usar primeiro:
- as memórias mais fortes
- as memórias que mudam decisão
- as memórias que evitam erro
- as memórias que desbloqueiam execução

## Regras

1. Não priorizar apenas o que é recente.
2. Não priorizar apenas o que é durável.
3. O ranking deve depender da tarefa atual.
4. Procedimentos comprovados devem subir quando houver tarefa semelhante.
5. Preferências do usuário devem subir quando afetarem o formato ou a abordagem da resposta.
6. Eventos episódicos só devem dominar se o contexto atual for continuação direta.
7. Ruído operacional deve ficar no fim.

## Critérios de qualidade

Um bom ranking:
- traz o que importa primeiro
- reduz distrações
- melhora foco do agente
- evita recuperação irrelevante
- acelera execução

## Regra suprema

Lembrar de muita coisa não basta.

É preciso lembrar primeiro do que mais importa.
