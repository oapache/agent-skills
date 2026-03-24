# Research Agent Setup

## Overview

Configuration for a research-focused autonomous agent.

## Recommended Skills

### Core
- meta-reasoning
- skill-selection
- context-awareness

### Research
- free-web-research
- deep-research
- abstraction

### Quality
- reflection
- confidence-estimation
- output-format

### Decision
- decision-making

## Agent Behavior

### 1. Understand Query
- Identify research question
- Determine scope
- Plan search strategy

### 2. Gather Information
- Search multiple sources
- Expand query variations
- Prioritize primary sources

### 3. Analyze
- Cross-reference findings
- Identify patterns
- Assess reliability

### 4. Synthesize
- Create coherent answer
- Support with evidence
- Acknowledge limitations

### 5. Present
- Structure clearly
- Use confidence levels
- Provide citations

## Example Flow

```
User: "Does WanGP work on RTX 3070?"

1. meta-reasoning → Research task, need multiple sources
2. context-awareness → GPU compatibility question
3. deep-research → 
   - Search WanGP requirements
   - Search RTX 3070 specs
   - Find user reports
4. confidence-estimation → Assess evidence strength
5. output-format → Structured answer with confidence
```

## Research Quality Standards

- Multiple sources
- Cross-validation
- Source attribution
- Uncertainty acknowledgment
- Practical recommendations

## Confidence Levels

### High
- Multiple consistent sources
- Official documentation
- Recent reports

### Medium
- Limited sources
- Some inconsistencies
- Older data

### Low
- Single source
- Contradicting reports
- Speculative

## Output Format

```markdown
## Research: [Topic]

### Summary
[2-3 sentence answer]

### Evidence
- [Source 1] - [Finding]
- [Source 2] - [Finding]

### Confidence: [HIGH/MEDIUM/LOW]

### Limitations
[Acknowledged uncertainties]

### Recommendation
[If applicable]
```

## Source Priority

1. Official documentation
2. GitHub repos/releases
3. Technical discussions
4. User reports
5. Blog posts/videos

## Validation Checklist

- [ ] Multiple sources consulted
- [ ] Sources verified
- [ ] Contradictions addressed
- [ ] Confidence assessed
- [ ] Limitations noted
