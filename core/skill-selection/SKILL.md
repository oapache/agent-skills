---
name: skill-selection
description: Seleciona quais skills devem ser utilizadas para resolver a tarefa, orquestrando comportamento do agente de forma estratégica e eficiente.
metadata: {"openclaw":{"emoji":"🧠","homepage":"https://github.com/seu-user/agent-skills/tree/main/skill-selection"}}
---

# Skill Selection

Use esta skill no início de qualquer tarefa ou sempre que houver dúvida sobre qual abordagem seguir.

## Objetivo

Garantir que o agente:
- escolha as skills corretas para cada situação
- não use todas as skills indiscriminadamente
- organize o fluxo de execução de forma eficiente
- adapte seu comportamento ao tipo de tarefa

---

## Regra principal

Nem toda skill deve ser usada.

Escolha apenas as necessárias.

---

## Processo de seleção

### 1. Classificar a tarefa

Identificar o tipo de problema:

- simples (resposta direta)
- técnico (código, sistema, análise)
- investigativo (pesquisa, exploração)
- operacional (execução de ações)
- ambíguo (falta contexto)
- iterativo (múltiplas etapas)

---

### 2. Mapear necessidades

Perguntar internamente:

- Precisa de planejamento?
- Precisa dividir tarefa?
- Precisa usar tools?
- Precisa buscar informação?
- Precisa memória?
- Precisa validar resultado?
- Pode gerar erro?
- Precisa revisar saída?

---

### 3. Selecionar skills

Ativar apenas as relevantes.

---

## Mapeamento de skills

### Para tarefas complexas
- task-decomposition
- planning
- state-management

### Para pesquisa
- deep-research
- free-web-research
- context-awareness

### Para execução
- tool-selection
- error-recovery

### Para qualidade
- reflection
- goal-verification

### Para continuidade
- persistent-memory

---

## Exemplos

### Exemplo 1
Pergunta: "WanGP funciona na RTX 3070?"

Skills:
- context-awareness
- deep-research
- tool-selection
- reflection

---

### Exemplo 2
Pergunta: "Crie uma API"

Skills:
- task-decomposition
- planning
- state-management
- reflection
- goal-verification

---

### Exemplo 3
Pergunta: "Corrige esse código"

Skills:
- context-awareness
- debugging
- reflection

---

### Exemplo 4
Pergunta: "Explique o que é REST"

Skills:
- nenhuma complexa
- apenas raciocínio

---

## Regras de prioridade

### Alta prioridade
- context-awareness
- reflection

### Condicional
- deep-research
- tool-selection
- task-decomposition
- error-recovery

### Finalização
- goal-verification

---

## Regras anti-caos

1. Não ativar todas as skills.
2. Não repetir skills sem necessidade.
3. Não usar skill sem propósito claro.
4. Não ignorar skills essenciais.

---

## Sinais de seleção ruim

- uso excessivo de skills
- ausência de planejamento em tarefas complexas
- ausência de validação final
- respostas desalinhadas

---

## Estratégia dinâmica

Durante a execução, o agente pode:

- adicionar novas skills
- remover skills desnecessárias
- mudar estratégia conforme progresso

---

## Comportamento esperado

O agente deve agir como um orquestrador:

- escolhe ferramentas mentais certas
- adapta abordagem
- evita desperdício
- mantém foco no objetivo

---

## Regra suprema

Não use todas as skills.

Use as skills certas.
