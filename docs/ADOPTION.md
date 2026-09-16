# Upstream and downstream adoption

```
NVIDIA / Unitree / LeRobot / Isaac ROS     ← upstream PRs (TARX in their graph)
        ↑ fork + patch
TARX public repos (this set of five)       ← downstream adoption (people use TARX)
        ↑ contracts only
TARX Computer / ops / memory               CLOSED
```

Upstream without downstream is unpaid NVIDIA labor with no TARX surface.
Downstream without upstream is a marketing org with no robotics proof.
Grok Bot does both.

## Upstream (TARX → their repos)

Credible only as merged or open PRs, not forks.

| Upstream | TARX fork | Open work |
|---|---|---|
| NVIDIA/Isaac-GR00T | tarx-ai/Isaac-GR00T | #748 comment; wait on #745 |
| NVlabs/GR00T-WholeBodyControl | tarx-ai/GR00T-WholeBodyControl | [#258](https://github.com/NVlabs/GR00T-WholeBodyControl/pull/258) |
| NVlabs/curobo | tarx-ai/curobo | [#715](https://github.com/NVlabs/curobo/pull/715) |
| NVIDIA/nemoclaw-community | tarx-ai/nemoclaw-community | `#73/#74 merged; #127 closed (wrong repo; do not reopen)` |
| isaac-sim/IsaacLab | tarx-ai/IsaacLab | fork only so far |
| NVIDIA-ISAAC-ROS/isaac_ros_common | tarx-ai/isaac_ros_common | Thor / JetPack common |
| NVIDIA-ISAAC-ROS/isaac_ros_physical_ai | tarx-ai/isaac_ros_physical_ai | humanoid WBC bring-up |
| huggingface/lerobot | tarx-ai/lerobot | `groot` policy type |
| unitreerobotics/* sdk2 ros model | tarx-ai/* | H2 Plus I/O |

## Downstream (their agents/devs → TARX)

They should hit these five, then MCP/CLI, not `tarx-os`.

| They want | Send them |
|---|---|
| Install TARX | tarx-cli + tarx-desktop |
| Governed actions | governed-agent-contracts |
| GitHub/Slack/Linear tether | tarx-examples |
| H2 Plus / GR00T overlay | tarx-robotics |
| Runtime internals | do not publish |
