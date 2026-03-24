# Agent Lifecycle

The lifecycle defines the execution flow from receiving a task to delivering the final output.

## Lifecycle Stages

```
┌─────────────────────────────────────────────────────────────────┐
│  1. META-REASONING                                              │
│     → Classify task type                                        │
│     → Define strategy                                           │
│     → Set depth level                                           │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  2. SKILL-SELECTION                                             │
│     → Choose relevant skills                                    │
│     → Define execution order                                    │
│     → Prepare pipeline                                          │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  3. CONTEXT-AWARENESS                                           │
│     → Understand user intent                                    │
│     → Gather relevant context                                   │
│     → Identify constraints                                      │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  4. TASK-DECOMPOSITION                                          │
│     → Break into subtasks                                       │
│     → Identify dependencies                                     │
│     → Define execution order                                    │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  5. PRIORITIZATION                                              │
│     → Order by impact                                           │
│     → Consider urgency                                           │
│     → Balance effort vs value                                   │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  6. STATE-MANAGEMENT                                            │
│     → Track progress                                            │
│     → Monitor status                                            │
│     → Manage checkpoints                                        │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  7. TOOL-SELECTION                                              │
│     → Choose appropriate tools                                  │
│     → Validate availability                                     │
│     → Plan execution                                            │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  8. EXECUTION                                                   │
│     → Execute subtasks                                          │
│     → Collect results                                           │
│     → Handle intermediate outputs                              │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  9. ERROR-RECOVERY                                              │
│     → Detect failures                                           │
│     → Classify errors                                           │
│     → Apply fallback strategies                                 │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  10. REFLECTION                                                 │
│     → Review output                                             │
│     → Check quality                                             │
│     → Identify improvements                                     │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  11. GOAL-VERIFICATION                                          │
│     → Validate completion                                       │
│     → Check requirements                                       │
│     → Confirm success                                          │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  12. CONFIDENCE-ESTIMATION                                      │
│     → Assess certainty                                          │
│     → Identify uncertainties                                    │
│     → Adjust language                                           │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────▼────────────────────────────────────┐
│  13. OUTPUT-FORMAT                                              │
│     → Structure response                                        │
│     → Apply formatting                                          │
│     → Ensure clarity                                           │
└─────────────────────────────────────────────────────────────────┘
```

## Simplified Flows

### Simple Task
```
meta-reasoning → context-awareness → reflection → output-format
```

### Complex Task
```
meta-reasoning → skill-selection → task-decomposition → prioritization → 
state-management → tool-selection → execution → error-recovery → 
reflection → goal-verification → output-format
```

### Research Task
```
meta-reasoning → context-awareness → deep-research → 
confidence-estimation → output-format
```

### Decision Task
```
meta-reasoning → decision-making → cost-awareness → 
output-format
```

## Loop Handling

The lifecycle supports loops for:
- Error recovery attempts
- Refinement iterations
- Multiple tool attempts

Maximum iterations: 3 per stage
