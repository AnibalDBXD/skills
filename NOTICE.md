# Upstream attribution

This repository redistributes a curated set of agent skills. The upstream projects, the snapshot currently vendored here, and their licenses are listed below. Full license texts live in [`licenses/`](licenses/).

| Upstream | Skills used here | Snapshot | License |
| --- | --- | --- | --- |
| [obra/superpowers](https://github.com/obra/superpowers) | `brainstorming`, `diagnosing-superpowers`, `dispatching-parallel-agents`, `executing-plans`, `finishing-a-development-branch`, `receiving-code-review`, `requesting-code-review`, `subagent-driven-development`, `systematic-debugging`, `test-driven-development`, `using-git-worktrees`, `using-superpowers`, `verification-before-completion`, `writing-plans`, `writing-skills` | `22f0b463e7a5e579904dd6211a520321035526f7` (v7.0.2, 2026-11-03) | MIT — [`licenses/superpowers-MIT.txt`](licenses/superpowers-MIT.txt) |
| [emilkowalski/skills](https://github.com/emilkowalski/skills) | `animate`, `animate-expo`, `animation-performance`, `animation-vocabulary`, `apple-design`, `choreograph`, `emil-design-eng`, `find-animation-opportunities`, `improve-animations`, `mobile-native`, `pick-ui-library`, `prototype`, `review-animations` | `64eb3deb9a5fbfa041faf783e0bc3fd635872e9c` (2026-11-15) | MIT — [`licenses/emilkowalski-MIT.txt`](licenses/emilkowalski-MIT.txt) |
| [pbakaus/impeccable](https://github.com/pbakaus/impeccable) | `impeccable` | `2fc5e1459efbbf06d92c7306517c286bf12490cf` (v4.11.1, 2026-11-26) | Apache 2.0 — [`licenses/impeccable-Apache-2.0.txt`](licenses/impeccable-Apache-2.0.txt) |
| [jakubkrehel/skills](https://github.com/jakubkrehel/skills) | `better-ui` | `672ae44ace6aaed65b86cbb1e2fd6fbea0e79578` (2026-11-18) | MIT — [`licenses/jakubkrehel-MIT.txt`](licenses/jakubkrehel-MIT.txt) |
| [uxKero/badesign-skill](https://github.com/uxKero/badesign-skill) | `badesign-skill` | `8273d49e9e72378e9b45e658dba4369e531e0a5d` (2026-09-13) | MIT — [`licenses/badesign-MIT.txt`](licenses/badesign-MIT.txt) |
| [stablyai/orca](https://github.com/stablyai/orca) | `orca-cli`, `orca-computer-use` | `4d4e19de072f9ffeb67c8db50463fa4fc1beb266` (2026-11-25) | MIT — [`licenses/orca-MIT.txt`](licenses/orca-MIT.txt) |
| [mattpocock/skills](https://github.com/mattpocock/skills) | `code-review` | `6f7f7831a625f040a8e06a0e7954826b87ce775a` (2026-11-25) | MIT — [`licenses/mattpocock-MIT.txt`](licenses/mattpocock-MIT.txt) |
| [warpdotdev/common-skills](https://github.com/warpdotdev/common-skills) | `review-pr` | `8792394ff1b655e0af451b8fabb68ef0cfcbd208` (2026-10-20) | MIT — [`licenses/warp-common-skills-MIT.txt`](licenses/warp-common-skills-MIT.txt) |

## Local curation changes

- `badesign-skill` carries `disable-model-invocation: true` so it remains available as an explicit second opinion without competing with `impeccable` for every broad UI-design request.
- Skills are copied into a flat repository layout so the Skills CLI can discover each directory. Relative sibling references inside the skills are preserved by that layout.
- No other upstream skill content is intentionally modified in this snapshot.

`find-skills` and `make-repo-contribution` are local utility skills maintained in this repository rather than copied from the upstream snapshots above.
