# Scoville Skillwriter

Scoville Skillwriter writes and reviews Skills and reusable prompts for current
frontier models. It keeps the goal, real constraints and useful context while
cutting repetition and unnecessary ceremony.

Scoville measures chili heat. Skillwriter keeps instructions sharp without
seasoning every sentence with another warning.

## How it works

- By default it writes for Claude Opus 5.5, Claude Fable 5.1+, GPT-6.1 Sol and
  GPT Astra 6+.
- The intended outcome, activation boundaries, permissions and acceptance
  criteria survive a revision. It asks only about material changes beyond what
  you requested or approved.
- An approved revision keeps the exact state from before the edit for
  comparison. A review returns findings and edits nothing.
- The host's Skill Creator owns Skill structure, packaging and format
  validation.
- It reports what it read in the source apart from what a model was actually
  observed doing.

## How to use

Ask it to write, simplify or review a Skill or a reusable prompt:

```text
Use Scoville Skillwriter to review this Skill for repetition and unclear activation. Report findings without editing.
```

## Install

Needs an Agent Skills host with filesystem access and its Skill Creator:
OpenAI's in Codex or Anthropic's in Claude Code. A standalone prompt needs no
Skill Creator.

Use `gpt-6.2-sol` or Claude Opus 5.5 at medium reasoning effort or higher. Below
that, steps get skipped more often.

Ask your agent host:

```text
Install this Skill for all my projects from this exact package directory:
https://github.com/benjaminstelzer/scoville-skillwriter/tree/main/scoville-skillwriter
Preserve personal settings and unrelated Skills. Report the installed location
and whether the host discovers the Skill.
```

The host needs write access to its Skills directory. The
[Codex](https://learn.chatgpt.com/docs/build-skills) and
[Claude Code](https://code.claude.com/docs/en/skills) Skills guides say where
that is. This Skill works on its own. The other Scoville Skills are in the
[Scoville Suite](https://github.com/benjaminstelzer/scoville-suite).

## Background

Skillwriter grew from maintaining Skills and reusable prompts in real
projects. Repeated rules and explanations made instructions longer without
making them clearer.

On one task that simplified an overloaded Skill, `gpt-6.1-sol` and Claude
Opus 5.5 kept every checked rule with Skillwriter and without it, so that
test shows neither an advantage nor harm.

The [full instructions](https://github.com/benjaminstelzer/scoville-skillwriter/blob/main/scoville-skillwriter/SKILL.md) are what the agent reads.
Its [sources](scoville-skillwriter/references/sources-and-evaluation.md) list
what the writing rules build on.

## License

MIT. See [LICENSE](LICENSE).
