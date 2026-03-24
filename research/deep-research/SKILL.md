---
name: deep-research
description: Realiza pesquisa aprofundada com expansão de consulta, variações de termos, coleta em múltiplas fontes, validação cruzada, síntese estruturada e identificação de incertezas.
metadata: {"openclaw":{"emoji":"🔎","homepage":"https://github.com/seu/oapache/deep-research"}}
---

# Deep Research

Use esta skill quando o usuário pedir investigação ampla, informações completas, comparação de fontes, validação técnica, análise detalhada ou pesquisa profunda sobre qualquer tema.

## Objetivo

Produzir respostas com alta cobertura, boa profundidade e qualidade de evidência.

O agente deve:
- entender a pergunta real
- decompor o tema em subquestões
- pesquisar em múltiplas fontes
- priorizar fontes primárias e técnicas
- validar consistência entre evidências
- apontar incertezas e lacunas
- entregar síntese útil, não apenas links

## Quando usar
- pesquisas técnicas
- comparação de ferramentas, modelos ou tecnologias
- compatibilidade de hardware e software
- análise de projetos, bibliotecas ou frameworks
- perguntas abertas que exigem investigação real
- temas desconhecidos ou ambíguos
- pedidos de "pesquise tudo", "aprofunde", "me traga o máximo possível"

## Regras principais

1. Nunca responder com base em uma única busca rasa.
2. Nunca parar na primeira fonte útil.
3. Sempre expandir a pesquisa em subtemas relevantes.
4. Priorizar fontes primárias antes de comunidade ou agregadores.
5. Confirmar afirmações importantes com mais de uma evidência quando possível.
6. Distinguir claramente:
   - fato confirmado
   - inferência provável
   - hipótese/incerteza
7. Não pedir esclarecimento cedo demais se houver caminho razoável para investigar.
8. Não devolver apenas links; devolver entendimento.
9. Se houver conflito entre fontes, explicitar o conflito.
10. Encerrar somente após cobrir o núcleo da pergunta e suas implicações práticas.

## Estratégia geral de pesquisa

Para toda pesquisa, seguir este fluxo:

### 1. Entender a pergunta
Identificar:
- o objeto principal
- o objetivo real do usuário
- o tipo de resposta esperada
- restrições implícitas
- recorte prático da pergunta

### 2. Decompor em subquestões
Transformar a pergunta em blocos investigáveis.

Exemplo:
Pergunta: "Isso roda numa RTX 3070?"

Subquestões:
- o que é a ferramenta?
- quais são os requisitos oficiais?
- há relatos reais de uso na RTX 3070?
- quais limitações existem?
- qual é a VRAM mínima aceitável?
- há otimizações ou perfis específicos?

### 3. Expandir termos de busca
O agente deve gerar:
- nome exato
- variações ortográficas
- aliases
- versões com números
- nomes antigos ou alternativos
- combinações com termos técnicos relevantes

### 4. Buscar em múltiplas fontes
Ordem de prioridade:

1. Repositório oficial
2. Documentação oficial
3. Páginas oficiais do projeto/modelo
4. Issues e discussões técnicas
5. Benchmarks, testes ou exemplos reais
6. Comunidade técnica relevante
7. Vídeos, blogs e fóruns como suporte secundário

### 5. Extrair dados relevantes
Coletar:
- o que é
- para que serve
- requisitos
- compatibilidade
- limitações
- performance
- setup
- riscos
- alternativas
- estado atual do projeto

### 6. Validar
Confirmar se a informação:
- vem da fonte original
- está atualizada
- é coerente com outras fontes
- é observação isolada ou padrão recorrente

### 7. Sintetizar
Responder de forma estruturada:
- identificação
- resumo técnico
- resposta objetiva
- detalhes importantes
- limitações
- incertezas
- recomendação prática

## Fontes prioritárias por tipo

### Projetos e software
- repositório oficial
- README
- docs
- release notes
- issues
- discussions

### Modelos de IA
- Hugging Face
- repositório oficial
- docs do autor
- exemplos de inferência
- requisitos de VRAM
- issues de instalação e compatibilidade

### Hardware e compatibilidade
- documentação oficial
- issues de usuários
- benchmarks
- tabelas de requisitos
- comparações práticas

### Bibliotecas e frameworks
- documentação oficial
- changelog
- issues
- exemplos de uso
- discussões sobre breaking changes

## Procedimento operacional

### Etapa 1. Resolver o nome
Se o termo for estranho ou raro:
- tentar o termo literal
- tentar versões sem aspas
- tentar aliases
- tentar variações prováveis
- tentar contexto técnico junto

### Etapa 2. Mapear o tema
Antes de responder, identificar:
- definição
- escopo
- status atual
- ecossistema
- dependências relevantes

### Etapa 3. Cobrir profundidade
A pesquisa deve tentar responder, quando aplicável:
- o que é?
- como funciona?
- requisitos?
- limitações?
- estado atual?
- compatibilidade?
- performance?
- riscos?
- alternativas?
- recomendação prática?

### Etapa 4. Cruzar evidência
Ao encontrar informação importante:
- confirmar em outra fonte
- verificar se é oficial ou relato informal
- marcar confiança da evidência

### Etapa 5. Produzir resposta final
A resposta deve conter:
- resumo em linguagem clara
- resposta direta à pergunta
- detalhes técnicos relevantes
- pontos de atenção
- o que está confirmado
- o que ainda é incerto

## Regras de profundidade

Uma pesquisa é considerada superficial se fizer apenas um destes:
- usar uma única query
- ler uma única fonte
- responder sem comparar evidências
- ignorar aliases e variações do termo
- ignorar limitações e contradições

Uma pesquisa é considerada profunda quando:
- cobre múltiplos subtemas
- usa múltiplas fontes
- valida os pontos críticos
- identifica conflitos
- entrega síntese contextualizada

## Regras anti-alucinação

1. Não assumir que o nome digitado está perfeito.
2. Não assumir que uma issue isolada representa regra geral.
3. Não transformar hipótese em fato.
4. Não esconder incerteza.
5. Não inventar compatibilidade sem evidência.
6. Não citar requisito sem indicar se é oficial ou empírico.

## Regras anti-preguiça

Antes de concluir "não encontrei", o agente deve tentar:
- pelo menos 3 buscas diferentes
- pelo menos 2 variações do termo
- pelo menos 2 tipos de fonte
- pelo menos 1 tentativa em fonte primária

## Heurísticas úteis

- "funciona em X GPU?" → buscar requisitos + relatos reais + issues
- "vale a pena?" → buscar comparação + limitações + estado atual
- "como instalar?" → buscar docs + README + issues de instalação
- "qual melhor?" → comparar critérios, não só opinião solta
- "pesquise tudo sobre isso" → decompor em definição, requisitos, compatibilidade, riscos, alternativas e status atual

## Estrutura sugerida para resposta

Sempre que possível, responder neste formato:

### 1. O que é
Definição curta e precisa.

### 2. Resposta direta
A resposta objetiva para a pergunta do usuário.

### 3. Evidências principais
Os fatos mais importantes levantados na pesquisa.

### 4. Limitações ou riscos
Onde a resposta pode mudar conforme contexto.

### 5. Recomendação prática
O que o usuário deveria fazer com base nisso.

## Critérios de qualidade

Uma boa pesquisa profunda deve:
- responder a pergunta real
- reduzir ambiguidades
- cobrir contexto importante
- ter base em evidência
- ser útil para decisão prática
- deixar claras as incertezas

## Comportamento esperado

O agente deve agir como um pesquisador técnico disciplinado:
- curioso
- sistemático
- cético
- orientado a evidência
- focado em resposta útil

## Regra suprema

Não pare quando encontrar uma resposta.

Pare quando entender o tema o suficiente para responder com confiança.
