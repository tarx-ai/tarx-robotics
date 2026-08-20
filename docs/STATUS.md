# Status — 2026-08-20

Honest snapshot. Update this file when something actually changes.

## Done today

- Public repo created: `tarx-ai/tarx-robotics`
- Forked leading stacks into `tarx-ai` (Isaac-GR00T, GR00T-WholeBodyControl, unitree_sdk2, unitree_sdk2_python, unitree_ros, unitree_model)
- Diagnosed grok-bot drop-off: NVIDIA NemoClaw PRs landed 2026-08-03, then the loop went idle. Grok Bot workstream remaining was Apollo hardware GTM, not robotics OSS.
- First GR00T-lane patch prepared: `gear_sonic[inference]` package name `Isaac-GR00T` → `gr00t`, and inference venv Python 3.10 → 3.12 (Isaac-GR00T requires `>=3.12,<3.13`)

## Not done

- No Unitree H2 Plus on the bench yet
- No Thor bring-up evidence
- No H2 Plus GR00T embodiment tag (public GR00T still documents G1 / SONIC first; H2 Plus reference workflow is expected later)
- `tarx-ai/tarx-hardware` stays **private** (partner/outreach notes, not public code)
- `tarx-ai/tarx-os` is **not** the robot OS and must not be made public (committed env files)

## Next 7 days

1. Land or iterate the GR00T-WBC install PR
2. Read Isaac-GR00T `getting_started/finetune_new_embodiment.md` and `real_world_deployment.md` against H2 Plus SDK2/ROS
3. Inventory `unitree_ros/robots/h2_plus` and `unitree_model/H2_Plus`
4. Daily grok-bot: one real upstream candidate, or a documented no-op if nothing qualifies
5. Keep GTM hardware outbound (`apollo-hardware-ramp`) separate from this OSS lane
