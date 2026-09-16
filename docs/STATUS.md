# Status — 2026-09-16 (midday downstream)

Honest snapshot. Tracker-only on `tarx-ai/tarx-robotics`. No NVIDIA/NVlabs comments this pass.

## Done this pass

- Public tracker: https://github.com/tarx-ai/tarx-robotics
- ADOPTION table: NemoClaw row now `#73/#74 merged; #127 closed (wrong repo; do not reopen)`
- README Related public TARX surface: five-set complete (`tarx.com`, `tarx-cli`, `tarx-desktop`, `tarx-examples`, `governed-agent-contracts`)
- NVIDIA-org `wantzjt` PRs: **no open**. Closed: nemoclaw-community #73/#74 **merged**; #72/#127 **closed**
- NVlabs `wantzjt` PRs still **OPEN**, reviews 0, review comments 0, issue comments 0 — leave them; do not comment:
  - [GR00T-WholeBodyControl#258](https://github.com/NVlabs/GR00T-WholeBodyControl/pull/258)
  - [curobo#715](https://github.com/NVlabs/curobo/pull/715)
- All 12 required public `tarx-ai` forks still exist: Isaac-GR00T, GR00T-WholeBodyControl, curobo, IsaacLab, isaac_ros_common, isaac_ros_physical_ai, nemoclaw-community, unitree_sdk2, unitree_sdk2_python, unitree_ros, unitree_model, lerobot
- tarx-robotics: 0 public forks, 0 open inbound PRs; topics: gr00t, humanoid, isaac, jetson, nvidia, robotics, unitree
- Five adoption READMEs: no secret dumps. `tarx-examples` Eve channels remain source/typechecked, **not** live-verified
- No `UNITREE_H2` tag. Do not wire `use_mean_std` (Isaac-GR00T#745 still no maintainer call)

## Not done

- No H2 Plus on the bench
- No Thor bring-up evidence
- Isaac Lab: forked only, no PR yet
- `tarx-os` GitHub repo is not TARX OS and stays private
- `tarx-hardware` stays private

## Next

1. Wait for review on WBC #258 and curobo #715; fix comments before any new PR
2. Isaac Lab / Isaac ROS / cuRobo Unitree gaps only with a real repro
3. Keep weekday 08:17 / 12:41 / 16:38; never two new upstream PRs the same day unless the second is a review fix
