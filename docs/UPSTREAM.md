# Upstream contribution log

## NVIDIA NemoClaw Community (2026-07-28 → 2026-08-03)

Grok-bot loop that proved the quality bar, then went idle.

- [#73 merged](https://github.com/NVIDIA/nemoclaw-community/pull/73) by NVIDIA (`apurvvkumaria`) — GitHub ETL opt-in
- [#74 merged](https://github.com/NVIDIA/nemoclaw-community/pull/74) by NVIDIA (`apurvvkumaria`) — Slack Socket Mode preflight
- [#72 closed](https://github.com/NVIDIA/nemoclaw-community/pull/72) — inference preflight; reused as product proof in TARX CLI

## Isaac GR00T / GR00T-WBC (opening 2026-08-20)

Observed on current `NVIDIA/Isaac-GR00T` `pyproject.toml`:

- `[project] name = "gr00t"`
- `requires-python = ">=3.12,<3.13"`

Observed on current `NVlabs/GR00T-WholeBodyControl`:

- `gear_sonic[inference]` depends on `Isaac-GR00T @ git+https://github.com/NVIDIA/Isaac-GR00T.git`
- `install_scripts/install_inference.sh` creates a Python 3.10 venv

That pair matches [Isaac-GR00T#748](https://github.com/NVIDIA/Isaac-GR00T/issues/748):

```
Package metadata name `gr00t` does not match given name `Isaac-GR00T`
```

Fix belongs in GR00T-WholeBodyControl, not Isaac-GR00T. Patch on
`tarx-ai/GR00T-WholeBodyControl` branch `fix/isaac-gr00t-dep-name-python312`.

## Do not

- Duplicate #748 with a second Isaac-GR00T issue
- Publish Unitree commercial proposals or hardware partner trackers
- Treat forks as contributions until a PR exists
