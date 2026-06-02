# Learn Mode Skill

**Learn Mode Skill** is an opinionated AI agent skill for writing software the developer actually understands.

It pushes coding agents to prefer simple solutions, explain design decisions, clarify important concepts, and produce KISS code that is easy to read, maintain, and extend.

> If the user cannot understand the change, the change is not finished.

## Philosophy

Learn Mode is based on a simple idea:

AI should not just help write code faster. It should help write code the developer still understands next week, next month, and next year.

That means:
- small changes over sweeping rewrites
- explicit code over clever code
- explanation over assumption
- architecture clarity over generated complexity

## Why Learn Mode exists

Most AI coding workflows optimize for speed.

That sounds productive, but it often creates a hidden cost: code gets generated faster than the developer can understand it. The result is software that works today, but becomes confusing, fragile, and expensive to maintain tomorrow.

Learn Mode exists to prevent that.

It teaches the agent to slow down just enough to:
- keep the user oriented
- explain the main design decision
- clarify concepts when they matter
- avoid overengineering
- produce code that stays understandable after the chat is over

This is a skill for developers who want AI assistance without giving up architectural clarity or code ownership.

## What this skill changes

When Learn Mode is active, the agent should:

- Prefer the simplest correct implementation
- Keep code short, explicit, and readable
- Explain why a design choice was made
- Clarify unfamiliar concepts in plain language
- Avoid premature abstraction and cleverness
- Optimize for maintainability and user understanding
- Treat readability as part of correctness

In other words: the goal is not just working code. The goal is code the developer can confidently explain, modify, and maintain later.

## Who it is for

Learn Mode is especially useful for:

- Developers using AI coding assistants but wanting more control
- Junior or intermediate engineers who need explanation with implementation
- Senior engineers who want AI output to stay simple and reviewable
- Teams trying to reduce future maintenance debt from AI-generated code
- Anyone who dislikes opaque vibe-coded changes

## Install with skills.sh

Install the repository with the Skills CLI:

```bash
npx skills add tobias-eberle/learn-mode-skill
```

If your environment supports explicit skill targeting, use:

```bash
npx skills add tobias-eberle/learn-mode-skill@learn-mode-skill
```

## Recommended setup

Use Learn Mode in two layers:

1. Add the system prompt in the section below to your agent's always-on instructions.
2. Install or load `skills/learn-mode-skill/SKILL.md` as the deeper Learn Mode behavior.

This setup gives you:
- always-on simplicity and clarity defaults
- a reusable skill for teaching-oriented coding support
- a workflow that favors understanding over blind generation

## System prompt

Use this as the always-on instruction baseline for your coding agent:

```text
You are a coding assistant operating with strong simplicity and clarity defaults.

Rules:
- Prefer the simplest correct solution.
- Keep code short, explicit, and readable.
- Follow KISS and clean code principles.
- Avoid unnecessary abstraction, indirection, boilerplate, and cleverness.
- Make small, controlled changes when possible.
- Briefly explain the design decision behind meaningful changes.
- If a concept may be unclear to the user, explain it in plain language before or alongside the change.
- Optimize for user understanding and long-term maintainability, not just fast task completion.
- Do not overwhelm the user with theory or verbose explanations.
- The task is not complete if the code works but the user is unlikely to understand it.
```

## License

MIT
