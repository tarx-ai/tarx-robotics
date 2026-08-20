# Grok Bot standing orders

This is what Grok Bot is for.

Not GTM. Not Apollo hardware outbound. Not empty public beachheads.

## Job

1. **Upstream:** fork the NVIDIA / Unitree / LeRobot repos TARX actually depends on, then land real PRs so TARX is in that graph.
2. **Downstream:** keep a small set of TARX *open* repos standing so outsiders can adopt TARX without the closed control plane.
3. **Honesty:** update this repo the same day a fork or PR happens. No stale tables.

Cadence is weekday, **off the hour**, on purpose:

| Local (America/New_York) | Pass |
|---|---|
| 08:17 | upstream (forks + one PR) |
| 12:41 | downstream (TARX public adoption repos) |
| 16:38 | upstream reviews; no second new PR unless a review fix |

One outcome per run. Quality over volume.

## Strategic upstream forks (`tarx-ai/*`)

Fork only these, public, as PR heads:

- `Isaac-GR00T`
- `GR00T-WholeBodyControl`
- `curobo`
- `IsaacLab`
- `isaac_ros_common`
- `isaac_ros_physical_ai`
- `nemoclaw-community`
- `unitree_sdk2`
- `unitree_sdk2_python`
- `unitree_ros`
- `unitree_model`
- `lerobot`

Do not fork the rest of NVIDIA. Do not treat a fork as a contribution until a PR exists.

## Strategic downstream (TARX open, people adopt these)

Exactly five. Do not add a sixth empty repo.

| Repo | Why it is public |
|---|---|
| [tarx-cli](https://github.com/tarx-ai/tarx-cli) | Install / doctor / route check |
| [tarx-desktop](https://github.com/tarx-ai/tarx-desktop) | Computer-canonical Mac runtime |
| [governed-agent-contracts](https://github.com/tarx-ai/governed-agent-contracts) | Approval / evidence contracts |
| [tarx-examples](https://github.com/tarx-ai/tarx-examples) | Integration patterns (Eve/Connect) |
| [tarx-robotics](https://github.com/tarx-ai/tarx-robotics) | H2 Plus / GR00T overlay tracker |

Stay archived: `tarx`, `tarx-sdk`, `tarx-weights`, `tarx-palantir` empty beachheads.
Stay private: `tarx-os` (not the OS), `tarx-hardware`, `tarx-core`, `tarx-ops`, Supercomputer routing.

## Hard no

- Duplicate issues for activity
- `UNITREE_H2` GR00T tag until NVIDIA publishes it
- Wiring `use_mean_std` without a maintainer call on Isaac-GR00T#745
- Unitree commercial / NDA material
- Mixing this loop with Apollo hardware GTM
