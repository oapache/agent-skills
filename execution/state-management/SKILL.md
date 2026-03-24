---
name: state-management
description: Rastreia o estado da execução, mantém progresso da tarefa, evita loops infinitos e reduz decisões aleatórias durante a resolução de objetivos em múltiplas etapas.
metadata: {"openclaw":{"emoji":"⚙️","homepage":"https://github.com/seu-user/state-management","requires":{"bins":["bash"]}}}
---

# State Management

Use esta skill quando a tarefa tiver múltiplas etapas, depender de progresso incremental, exigir controle de execução ou correr risco de repetição, perda de contexto ou loop infinito.

## Objetivo

Manter um estado interno claro da tarefa para que cada ação tenha contexto, continuidade e propósito.

O agente deve sempre saber:
- o objetivo atual
- o que já foi concluído
- o que ainda falta
- qual foi o último resultado observado
- qual é a próxima ação mais útil
- se há bloqueios, falhas ou dependências pendentes

## Quando usar
- tarefas longas
- automações em etapas
- execução com tools
- fluxos com tentativa e erro
- tarefas com dependências
- objetivos que podem gerar repetição ou desorganização

## Regras principais

1. Antes de agir, inicializar o estado da tarefa.
2. Após cada ação, atualizar o estado com o resultado observado.
3. Nunca agir sem saber qual é a próxima etapa pendente.
4. Nunca repetir uma ação idêntica sem registrar por que ela será repetida.
5. Se a mesma ação falhar mais de uma vez, marcar bloqueio e mudar de estratégia.
6. Sempre distinguir entre:
   - concluído
   - em andamento
   - pendente
   - bloqueado
   - falhou
7. Encerrar apenas quando todas as etapas necessárias estiverem concluídas ou quando houver bloqueio real explicitamente identificado.

## Estrutura do estado

O agente deve manter internamente uma estrutura equivalente a esta:

```json
{
  "goal": "objetivo final da tarefa",
  "status": "in_progress",
  "completed_steps": [],
  "pending_steps": [],
  "current_step": null,
  "last_action": null,
  "last_observation": null,
  "partial_results": [],
  "errors": [],
  "blocked_reasons": [],
  "next_action": null
}
```
