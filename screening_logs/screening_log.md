# Screening Log — AI-Driven Cybersecurity Survey (N=70 Final Corpus)

**Paper:** AI-Driven Cybersecurity: A Structured Survey of Defense, Offense, Autonomy, and Emerging Security Challenges  
**Screener 1 (primary):** N. S. Ahire  
**Screener 2 (audit):** D. D. Ambawade  
**Cohen's κ (inclusion/exclusion on 30 randomly sampled records from Stage 2):** 0.88  
**Legend:** ✓ = Included | EC1/EC2/EC3/EC4 = Excluded (criterion) | OS = Out of scope

---

## Inclusion / Exclusion Criteria Reference

**Inclusion (all four must be met):**
- IC1: Peer-reviewed journal or flagship conference (IEEE, Elsevier, ACM, Springer, MDPI)
- IC2: Explicit architectural or empirical contribution to AI-driven defense, offense, or security of AI systems
- IC3: Publication date 2019–2026
- IC4: Substantive evidence bearing on at least one RQ

**Exclusion (any one triggers exclusion):**
- EC1: Non-peer-reviewed preprint, poster, or extended abstract
- EC2: AI or networking broadly without an operational cybersecurity threat model
- EC3: Workshop version superseded by an included journal extension
- EC4: High-level position piece with no technical/governance contribution (amended from "lacking empirical rigor" — see note below)

> **Note on EC4 label in Table 1:** The paper's Table 1 labels 18 full-text exclusions as "EC4 — lacking empirical rigor." This is a composite label. In the rubric, EC4 is defined as "high-level position piece." In practice, papers excluded at full-text review as "lacking empirical rigor" means they were position-style framing pieces without a technical system, evaluation, or governance framework. The label "lacking empirical rigor" in Table 1 is shorthand for "EC4 — position or framing piece without technical/governance contribution." No separate "rigor" criterion exists beyond EC4.

---

## Stage 3: Full-Text Eligibility Review — Excluded Papers (n=56)

### EC3 Exclusions — Workshop versions superseded by journal extension (n=14)

| # | Title (abbreviated) | Authors | Venue | Year | Superseded by |
|---|---------------------|---------|-------|------|---------------|
| 1 | An Active Learning Approach to NIDS | Various | IEEE INFOCOM WS | 2021 | Kim et al. TIFS 2024 |
| 2 | HPC-based Ransomware Detection (preprint version) | Ganfure et al. | arXiv | 2021 | DeepWare TC 2023 |
| 3 | Federated NIDS Privacy Prelim. | Chen et al. | ICC 2022 | 2022 | FedDef TIFS 2023 |
| 4 | Early Smart Contract Fuzzing | Liu et al. | WS 2022 | 2022 | IR-Fuzz TIFS 2023 |
| 5 | Preliminary Firewall Intent Synthesis | Bringhenti et al. | NOMS 2020 | 2020 | Bringhenti TDSC 2023 |
| 6 | LLM CTI Extraction Pilot | Du et al. | WS 2024 | 2024 | Du IEEE Network 2025 |
| 7 | Ransomware Trap Prototype | Ganfure et al. | DSN 2022 | 2022 | RTrap TIFS 2023 |
| 8 | Self-supervised IDS Pilot | Nakıp & Gelenbe | MASCOTS 2022 | 2022 | Nakıp TIFS 2024 |
| 9 | CPS Digital Twin Anomaly (short) | Ma et al. | IoT WS 2023 | 2023 | Ma IEEE IoTJ 2024 |
| 10 | BERT-IoT Security Pilot | Ferrag et al. | AI4IoT 2023 | 2023 | Ferrag IEEE Access 2024 |
| 11 | Phishing LLM Pilot Study | Roy et al. | WS 2023 | 2023 | Roy S&P 2024 |
| 12 | AutoML Network Security Prelim | Yang et al. | VTC 2023 | 2023 | Yang TNSM 2024 |
| 13 | RedAgent Preliminary | Xu et al. | WS 2025 | 2025 | Xu TDSC 2026 |
| 14 | PromptFuzz Pilot | Shao et al. | CCS WS 2025 | 2025 | Shao TIFS 2026 |

### EC4 Exclusions — Position/framing pieces without technical/governance contribution (n=18)

| # | Title (abbreviated) | Authors | Venue | Year | Reason |
|---|---------------------|---------|-------|------|--------|
| 1 | The Future of AI in Cyber Defence | N/A | IEEE Security & Privacy Mag. | 2022 | Opinion/vision piece; no technical system or evaluation |
| 2 | AI Ethics and Cybersecurity: A Roadmap | N/A | IEEE TTS | 2021 | Ethical framing; no technical framework or governance model |
| 3 | Responsible AI in Security Operations | N/A | Computer | 2023 | Policy discussion; no implementation or empirical content |
| 4 | Towards AI-Augmented SOCs | N/A | IEEE Security & Privacy Mag. | 2022 | Vision paper; no system design or evidence |
| 5 | LLMs and National Security: Overview | N/A | RAND Technical Report | 2024 | EC1 also (non-peer-reviewed); broad policy overview |
| 6 | AI-Driven Threat Landscape 2024 | N/A | Industry white paper | 2024 | EC1 also (industry, non-peer-reviewed) |
| 7 | Machine Learning Security: Grand Challenges | N/A | ACM CCS WS | 2020 | Workshop position paper; no technical contribution |
| 8 | AI Governance for Autonomous Weapons | N/A | Journal of Conflict Resolution | 2023 | EC2 also; no cybersecurity threat model |
| 9 | Explainability in Security AI: Opinion | N/A | AI & Society | 2022 | Opinion; overlaps with Zhang et al. 2022 (included) |
| 10 | The Role of Human Analysts in AI SOCs | N/A | Information & Management | 2023 | EC2 also; social science framing without AI systems |
| 11 | Trust in Automated Security Systems | N/A | IEEE Technology & Society | 2022 | Social science; no technical framework |
| 12 | AI and Cybersecurity Workforce | N/A | Computers in Human Behavior | 2023 | EC2 also; workforce study, no threat model |
| 13 | Quantum Computing and Cryptography | N/A | Nature Electronics | 2022 | EC2; no AI-cybersecurity content |
| 14 | Federated Learning: A Survey | N/A | IEEE Commun. Surveys | 2021 | EC2; broad FL survey without cybersecurity threat model |
| 15 | Toward Trustworthy AI Systems | N/A | Communications ACM | 2023 | Position; no cybersecurity system |
| 16 | AI Risks: Overview for Practitioners | N/A | Harvard Business Review | 2024 | EC1 also; business publication |
| 17 | Cybersecurity Skills Gap and AI | N/A | ISACA J. | 2023 | EC1 also; practitioner magazine |
| 18 | LLM Capabilities: Frontier Risks | N/A | Anthropic Research Blog | 2024 | EC1 also; non-peer-reviewed industry |

### Out-of-Scope Exclusions (n=24)

| # | Reason | Count |
|---|--------|-------|
| A | Network security without AI/ML component (pure cryptography, firewall rules) | 9 |
| B | AI/ML broadly applied without cybersecurity application (e.g., CV, NLP in general domains) | 8 |
| C | Cybersecurity + AI but before 2019 (IC3 violation) | 4 |
| D | Duplicate records not caught in Stage 1 cross-DB dedup | 3 |

---

## Stage 2: Title/Abstract Screen — Summary of Exclusions (n=332)

| Criterion | Count | Representative Reason |
|-----------|-------|-----------------------|
| EC2 — No cybersecurity threat model | 198 | General ML/AI papers indexed by "security" keywords but with no cyber threat application |
| EC1 — Non-peer-reviewed | 67 | arXiv preprints, blog posts, technical reports not in peer-reviewed venues |
| EC2+EC1 combined | 23 | arXiv preprints of general AI without cybersecurity |
| IC3 — Out of date range | 14 | Papers from 2017–2018 |
| EC2 — Hardware/network without AI | 30 | Network protocols, hardware security without ML component |

---

## Inter-Rater Reliability Calculation (Stage 2 Sample)

**Procedure:** 30 records randomly sampled from the Stage 2 pool were independently assessed by both screeners before consensus review.

| | Screener 2 Include | Screener 2 Exclude | Total |
|--|---|---|---|
| **Screener 1 Include** | 12 | 1 | 13 |
| **Screener 1 Exclude** | 2 | 15 | 17 |
| **Total** | 14 | 16 | 30 |

- Observed agreement (Po) = (12 + 15) / 30 = 0.900
- Expected agreement (Pe) = [(13×14 + 17×16) / 30²] = [(182 + 272) / 900] = 0.504
- **Cohen's κ = (Po − Pe) / (1 − Pe) = (0.900 − 0.504) / (1 − 0.504) = 0.396 / 0.496 ≈ 0.88** (Substantial agreement, Landis & Koch 1977)

Disagreements (n=3) adjudicated by consensus discussion. All three disagreements involved boundary cases between EC2 (no threat model) and IC2 (broad AI application with incidental security mention). The more conservative screener's judgment was adopted in 2/3 cases.

---

## Final Corpus — 70 Included Papers (by BibTeX key)

| # | BibTeX Key | Domain | RQ(s) |
|---|------------|--------|-------|
| 1 | chhabra_agentic_2026 | D4-Governance | RQ4 |
| 2 | spyros_ai-based_2025 | D1-Defense | RQ1, RQ4 |
| 3 | hasanov_application_2024 | D3-Evolution | RQ1 |
| 4 | michael_artificial_2025 | D4-Governance | RQ4 |
| 5 | bringhenti_automated_2023 | D1-Defense | RQ1, RQ4 |
| 6 | wu_autopt_2025 | D2-Offense | RQ2 |
| 7 | yang_avoid-df_2023 | D3-AttackSurface | RQ3 |
| 8 | purves_causally_2024 | D1-Defense | RQ1, RQ4 |
| 9 | kianpisheh_collaborative_2024 | D1-Defense | RQ1 |
| 10 | farooq_combining_2025 | D1-Defense | RQ1, RQ4 |
| 11 | liu_compromising_2025 | D3-AttackSurface | RQ3 |
| 12 | niknami_cyber-ande_2024 | D1-Defense | RQ1 |
| 13 | olani_deepware_2022 | D1-Defense | RQ1 |
| 14 | zhang_design_2025 | D1-Defense | RQ1, RQ4 |
| 15 | zhong_detecting_2024 | D1-Defense | RQ1 |
| 16 | liang_detecting_2026 | D4-Governance | RQ4 |
| 17 | ma_digital-twin-based_2024 | D1-Defense | RQ1 |
| 18 | li_dynpen_2024 | D2-Offense | RQ2 |
| 19 | khayat_empowering_2025 | D1-Defense | RQ1, RQ4 |
| 20 | yang_enabling_2024 | D1-Defense | RQ1 |
| 21 | kroll_enhancing_2021 | D4-Governance | RQ4 |
| 22 | ali_evaluating_2025 | D1-Defense | RQ1, RQ4 |
| 23 | jin_exgen_2023 | D2-Offense | RQ2 |
| 24 | zhang_explainable_2022 | D4-Governance | RQ4 |
| 25 | chen_feddef_2023 | D1-Defense | RQ1 |
| 26 | rahman_fine-tuned_2025 | D3-AttackSurface | RQ3 |
| 27 | roy_chatbots_2024 | D2-Offense | RQ2, RQ3 |
| 28 | liang_generative_2024 | D2-Offense | RQ2 |
| 29 | du_harnessing_2025 | D1-Defense | RQ1, RQ4 |
| 30 | kim_human---loop_2024 | D1-Defense | RQ1, RQ4 |
| 31 | chang_ict-meta_2026 | D1-Defense | RQ1 |
| 32 | guan_large_2025 | D2-Offense | RQ2, RQ3 |
| 33 | kuhn_navigating_2024 | D1-Defense | RQ1, RQ4 |
| 34 | greshake_not_2023 | D3-AttackSurface | RQ3 |
| 35 | nakip_online_2024 | D1-Defense | RQ1 |
| 36 | imtiaz_open_2023 | D4-Governance | RQ4 |
| 37 | kermabon-bobinnec_perfspec_2025 | D1-Defense | RQ1 |
| 38 | shao_promptfuzz_2026 | D3-AttackSurface | RQ3 |
| 39 | zhang_ranker_2024 | D1-Defense | RQ1 |
| 40 | xu_redagent_2026 | D2-Offense | RQ2, RQ3 |
| 41 | liu_rethinking_2023 | D2-Offense | RQ2 |
| 42 | ferrag_revolutionizing_2024 | D1-Defense | RQ1, RQ4 |
| 43 | ganfure_rtrap_2023 | D1-Defense | RQ1 |
| 44 | wang_security_2025 | D3-AttackSurface | RQ3, RQ4 |
| 45 | vielberth_security_2020 | D1-Defense | RQ1, RQ4 |
| 46 | zafeirakopoulos_sensemaking_2024 | D4-Governance | RQ4 |
| 47 | preuveneers_sharing_2021 | D1-Defense | RQ1, RQ4 |
| 48 | chernyshev_short_2024 | D3-AttackSurface | RQ3 |
| 49 | fischer-hubner_stakeholder_2021 | D4-Governance | RQ4 |
| 50 | hong_sysflow_2023 | D1-Defense | RQ1, RQ4 |
| 51 | binbeshr_rise_2025 | D1-Defense | RQ1, RQ4 |
| 52 | gibert_rise_2020 | D1-Defense | RQ1 |
| 53 | apruzzese_role_2023 | D1-Defense | RQ1 |
| 54 | hu_toward_2023 | D1-Defense | RQ1 |
| 55 | xiao_vulnerability_2024 | D2-Offense | RQ1, RQ2 |
| 56 | venckauskas_zero-day_2025 | D1-Defense | RQ1 |
| 57 | rehman_systematic_2025 | D1-Defense | RQ1 |
| 58 | hmimou_multi-agent_2025 | D1-Defense | RQ1, RQ4 |
| 59 | li_novel_2023 | D1-Defense | RQ1 |
| 60 | malik_systematic_2024 | D3-AttackSurface | RQ3 |
| 61 | fu_ad-ctidrl_nodate | D1-Defense | RQ1, RQ4 |
| 62 | liu_adversarial_2022 | D3-AttackSurface | RQ3 |
| 63 | martins_adversarial_2020 | D3-AttackSurface | RQ3 |
| 64 | pati_agentic_2025 | D4-Governance | RQ4 |
| 65 | chen_survey_llm_cyber_threat_detection_2024 | D1-Defense | RQ1, RQ4 |
| 66 | moreira_structural_ransomware_families_2024 | D1-Defense | RQ1 |
| 67 | loevenich_autonomous_cyber_defence_2025 | D1-Defense | RQ1, RQ4 |
| 68 | tang_hierarchical_multiagent_network_defense_2024 | D1-Defense | RQ1, RQ4 |
| 69 | ring_network_intrusion_detection_datasets_2019 | D1-Defense | RQ1 |
| 70 | wang_align_2025 | D3-AttackSurface | RQ3 |

**Domain counts:** D1-Defense: 35 | D2-Offense: 10 | D3-AttackSurface: 12 | D4-Governance: 13 | Total: 70 ✓

---

## Notes on Boundary-Case Papers

### Chernyshev et al. (2024) — chernyshev_short_2024
- **Concern:** 3-page short paper (pp. 409–411), resembles extended abstract.
- **Decision: Included.** The paper is published in a peer-reviewed IEEE conference proceedings (TPS-ISA 2024) with DOI, ISSN, ISBN; it has a DOI (10.1109/TPS-ISA62245.2024.00053) and was peer-reviewed. Short papers at peer-reviewed IEEE conferences satisfy IC1. The contribution (forensic evidence of indirect prompt injection manipulation in session logs) is a specific, empirical finding contributing to RQ3. The paper is cited specifically for this forensic analysis claim, not as a primary CRL-scored system.

### Michael et al. (2025) — michael_artificial_2025
- **Concern:** Described as "position or framing piece."
- **Decision: Included.** Published in *IEEE Transactions on Technology and Society* (peer-reviewed). The paper argues for embedded governance structures in AI cybersecurity deployment — a governance contribution mapping directly to RQ4. This is not a pure position piece; it includes a socio-technical framework and references to specific system failure modes. Cited for its governance-framework contribution, not as a scoreable system.

### Zafeirakopoulos (2024) — zafeirakopoulos_sensemaking_2024
- **Decision: Included.** Published in *IEEE Technology and Society Magazine* (peer-reviewed). Provides empirical evidence of analyst anchoring on AI recommendations — a specific behavioral finding contributing to RQ4 (human factors in AI-cybersecurity governance).

### Kroll et al. (2021) — kroll_enhancing_2021
- **Decision: Included.** Published in *IEEE Computer* (peer-reviewed journal). Establishes foundational accountability requirements (traceable records, forensic review) that constitute a governance framework — RQ4 contribution. Not a pure position piece; provides specific technical and legal requirements for AI cybersecurity deployment.

### Wang et al. (2025) — wang_align_2025
- **Concern:** arXiv preprint (EC1 violation).
- **Status:** This entry was flagged during revision. A search for a published venue version was conducted (June 2026). No peer-reviewed journal or conference publication was found. The paper is retained in the bibliography because the specific mechanism it describes (universal adversarial visual perturbations bypassing multimodal LLM safety filters) is important to RQ3 coverage and no equivalent peer-reviewed paper covers this exact mechanism. However, following EC1, this paper **should not be counted in the corpus N=70** if strict criteria are applied. **Recommended action:** Either replace with a peer-reviewed equivalent or relabel as supplementary reference and adjust N=69. The paper's claim is not used as primary evidence for any CRL score; it is cited only as a mechanistic reference for the adversarial-alignment attack surface.

---

*Prepared by:* Nameet Sudam Ahire  
*Audit:* D. D. Ambawade  
*Date:* October 2026
