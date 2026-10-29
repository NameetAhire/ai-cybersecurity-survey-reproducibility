# Reproducibility Package — README

## Toward Trustworthy Autonomous Cybersecurity: A Capability-Readiness Framework, Attack-Surface Taxonomy, and Reference Architecture for Agentic AI

**Authors:** Nameet Sudam Ahire, Dayanand D. Ambawade  
**Institution:** Sardar Patel Institute of Technology, Mumbai, India  
**Target Journal:** Journal of Information Security and Applications (JISA), Elsevier  

---

## Package Contents

```
reproducibility/
├── README.md                          ← This file
├── corpus_index.json                  ← Full metadata for all 70 corpus papers
├── search_logs/
│   └── database_search_protocol.md   ← Exact queries, dates, hit counts per database
├── screening_logs/
│   └── screening_log.md              ← Per-paper include/exclude decisions + κ calculation
├── crl_scoring/
│   ├── crl_scoring_sheet.md          ← Per-system, per-dimension scores with evidence quotes
│   └── claim_verification_log.md     ← Every quantitative claim mapped to source page/table
└── scripts/
    └── crl_sensitivity_analysis.py   ← Recomputes all CRL scores and Spearman correlations
```

---

## How to Verify the CRL Analysis

```bash
pip install scipy numpy
python scripts/crl_sensitivity_analysis.py
```

Expected output confirms:
- All dimension means: D=3.60, I=2.30, A=2.80, R=2.40, E=2.90
- Composite CRL mean = 2.80, SD = 0.34
- Spearman ρ: R-heavy=0.94, A-heavy=0.96, E-heavy=0.97
- Zero qualifying systems under pilot-eligibility criterion

---

## Corpus Summary

- **N = 70** peer-reviewed publications, 2019–2026
- **Databases searched:** IEEE Xplore (387), ScienceDirect (89), Scopus (62), Google Scholar (68), SpringerLink (36)
- **Total raw hits:** 642 | **After cross-database dedup:** 458 | **Final corpus:** 70
- **Domain breakdown:** Defense 35 (50%) | Offense 10 (14.3%) | AI Attack Surface 12 (17.1%) | Governance 13 (18.6%)

### Note on wang_align_2025
Paper #70 (Wang et al., 2025, arXiv:2506.01307) is an arXiv preprint flagged under EC1. It is retained in the bibliography as a mechanistic reference for adversarial visual alignment attacks (RQ3) but is not used as a primary CRL-scored system. If strict EC1 enforcement is required, N should be adjusted to 69.

---

## CRL Framework

**10 primary defensive systems** scored on 5 dimensions (D, I, A, R, E), each 1–5.

**Non-compensatory pilot-eligibility criterion (Eq. 1 in paper):**
```
CRL >= 3.60 AND min(D,I,A) >= 3 AND R >= 3 AND E >= 4
```
Result: **0 of 10 systems qualify** — primary blocker is E (no system has independent cyber-range or operational-pilot evidence).

**2 exploratory profiles** (DynPen offensive, LLM Phishbot) included in secondary table for completeness; not compared against defensive rubric for D dimension.

---

## Inter-Rater Agreement

- **Screening κ (Stage 2, 30-record sample):** κ = 0.88 (substantial agreement, Landis & Koch 1977)
- **CRL scoring verification:** Supervisor (D.D. Ambawade) independently reviewed all 10 primary system scores; consensus adjudication on 7/50 cells; κ_scoring = 0.82

---

## Claim Verification

See `crl_scoring/claim_verification_log.md` for full source-page verification of:
- Hmimou: 93.6% accuracy, 41.3% FP reduction ✓
- Kim (HiTL): up to 79% lower MTTD ✓  
- Zhang (Ranker): 99.43% F1, 0.11% FPR, 68 families, 95% pre-1-file containment ✓
- Ganfure (DeepWare): 98.6% recall, MCC 0.968 ✓
- Imtiaz: 4,377 advisories ✓
- Liu IR-Fuzz: 12,349 contracts (>12,000) ✓
- Hasanov: 177 studies ✓
- **Ring et al. N correction:** Paper Table 3 shows "40+" but actual N = 36 datasets surveyed

---

## Contact

Corresponding author: Nameet Sudam Ahire — nameet.ahire25@spit.ac.in
