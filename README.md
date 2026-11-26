# Agent Skills

Personal curated collection of agent skills for Kimi Code, Claude Code, Devin, Codex, and compatible agents.

The collection is intentionally curated rather than exhaustive: overlapping broad skills are removed or made manual, while narrow skills with clear routing stay automatic.

## Install on another machine

Prerequisites: [Node.js](https://nodejs.org/) (for `npx`) and the [Skills CLI](https://skills.sh).

Install a single skill:

```bash
npx skills add AnibalDBXD/skills@<skill-name> -y
```

Install selected skills:

```bash
npx skills add AnibalDBXD/skills --skill test-driven-development systematic-debugging verification-before-completion -y
```

Install everything at once:

```bash
npx skills add AnibalDBXD/skills -y
```

Then restart your agent session so the skill catalog reloads.

> **Note:** installing everything includes Superpowers. That is a deliberately opinionated development methodology: it asks agents to brainstorm, plan, test first, review, and verify before claiming completion. Install only the skills you want if you prefer a lighter agent.

## Keeping in sync

After adding, removing, or editing skills on any machine:

```bash
git add -A && git commit -m "Update skills" && git push
# and on the other machines:
npx skills update
```

Upstream sources, snapshot commits, and license texts are tracked in [NOTICE.md](NOTICE.md).

## Curation rules

1. **Superpowers owns the software-development workflow.** The older `implement` and `tdd` skills were removed because they contradicted and duplicated `executing-plans`, `subagent-driven-development`, and `test-driven-development`.
2. **`impeccable` is the broad automatic UI-design skill.** `badesign-skill` remains available as a manual second opinion, but is hidden from automatic invocation so the two do not compete for every design request.
3. **Motion skills are narrow and lifecycle-based.** Build with `animate`, `animate-expo`, `choreograph`, or `apple-design`; audit with `improve-animations`; find missing motion with `find-animation-opportunities`; debug jank with `animation-performance`; review only when explicitly requested with `review-animations`.
4. **Tool-specific skills stay scoped.** Orca skills only apply to Orca; `review-pr` only applies to machine-readable PR-review workflows; `code-review` remains for explicit branch/diff reviews.
5. **Deprecated upstream names are not kept as aliases.** `computer-use` was replaced by the upstream-renamed `orca-computer-use`.

## Skills

### Software development workflow — Superpowers

| Skill | Purpose |
| --- | --- |
| using-superpowers | Bootstrap skill-use discipline at the start of a conversation |
| brainstorming | Draw out intent and design before building |
| writing-plans | Turn an approved design into a detailed implementation plan |
| executing-plans | Execute a plan inline, task by task |
| subagent-driven-development | Execute independent plan tasks through reviewed subagents |
| dispatching-parallel-agents | Coordinate independent parallel agent work |
| using-git-worktrees | Isolate feature work in a worktree |
| test-driven-development | Strict red-green-refactor implementation |
| systematic-debugging | Root-cause debugging before fixes |
| verification-before-completion | Require evidence before claiming success |
| requesting-code-review | Request review at task and merge gates |
| receiving-code-review | Evaluate and respond to review feedback rigorously |
| finishing-a-development-branch | Decide how to integrate completed work |
| writing-skills | Create and test new skills |
| diagnosing-superpowers | Diagnose when a Superpowers session went wrong |

### Reviews, contribution, and discovery

| Skill | Purpose |
| --- | --- |
| code-review | Review a branch or diff against repository standards and the originating spec |
| review-pr | Produce machine-readable `review.json` feedback for automated PR workflows |
| make-repo-contribution | Follow repository contribution rules for issues, branches, commits, and PRs |
| find-skills | Discover and install skills from the open skills ecosystem |

### Interface design and polish

| Skill | Purpose |
| --- | --- |
| impeccable | Broad product/UI design, redesign, critique, audit, polish, motion, accessibility, and design-system workflow |
| better-ui | Exact surface and icon polish values: radii, optical alignment, shadows, outlines, icon states |
| badesign-skill | Manual-only concise design judgment and anti-generic-UI checklist |

### Motion, interaction, and mobile

| Skill | Purpose |
| --- | --- |
| animate | Build a web animation from scratch |
| animate-expo | Build animations and gestures in React Native/Expo |
| choreograph | Coordinate multi-element and sequenced motion |
| animation-performance | Diagnose and fix dropped frames/janky motion |
| animation-vocabulary | Translate vague motion descriptions into exact terms |
| apple-design | Apple-style fluid interfaces, springs, gestures, momentum, and materials |
| emil-design-eng | Emil Kowalski's fallback design-engineering philosophy for component interactions and polish |
| find-animation-opportunities | Find missing motion opportunities without editing code |
| improve-animations | Audit existing motion and write prioritized implementation plans |
| mobile-native | Make web apps feel native on phones |
| pick-ui-library | Manual-only curated frontend library picker |
| prototype | Manual-only multi-variant UI prototyping behind a visual picker |
| review-animations | Manual-only strict review of animation code |

### Platform/tool-specific

| Skill | Purpose |
| --- | --- |
| orca-cli | Operate Orca worktrees, terminals, repos, automation, and embedded browser |
| orca-computer-use | Drive local application GUIs through Orca computer use |

## Upgrade notes

- `implement` was removed; use `executing-plans` or `subagent-driven-development` depending on whether the work should run inline or through subagents.
- `tdd` was removed; use `test-driven-development`.
- `computer-use` was removed; use `orca-computer-use`.
- `badesign-skill`, `pick-ui-library`, `prototype`, and `review-animations` are manual-only (`disable-model-invocation: true`). Invoke them explicitly by name when wanted.
