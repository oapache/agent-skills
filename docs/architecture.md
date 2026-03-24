# Architecture

## Overview

The Agent Skills framework is a modular cognitive system designed for autonomous agents. It provides a collection of composable skills that can be dynamically selected and combined based on task requirements.

## Design Principles

1. **Single Responsibility** - Each skill has one clear purpose
2. **Composability** - Skills work together in chains
3. **Context-Aware** - Skills adapt to task type
4. **Minimal** - No unnecessary complexity

## System Components

```
┌─────────────────────────────────────────────────┐
│                 Meta Controller                  │
│  (meta-reasoning → skill-selection)              │
└─────────────────────┬───────────────────────────┘
                      │
          ┌───────────▼───────────┐
          │    Skill Pipeline     │
          │                       │
          │  ┌─────┐  ┌─────┐   │
          │  │Skill│→ │Skill│→  │
          │  └─────┘  └─────┘   │
          │      ↓               │
          │  ┌─────────┐        │
          │  │Output   │        │
          │  └─────────┘        │
          └─────────────────────┘
```

## Skill Categories

### Core Skills
Fundamental cognitive abilities:
- autonomous-agent-core: Main execution loop
- skill-selection: Dynamic skill selection
- meta-reasoning: Strategy selection
- abstraction: Problem simplification
- creativity: Creative problem solving
- security-awareness: Security considerations

### Execution Skills
Task execution and control:
- task-decomposition: Breaking down tasks
- prioritization: Ordering by impact
- state-management: Tracking progress
- tool-selection: Choosing right tools
- error-recovery: Handling failures
- cost-awareness: Resource optimization

### Research Skills
Information gathering:
- context-awareness: Understanding context
- free-web-research: Web search
- deep-research: Deep investigation

### Memory Skills
Persistence:
- persistent-memory: Long-term memory

### Quality Skills
Validation:
- reflection: Self-review
- goal-verification: Completion check
- output-format: Presentation
- confidence-estimation: Uncertainty measurement

### Decision Skills
Decision making:
- decision-making: Option evaluation

## Data Flow

```
Input → Meta → Skills → Output → Validation → Complete
```

## Configuration

Skills can be enabled/disabled based on:
- Task type
- User preferences
- Resource constraints
- Security requirements

## Extensibility

Add new skills by:
1. Creating skill folder
2. Adding SKILL.md with proper format
3. Categorizing appropriately
4. Updating documentation
