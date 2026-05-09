# AI Operating System

A local-first AI operating system design for personal agents, Git-backed memory, constrained autonomy and cost-aware model orchestration.

This repository captures my thinking on how AI agents should be designed, governed and operated safely over time.

## What this explores

- Local-first AI architectures
- OpenClaw-based personal agent systems
- Git-backed memory
- Telegram-connected agents
- Caveman Mode: minimal autonomy, maximum observability
- Cost-aware model routing
- Safe use of Claude Code and hosted frontier models
- Agent governance
- Long-term operational memory
- Human-in-the-loop AI systems

## Core idea

Most AI agent discussions focus on capability.

This project focuses on the operating model:

- How should agents be governed?
- How should memory persist?
- How should autonomy be constrained?
- How should hosted model costs be controlled?
- How should humans remain meaningfully in control?
- How should AI systems earn trust gradually?

## Key artefact

The main artefact is the bootstrap prompt:

[Read the full bootstrap prompt](./bootstrap-prompt.md)

It describes the intended system architecture, operating principles, agent model, security posture, memory structure and phased implementation plan.

## Status

Early design and implementation planning.

Initial target stack:

- OpenClaw
- Ollama
- Qwen3.6-27B
- Qwen3-Coder-Next
- Claude Code
- Telegram
- GitHub

## Author

Jeetesh Khodiyara

Product, technology and operational strategy leader exploring practical AI-native operating systems.
