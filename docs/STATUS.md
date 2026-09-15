# Status — 2026-09-15 (midday downstream)

Honest snapshot.

## Done today

- Public tracker: https://github.com/tarx-ai/tarx-robotics
- TARX OS dependency map: [docs/CORE_DEPS.md](CORE_DEPS.md)
- NVIDIA repo map: [docs/NVIDIA_REPOS.md](NVIDIA_REPOS.md)
- Public forks (PR heads, still listed): Isaac-GR00T, GR00T-WholeBodyControl, IsaacLab, curobo, nemoclaw-community, unitree_sdk2 / python / ros / model
- Open wantzjt NVIDIA/NVlabs PRs (no review comments to fix):
  - https://github.com/NVlabs/GR00T-WholeBodyControl/pull/258
  - https://github.com/NVlabs/curobo/pull/715 (Unitree G1 IK / #706)
- Closed this cycle: NVIDIA/nemoclaw-community#127 — maintainers closed 2026-08-20 (scope: belongs in NVIDIA/NemoClaw, not community examples). Do not reopen there.
- GR00T #745: still no maintainer call; do not wire `use_mean_std`
- tarx-robotics itself has zero public forks and no open inbound PRs

## Not done

- No H2 Plus on the bench
- No Thor bring-up evidence
- Isaac Lab: forked only, no PR yet
- `tarx-os` GitHub repo is not TARX OS and stays private
- This session has no GitHub connector on the Grok Bot computer; write landed via Github Hawk

## Next

1. Wait for review on WBC #258 and curobo #715; fix comments before any new PR
2. Isaac Lab Python 3.12 / Thor install gap only if a real repro exists
3. Keep weekday 08:17 / 12:41 / 16:38; never two new upstream PRs the same day unless the second is a review fix
