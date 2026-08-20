# Stack map — Unitree H2 Plus + Isaac GR00T

Public reference (NVIDIA, May 31 2026): Isaac GR00T Reference Humanoid =
Unitree H2 Plus body + Sharpa Wave hands + Jetson Thor + Isaac GR00T software.
Availability: late 2026. G1 GR00T workflow is the current public software path.

## Layers TARX will implement against

### 1. Foundation model

- Repo: NVIDIA/Isaac-GR00T (package name `gr00t`, Python 3.12)
- Current GA model: GR00T N1.7 VLA
- Embodiment tags today include `UNITREE_G1` and `UNITREE_G1_SONIC`
- H2 Plus embodiment is the gap this lane is preparing for

### 2. Whole-body control

- Repo: NVlabs/GR00T-WholeBodyControl
- Decoupled WBC (GR00T N1.5/N1.6) and GEAR-SONIC (N1.7 end-to-end)
- Install extra `gear_sonic[inference]` is the GR00T client path

### 3. Robot OS / I/O

- `unitree_sdk2` — C++ SDK for H2 (and G1/H1/Go2/…)
- `unitree_sdk2_python` — Python bindings
- `unitree_ros` — robot descriptions, including `robots/h2_plus`
- `unitree_model` — USD, including `H2_Plus`

### 4. TARX overlay (this repo, later)

- Local policy/approval around robot actions (governed-agent-contracts)
- Computer-on-Thor runtime contract (no silent cloud escalation)
- Skill/data loop: teleop collect → finetune GR00T → deploy SONIC

## Working assumption

Until NVIDIA publishes an H2 Plus GR00T workflow, develop against G1/SONIC
public APIs and keep H2 Plus notes in this repo as a delta (DoF, hands, Thor).
Do not invent an unofficial `UNITREE_H2` tag and present it as upstream.
