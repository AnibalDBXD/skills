# Agent Skills

Personal collection of agent skills (Kimi Code / Claude Code / compatible agents).

## Install on another machine

Prerequisites: [Node.js](https://nodejs.org/) (for `npx`) and the [Skills CLI](https://skills.sh).

Install a single skill:

```bash
npx skills add AnibalDBXD/skills@<skill-name> -y
```

Install everything at once:

```bash
npx skills add AnibalDBXD/skills -y
```

Then restart your agent session so the skill catalog reloads.

## Keeping in sync

After adding, removing, or editing skills on any machine:

```bash
git add -A && git commit -m "Update skills" && git push
# and on the other machines:
npx skills update
```

## Skills

| Skill | Purpose |
|---|---|
| animate | Build web animations from scratch |
| animate-expo | Animations in React Native / Expo |
| animation-vocabulary | Glossary of motion/UI effect terms |
| apple-design | Apple's design & motion approach for the web |
| badesign-skill | General UI design judgment |
| better-ui | UI polish details (radius, alignment, depth, hit areas) |
| code-review | Review changes vs. repo standards and spec |
| computer-use | Drive GUI apps via `orca computer` |
| emil-design-eng | Emil Kowalski's design-engineering philosophy |
| find-animation-opportunities | Find what should animate (read-only audit) |
| find-skills | Discover and install skills from skills.sh |
| impeccable | Broad frontend design/polish/redesign skill |
| implement | Implement a ticket/spec with TDD + green validations (invoke manually) |
| improve-animations | Audit and plan motion improvements (read-only) |
| make-repo-contribution | Follow repo guidelines/templates for issues, commits, PRs |
| mobile-native | Make web apps feel native on phones |
| orca-cli | Operate Orca worktrees, terminals, repos |
| pick-ui-library | Choose a UI library |
| prototype | Prototyping |
| review-animations | Review animation code |
| review-pr | Structured PR diff review against spec |
| tdd | Test-driven development (red-green-refactor) |
