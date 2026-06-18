# JNK3 Selectivity Program — Synthesis Brief

*Generated 2026-06-18T00:28:49Z. Internal evidence document — not for external distribution.*

---

## Program Objective

Convert compute into drugs: design a selective JNK3 inhibitor worth licensing — not watch cold silicon mold. Lead: JTX005 — primary amide · JNK3 21 nM · >=476x dual JNK1/2-sel. Developability / assay gate: potency ≤100 nM (JNK3 IC₅₀), LLE ≥3, cLogP ≤5.5, PSA ≤95 Å² for synthesis and Klyne isoform assay.

## Top Synthesis Candidates

Ranked by combined score = LLE × log₁₀(JNK2_fold × JNK1_fold). Gate: pIC₅₀ ≥7.0, JNK2_fold ≥5×, JNK1_fold ≥10×, cLogP ≤6. Reference (JTX009) appended regardless of gate rank.

| Compound   | Series                 | JNK3 IC₅₀  | JNK2×   | JNK1×   | cLogP  | LLE   | Notes / rationale                                    |
| ---------- | ---------------------- | ---------- | ------- | ------- | ------ | ----- | ---------------------------------------------------- |
| jtx080     | sel_triazine           | 48.5       | 31      | 130     | 2.39   | 4.92  | JNK2 selectivity 31.2x                               |
| jtx079     | sel_pyrimidyl          | 35.3       | 13      | 200     | 2.31   | 5.14  | JNK2 selectivity 12.6x                               |
| JTX005     | sel_thioamide_core     | 21.0       | 480     | 476     | 4.72   | 2.96  | JNK2 selectivity 480×                                |
| JTX024     | sel_difluoro_series_a  | 61.0       | 100     | 164     | 3.80   | 3.41  | JNK2 selectivity 100×                                |
| JTX015     | sel_series_a_core      | 62.0       | 58      | 161     | 3.66   | 3.55  | JNK2 selectivity 58×                                 |
| JTX009 (ref) | sel_halogen_planar     | 10.0       | 17      | 334     | 4.32   | 3.68  | JNK2 selectivity 17×                                 |

Score formula: LLE × log₁₀(JNK2× × JNK1×). Top ranked: jtx080, jtx079, JTX005, JTX024, JTX015.

---

## Three-Mechanism SAR Map

Three structurally non-competing mechanisms each deliver measurable JNK3 bias. Combinations are untested but geometrically compatible.

### Mechanism 1 — Glycine-loop clamp

Heteroaryl caps that cinch the glycine loop above the ATP plane in its open conformation. Exemplars: **JTX075** (174 nM, 17× JNK2, 66× JNK1) and **JTX076** (145 nM, 14× JNK2, 32× JNK1). WuXi-derived indazole-oxazine and indazole-pyrimidine caps. The open conformation is more accessible in JNK3 than JNK1/2, giving the structural basis for selectivity. This is the most transferable vector — appending a rigid polar glycine-loop cap to any Series A/B scaffold should preserve selectivity gain.

### Mechanism 2 — Electrostatic Lys93 bias

Polar aniline replacements that lean into the Lys93/Lys155 electrostatic asymmetry unique to JNK3 near the solvent front. Exemplars: **JTX079** (35 nM, 13× JNK2, 200× JNK1, cLogP 2.31, LLE 4.14 — best LLE in panel) and **JTX080** (49 nM, 31× JNK2, 130× JNK1, cLogP 2.39). Both replace the fluorobenzyl anilide with pyrimidyl or difluoro-azaanilide groups. Low cLogP and high LLE make these the most PK-friendly leads in the dataset. Mechanism confirmed orthogonal to glycine-loop clamp.

### Mechanism 3 — Back-pocket steric discrimination

Extended aromatic tail past the Met146 gatekeeper creates a steric clash in the shallower JNK1/JNK2 back pocket while fitting the wider JNK3 cleft. Exemplar: **JTX077** (411 nM, 24× JNK2, 74× JNK1) via biaryl nitrile extension. Also captured in the macrocyclic design **JTX081** (81 nM, 6× JNK2, 39× JNK1) which additionally stabilises the JNK3-specific Lys93 water chain. Potency trade-off is a concern for this mechanism alone; combining it with mechanism 1 or 2 is the preferred path.

---

## Active Design Vectors (Unexploited)

### Vector A — Met146 σ-hole realignment

The fluorobenzyl C–F bond in current Series A/B compounds does not satisfy σ-hole criteria for Met146 (observed: 3.5–3.7 Å, 102–139°; requirement: <3.0 Å, >150°). **Testable hypothesis:** replace fluorobenzyl with iodobenzyl at the carbon-15 position of JTX015. Computed pose (7s1n co-crystal aligned) gives C–I···S ≈ 2.95 Å at 180°. Expected: enhanced gatekeeper engagement without displacing hinge or Lys93 contacts. Predicted cLogP lift: +1.27 (to 4.93 — within guardrail). Synthesis: single Pd-catalysed aryl iodination step from JTX015.

### Vector B — αD-helix hydrophobic wing

A hydrophobic extension from the biaryl system toward the αD-helix would clamp the back-pocket conformation and reduce entropy of binding. No analogue yet synthesised. **Testable hypothesis:** extend the biaryl tail of JTX033 (24 nM, 11× JNK2, 293× JNK1) with a methylcyclopropyl or tert-butyl group at the para position of Ring B. Expected: maintained selectivity with improved binding affinity via reduced conformational entropy. MW and cLogP flags require monitoring. Requires redocking and paired-model scoring before synthesis commitment.

---

## Synthesis Gate Criteria

- JNK3 IC₅₀ ≤ 100 nM (pIC₅₀ ≥ 7.0)
- Selectivity: ≥ 10× vs JNK2, ≥ 30× vs JNK1 (preferred ≥ 100× JNK1)
- LLE ≥ 3.0 at measured potency (preferred ≥ 3.5)
- cLogP ≤ 5.5 (flag at > 5.3 for parallel PK assay)
- PSA ≤ 95 Å² (flag at > 85 Å² for permeability note)
- MW ≤ 500 preferred; MW ≤ 550 acceptable with LLE ≥ 3.5
- No Cys154 covalent warhead claims without calibrated IC₅₀ data (JTX060_warhead disqualified: 10,000 nM WuXi report vs. invalidated 15 nM claim)
- Halogen vector rationale requires explicit σ-hole geometry audit before synthesis justification

---

## RBFE Prioritisation

No open RBFE pairs detected in this packet. Recommend adding the top candidate vs. JTX009 reference as the first RBFE edge to close the global rank.

---

## Evidence Basis

- Selectivity round 1: `sar/jnk3_selectivity_round1.csv` (present)
- Selectivity round 2: `sar/jnk3_selectivity_round2.csv` (present)
- Pocket notes: `sar/jnk3_pocket_sar.md`
- Reference co-crystal: 7s1n (JTX009 pose)
- Evidence board: `sar_operator_insight.html` (this packet)
- Packet generated: `2026-06-18T00:28:49Z`

*This brief is derived from observed computational and biochemical data. Synthesis decisions require wet-lab confirmation. No synthesis requests, emails, or external communications are emitted by this document.*
