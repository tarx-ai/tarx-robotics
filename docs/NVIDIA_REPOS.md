# NVIDIA contribution map

Cadence: weekdays, two passes (morning + afternoon America/New_York).
Quality bar: one real reviewable change per pass, or a documented no-op.
Identity: `wantzjt` / `tarx-ai` forks as PR heads. DCO on every PR.

## Active now

| Repo | Why TARX OS cares | Current work |
|---|---|---|
| [NVIDIA/Isaac-GR00T](https://github.com/NVIDIA/Isaac-GR00T) | VLA core dep | Watch #748; do not wire `use_mean_std` until NVIDIA picks #745 |
| [NVlabs/GR00T-WholeBodyControl](https://github.com/NVlabs/GR00T-WholeBodyControl) | SONIC / H2 body control | [#258](https://github.com/NVlabs/GR00T-WholeBodyControl/pull/258) open |
| [NVlabs/curobo](https://github.com/NVlabs/curobo) | G1/H2 motion | G1 IK benchmark / cspace (#706) |
| [NVIDIA/nemoclaw-community](https://github.com/NVIDIA/nemoclaw-community) | Agent harness TARX already ships into | #73/#74 merged; macOS doctor #103 |
| [isaac-sim/IsaacLab](https://github.com/isaac-sim/IsaacLab) | Train before Thor deploy | Forked; next: install/docs vs Python 3.12 |

## Next (do not spray empty forks)

| Repo | When to touch |
|---|---|
| NVIDIA-ISAAC-ROS/* | Thor camera / NITROS bring-up |
| isaac-sim/IsaacSim | Only with a Lab-blocking sim bug |
| NVIDIA/TensorRT or TensorRT-LLM | Thor engine-build failures (GR00T #575 family) |
| huggingface/lerobot | `groot` policy type interop |

## Hard no

- Duplicate issues for activity
- Drive-by README rewrites
- Opening `tarx-os` or `tarx-hardware`
- Claiming H2 hardware in-house
- Wiring GR00T `use_mean_std` without a maintainer decision on #745
