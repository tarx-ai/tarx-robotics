# Status — 2026-09-16 (morning upstream)

Honest snapshot. Tracker-only. No new NVIDIA/NVlabs PR this pass (reviews beat new work; none arrived).

## Done this pass

- Public tracker: https://github.com/tarx-ai/tarx-robotics
- TARX OS dependency map: [docs/CORE_DEPS.md](CORE_DEPS.md)
- NVIDIA repo map: [docs/NVIDIA_REPOS.md](NVIDIA_REPOS.md)
- Fork check (all 12 required public `tarx-ai` forks **exist**; none forked today):
  - [Isaac-GR00T](https://github.com/tarx-ai/Isaac-GR00T) ← NVIDIA/Isaac-GR00T
  - [GR00T-WholeBodyControl](https://github.com/tarx-ai/GR00T-WholeBodyControl) ← NVlabs
  - [curobo](https://github.com/tarx-ai/curobo) ← NVlabs
  - [IsaacLab](https://github.com/tarx-ai/IsaacLab) ← isaac-sim/IsaacLab
  - [isaac_ros_common](https://github.com/tarx-ai/isaac_ros_common) ← NVIDIA-ISAAC-ROS
  - [isaac_ros_physical_ai](https://github.com/tarx-ai/isaac_ros_physical_ai) ← NVIDIA-ISAAC-ROS
  - [nemoclaw-community](https://github.com/tarx-ai/nemoclaw-community) ← NVIDIA
  - [unitree_sdk2](https://github.com/tarx-ai/unitree_sdk2), [unitree_sdk2_python](https://github.com/tarx-ai/unitree_sdk2_python), [unitree_ros](https://github.com/tarx-ai/unitree_ros), [unitree_model](https://github.com/tarx-ai/unitree_model) ← unitreerobotics
  - [lerobot](https://github.com/tarx-ai/lerobot) ← huggingface/lerobot
- Babysit (read-only; no new comments):
  - [NVlabs/GR00T-WholeBodyControl#258](https://github.com/NVlabs/GR00T-WholeBodyControl/pull/258) — still **OPEN**. Reviews: 0. Review comments: 0. Issue comments: 0. Leave it.
  - [NVlabs/curobo#715](https://github.com/NVlabs/curobo/pull/715) — still **OPEN**. Reviews: 0. Review comments: 0. Issue comments: 0. Leave it.
  - [NVIDIA/nemoclaw-community#127](https://github.com/NVIDIA/nemoclaw-community/pull/127) — remains **CLOSED** (2026-08-20; scope belongs in NVIDIA/NemoClaw). Do not reopen. Do not comment.
- Open `wantzjt` PRs on NVlabs: **only** #258 and #715. Open on NVIDIA orgs: **none**. No newer open PR than those.
- GR00T #745: still no maintainer call; do not wire `use_mean_std`
- No `UNITREE_H2` tag invented or applied
- tarx-robotics: zero public forks; no open inbound PRs

## Not done

- No H2 Plus on the bench
- No Thor bring-up evidence
- Isaac Lab: forked only, no PR yet
- `tarx-os` GitHub repo is not TARX OS and stays private
- `tarx-hardware` stays private
- No confidential Unitree commercial docs in this tracker

## Next

1. Wait for review on WBC #258 and curobo #715; fix comments before any new PR
2. Isaac Lab / Isaac ROS / cuRobo Unitree gaps only with a real repro
3. Keep weekday 08:17 / 12:41 / 16:38; never two new upstream PRs the same day unless the second is a review fix
