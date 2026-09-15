# Status — 2026-09-15 (afternoon NVIDIA pass)

Honest snapshot. Tracker-only. No new upstream PR this pass.

## Done today

- Public tracker: https://github.com/tarx-ai/tarx-robotics
- TARX OS dependency map: [docs/CORE_DEPS.md](CORE_DEPS.md)
- NVIDIA repo map: [docs/NVIDIA_REPOS.md](NVIDIA_REPOS.md)
- Midday honesty pass already on main: `639b5b5` (STATUS + README #127 closed state)
- Afternoon re-check of public PR pages (documented no-op; cadence forbids a second new upstream PR the same day unless it is a review fix):
  - [NVlabs/GR00T-WholeBodyControl#258](https://github.com/NVlabs/GR00T-WholeBodyControl/pull/258) — still **OPEN**. Reviewers: none. Review comments: 0. Commits: 2 (2026-08-20). Participant: `wantzjt` only.
  - [NVlabs/curobo#715](https://github.com/NVlabs/curobo/pull/715) — still **OPEN**. Reviewers: none. Review comments: 0. Linked to [#706](https://github.com/NVlabs/curobo/issues/706). Commits: 2 (2026-08-20). Participant: `wantzjt` only.
  - [NVIDIA/nemoclaw-community#127](https://github.com/NVIDIA/nemoclaw-community/pull/127) — remains **CLOSED** by `apurvvkumaria` (2026-08-20). Scope: belongs in NVIDIA/NemoClaw, not community examples. Do not reopen. Do not file NemoClaw docs this pass.
- [NVIDIA/Isaac-GR00T](https://github.com/NVIDIA/Isaac-GR00T): no open `wantzjt` PR. Do not wire `use_mean_std`; no maintainer call on #745.
- Public forks (PR heads, still listed): Isaac-GR00T, GR00T-WholeBodyControl, IsaacLab, curobo, nemoclaw-community, unitree_sdk2 / python / ros / model
- tarx-robotics itself has zero public forks and no open inbound PRs

## Not done

- No H2 Plus on the bench
- No Thor bring-up evidence
- No UNITREE_H2 / invented GR00T tags
- Isaac Lab: forked only, no PR yet
- `tarx-os` GitHub repo is not TARX OS and stays private
- `tarx-hardware` stays private
- No confidential Unitree commercial docs in this tracker
- This session has no GitHub connector on the Grok Bot computer; write landed via Github Hawk

## Next

1. Wait for review on WBC #258 and curobo #715; fix comments before any new PR
2. Isaac Lab / Isaac ROS / cuRobo Unitree gaps only with a real repro — not today
3. Keep weekday 08:17 / 12:41 / 16:38; never two new upstream PRs the same day unless the second is a review fix
