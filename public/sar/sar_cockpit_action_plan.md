# SAR Cockpit Action Plan

- Status: `ready_to_queue`
- Action: recover docked pose before geometry claims
- Candidate: `JTY027_aniline_diF_2F6Me_benzamide`
- Proof source: `pbcnet_pair_ranking + openfe_rbfe_edges_missing + docking_ops_run_summary_scan`
- Queue: `/usr/local/jldos/.codex/experiment_queue.json`
- Runs root: `/usr/local/jldos/.codex/experiment_runs`

## Commands

- Enqueue: `pixi run sdf experiments --repo-root /usr/local/jldos --queue /usr/local/jldos/.codex/experiment_queue.json --runs-root /usr/local/jldos/.codex/experiment_runs enqueue --title 'Act on SAR cockpit recommendation: SAR FLOW' --created-by science-ops --slug jty-sar-cockpit-pbcnet-openfe-rank-continue-admitted-sar-pose-evidence-2f6me-benzamide --priority 140 --workdir /usr/local/jldos --metadata-json '{"action_plan_path": "/home/jldos/.local/share/asiflogic-site/public/sar/sar_cockpit_action_plan.json", "execution_mode": "agent", "recommendation_slug": "jty-sar-cockpit-pbcnet-openfe-rank-continue-admitted-sar-pose-evidence-2f6me-benzamide", "surface": "jty_sar_cockpit"}' --shell-command 'pixi run sdf rbfe jty027-sar-cron-tick --repo-root /usr/local/jldos --shared-runs-root /workspace/jldos_outputs/shared_runs --output-root /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy --gnina-device 0 --gnina-cpu 8 --max-parallel-panels 1 && pixi run sdf jty-sar-insight --repo-root /usr/local/jldos --shared-runs-root /workspace/jldos_outputs/shared_runs --output-dir /home/jldos/.local/share/asiflogic-site/public/sar --json' --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_operator_insight.json --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_operator_insight.html --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_cockpit_action_plan.json --artifact /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/panel_queue.json --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_operator_insight.md --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_science_ranking.csv --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_science_ranking.svg --artifact /home/jldos/.local/share/asiflogic-site/public/sar/global_sar_rank_rows.csv --artifact /home/jldos/.local/share/asiflogic-site/public/sar/rank_integration_debt.csv --artifact /home/jldos/.local/share/asiflogic-site/public/sar/jty_reality_anchor_calibration_policy.json --artifact /home/jldos/.local/share/asiflogic-site/public/sar/docking_ops_history.csv --artifact /home/jldos/.local/share/asiflogic-site/public/sar/pbcnet_panel_members.csv`
- Run next: `pixi run sdf experiments --repo-root /usr/local/jldos --queue /usr/local/jldos/.codex/experiment_queue.json --runs-root /usr/local/jldos/.codex/experiment_runs run-next --worker <agent> --json`
- Human take-next: `pixi run sdf experiments --repo-root /usr/local/jldos --queue /usr/local/jldos/.codex/experiment_queue.json --runs-root /usr/local/jldos/.codex/experiment_runs take-next --operator <name> --json`

## Guardrails

- Do not present SAR liveness, queue activity, or docking affinity as rank progress; rank progress must come from the PBCNet/OpenFE-anchored science ranking.
- Do not stop or restart compute from this action plan.
- Do not send email, Pano review, synthesis request, or wet-review handoff without explicit operator permission.
- lys_anchor_water: Do not claim a durable Lys93 bridge for JTY. Lys93-adjacent water is weak/transient; rerun the check only when it would change a ranked SAR decision.
- halogen_vector_claims: Treat halogen or sigma-hole rationales as unproven until geometry is explicitly audited. Halogen-bearing candidates can remain in SAR, but unaudited vector language cannot justify synthesis.
- solvent_ledge_water_shell_probes: 2OcPr, 2Cyano, and 2CF3 require water/site perception or contact-map overlays before any wet-review claim. Solvent-ledge probes are hypothesis carriers until water/site or contact-map context is attached.
