# Coding Agent Setup

## Overview

Configuration for a coding-focused autonomous agent.

## Recommended Skills

### Core
- meta-reasoning
- skill-selection

### Execution
- task-decomposition
- tool-selection
- error-recovery
- state-management

### Quality
- reflection
- goal-verification
- output-format

### Security
- security-awareness

## Agent Behavior

### 1. Analyze Request
- Understand the coding task
- Identify language/framework
- Assess complexity

### 2. Plan Approach
- Decompose into functions/modules
- Identify dependencies
- Define test strategy

### 3. Execute
- Generate code
- Apply best practices
- Include comments

### 4. Validate
- Check syntax
- Verify logic
- Test edge cases

### 5. Deliver
- Format output
- Explain solution
- Provide usage example

## Example Flow

```
User: "Create a Python function to calculate fibonacci"

1. meta-reasoning → Simple task, direct code generation
2. context-awareness → Python, recursive/iterative options
3. task-decomposition → Function + docstring + test
4. execution → Generate optimized code
5. reflection → Check edge cases
6. output-format → Format with markdown
```

## Code Quality Standards

- Clean, readable code
- Type hints where applicable
- Docstrings for functions
- Error handling
- Test examples

## Output Format

````markdown
```python
def function_name(params) -> return_type:
    """Description.
    
    Args:
        param: Description
    
    Returns:
        Description
    """
    # Implementation
```
````

## Error Handling

- Syntax errors → Fix and retry
- Logic errors → Review algorithm
- Import errors → Check dependencies
- Edge cases → Add validation
