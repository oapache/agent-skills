---
name: free-web-research
description: Pesquisa termos desconhecidos na internet usando busca pública, variações de nome e fontes técnicas antes de pedir esclarecimento ao usuário.
metadata: {"openclaw":{"emoji":"🌐","homepage":"https://github.com/oapache/free-web-research"}}
---

# Free Web Research

Use esta skill quando o usuário mencionar um termo desconhecido, um projeto, software, biblioteca, ferramenta ou nome possivelmente ambíguo.

## Objetivo

Encontrar informações públicas úteis na internet antes de pedir esclarecimento ao usuário.

## Regras principais

1. Nunca pedir contexto imediatamente para um termo desconhecido sem antes tentar pesquisar.
2. Sempre testar variações prováveis do nome.
3. Priorizar fontes técnicas e primárias.
4. Se houver múltiplos significados, escolher o mais provável com base no contexto.
5. Só pedir esclarecimento ao usuário se, depois da pesquisa, o termo continuar ambíguo.

## Estratégia de busca

Ao receber um termo desconhecido:
- pesquisar o termo exato entre aspas
- pesquisar versões sem aspas
- pesquisar variações ortográficas prováveis
- combinar com palavras como:
  - github
  - docs
  - huggingface
  - requirements
  - install
  - rtx 3070
  - vram
  - issue

## Fontes prioritárias

1. Repositório oficial
2. Documentação oficial
3. Página do modelo
4. Issues e discussões técnicas
5. Comunidade técnica relevante

## Procedimento

### 1. Resolver o nome
Gerar variações prováveis:
- singular/plural
- acrônimo expandido
- trocas comuns
- versões com números
- possíveis nomes alternativos

### 2. Buscar
Executar buscas públicas nas fontes prioritárias.

### 3. Validar
Confirmar:
- o que é
- para que serve
- requisitos
- compatibilidade com o hardware citado
- limitações conhecidas

### 4. Responder
Entregar:
- identificação do projeto
- resumo do que ele faz
- resposta objetiva à pergunta do usuário
- incertezas, se houver

## Regra anti-preguiça

Não devolver "não encontrei" sem antes:
- tentar ao menos 3 buscas
- testar variação do nome
- consultar ao menos 2 fontes técnicas
