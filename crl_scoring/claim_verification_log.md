# Verified Claim Cross-Reference Log

**Paper:** AI-Driven Cybersecurity: A Structured Survey of Defense, Offense, Autonomy, and Emerging Security Challenges  
**Purpose:** Documents each quantitative or specific claim made in the paper, its source location in the cited paper, and verification status.

---

## Quantitative Claims — Defense Section

### Claim 1: Multi-Agent NIDS — 93.6% accuracy and 41.3% false-positive reduction
- **Paper statement (§4.4, §1):** "Multi-agent LLM pipelines report 93.6% threat-detection accuracy with 41.3% false-positive reduction"
- **Source:** Hmimou Y. et al. (2025), *IEEE Access*, 13, 150199–150215. DOI: 10.1109/ACCESS.2025.3602681
- **Location in source:** Table 3 (Performance Comparison), p. 150208; Abstract, p. 150199
- **Exact text in source:** "The proposed multi-agent system achieves 93.6% accuracy and reduces false positives by 41.3% compared to the single-agent baseline."
- **Status:** ✓ VERIFIED

### Claim 2: HiTL NIDS — 79% lower time-to-detection
- **Paper statement (§4.1):** "reporting up to 79% lower time-to-detection"
- **Source:** Kim Y., Dán G., Zhu Q. (2024), *IEEE TIFS*, 19, 8658–8672. DOI: 10.1109/TIFS.2024.3434647
- **Location in source:** Section IV.B, Table II, p. 8667 — MTTD comparison: HiTL-AL vs. passive learning baseline
- **Exact text in source:** "The proposed HiTL active learning framework achieves up to 79% reduction in mean time-to-detection compared to passive learning."
- **Qualifier:** "up to" — the 79% is the maximum reduction across tested scenarios; mean reduction is ~62%. The paper correctly uses "up to."
- **Status:** ✓ VERIFIED

### Claim 3: Ranker — 99.43% F1, 0.11% FPR, 68 families, 95% caught before >1 file encrypted
- **Paper statement (§4.2):** "Ranker monitors kernel-level filesystem behaviour, reporting 99.43% F1 with 0.11% false-positive rate across 68 ransomware families---95% of attacks caught before more than one file is encrypted"
- **Source:** Zhang H. et al. (2024), *IEEE TIFS*, 19, 6113–6127. DOI: 10.1109/TIFS.2024.3410511
- **Locations in source:**
  - F1 = 99.43%: Table II, p. 6119, row "Ranker (ours)"
  - FPR = 0.11%: Table II, p. 6119, same row
  - 68 ransomware families: Section IV.A, p. 6117: "We collected samples from 68 ransomware families"
  - 95% containment before >1 file: Section IV.B, p. 6121: "Ranker contained 95.2% of attacks before more than one file was encrypted"
- **Status:** ✓ VERIFIED (all four sub-claims)

### Claim 4: DeepWare — 98.6% recall, MCC 0.968
- **Paper statement (§4.2):** "DeepWare images HPC workload traces via CNNs, achieving 98.6% recall at MCC 0.968 below the OS evasion layer"
- **Source:** Ganfure G.O. et al. (2023), *IEEE Transactions on Computers*, 72(3), 600–613. DOI: 10.1109/TC.2022.3173149
- **Location in source:** Table III (Detection Performance), p. 608
- **Exact text in source:** "DeepWare achieves 98.6% recall and MCC of 0.968 across 30 ransomware families."
- **Note:** Paper claims "below the OS evasion layer" — source confirms: "the CNN operates on raw hardware performance counter data, below the OS abstraction layer" (Section I, p. 601). ✓
- **Status:** ✓ VERIFIED

### Claim 5: Supply Chain — 4,377 open-source security advisories
- **Paper statement (§7.1):** "An empirical study of 4,377 open-source security advisories found vulnerability disclosure and patch adoption separated by weeks to months"
- **Source:** Imtiaz N., Khanom A., Williams L. (2023), *IEEE TSE*, 49(4), 1540–1560. DOI: 10.1109/TSE.2022.3181010
- **Location in source:** Section III.A, p. 1543: "We analysed 4,377 security advisories from GitHub Advisory Database"; Section IV (Results), p. 1548–1552 confirming disclosure-patch gap.
- **Status:** ✓ VERIFIED

### Claim 6: IR-Fuzz — more than 12,000 smart contracts
- **Paper statement (§5.2):** "IR-Fuzz applies invocation-ordering fuzzing across more than 12,000 deployed smart contracts"
- **Source:** Liu Z. et al. (2023), *IEEE TIFS*, 18, 1237–1251. DOI: 10.1109/TIFS.2023.3237370
- **Location in source:** Section IV.A, p. 1242: "We evaluate IR-Fuzz on a dataset of 12,349 deployed smart contracts collected from Etherscan."
- **Status:** ✓ VERIFIED (12,349 > 12,000 ✓)

### Claim 7: Hasanov et al. — 177 studies
- **Paper statement (§3.3, Table 3):** "Reviews across 177 LLM cybersecurity studies"
- **Source:** Hasanov I. et al. (2024), *IEEE Access*, 12, 176751–176778. DOI: 10.1109/ACCESS.2024.3505983
- **Location in source:** Abstract, p. 176751; Section III.B, p. 176758: "A total of 177 studies were included in the systematic literature review after applying inclusion/exclusion criteria."
- **Status:** ✓ VERIFIED

---

## Survey Comparison Table (Table 3) — N-Count Verification

### Ring et al. (2019) — "40+" in Table 3
- **Source:** Ring M. et al. (2019), *Computers & Security*, 86, 147–167. DOI: 10.1016/j.cose.2019.06.005
- **Actual N from source:** Section IV, p. 150: "We surveyed 36 publicly available network intrusion detection datasets."
- **Assessment:** 36 < 40. The "40+" label in Table 3 is **inaccurate**. Should be corrected to "36."
- **Action:** Correct Table 3 to show "36" for Ring et al. See §tex-correction notes.

### Martins et al. (2020) — "80+" in Table 3
- **Source:** Martins N. et al. (2020), *IEEE Access*, 8, 35403–35419. DOI: 10.1109/ACCESS.2020.2974752
- **Actual N from source:** Abstract: "We systematically review 85 studies on adversarial ML applied to intrusion detection and malware scenarios."
- **Assessment:** 85 > 80 ✓. "80+" is accurate.
- **Status:** ✓ VERIFIED

### Gibert et al. (2020) — "100+" in Table 3
- **Source:** Gibert D. et al. (2020), *JNCA*, 153, 102526. DOI: 10.1016/j.jnca.2019.102526
- **Actual N from source:** Section II, p. 4: "This survey covers over 130 papers on machine learning-based malware detection."
- **Assessment:** 130 > 100 ✓. "100+" is accurate.
- **Status:** ✓ VERIFIED

### Zhang et al. (2022) — "100+" in Table 3
- **Source:** Zhang Z. et al. (2022), *IEEE Access*, 10, 93104–93139. DOI: 10.1109/ACCESS.2022.3204051
- **Actual N from source:** Section I: "We survey over 150 papers on XAI applications in cybersecurity."
- **Assessment:** 150 > 100 ✓. "100+" is accurate.
- **Status:** ✓ VERIFIED

### Apruzzese et al. (2023) — "80+" in Table 3
- **Source:** Apruzzese G. et al. (2023), *Digital Threats*, 4(1). DOI: 10.1145/3545574
- **Actual N from source:** Abstract: "We analyze 85 papers on the role of ML in cybersecurity."
- **Assessment:** 85 > 80 ✓. "80+" is accurate.
- **Status:** ✓ VERIFIED

### Malik et al. (2024) — "100+" in Table 3
- **Source:** Malik J. et al. (2024), *IEEE Access*, 12, 99382–99421. DOI: 10.1109/ACCESS.2024.3423323
- **Actual N from source:** Abstract: "We conduct a systematic review of 120+ papers."
- **Assessment:** 120 > 100 ✓. "100+" is accurate.
- **Status:** ✓ VERIFIED

### Rehman et al. (2025) — "50+" in Table 3
- **Source:** Rehman H.M.R. et al. (2025), *Journal of Big Data*, 12, 264. DOI: 10.1186/s40537-025-01323-2
- **Actual N from source:** Abstract: "A total of 67 primary studies were included."
- **Assessment:** 67 > 50 ✓. "50+" is accurate.
- **Status:** ✓ VERIFIED

---

## Table 3 Correction Required

| Survey | Current Table 3 value | Correct value | Action |
|--------|----------------------|---------------|--------|
| Ring et al. 2019 | 40+ | **36** | Correct in .tex |

---

## Partial/Checkmark Criteria (Table 3) — Written Definitions

| Symbol | Meaning |
|--------|---------|
| ✓ | The survey explicitly addresses this dimension with dedicated sections and/or formal evaluation of systems on this axis |
| Partial | The survey touches on the dimension incidentally or tangentially, without it being a primary structural or analytical focus |
| --- | The dimension is not addressed |

**Applied criteria:**
- **AI Defense ✓:** Survey has ≥1 section dedicated to AI-based defensive systems with evaluation
- **AI Offense ✓:** Survey explicitly covers offensive use of AI (pen-testing, exploit, social engineering)
- **AI Attack Surface ✓:** Survey explicitly covers attacks *on* AI systems (adversarial ML, prompt injection, etc.)
- **Agentic AI ✓:** Survey covers goal-directed, autonomous multi-step AI agents
- **Autonomy Spectrum ✓:** Survey systematically characterises autonomy levels across reviewed systems
- **Structured Evaluation ✓:** Survey applies a repeatable quantitative scoring framework to a set of representative systems
- **Ref. Architecture ✓:** Survey proposes a concrete reference architecture grounded in corpus evidence

---

## Statistical Claim Verification

### Abstract: "dimension means D̄=3.60, Ī=2.30, Ā=2.80, R̄=2.40, Ē=2.90, CRL̄=2.80 (SD=0.34)"

Verified by `crl_sensitivity_analysis.py` (see scripts/). All values correct to 2 d.p.

### Sensitivity Analysis: ρ_R=0.94, ρ_A=0.96, ρ_E=0.97
Verified by `crl_sensitivity_analysis.py`. Values confirmed.

### Non-compensatory criterion: "zero defensive systems qualify"
Verified: E≤3 for all 10 systems; E≥4 required. Zero qualify. ✓

---

*Prepared by:* Nameet Sudam Ahire  
*Date:* October 2026
