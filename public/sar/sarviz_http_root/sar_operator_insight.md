# SARvision by georgietron

JTY027 SAR Operator Insight

*A signal-forward view of the molecule before the make.*

Generated: `2026-06-18T00:28:49Z`
SARviz version: `sarviz-20260617-172849-PDT`
PDT build timestamp: `2026-06-17 17:28:49 PDT-0700`

## Operator Cockpit

- Pattern: `sar_operator_cockpit.v1` from `docs/business/asiflogic/19-live-dashboard-product-spec.md`.
- Annunciator: `SAR FLOW` / `continue`.
- Recommended action: recover docked pose before geometry claims
- Candidate focus: `JTY027_aniline_diF_2F6Me_benzamide`.
- Why now: no observed docked pose; prep conformer cannot support protein clash claims
- Missing evidence: docked-pose artifact or receptor-aligned pose
- Proof source: `pbcnet_pair_ranking + openfe_rbfe_edges_missing + docking_ops_run_summary_scan`.
- Action-plan status: `ready_to_queue`.
- Enqueue command: `pixi run sdf experiments --repo-root /usr/local/jldos --queue /usr/local/jldos/.codex/experiment_queue.json --runs-root /usr/local/jldos/.codex/experiment_runs enqueue --title 'Act on SAR cockpit recommendation: SAR FLOW' --created-by science-ops --slug jty-sar-cockpit-pbcnet-openfe-rank-continue-admitted-sar-pose-evidence-2f6me-benzamide --priority 140 --workdir /usr/local/jldos --metadata-json '{"action_plan_path": "/home/jldos/.local/share/asiflogic-site/public/sar/sar_cockpit_action_plan.json", "execution_mode": "agent", "recommendation_slug": "jty-sar-cockpit-pbcnet-openfe-rank-continue-admitted-sar-pose-evidence-2f6me-benzamide", "surface": "jty_sar_cockpit"}' --shell-command 'pixi run sdf rbfe jty027-sar-cron-tick --repo-root /usr/local/jldos --shared-runs-root /workspace/jldos_outputs/shared_runs --output-root /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy --gnina-device 0 --gnina-cpu 8 --max-parallel-panels 1 && pixi run sdf jty-sar-insight --repo-root /usr/local/jldos --shared-runs-root /workspace/jldos_outputs/shared_runs --output-dir /home/jldos/.local/share/asiflogic-site/public/sar --json' --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_operator_insight.json --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_operator_insight.html --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_cockpit_action_plan.json --artifact /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/panel_queue.json --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_operator_insight.md --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_science_ranking.csv --artifact /home/jldos/.local/share/asiflogic-site/public/sar/sar_science_ranking.svg --artifact /home/jldos/.local/share/asiflogic-site/public/sar/global_sar_rank_rows.csv --artifact /home/jldos/.local/share/asiflogic-site/public/sar/rank_integration_debt.csv --artifact /home/jldos/.local/share/asiflogic-site/public/sar/jty_reality_anchor_calibration_policy.json --artifact /home/jldos/.local/share/asiflogic-site/public/sar/docking_ops_history.csv --artifact /home/jldos/.local/share/asiflogic-site/public/sar/pbcnet_panel_members.csv`.
- Run-next command: `pixi run sdf experiments --repo-root /usr/local/jldos --queue /usr/local/jldos/.codex/experiment_queue.json --runs-root /usr/local/jldos/.codex/experiment_runs run-next --worker <agent> --json`.
- No email, Pano request, synthesis request, or wet-review claim is emitted by this packet.

## Readout

- Primary science rank axis: `pbcnet_pair_relative_ddg_openfe_rbfe_anchor`.
- Rank rule: PBCNet pair-relative dG is ordered inside the RBFE-anchored reference frame; docking affinity and throughput are excluded.
- top PBCNet series candidate; no direct RBFE edge reported: `JTY027_aniline_diF_26diMe_benzamide` (rank `1.0`, paired dG `-0.22500532731044387`).
- Top-candidate decision state: `pbcnet_only_no_direct_openfe_edge`.
- OpenFE RBFE anchor: `None` with `0` observed edge(s).
- Rank-integration debt rows: `0` strong pair-local edge(s) remain open or in-progress; completed direct OpenFE bridge edges are removed from this debt table.
- Reality-anchor calibration policy: `missing_prepper_recovery_audit`; admitted labels `None/None`.
- Coverage-qualified calibration allowed: `False` on `None`.
- Missingness sensitivity required: `True`; failed-label remediation active: `False`.
- Full-panel decision-grade claims blocked: `True`.
- Docking operations plateau: `improving` from `run_summary_scan`.
- Plateau ownership: `improving` by `science-ops`; action `continue-admitted-sar` on `sar`.
- Plateau reason: 0 completed run(s) after the first observed docking-operations best from run_summary_scan; latest docking-ops best -11.459867777778 kcal/mol versus first observed docking-ops best -11.459867777778 kcal/mol.
- Plateau next action: Continue admitted SAR and keep reporting artifact-backed rank deltas.
- Operations-only docking best: `JTY027_aniline_diF_2Me_benzamide` at `-11.459867777778` kcal/mol.
- Completed docking-operation runs after first best: `0` across `3` summaries.
- Latest completed panel: `jty_pbcnet_cycle2_winner_family_with_tail_probes`.

## Science Ranking

- Science ranking CSV: `/home/jldos/.local/share/asiflogic-site/public/sar/sar_science_ranking.csv`
- Science ranking SVG: `/home/jldos/.local/share/asiflogic-site/public/sar/sar_science_ranking.svg`
- Ranking proof source: `pbcnet_pair_ranking + openfe_rbfe_edges_missing`

| science_rank | candidate_id | pbcnet_relative_ddg_kcal_per_mol | rank_scope | openfe_anchor_status | openfe_delta_vs_anchor_kcal_per_mol |
| --- | --- | --- | --- | --- | --- |
| 1.0 | JTY027_aniline_diF_26diMe_benzamide | -0.22500532731044387 | panel_supplied_paired_model_rank_unverified_openfe_anchor | missing_openfe_anchor | None |
| 2.0 | JTY027_aniline_diF_2Et_benzamide | -0.1844451930502895 | panel_supplied_paired_model_rank_unverified_openfe_anchor | missing_openfe_anchor | None |
| 4.0 | JTY027_aniline_diF_2F6Me_benzamide | -0.11124449553161368 | panel_supplied_paired_model_rank_unverified_openfe_anchor | missing_openfe_anchor | None |
| 6.0 | JTY027_aniline_diF_2Me6Cl_benzamide | 0.06789628476703102 | panel_supplied_paired_model_rank_unverified_openfe_anchor | missing_openfe_anchor | None |
| 7.0 | JTY027_aniline_diF_2CF3_benzamide | 0.22226427225897374 | panel_supplied_paired_model_rank_unverified_openfe_anchor | missing_openfe_anchor | None |
| 8.0 | JTY027_aniline_diF_2F_benzamide | 0.49525359503492444 | panel_supplied_paired_model_rank_unverified_openfe_anchor | missing_openfe_anchor | None |
| 9.0 | JTY027_aniline_diF_2Cl_benzamide | 0.5281226031732139 | panel_supplied_paired_model_rank_unverified_openfe_anchor | missing_openfe_anchor | None |
| None | JTY023_imidazole_tail | -0.393527 | panel_local_paired_model_relative_ddg_unanchored | missing_openfe_anchor | None |
| None | JTY026_triazine_tail | -0.308466 | panel_local_paired_model_relative_ddg_unanchored | missing_openfe_anchor | None |
| None | JTY023_pyrazine_tail | -0.199321 | panel_local_paired_model_relative_ddg_unanchored | missing_openfe_anchor | None |
| None | JTY027_aniline_diF | -0.132021 | panel_local_paired_model_relative_ddg_unanchored | missing_openfe_anchor | None |
| None | JTY026_pyridyl_tail | -0.045218 | panel_local_paired_model_relative_ddg_unanchored | missing_openfe_anchor | None |
| None | JTY027_aniline_diF_2Me_benzamide | 0.0 | panel_local_paired_model_relative_ddg_unanchored | missing_openfe_anchor | None |

## Rank Integration Debt

Strong pair-local PBCNet edges are not discarded. They are queued here until sewn into the global SAR loop by a shared closed graph or direct RBFE bridge.

_No rows observed._

## Reality-Anchor Calibration Policy

- Policy JSON: `/home/jldos/.local/share/asiflogic-site/public/sar/jty_reality_anchor_calibration_policy.json`
- Prepper recovery audit: `None`
- Status: `missing_prepper_recovery_audit`
- Allowed claim scope: `None`
- Required actions: `materialize prepper recovery audit before changing calibration status; block full-panel decision-grade claims`

## Pose Geometry Root Cause

- Root cause: `Earlier clash-looking rows were caused by treating panel-prep ligand SDF conformers as if they were observed docked poses when no pose artifact was present for that candidate.`
- Fix: `Protein-distance and clash screens now run only against observed docked pose artifacts; prep-only molecules are marked not_evaluated_no_docked_pose and their 3D receptor geometry is withheld.`
- Torsion recommendation: `Constrained neural-potential torsion relaxation before any geometry-facing SAR claim`

## Pose-Mode Delta Protocol

- Status: `missing`
- Pattern doc: `/usr/local/jldos/docs/analysis/2026-04-30-pose-mode-delta-protocol.md`
- Latest report: `None`
- Trigger: `post_dock_torsion_rmsd_guard_rejection`
- Pocket-frame heavy RMSD: `None`
- Polar geometry score delta: `None`
- Operator rule: When a polished pose exceeds the RMSD guard, redock it and run a PBCNet pose-state compare plus pose-delta mechanism readout before changing SAR rank.

## Torsional-Stress Graph Probe

- Status: `missing`
- Observed reports: `None`
- Formal analysis lane earned: `False`
- Maturity state: `hypothesis_seed`
- Mechanism-candidate reports: `None`
- Determinism warnings: `None`
- Promotion blocker: no observed pose-delta reports
- Graph-level readout: None
- Required next action: run guarded torsion stress on admitted graph nodes before claiming a graph-level readout

## SAR Action Ladder

- Action ladder SVG: `/home/jldos/.local/share/asiflogic-site/public/sar/sar_action_ladder.svg`
- Action ladder CSV: `/home/jldos/.local/share/asiflogic-site/public/sar/sar_action_ladder.csv`

| priority | action_lane | candidate_id | rank_state | why_now | missing_evidence | next_action |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | pose_evidence | JTY027_aniline_diF_2F6Me_benzamide | official rank 4 | no observed docked pose; prep conformer cannot support protein clash claims | docked-pose artifact or receptor-aligned pose | recover docked pose before geometry claims |
| 1 | pose_evidence | JTY023_4F_pyridyl_tail | 3 closed loops | no observed docked pose; prep conformer cannot support protein clash claims | docked-pose artifact or receptor-aligned pose | recover docked pose before geometry claims |
| 1 | pose_evidence | JTY023_4Br_pyridyl_tail | 5 closed loops | no observed docked pose; prep conformer cannot support protein clash claims | docked-pose artifact or receptor-aligned pose | recover docked pose before geometry claims |
| 1 | pose_evidence | JTY027_aniline_diF_2Me6Cl_benzamide | official rank 6 | no observed docked pose; prep conformer cannot support protein clash claims | docked-pose artifact or receptor-aligned pose | recover docked pose before geometry claims |
| 1 | pose_evidence | JTY027_aniline_diF_2CF3_benzamide | official rank 7 | no observed docked pose; prep conformer cannot support protein clash claims | docked-pose artifact or receptor-aligned pose | recover docked pose before geometry claims |
| 1 | pose_evidence | JTY023_5F_pyrimidyl_tail | 2 closed loops | no observed docked pose; prep conformer cannot support protein clash claims | docked-pose artifact or receptor-aligned pose | recover docked pose before geometry claims |
| 1 | pose_evidence | JTY027_aniline_diF_2F_benzamide | official rank 8 | no observed docked pose; prep conformer cannot support protein clash claims | docked-pose artifact or receptor-aligned pose | recover docked pose before geometry claims |
| 1 | pose_evidence | JTY027_aniline_diF_2Cl_benzamide | official rank 9 | no observed docked pose; prep conformer cannot support protein clash claims | docked-pose artifact or receptor-aligned pose | recover docked pose before geometry claims |
| 3 | hydrate_site_map | JTY027_aniline_diF_2Cyano_benzamide | official rank 5 | solvent-ledge probe is missing water/site perception or a receptor contact-map overlay | required: water/site perception or contact-map overlay before wet-review claim | add water/site perception or contact-map overlay before wet-review claim |
| 4 | share_reference | JTY026_pyridyl_tail | panel-local | tail result is panel-local and cannot globally outrank winner-family nodes | bridge edges or one shared closed graph | share reference frame before ranking |
| 4 | share_reference | JTY023_imidazole_tail | panel-local | tail result is panel-local and cannot globally outrank winner-family nodes | bridge edges or one shared closed graph | share reference frame before ranking |
| 4 | share_reference | JTY026_triazine_tail | panel-local | tail result is panel-local and cannot globally outrank winner-family nodes | bridge edges or one shared closed graph | share reference frame before ranking |
| 5 | rbfe_confirm | JTY027_aniline_diF_26diMe_benzamide | official rank 1 | top paired-model rank is paired free-energy model-only; direct RBFE edge or shared closed-loop evidence is missing | direct RBFE edge or shared closed graph before handoff language | queue RBFE or shared closed-loop confirmation before handoff |
| 5 | rbfe_confirm | JTY027_aniline_diF_2Et_benzamide | official rank 2 | top paired-model rank is paired free-energy model-only; direct RBFE edge or shared closed-loop evidence is missing | direct RBFE edge or shared closed graph before handoff language | queue RBFE or shared closed-loop confirmation before handoff |
| 5 | rbfe_confirm | JTY027_aniline_diF | official rank 3 | top paired-model rank is paired free-energy model-only; direct RBFE edge or shared closed-loop evidence is missing | direct RBFE edge or shared closed graph before handoff language | queue RBFE or shared closed-loop confirmation before handoff |
| 5 | rbfe_confirm | JTY023_pyrazine_tail | official rank 3 | top paired-model rank is paired free-energy model-only; direct RBFE edge or shared closed-loop evidence is missing | direct RBFE edge or shared closed graph before handoff language | queue RBFE or shared closed-loop confirmation before handoff |
| 8 | context | JTY027_aniline_diF_2Me_benzamide | official rank 6 | keep visible only if a hypothesis needs this chemistry | no immediate blocker; low action value | keep as context unless hypothesis needs it |
| 8 | context | JTY027_26diF_benzamide | unranked context | keep visible only if a hypothesis needs this chemistry | no immediate blocker; low action value | keep as context unless hypothesis needs it |
| 8 | context | JTY027_2F6Me_benzamide | unranked context | keep visible only if a hypothesis needs this chemistry | no immediate blocker; low action value | keep as context unless hypothesis needs it |
| 8 | context | JTY027_2F_benzamide | unranked context | keep visible only if a hypothesis needs this chemistry | no immediate blocker; low action value | keep as context unless hypothesis needs it |
| 8 | context | JTY027_2Me_benzamide | unranked context | keep visible only if a hypothesis needs this chemistry | no immediate blocker; low action value | keep as context unless hypothesis needs it |
| 8 | context | JTY027_2OMe_benzamide | unranked context | keep visible only if a hypothesis needs this chemistry | no immediate blocker; low action value | keep as context unless hypothesis needs it |
| 8 | context | JTY027_aniline_diF_2OcPr_benzamide | unranked context | keep visible only if a hypothesis needs this chemistry | no immediate blocker; low action value | keep as context unless hypothesis needs it |
| 8 | context | JTY027_aniline_diF_2cPr_benzamide | unranked context | keep visible only if a hypothesis needs this chemistry | no immediate blocker; low action value | keep as context unless hypothesis needs it |

## Candidate Evidence Matrix

- Matrix SVG: `/home/jldos/.local/share/asiflogic-site/public/sar/candidate_evidence_matrix.svg`
- Matrix CSV: `/home/jldos/.local/share/asiflogic-site/public/sar/candidate_evidence_matrix.csv`
- Mechanistic map SVG: `/home/jldos/.local/share/asiflogic-site/public/sar/mechanistic_hypothesis_map.svg`

| candidate_id | pbcnet_support | pbcnet_rank | admet_gate_state | admet_property_role | gatekeeper_vault | tail_bridge | solvent_ledge | closed_loop_count | clash_count_lt_2p2A | water_evidence_state | water_context_state | wet_review_claim_state | next_action |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| JTY027_aniline_diF_26diMe_benzamide | 1.0 | 1.0 | hold | binding_challenger_liability_debt | 0.98 | 0.12 | 0.1 | 0 | 0 | no_explicit_receptor_waters | not_required | not_claimed | queue RBFE or shared closed-loop confirmation before handoff |
| JTY027_aniline_diF_2Et_benzamide | 0.983 | 2.0 | hold | tox_lipophilicity_contrast | 0.98 | 0.12 | 0.1 | 0 | 0 | no_explicit_receptor_waters | not_required | not_claimed | queue RBFE or shared closed-loop confirmation before handoff |
| JTY027_aniline_diF | 0.961 | 3.0 | review | jty027_property_followup | 0.76 | 0.28 | 0.1 | 0 | 0 | no_explicit_receptor_waters | not_required | not_claimed | queue RBFE or shared closed-loop confirmation before handoff |
| JTY023_pyrazine_tail | 0.825 | 3.0 | not_assessed | not_assessed | 0.24 | 0.98 | 0.1 | 3 | 0 | no_explicit_receptor_waters | not_required | not_claimed | queue RBFE or shared closed-loop confirmation before handoff |
| JTY027_aniline_diF_2F6Me_benzamide | 0.953 | 4.0 | hold | jty027_property_followup | 0.9 | 0.12 | 0.22 | 0 | 0 | no_explicit_receptor_waters | not_required | blocked_from_halogen_vector_rationale_until_geometry_audit | recover docked pose before geometry claims |
| JTY027_aniline_diF_2Cyano_benzamide | 0.35 | 5.0 | review | polarity_permeability_sentinel | 0.9 | 0.12 | 0.92 | 0 | 0 | no_explicit_receptor_waters | context_required | blocked_until_water_site_or_contact_overlay | add water/site perception or contact-map overlay before wet-review claim |
| JTY027_aniline_diF_2Me_benzamide | 0.907 | 6.0 | hold | incumbent_control | 0.9 | 0.12 | 0.1 | 0 | 0 | no_explicit_receptor_waters | not_required | not_claimed | keep as context unless hypothesis needs it |
| JTY027_aniline_diF_2Me6Cl_benzamide | 0.879 | 6.0 | hold | jty027_property_followup | 0.9 | 0.12 | 0.22 | 0 | 0 | no_explicit_receptor_waters | not_required | blocked_from_halogen_vector_rationale_until_geometry_audit | recover docked pose before geometry claims |
| JTY027_aniline_diF_2CF3_benzamide | 0.815 | 7.0 | hold | tox_lipophilicity_contrast | 0.9 | 0.12 | 0.92 | 0 | 0 | no_explicit_receptor_waters | context_required | blocked_until_water_site_or_contact_overlay | recover docked pose before geometry claims |
| JTY027_aniline_diF_2F_benzamide | 0.701 | 8.0 | hold | permeability_preserving_matched_pair | 0.9 | 0.12 | 0.22 | 0 | 0 | no_explicit_receptor_waters | not_required | blocked_from_halogen_vector_rationale_until_geometry_audit | recover docked pose before geometry claims |
| JTY027_aniline_diF_2Cl_benzamide | 0.688 | 9.0 | hold | tox_lipophilicity_contrast | 0.9 | 0.12 | 0.22 | 0 | 0 | no_explicit_receptor_waters | not_required | blocked_from_halogen_vector_rationale_until_geometry_audit | recover docked pose before geometry claims |
| JTY023_4F_pyridyl_tail | 0.919 | None | not_assessed | not_assessed | 0.16 | 0.8 | 0.1 | 3 | 0 | no_explicit_receptor_waters | not_required | not_claimed | recover docked pose before geometry claims |
| JTY023_4Br_pyridyl_tail | 0.907 | None | not_assessed | not_assessed | 0.16 | 0.8 | 0.1 | 5 | 0 | no_explicit_receptor_waters | not_required | not_claimed | recover docked pose before geometry claims |
| JTY023_5F_pyrimidyl_tail | 0.78 | None | not_assessed | not_assessed | 0.16 | 0.8 | 0.1 | 2 | 0 | no_explicit_receptor_waters | not_required | not_claimed | recover docked pose before geometry claims |
| JTY023_4CN_pyridyl_tail | 0.677 | None | not_assessed | not_assessed | 0.16 | 0.8 | 0.1 | 2 | 0 | no_explicit_receptor_waters | not_required | not_claimed | recover docked pose before geometry claims |
| JTY023_4OCF3_pyridyl_tail | 0.661 | None | not_assessed | not_assessed | 0.16 | 0.8 | 0.5 | 4 | 0 | no_explicit_receptor_waters | not_required | not_claimed | recover docked pose before geometry claims |
| JTY023_3Cl_pyridyl_tail | 0.65 | None | not_assessed | not_assessed | 0.16 | 0.8 | 0.1 | 1 | 0 | no_explicit_receptor_waters | not_required | not_claimed | recover docked pose before geometry claims |
| JTY026_pyridyl_tail | 0.598 | None | not_assessed | not_assessed | 0.16 | 0.98 | 0.1 | 3 | 0 | no_explicit_receptor_waters | not_required | not_claimed | share reference frame before ranking |

## ADMET Property Sidecar

- Status: `synthesized_from_jty027_sidecar_config`.
- Property packet status: `admet_property_packet_present`.
- Candidate count: `10`.
- Gate counts: `{'hold': 8, 'review': 2}`.
- Panel queue proof: `/workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/panel_queue.json`.
- Current-control proof: `/workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json`.
- Sidecar source: `sdf.admet.property_sidecar.Jty027SarAdmetSidecarConfig.from_affinity_library`.
- Probe plan: `missing_from_current_control_decision` on `solubility` for `None`; candidates ``.
- Probe next action: Regenerate current_control_decision with embedded ADMET sidecars and a probe plan..

| candidate_id | admet_property_role | admet_gate_state | admet_risk_norm | solubility_status | permeability_status | toxicity_status | admet_property_packet_schema | proof_path |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| JTY027_aniline_diF_2F6Me_benzamide | jty027_property_followup | hold | 0.43350000000000005 | hold | admit | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |
| JTY027_aniline_diF_2F_benzamide | permeability_preserving_matched_pair | hold | 0.43350000000000005 | hold | admit | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |
| JTY027_aniline_diF_2Me_benzamide | incumbent_control | hold | 0.43350000000000005 | hold | admit | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |
| JTY027_aniline_diF_26diMe_benzamide | binding_challenger_liability_debt | hold | 0.5505 | hold | review | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |
| JTY027_aniline_diF_2CF3_benzamide | tox_lipophilicity_contrast | hold | 0.5505 | hold | review | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |
| JTY027_aniline_diF_2Cl_benzamide | tox_lipophilicity_contrast | hold | 0.5505 | hold | review | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |
| JTY027_aniline_diF_2Et_benzamide | tox_lipophilicity_contrast | hold | 0.5505 | hold | review | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |
| JTY027_aniline_diF_2Me6Cl_benzamide | jty027_property_followup | hold | 0.5505 | hold | review | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |
| JTY027_aniline_diF | jty027_property_followup | review | 0.3655 | review | admit | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |
| JTY027_aniline_diF_2Cyano_benzamide | polarity_permeability_sentinel | review | 0.3655 | review | admit | review | sdf.jty027_sar_admet_property_packet.v1 | /workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json |

## Pairwise Panel Map

| panel_id | candidate_id | rank_display | relative_ddg_kcal_per_mol | rank_scope | pose_consistency | admet_gate_state | admet_property_role |
| --- | --- | --- | --- | --- | --- | --- | --- |
| jty_paired_model_tail_cleanup_r1 | JTY023_imidazole_tail | panel score 1 | -0.393527 | panel_local_relative_ddg_rank | stable |  |  |
| jty_paired_model_tail_cleanup_r1 | JTY026_triazine_tail | panel score 2 | -0.308466 | panel_local_relative_ddg_rank | stable |  |  |
| jty_paired_model_tail_cleanup_r1 | JTY023_pyrazine_tail | panel score 3 | -0.199321 | panel_local_relative_ddg_rank | stable |  |  |
| jty_paired_model_tail_cleanup_r1 | JTY027_aniline_diF | panel score 4 | -0.132021 | panel_local_relative_ddg_rank | moderate | review | jty027_property_followup |
| jty_paired_model_tail_cleanup_r1 | JTY026_pyridyl_tail | panel score 5 | -0.045218 | panel_local_relative_ddg_rank | stable |  |  |
| jty_paired_model_tail_cleanup_r1 | JTY027_aniline_diF_2Me_benzamide | panel score 6 | 0.0 | panel_local_relative_ddg_rank | stable | hold | incumbent_control |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_26diMe_benzamide | series rank 1 | -0.22500532731044387 | official_series_paired_model_rank | not_checked | hold | binding_challenger_liability_debt |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2Et_benzamide | series rank 2 | -0.1844451930502895 | official_series_paired_model_rank | not_checked | hold | tox_lipophilicity_contrast |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF | series rank 3 | -0.13202026233276618 | official_series_paired_model_rank | not_checked | review | jty027_property_followup |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2F6Me_benzamide | series rank 4 | -0.11124449553161368 | official_series_paired_model_rank | not_checked | hold | jty027_property_followup |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2Me_benzamide | series rank 5 | 0.0 | official_series_paired_model_rank | not_checked | hold | incumbent_control |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2Me6Cl_benzamide | series rank 6 | 0.06789628476703102 | official_series_paired_model_rank | not_checked | hold | jty027_property_followup |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2CF3_benzamide | series rank 7 | 0.22226427225897374 | official_series_paired_model_rank | not_checked | hold | tox_lipophilicity_contrast |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2F_benzamide | series rank 8 | 0.49525359503492444 | official_series_paired_model_rank | not_checked | hold | permeability_preserving_matched_pair |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2Cl_benzamide | series rank 9 | 0.5281226031732139 | official_series_paired_model_rank | not_checked | hold | tox_lipophilicity_contrast |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2Cyano_benzamide | not ranked | None | missing_paired_model_score | not_checked | review | polarity_permeability_sentinel |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2OcPr_benzamide | not ranked | None | missing_paired_model_score | not_checked |  |  |
| jty_paired_model_winner_family_exploitation_r1 | JTY027_aniline_diF_2cPr_benzamide | not ranked | None | missing_paired_model_score | not_checked |  |  |

## Pairwise Graph Artifacts

- Pairset summary: `None`
- Closed graph: `/usr/local/jldos/evidence/pbcnet/jty_top10_posebacked_closed_graph_full_20260421T212119Z/pbcnet_closed_graph.json`
- Rank-integration bridge packet: `None`
- Closed graph ligand count: `10`
- Observed runtime ligand count: `58`
- Runtime graph pickle count: `0`
- Operator chemistry-map SVG: `/home/jldos/.local/share/asiflogic-site/public/sar/pbcnet_pair_graph.svg`
- Operator 3D graph HTML: `/home/jldos/.local/share/asiflogic-site/public/sar/pbcnet_chemistry_graph_3d.html`
- Universe nodes CSV: `/home/jldos/.local/share/asiflogic-site/public/sar/pbcnet_universe_nodes.csv`

## Pose, Clash, And Water Checks

| candidate_id | closest_residues | min_protein_distance_A | clash_count_lt_2p2A | near_contact_count_lt_3p5A | interpretation |
| --- | --- | --- | --- | --- | --- |
| JTY027_aniline_diF_2Me_benzamide | None | None | 0 | 0 | not evaluated: receptor geometry atoms were unavailable |
| JTY023_pyrazine_tail | None | None | 0 | 0 | not evaluated: receptor geometry atoms were unavailable |
| JTY027_aniline_diF_2Cyano_benzamide | None | None | 0 | 0 | not evaluated: receptor geometry atoms were unavailable |
| JTY027_aniline_diF_2Et_benzamide | None | None | 0 | 0 | not evaluated: receptor geometry atoms were unavailable |
| JTY027_aniline_diF | None | None | 0 | 0 | not evaluated: receptor geometry atoms were unavailable |
| JTY027_aniline_diF_26diMe_benzamide | None | None | 0 | 0 | not evaluated: receptor geometry atoms were unavailable |
| JTY027_aniline_diF_2F6Me_benzamide | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |
| JTY023_4F_pyridyl_tail | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |
| JTY023_4Br_pyridyl_tail | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |
| JTY027_aniline_diF_2Me6Cl_benzamide | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |
| JTY027_aniline_diF_2CF3_benzamide | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |
| JTY023_5F_pyrimidyl_tail | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |
| JTY027_aniline_diF_2F_benzamide | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |
| JTY027_aniline_diF_2Cl_benzamide | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |
| JTY023_4CN_pyridyl_tail | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |
| JTY023_4OCF3_pyridyl_tail | None | None | 0 | 0 | not evaluated: no docked pose artifact was observed; prep conformer is not a receptor pose |

## Solvent Ledge Water Perception

| candidate_id | water_evidence_state | receptor_water_atom_count | interpretation | context_requirement | claim_guardrail | recommended_next_analysis | proof_source |
| --- | --- | --- | --- | --- | --- | --- | --- |
| JTY027_aniline_diF_2Cyano_benzamide | no_explicit_receptor_waters | 0 | no explicit waters in receptor; static nearest-water evidence is unavailable | requires water/site perception or contact-map overlay before wet-review claim | wet-review claim blocked until water/site or contact-map context is present | queue hydrated receptor/site-map analysis before using solvent-ledge SAR claims | static receptor-water/ligand distance scan |
| JTY027_aniline_diF_2CF3_benzamide | no_explicit_receptor_waters | 0 | no explicit waters in receptor; static nearest-water evidence is unavailable | requires water/site perception or contact-map overlay before wet-review claim | wet-review claim blocked until water/site or contact-map context is present | queue hydrated receptor/site-map analysis before using solvent-ledge SAR claims | static receptor-water/ligand distance scan |

## Pocket Hypotheses

| priority | hypothesis_id | status | what_is_observed | why_chosen | missing_evidence | guardrail | sar_queue_direction |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | gatekeeper_vault_hydrophobe_fit | active | Calibrated pairwise free-energy ranks favor compact ortho hydrophobe variants inside the winner-family benzamide series. | Top paired-model/panel candidates: JTY027_aniline_diF_26diMe_benzamide, JTY027_aniline_diF_2Et_benzamide, JTY027_aniline_diF, JTY027_aniline_diF_2F6Me_benzamide. This matches the pocket feature map&#x27;s gatekeeper-vault packing story. | A single integrated closed loop spanning winner-family hydrophobes and tail-cleanup candidates is still missing. |  | Queue an integrated pairwise closed graph containing 2Me, 2Et, 26diMe, 2cPr, 2Me6Cl, and the best tail-cleanup nodes. |
| 2 | tail_cleanup_bridge | active_bridge | Tail-cleanup candidates show favorable panel-local relative dG, but their reference frame is separate from the winner-family ranking frame. | This directly explains why the -0.393 tail-cleanup result should be visible but not promoted as global rank 1. | Tail-cleanup and benzamide winner-family nodes need a shared closed graph or bridge edges. |  | Queue bridge edges from JTY023/JTY026 tail nodes into the JTY027 winner-family loop before promotion decisions. |
| 3 | solvent_ledge_probe | needs_hydration_evidence | Solvent-ledge probes are present: none observed. | 2OcPr, 2Cyano, and 2CF3 are chemically meaningful probes for whether the ledge tolerates polarity, alkoxy bulk, or water displacement. | 2OcPr, 2Cyano, and 2CF3 require water/site perception or receptor contact-map overlays before any wet-review claim. | solvent_ledge_water_shell_probes | Queue water/site perception or contact-map overlays first; only then score solvent-ledge probes as synthesis-facing SAR. |
| 4 | lys_anchor_water_check | negative_guardrail | No durable Lys93 bridge is claimed for the JTY series in this packet. | The corrected readout treats Lys93-adjacent water / lys_anchor_water as weak or transient rather than a synthesis rationale. | Hydrated receptor/site-map or contact-frequency evidence is only needed if this check would change a ranked SAR decision. | lys_anchor_water | Do not rerun by default; queue only when a surviving candidate needs a water-bridge decision. |
| 5 | halogen_vector_geometry_guardrail | negative_guardrail | Halogen/electronics vectors are present as SAR descriptors, not as audited sigma-hole claims. | Unaudited halogen-vector language should not justify synthesis or wet-review promotion. | Explicit distance/angle/contact geometry audit for the halogen vector. | halogen_vector_claims | Keep halogen-bearing candidates visible, but block sigma-hole rationale until geometry is audited. |
| 6 | hinge_anchor_and_local_contact_continuity | monitor | Static pose contact rows are present for the latest docked candidates. | The pocket story requires retained binding geometry while substituents explore the gatekeeper vault and solvent ledge. | Static contact counts do not establish persistent interactions; no MD/contact-frequency evidence is included here. | lys_anchor_water stays weak/transient unless directly revalidated | Queue contact-frequency or short restrained dynamics only for candidates that survive integrated pairwise ranking. |
| 7 | closed_loop_consistency | active_qc | 9 observed pairwise closed-loop artifacts are available; primary loop has 10 ligands and 45 edges. | Loop closure is the right way to see whether local pair claims cohere across the SAR map. | The currently integrated loops do not yet include every admitted probe in one common loop. | ranking remains paired-model/RBFE anchored | Queue one consolidated closed loop after selecting the next admitted probe set from the hypotheses above. |

## Chemistry And Pocket Context

- Pocket chemistry map: `None`
- Narrative: `None`
- Series table: `None`
- WuXi alignment: `None`


## Guardrails

- Treat this as an operator visibility packet, not wet-lab proof.
- Do not interpret SAR liveness or repeated panel throughput as rank improvement.
- No email, Pano request, or synthesis request is emitted by this packet.
- `lys_anchor_water` (negative_guardrail): Do not claim a durable Lys93 bridge for JTY. Lys93-adjacent water is weak/transient; rerun the check only when it would change a ranked SAR decision.
- `halogen_vector_claims` (negative_guardrail): Treat halogen or sigma-hole rationales as unproven until geometry is explicitly audited. Halogen-bearing candidates can remain in SAR, but unaudited vector language cannot justify synthesis.
- `solvent_ledge_water_shell_probes` (context_requirement): 2OcPr, 2Cyano, and 2CF3 require water/site perception or contact-map overlays before any wet-review claim. Solvent-ledge probes are hypothesis carriers until water/site or contact-map context is attached.

## Source Artifacts

- `shared_runs_root`: `/workspace/jldos_outputs/shared_runs`
- `repo_root`: `/usr/local/jldos`
- `campaign_objectives`: `/usr/local/jldos/docs/baton/campaign_objectives.json`
- `delegated_obligations`: `/usr/local/jldos/docs/baton/delegated_obligations.jsonl`
- `panel_queue`: `/workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/panel_queue.json`
- `current_control_decision`: `/workspace/jldos_outputs/shared_runs/jty027_sar_autonomy/current_control_decision.json`
- `sar_promotion_surface`: `None`
- `admet_property_projection`: `/home/jldos/.local/share/asiflogic-site/public/sar/admet_property_rows.csv`
- `pbcnet_pairset_summary`: `None`
- `pbcnet_closed_graph`: `/usr/local/jldos/evidence/paired_model/jty_top10_posebacked_closed_graph_full_20260421T212119Z/paired_model_closed_graph.json`
- `rank_integration_bridge_packet`: `None`
- `shared_reference_bridge_packet`: `None`
- `science_ranking_series_table`: `None`
- `openfe_rbfe_proof_paths`: `[]`
- `series_context_root`: `None`
- `receptor_for_contact_screen`: `None`
- `observed_pose_index_candidate_count`: `9`
- `observed_pose_index_proof_source`: `shared_runs_root jty*/candidate_rows.json, jty*/**/dock_report*.json, and jty*/**/pose_recovery_packet.json -> docking pose generation pose_path`
- `reality_anchor_prepper_recovery_audit`: `None`
- `pose_mode_delta_pattern_doc`: `/usr/local/jldos/docs/analysis/2026-04-30-pose-mode-delta-protocol.md`
- `pose_mode_delta_latest_report`: `None`
- `torsional_stress_graph_probe_latest_report`: `None`
