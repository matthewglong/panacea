---
description: "Start a Socratic tutoring session on a topic or question"
allowed-tools:
  - Read
  - Grep
  - Glob
  - Task
argument-hint: "<topic>"
---

# /tutor command

The user wants to start a Socratic tutoring session on the following topic:

**{{ topic }}**

Launch the `socrates` agent to guide the student through this topic using Socratic questioning. The agent should:

1. Acknowledge the topic the student wants to explore
2. Ask an opening question to gauge the student's current understanding
3. Continue with Socratic dialogue from there

Do NOT provide any direct answers or explanations about the topic. All learning must happen through guided questioning.
