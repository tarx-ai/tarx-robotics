# TARX Robotics

Public beachhead for TARX work on **Unitree H2 Plus** and **NVIDIA Isaac GR00T**.

TARX is preparing the software/OS overlay that sits on the NVIDIA Isaac GR00T
reference humanoid: Unitree H2 Plus chassis, Sharpa Wave hands, Jetson Thor
onboard compute, and Isaac GR00T models/workflows. This repo is the public
tracker, integration notes, and contribution log. It is **not** a dump of
private partner docs, and it does not claim hardware already in-house.

**Status:** software-first. Hardware bring-up follows the public GR00T / Unitree
stack. Canonical product runtime remains TARX Computer; this repo is the
robotics lane.

## Why this exists

1. Show the exact public forks and upstream repos TARX is working against.
2. Track real contributions to leading robotics repositories (not empty forks).
3. Document the H2 Plus OS/runtime plan as it is proven, not as marketing.

## Public forks (TARX org)

| Upstream | TARX fork | Role |
|---|---|---|
| [NVIDIA/Isaac-GR00T](https://github.com/NVIDIA/Isaac-GR00T) | [tarx-ai/Isaac-GR00T](https://github.com/tarx-ai/Isaac-GR00T) | VLA foundation model (N1.7) |
| [NVlabs/GR00T-WholeBodyControl](https://github.com/NVlabs/GR00T-WholeBodyControl) | [tarx-ai/GR00T-WholeBodyControl](https://github.com/tarx-ai/GR00T-WholeBodyControl) | Humanoid whole-body control (GEAR-SONIC) |
| [unitreerobotics/unitree_sdk2](https://github.com/unitreerobotics/unitree_sdk2) | [tarx-ai/unitree_sdk2](https://github.com/tarx-ai/unitree_sdk2) | Real-robot SDK (Go2, B2, H1, G1, H2, R1, A2) |
| [unitreerobotics/unitree_sdk2_python](https://github.com/unitreerobotics/unitree_sdk2_python) | [tarx-ai/unitree_sdk2_python](https://github.com/tarx-ai/unitree_sdk2_python) | Python SDK bindings |
| [unitreerobotics/unitree_ros](https://github.com/unitreerobotics/unitree_ros) | [tarx-ai/unitree_ros](https://github.com/tarx-ai/unitree_ros) | ROS descriptions, including H2 Plus |
| [unitreerobotics/unitree_model](https://github.com/unitreerobotics/unitree_model) | [tarx-ai/unitree_model](https://github.com/tarx-ai/unitree_model) | USD assets, including H2 Plus |

## Target stack (H2 Plus OS layer)

```
Language / skills     TARX Computer  ↔  Isaac GR00T N1.7 (VLA)
Whole-body control    GEAR-SONIC / GR00T-WBC
Robot I/O             Unitree SDK2 + ROS descriptions
Onboard compute       NVIDIA Jetson Thor (reference design)
Body                  Unitree H2 Plus + Sharpa Wave hands
```

See [docs/STACK.md](docs/STACK.md) for the working map and
[docs/STATUS.md](docs/STATUS.md) for what is actually done vs. planned.

## Upstream contributions

Quality bar: one real, reviewable change at a time. No empty forks, no
duplicate issues, no confidential partner material.

| Date | Upstream | Change | State |
|---|---|---|---|
| 2026-07-28 | [NVIDIA/nemoclaw-community#73](https://github.com/NVIDIA/nemoclaw-community/pull/73) | Gate GitHub source ETL behind explicit opt-in | **merged** |
| 2026-07-28 | [NVIDIA/nemoclaw-community#74](https://github.com/NVIDIA/nemoclaw-community/pull/74) | Validate Slack Socket Mode scope before setup | **merged** |
| 2026-07-28 | [NVIDIA/nemoclaw-community#72](https://github.com/NVIDIA/nemoclaw-community/pull/72) | Fail-fast inference preflight | closed (not merged) |
| 2026-08-20 | [NVlabs/GR00T-WholeBodyControl#258](https://github.com/NVlabs/GR00T-WholeBodyControl/pull/258) | Fix `gear_sonic[inference]` package name + Python 3.12 | **open** |

Details: [docs/UPSTREAM.md](docs/UPSTREAM.md).

## What this repo will grow into

- H2 Plus bring-up notes (SDK2, ROS, cameras, hands)
- GR00T N1.7 embodiment config for H2 Plus (when the public workflow lands)
- Local runtime contract: TARX Computer on Thor, approval/evidence around robot actions
- Reproducers and patches destined for upstream, not a private fork forever

## What this repo will not become

- A place for partner outreach, pricing, or NDAs
- A marketing landing page
- A claim that TARX has replaced Unitree or NVIDIA software

## Related public TARX surface

- [tarx.com](https://tarx.com)
- [tarx-ai/tarx-desktop](https://github.com/tarx-ai/tarx-desktop)
- [tarx-ai/governed-agent-contracts](https://github.com/tarx-ai/governed-agent-contracts)

Private hardware design notes stay in `tarx-ai/tarx-hardware`.

## License

Apache-2.0 for TARX-authored files in this repository. Upstream forks keep
their original licenses.
