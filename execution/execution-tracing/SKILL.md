---
name: execution-tracing
description: Registra ações, decisões e resultados durante a execução para permitir análise e debugging.
metadata: {"openclaw":{"emoji":"📡","homepage":"https://github.com/oapache/agent-skills/tree/main/execution-tracing"}}
---

# Execution Tracing

Use durante toda execução relevante.

## Objetivo
Criar rastreabilidade completa do comportamento.

## Registrar

- ação executada
- skill utilizada
- decisão tomada
- tool chamada
- resultado obtido
- erro ocorrido
- mudança de estratégia

## Formato

```json
{
  "step": "",
  "skill": "",
  "action": "",
  "result": "",
  "status": ""
}
```

## Regras

- registrar antes de agir
- atualizar após resultado
- mantertrace para análise

## Regra suprema

Se não foi registrado, não aconteceu.
