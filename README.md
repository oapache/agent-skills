# 🧠 Agent Skills Pack

A modular cognitive skill system for autonomous agents using OpenClaw.

## 🚀 Overview

This repository provides a complete set of composable skills to build autonomous agents capable of:

- reasoning
- planning
- researching
- executing tasks
- handling errors
- validating results
- making decisions

## 🧩 Skill Categories

### Core
- autonomous-agent-core
- skill-selection
- meta-reasoning
- abstraction
- creativity
- security-awareness

### Execution
- task-decomposition
- prioritization
- state-management
- tool-selection
- error-recovery
- cost-awareness

### Research
- context-awareness
- free-web-research
- deep-research

### Memory
- persistent-memory

### Quality
- reflection
- goal-verification
- output-format
- confidence-estimation

### Decision
- decision-making

## 🔁 Agent Lifecycle

```
meta-reasoning → skill-selection → context-awareness → task-decomposition → 
prioritization → state-management → tool-selection → execution → 
error-recovery → reflection → goal-verification → confidence-estimation → output-format
```

## ⚙️ Usage

Clone into your OpenClaw skills directory:

```bash
git clone https://github.com/oapache/agent-skills ~/.openclaw/workspace/skills
```

## 📁 Structure

```
agent-skills/
├── README.md
├── LICENSE
├── skills/
│   ├── core/
│   ├── execution/
│   ├── research/
│   ├── memory/
│   ├── quality/
│   ├── decision/
├── docs/
│   ├── architecture.md
│   ├── lifecycle.md
│   ├── skill-guide.md
└── examples/
    ├── coding-agent.md
    ├── research-agent.md
```

## 📚 Documentation

- [Architecture](docs/architecture.md) - System design
- [Lifecycle](docs/lifecycle.md) - Execution flow
- [Skill Guide](docs/skill-guide.md) - How to use skills
- [Examples](examples/) - Agent configurations

## ⚡ Quick Start

1. Identify the task type
2. Select relevant skills
3. Follow the lifecycle
4. Validate output

## 📖 License

MIT - See LICENSE file
