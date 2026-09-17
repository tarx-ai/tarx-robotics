# Status — 2026-09-17 (morning upstream)

Honest snapshot. Documented no-op. No new upstream PR. No comments on waiting PRs.

## Done this pass

- Public tracker: https://github.com/tarx-ai/tarx-robotics
- Confirmed still waiting (read-only; do not comment):
  - [NVlabs/GR00T-WholeBodyControl#258](https://github.com/NVlabs/GR00T-WholeBodyControl/pull/258) — **OPEN**. Reviews: 0. Review comments: 0. No maintainer change request. Branch: `tarx-ai/GR00T-WholeBodyControl` `fix/isaac-gr00t-dep-name-python312`. Related [Isaac-GR00T#748](https://github.com/NVIDIA/Isaac-GR00T/issues/748) still open.
  - [NVlabs/curobo#715](https://github.com/NVlabs/curobo/pull/715) — **OPEN**. Reviews: 0. Review comments: 0. Leave it.
- Searched open Isaac-GR00T issues (#773 eval table, #771 delta_indices, #767 test marker, #761 training loss, #760 REAL_G1 sim, #749 select_layer docs, #748 install name). None is a small justified TARX patch today without inventing `UNITREE_H2` or duplicating #748 (already covered by #258).
- Considered GR00T-WholeBodyControl #259 (h2.py actuator vs urdf) and nearby open issues (#273/#269/#268/#252/#247): research/hardware or needs file-level one-line proof — not a docs/install PR today.
- Cadence: reviews beat new work. Prior STATUS already said wait for #258/#715. No second upstream PR.

## Not done

- No H2 Plus on the bench
- No Thor bring-up evidence
- Isaac Lab: forked only, no PR yet
- `tarx-os` GitHub repo is not TARX OS and stays private
- `tarx-hardware` stays private
- Do not wire `use_mean_std` (Isaac-GR00T#745 still no maintainer call)
- No `UNITREE_H2` tag

## Next

1. Wait for review on WBC #258 and curobo #715; fix comments before any new PR
2. Isaac Lab / Isaac ROS / cuRobo Unitree gaps only with a real repro
3. Keep weekday 08:17 / 12:41 / 16:38; never two new upstream PRs the same day unless the second is a review fix
