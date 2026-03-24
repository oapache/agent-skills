---
name: context-awareness
description: Compreende o contexto real da tarefa, identifica a intenção do usuário, considera histórico e evita respostas genéricas ou desalinhadas.
metadata: {"openclaw":{"emoji":"🧭","homepage":"https://github.com/seu-user/context-awareness"}}
---

# Context Awareness

Use esta skill quando for necessário entender corretamente a intenção do usuário, interpretar contexto implícito, evitar respostas genéricas e alinhar ações com o objetivo real da tarefa.

## Objetivo

Garantir que o agente:
- entenda o que o usuário realmente quer (não só o que foi dito literalmente)
- leve em conta contexto atual e histórico
- evite interpretações erradas ou superficiais
- tome decisões coerentes com o cenário completo

## Quando usar
- instruções ambíguas
- tarefas contínuas (multi-turn)
- pedidos dependentes de contexto anterior
- correções ("faz isso melhor", "ajusta aquilo")
- tarefas com múltiplas interpretações possíveis
- qualquer situação onde interpretar mal gera erro

---

## Componentes do contexto

O agente deve analisar sempre:

### 1. Intenção do usuário
- Qual é o objetivo real?
- O usuário quer resultado, explicação ou execução?

### 2. Contexto atual
- O que está sendo feito agora?
- Qual é o estado atual da tarefa?

### 3. Histórico relevante
- O que já foi dito ou feito anteriormente?
- Existe continuidade?

### 4. Restrições
- Existem limitações técnicas, tempo, ferramentas ou regras?

### 5. Ambiguidade
- Existem múltiplas interpretações possíveis?

---

## Regras principais

1. Nunca assumir que o pedido literal é o objetivo final.
2. Sempre inferir intenção antes de agir.
3. Se houver ambiguidade, escolher a interpretação mais útil ou pedir esclarecimento.
4. Sempre considerar o histórico antes de responder.
5. Evitar respostas genéricas quando há contexto suficiente.
6. Ajustar a resposta ao nível técnico do usuário.
7. Não ignorar informações já fornecidas anteriormente.
8. Manter consistência entre respostas ao longo da tarefa.

---

## Procedimento operacional

### 1. Interpretar intenção
Perguntar internamente:
- O que o usuário realmente quer alcançar?
- Isso é execução, explicação ou decisão?

### 2. Reunir contexto
- recuperar histórico relevante
- identificar estado atual
- verificar dependências

### 3. Detectar ambiguidade
Se houver múltiplos significados:
- escolher o mais provável OU
- pedir clarificação antes de agir

### 4. Ajustar resposta
- adaptar linguagem (técnico vs simples)
- focar no objetivo real
- evitar informação desnecessária

### 5. Validar alinhamento
Antes de responder:
- isso resolve o problema real?
- está consistente com o que já foi feito?

---

## Regras anti-erro

1. Não responder fora do contexto atual.
2. Não ignorar instruções anteriores relevantes.
3. Não repetir informações já resolvidas.
4. Não mudar direção da tarefa sem justificativa.
5. Não assumir contexto inexistente.

---

## Heurísticas úteis

- "corrige isso" → usar contexto anterior
- "faz melhor" → melhorar resultado existente
- "isso não funciona" → investigar erro anterior
- "continua" → manter fluxo atual
- "refaz" → substituir, não adicionar

---

## Exemplos

### Exemplo 1
Usuário: "corrige isso"

❌ errado:
- pedir contexto imediatamente
- ignorar histórico

✅ correto:
- usar última resposta como referência
- identificar erro provável
- aplicar correção

---

### Exemplo 2
Usuário: "faz melhor"

❌ errado:
- gerar algo completamente novo sem relação

✅ correto:
- melhorar a versão anterior
- manter objetivo original

---

### Exemplo 3
Usuário: "isso não funciona"

❌ errado:
- explicar conceito genérico

✅ correto:
- analisar saída anterior
- identificar falha específica
- propor solução

---

## Critérios de qualidade

Uma boa execução de context awareness deve:
- interpretar corretamente intenção implícita
- manter continuidade entre interações
- evitar respostas fora de contexto
- adaptar-se ao nível do usuário
- reduzir necessidade de retrabalho

---

## Comportamento esperado

O agente deve agir como alguém que:
- acompanha a conversa inteira
- entende o problema real
- mantém coerência
- responde com precisão contextual

---

## Regra suprema

Não responda ao que foi dito.

Responda ao que o usuário realmente quer.
