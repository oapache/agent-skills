# Skill Guide

## Overview

Skills are modular cognitive units that can be dynamically selected based on task requirements.

## SKILL.md Format

Every skill must have a `SKILL.md` file with this structure:

```yaml
---
name: skill-name
description: Short clear description.
metadata: {"openclaw":{"emoji":"🧠","homepage":"..."}}
---

# Skill Name

## Objective
What this skill achieves.

## Process
1. Step one
2. Step two
3. Step three

## Rules
- Rule one
- Rule two

## Supreme Rule
The most important principle.
```

## When to Create a Skill

✅ **Create when:**
- Repeated behavior pattern exists
- Reusable logic across tasks
- Clear cognitive pattern identified
- Single, well-defined responsibility

❌ **Don't create when:**
- Trivial one-line logic
- Overlapping functionality
- Unclear purpose
- Only used once

## Skill Quality Checklist

- [ ] Clear, descriptive name
- [ ] Single responsibility
- [ ] No overlap with existing skills
- [ ] Follows SKILL.md format
- [ ] Has objective, process, rules
- [ ] Includes supreme rule
- [ ] Appropriate emoji
- [ ] Useful for target use cases

## Skill Selection Matrix

| Task Type | Required Skills |
|-----------|----------------|
| Simple Q&A | context-awareness, reflection |
| Technical | tool-selection, error-recovery |
| Research | deep-research, confidence-estimation |
| Decision | decision-making, cost-awareness |
| Complex | task-decomposition, prioritization, state-management |
| Creative | creativity, abstraction |
| Critical | security-awareness, goal-verification |

## Anti-Patterns

### ❌ Skill Overlap
```
Skill A: "Does everything"
Skill B: "Also does everything"
```
**Fix:** Split into focused skills

### ❌ Vague Skill
```
Skill: "Handles things"
```
**Fix:** Define specific purpose

### ❌ Over-Engineering
```
Skill: 500 lines, 50 rules
```
**Fix:** Keep simple, single responsibility

## Best Practices

1. **Keep skills small** - One purpose, few rules
2. **Use consistent format** - SKILL.md standard
3. **Name clearly** - Action verb + object
4. **Document edge cases** - When NOT to use
5. **Include examples** - Show correct usage

## Skill Dependencies

Skills may depend on others:
- execution → core
- research → context-awareness
- quality → execution

Dependency order matters in lifecycle.

## Testing Skills

Test a skill by:
1. Using it in a relevant task
2. Checking output quality
3. Verifying rule adherence
4. Measuring improvement

## Maintenance

Review skills periodically:
- Remove unused skills
- Merge overlapping skills
- Update outdated rules
- Add missing capabilities
