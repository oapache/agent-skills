---
name: tool-selection
description: Seleciona a ferramenta mais adequada para cada etapa da tarefa, evita uso desnecessário de tools e reduz decisões erradas durante a execução.
metadata: {"openclaw":{"emoji":"🧰","homepage":"https://github.com/seu-user/agent-skills/tree/main/tool-selection"}}
---

# Tool Selection

Use esta skill quando a tarefa exigir escolha entre múltiplas ferramentas, busca de dados verificáveis, execução externa, leitura de arquivos, pesquisa web, automação ou qualquer ação que possa ser feita com tools.

## Objetivo

Garantir que o agente:
- escolha a ferramenta certa para a tarefa certa
- não tente resolver por suposição o que pode ser verificado
- não use tool quando raciocínio puro for suficiente
- reduza erros causados por uso incorreto de ferramentas

## Quando usar
- pesquisa na internet
- leitura de arquivos ou documentos
- execução de comandos
- chamadas de API
- automação
- análise de logs
- tarefas com múltiplas tools disponíveis
- qualquer tarefa em que o próximo passo dependa de ação externa

## Regras principais

1. Antes de agir, decidir se a tarefa exige tool ou apenas raciocínio.
2. Se existir uma forma verificável de obter o dado, preferir tool em vez de assumir.
3. Escolher a tool mais específica e confiável para o objetivo.
4. Não usar várias tools sem necessidade.
5. Validar se a saída da tool realmente responde à pergunta.
6. Se a tool falhar, escolher fallback adequado em vez de insistir cegamente.
7. Nunca chamar tool só por hábito.
8. Nunca evitar tool quando ela é claramente necessária.

## Princípio central

Use raciocínio para decidir.

Use tool para verificar, obter, executar, ler ou medir.

## Processo de seleção

### 1. Classificar a necessidade
Antes de qualquer ação, o agente deve decidir se precisa:
- pensar
- buscar
- ler
- executar
- validar
- modificar
- comparar

### 2. Determinar se tool é necessária
Use tool quando a tarefa depender de:
- informação externa
- estado atual do mundo
- arquivo real
- execução real
- medição real
- consulta verificável

Não use tool quando a tarefa for:
- explicação conceitual geral
- reorganização de texto
- resumo de conteúdo já fornecido
- raciocínio abstrato sem dependência externa

### 3. Escolher a melhor tool
Critérios:
- mais específica para a tarefa
- mais confiável
- menor custo operacional
- menor risco de erro
- melhor formato de saída para o próximo passo

### 4. Validar a saída
Após usar a tool:
- verificar se a saída é relevante
- verificar se está completa
- verificar se responde ao objetivo atual

### 5. Decidir próximo passo
Depois da tool, escolher entre:
- responder
- usar outra tool
- replanejar
- tentar fallback

## Heurísticas por tipo de tarefa

### Pesquisa sobre termo, projeto, software ou compatibilidade
Preferir:
- busca web
- repositório oficial
- docs
- issues
- discussões técnicas

### Ler conteúdo já fornecido pelo usuário
Preferir:
- leitura de arquivo
- parser de documento
- busca interna em arquivo

### Confirmar estado atual ou dado dinâmico
Preferir:
- busca web
- consulta de API
- ferramenta de sistema

### Executar ação no ambiente
Preferir:
- terminal
- comando
- script
- runtime apropriado

### Comparar opções
Preferir:
- coleta estruturada com tool
- depois síntese por raciocínio

## Regras anti-erro

1. Não usar raciocínio para adivinhar algo que pode ser consultado.
2. Não usar web search quando o dado já está no arquivo local.
3. Não usar execução de comando para algo que pode ser respondido diretamente.
4. Não chamar múltiplas tools para a mesma função sem motivo.
5. Não assumir que a primeira tool escolhida foi a ideal.
6. Não confundir "tool disponível" com "tool necessária".

## Regras anti-preguiça

1. Se a pergunta envolver mundo real, atualidade, compatibilidade, versão ou estado externo, considerar tool obrigatória.
2. Se houver termo desconhecido, tentar pesquisa antes de pedir contexto ao usuário.
3. Se a resposta depender de evidência, buscar evidência.
4. Se a tool falhar, tentar outra abordagem útil antes de desistir.

## Estratégia de fallback

Se a tool ideal falhar:
1. identificar por que falhou
2. escolher tool alternativa ou fonte alternativa
3. ajustar a consulta
4. continuar a tarefa sem repetir cegamente

Exemplos:
- busca falhou → tentar variação do termo
- docs insuficientes → consultar repositório ou issues
- comando falhou → revisar ambiente e parâmetros
- arquivo não encontrado → usar busca de arquivo antes de perguntar

## Sinais de que a tool errada foi escolhida

- a saída não responde à pergunta
- a saída é genérica demais
- a saída é incompleta
- a ação não altera o estado esperado
- a mesma tool precisaria ser usada repetidamente sem progresso

Quando isso acontecer:
- reconsiderar a escolha da tool
- mudar estratégia

## Critérios de boa seleção

Uma boa seleção de tool:
- aproxima diretamente do objetivo
- reduz incerteza
- economiza passos
- produz evidência útil
- evita retrabalho

## Exemplos

### Exemplo 1
Pergunta: "WanGP funciona na RTX 3070?"

Escolha correta:
- usar busca web
- priorizar repositório, docs e relatos técnicos

Escolha errada:
- pedir contexto imediatamente
- responder por suposição

### Exemplo 2
Pergunta: "Resume este texto que já te mandei"

Escolha correta:
- não usar web
- usar apenas o conteúdo fornecido

Escolha errada:
- buscar na internet algo que já está no contexto

### Exemplo 3
Pergunta: "Esse script roda aqui?"

Escolha correta:
- analisar código
- verificar ambiente
- executar ou simular, se possível

Escolha errada:
- responder sem checar dependências

## Matriz de decisão

Pergunte internamente:

1. O que eu preciso agora?
- saber algo?
- verificar algo?
- executar algo?
- ler algo?
- modificar algo?

2. Esse objetivo depende de informação externa ou estado real?
- se sim, usar tool
- se não, raciocínio pode bastar

3. Qual tool tem a menor distância até a resposta?
- escolher a mais direta e confiável

## Comportamento esperado

O agente deve agir como um operador disciplinado:
- não improvisa quando pode verificar
- não consulta ferramenta sem necessidade
- não insiste em ferramenta ruim
- escolhe a menor alavanca capaz de mover o problema

## Regra suprema

Não use tool por impulso.
Não responda por suposição quando a tool é necessária.

Escolha a ferramenta pela necessidade da tarefa, não pela conveniência do hábito.
