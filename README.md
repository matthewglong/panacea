# So-Crates

A Claude Code plugin that transforms Claude into a Socratic tutor — guiding learning through probing questions instead of giving direct answers.

## Installation

Add this plugin to your Claude Code setup by placing it in your plugins directory or cloning the repository:

```bash
git clone <repo-url> ~/.claude/plugins/so-crates
```

## Usage

Start a tutoring session with the `/tutor` command:

```
/tutor recursion
/tutor how does binary search work
/tutor why is my React component re-rendering
```

The tutor will ask questions to gauge your understanding and guide you toward the answer step by step. It will never give you the answer directly.

## Components

### `/tutor` Command

Launches a Socratic tutoring session on any topic. Pass your question or topic as an argument.

### Socratic Tutor Agent

An autonomous agent that guides students through Socratic dialogue. It has read-only access to your codebase (Read, Grep, Glob) so it can ask relevant questions about your actual code — but it will never write solutions for you.

Automatically triggered when you ask to "learn", "understand", or explore a concept.

### Socratic Method Skill

Reference material on Socratic questioning techniques including six question types, adaptive scaffolding strategies by skill level, and common anti-patterns to avoid.

### Overseer Hook

A `SubagentStop` hook that reviews every tutor response before it reaches you. If the tutor accidentally leaks a direct answer, the hook blocks the response and forces a rephrase. This ensures the no-direct-answers rule is enforced even if the tutor's system prompt is insufficient.

## How It Works

1. You ask `/tutor <topic>` or describe something you want to learn
2. The so-crates agent starts a dialogue, asking questions to assess your level
3. It adapts its questions based on your responses — simpler for beginners, more probing for advanced students
4. The overseer hook screens every response to ensure no answers leak through
5. When you reach understanding, the tutor asks you to summarize what you learned

## License

MIT
