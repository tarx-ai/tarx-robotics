# TARX OS ↔ NVIDIA core dependencies

TARX OS is the **governed local runtime** (Computer by default, Supercomputer
by permission). It does **not** replace NVIDIA or Unitree software. It sits
above them: policy, memory, approvals, evidence, and routing.

Public contract surface: `tarx-cli`, `governed-agent-contracts`, `tarx-desktop`,
this repo. Private control plane (`tarx-ops`, `tarx-core`, Supercomputer routing)
stays closed. The GitHub repo named `tarx-os` is a stale Next.js dump and is
**not** the OS.

## Dependency stack (H2 Plus lane)

```
TARX Computer overlay     policy, memory, approval, evidence     CLOSED runtime / OPEN contracts
        ↑
Isaac GR00T N1.7          VLA / skills                           NVIDIA/Isaac-GR00T
GEAR-SONIC / GR00T-WBC    whole-body control                     NVlabs/GR00T-WholeBodyControl
cuRobo / cuMotion         motion generation (research/product)   NVlabs/curobo
Isaac ROS + NITROS        cameras, perception, Thor deploy       NVIDIA-ISAAC-ROS
Isaac Lab + Isaac Sim     train / sim                            isaac-sim/IsaacLab
Unitree SDK2 + ROS/USD    robot I/O, H2 Plus descriptions        unitreerobotics/*
JetPack / CUDA / TensorRT Thor onboard compute                   CUDA 13.2 / JP 7.x on Thor
```

## Pinned public versions (software-first, 2026-08-20)

| Layer | Package / product | Constraint that TARX OS must honor |
|---|---|---|
| Language | Python | **3.12** for GR00T N1.7 (`requires-python >=3.12,<3.13`) |
| VLA | `gr00t` (not `Isaac-GR00T`) | PEP 508 name in `NVIDIA/Isaac-GR00T` pyproject |
| WBC | `gear_sonic[inference]` | Pulls `gr00t` from git; inference venv must be 3.12 |
| Motion | cuRobo `unitree_g1.yml` | cspace must match kinematic tree after #678 |
| Edge | Jetson AGX Thor | GR00T N1.7 ~8.9 Hz eager / 12.4 Hz TensorRT |
| Train | Isaac Lab 3.x + Isaac Sim | Separate from onboard Thor runtime |
| Robot I/O | unitree_sdk2 | H2 / G1 / H1 real robot |
| TARX overlay | Computer + contracts | No silent cloud; robot actions are approved effects |

Do not invent an unofficial `UNITREE_H2` GR00T embodiment tag. Public GR00T
still documents `UNITREE_G1` / `UNITREE_G1_SONIC`. H2 Plus is a delta on that
path until NVIDIA publishes the reference workflow.

## What TARX OS owns vs what NVIDIA owns

| Concern | Owner |
|---|---|
| Joint commands, WBC, VLA weights | NVIDIA + Unitree |
| Cameras, NITROS, Thor JetPack | NVIDIA Isaac ROS |
| Simulation / RL | Isaac Lab |
| Whether a skill may run, on which model, with what evidence | **TARX OS** |
| Partner commercials, SKUs, NDAs | never in this public repo |

## Related public TARX contracts

- [tarx-cli](https://github.com/tarx-ai/tarx-cli) — `tarx route check local`
- [governed-agent-contracts](https://github.com/tarx-ai/governed-agent-contracts) — proposal → decision → result
- [tarx-desktop](https://github.com/tarx-ai/tarx-desktop) — Computer-canonical Mac runtime
