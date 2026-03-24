---
name: autonomous-agent-core
description: Planeja, executa em loop, usa ferramentas, valida resultados e corrige erros ao resolver tarefas complexas.
metadata: {"openclaw":{"emoji":"🧠","homepage":"https://github.com/seu-user/autonomous-agent-core","requires":{"bins":["bash"]}}}
---

# Autonomous Agent Core

Use esta skill quando o usuário pedir execução autônoma, resolução em múltiplas etapas, planejamento, uso de ferramentas, validação de resultado ou correção iterativa.

## Quando usar
- Tarefas com vários passos
- Automação
- Execução orientada a objetivo
- Uso de ferramentas, scripts ou comandos
- Casos em que seja necessário revisar a própria saída

## Regras operacionais
1. Sempre decompor tarefas complexas em subtarefas.
2. Antes de agir, definir objetivo, restrições e próximo passo.
3. Operar no ciclo: pensar → agir → observar → corrigir.
4. Usar ferramentas em vez de adivinhar quando houver forma verificável de obter dados.
5. Validar o resultado antes de encerrar.
6. Se houver falha, tentar outra abordagem em vez de repetir cegamente.
7. Encerrar apenas quando o objetivo estiver realmente concluído.

## Procedimento
### 1. Planejar
- Identificar objetivo final
- Listar subtarefas
- Definir ordem de execução

### 2. Executar
- Realizar a menor ação útil seguinte
- Registrar resultado observado

### 3. Refletir
- Verificar se a ação aproximou do objetivo
- Detectar erros, lacunas ou inconsistências

### 4. Ajustar
- Replanejar se necessário
- Repetir até concluir

## Critérios de qualidade
- Resultado verificável
- Sem etapas faltando
- Sem assumir fatos não confirmados
- Sem encerrar cedo demais
