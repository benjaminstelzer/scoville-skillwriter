# Scoville Skillwriter

Scoville Skillwriter writes and reviews Skills and reusable prompts for current
frontier models. It keeps the goal, real constraints and useful context while
cutting repetition and unnecessary ceremony.

Scoville measures chili heat. Skillwriter keeps instructions sharp without
seasoning every sentence with another warning.

## How it works

It combines shared instruction-design rules with an authoring workflow. Approved
revisions preserve the exact pre-edit state for comparison; reviews return
findings without editing. The host's Skill Creator owns Skill structure,
packaging and format validation. Source review and format validation are
reported separately from observed model behavior.

## What it enforces

It preserves the intended outcome, activation boundaries, permissions and
acceptance criteria. It asks only about material changes beyond the request or
prior approval. Changed instructions and affected consumers are checked together
in the existing source review.

## What it costs

The Skill has no paid service calls. Host model usage and any explicitly requested evaluation have their usual costs.

## How it was developed

Maintained in the Scoville Suite source project. Standalone and Suite packages share the same instruction-design source.

### Model tests

On 2026-10-29, controlled local tests in Codex with `gpt-6.1-sol` / `low` loaded
the public Skillwriter entry and the host's Skill Creator. The approved,
limited revision was applied with an exact pre-edit copy retained; metadata
and boundaries were preserved, and a separate review-only copy stayed unchanged.
The host's format validator passed. These observations cover the tested revision
and review cases. This run did not cover other authoring cases, installed
discovery or current Claude behavior; the edited Skills were not executed.

A separate standalone-prompt revision preserved the requested meaning and
baseline. The agent also read Skill Creator outside that fixture's permitted
scope. The task result passed; compliance with that reading boundary did not.

## Compatibility

Requires an Agent Skills host with filesystem access and its Skill Creator for
Skill authoring: OpenAI's in Codex or Anthropic's in Claude Code. Standalone
prompts need no Skill Creator. No runtime scripts or network access are required.

## Install

This Skill works independently. Other Scoville Skills are optional.

### Install this Skill

Ask your agent host:

```text
Install this Skill for all my projects from this exact package directory:
https://github.com/benjaminstelzer/scoville-skillwriter/tree/main/scoville-skillwriter
Preserve personal settings and unrelated Skills. Report the installed location
and whether the host discovers the Skill.
```

The host needs permission to write to its Skills directory. The
[Codex Skills guide](https://learn.chatgpt.com/docs/build-skills) and the
[Claude Code Skills guide](https://code.claude.com/docs/en/skills)
list the locations for each host.

### Install the complete Scoville suite

The complete suite is in the
[Scoville Suite monorepo](https://github.com/benjaminstelzer/scoville-suite).
Install its released Skill packages, not development templates.

## How to use

Ask to write, simplify or review a Skill or reusable prompt, or invoke `$scoville-skillwriter`. For a revision, it respects already approved changes and asks only for changes outside that approval.

## Sources

See the [full instructions](https://github.com/benjaminstelzer/scoville-skillwriter/blob/main/scoville-skillwriter/SKILL.md) and their sources-and-evaluation
reference for the authoring guidance and the distinction between source review,
format validation and observed model behavior. The Skill is also available as
[Scoville Skillwriter](https://github.com/benjaminstelzer/scoville-skillwriter)
outside the suite.

## Family

- [Code](https://github.com/benjaminstelzer/scoville-code) covers engineering scope, implementation, risk and validation.
- [Plan](https://github.com/benjaminstelzer/scoville-plan) keeps Plans, Work Items, Decisions and their status in the repository.
- [UI](https://github.com/benjaminstelzer/scoville-ui) covers UI implementation, information structure, accessibility and rendered checks, with an optional WordPress adapter.
- [Handoff](https://github.com/benjaminstelzer/scoville-handoff) passes active work to another agent or session.
- [Project Context Cleanup](https://github.com/benjaminstelzer/scoville-suite) keeps requested project rules and index text concise without losing required context.
- [Skillwriter](https://github.com/benjaminstelzer/scoville-skillwriter) writes, simplifies and reviews Skills and reusable agent prompts.

## License

MIT. See [LICENSE](LICENSE).
