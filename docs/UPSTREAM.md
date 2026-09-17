# Upstream contribution log

## NVIDIA NemoClaw Community (2026-07-28 → 2026-08-03)

Grok-bot loop that proved the quality bar, then went idle.

- [#73 merged](https://github.com/NVIDIA/nemoclaw-community/pull/73) by NVIDIA (`apurvvkumaria`) — GitHub ETL opt-in
- [#74 merged](https://github.com/NVIDIA/nemoclaw-community/pull/74) by NVIDIA (`apurvvkumaria`) — Slack Socket Mode preflight
- [#72 closed](https://github.com/NVIDIA/nemoclaw-community/pull/72) — inference preflight; reused as product proof in TARX CLI

## Isaac GR00T / GR00T-WBC (2026-08-20)

Observed on current `NVIDIA/Isaac-GR00T` `pyproject.toml`:

- `[project] name = "gr00t"`
- `requires-python = ">=3.12,<3.13"`

Observed on current `NVlabs/GR00T-WholeBodyControl`:

- `gear_sonic[inference]` depended on `Isaac-GR00T @ git+https://github.com/NVIDIA/Isaac-GR00T.git`
- `install_scripts/install_inference.sh` created a Python 3.10 venv

That pair matches [Isaac-GR00T#748](https://github.com/NVIDIA/Isaac-GR00T/issues/748):

```
Package metadata name `gr00t` does not match given name `Isaac-GR00T`
```

Fix is in GR00T-WholeBodyControl, not Isaac-GR00T.

- Branch: `tarx-ai/GR00T-WholeBodyControl` `fix/isaac-gr00t-dep-name-python312`
- PR: https://github.com/NVlabs/GR00T-WholeBodyControl/pull/258
- Still waiting on #258/#715 as of 2026-09-17
- Issue comment: https://github.com/NVIDIA/Isaac-GR00T/issues/748#issuecomment-5361863159

## Do not

- Duplicate #748 with a second Isaac-GR00T issue
- Publish Unitree commercial proposals or hardware partner trackers
- Treat forks as contributions until a PR exists
