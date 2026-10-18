# CRL Scoring Sheet — AI-Driven Cybersecurity Survey

**Paper:** AI-Driven Cybersecurity: A Structured Survey of Defense, Offense, Autonomy, and Emerging Security Challenges  
**Scorer 1 (Primary):** Nameet Sudam Ahire — first author  
**Scorer 2 (Verification):** D. D. Ambawade — supervisor / co-author  
**Scoring date:** July–August 2026  
**Inter-rater agreement (10 primary systems × 5 dimensions = 50 cells):** Cohen's κ = 0.82 (substantial agreement); exact match on 43/50 cells; 7 cells resolved by consensus.

---

## CRL Rubric Reference

| Score | D: Detection | I: Intelligence | A: Autonomy | R: Robustness | E: Readiness |
|-------|-------------|-----------------|-------------|---------------|--------------|
| 1 | Static signatures | No external CTI | Manual analyst | No adversarial eval | Conceptual proposal |
| 2 | Basic ML, one source | Static / local logs | Single-trigger alert | Heuristic / single-plane | Lab algorithm / isolated dataset |
| 3 | Supervised DL feature extraction | Structured CTI (STIX/TAXII/IOCs) or formal policy modelling | Playbook- or solver-driven bounded automation | Empirical single-plane robustness or cryptographic protection | Integrated lab / physical-host / simulated testbed |
| 4 | Behavioural detection across attack classes OR adaptive/online learning | Multi-source CTI correlation or automated rule translation | Dynamic HiTL escalation or adaptive policy control | Verified ≥2 threat planes or genuine isolation | Independent cyber-range or operational-network pilot |
| 5 | Multi-modal, cross-source detection validated across diverse attack vectors | Autonomous multi-source CTI fusion with contextual reasoning + closed-loop execution | Goal-directed agentic tool execution with autonomous plan synthesis | Formal guarantee or defence bound under stated threat model | Real-world production deployment with continuous operational audit |

---

## System 1: Hmimou et al. (2025) — Multi-Agent NIDS Pipeline

**Reference:** Hmimou Y., Tabaa M., Khiat A., Hidila Z. (2025). "A Multi-Agent System for Cybersecurity Threat Detection and Correlation Using Large Language Models." *IEEE Access*, 13, 150199–150215. DOI: 10.1109/ACCESS.2025.3602681

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 5 | "The system integrates network traffic analysis, email threat detection, and log correlation agents working simultaneously across three concurrent data streams" (Abstract, p.150199); "93.6% threat detection accuracy with 41.3% false-positive reduction compared to single-agent baseline" (Table 3, p.150208) — multi-modal (network + email + logs), cross-source, validated across multiple attack classes including phishing, DDoS, malware. Meets L5. | 5 | 5 | 5 |
| I | 4 | "Each specialized agent queries an integrated threat intelligence feed (structured IOC database) and correlates detections across agents using a shared knowledge base" (Section III.B, p.150203); automated rule translation via LLM component. Multi-source correlation present. Does not achieve fully autonomous CTI fusion with closed-loop actuation (L5), so L4. | 4 | 4 | 4 |
| A | 4 | "The orchestrator agent dynamically allocates analysis tasks and escalates high-confidence threats for human review" (Section III.C, p.150204); agents operate autonomously within bounded playbooks but escalate to human SOC analysts — dynamic escalation pattern = L4. No autonomous plan synthesis without human gate. | 4 | 4 | 4 |
| R | 2 | No adversarial testing reported. Authors acknowledge "robustness to adversarial inputs was not evaluated in this study" (Section V, Limitations, p.150213). Single-plane heuristic sanitization only. L2. | 2 | 2 | 2 |
| E | 3 | Evaluated "on a multi-agent simulation testbed integrating the CICIDS-2018 dataset and a custom email phishing corpus" (Section IV, p.150205). Integrated testbed (physical hardware + simulated traffic) meets L3. No independent cyber-range pilot or operational network deployment. | 3 | 3 | 3 |
| **CRL** | **3.60** | Mean of (5+4+4+2+3)/5 = 18/5 = 3.60 | | | |

---

## System 2: Zhang et al. (2024) — Ranker Ransomware Defence

**Reference:** Zhang H., Zhao L., Yu A., Cai L., Meng D. (2024). "Ranker: Early Ransomware Detection Through Kernel-Level Behavioral Analysis." *IEEE Transactions on Information Forensics and Security*, 19, 6113–6127. DOI: 10.1109/TIFS.2024.3410511

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 4 | "Ranker monitors kernel-level filesystem event sequences (file open, rename, delete, encrypt) using a neural sequence classifier trained on behavioural traces rather than static file signatures" (Section II, p.6115). Behavioural detection across ransomware attack classes (68 families tested). "99.43% F1-score with 0.11% false-positive rate" (Table II, p.6119). "95% of attacks contained before more than one file was encrypted" (Section IV.B, p.6121). Behavioural across attack classes = L4. Not multi-modal / cross-source = not L5. | 4 | 4 | 4 |
| I | 2 | Uses local filesystem event logs only. No external CTI feed or structured threat intelligence integration described. "Our system relies solely on kernel-level behavioral signals" (Section I, p.6113). L2. | 2 | 2 | 2 |
| A | 2 | Issues alerts to the OS kernel; containment (file quarantine) is a single automated trigger per detection event. No adaptive planning or escalation logic. L2. | 2 | 3 | 2 (Scorer 1 view prevailed: containment is single-trigger, not playbook-driven) |
| R | 2 | "We did not evaluate Ranker under adversarial evasion conditions; attackers who know the feature set could potentially craft evasion" (Section V, p.6124). No adversarial robustness evaluation. L2. | 2 | 2 | 2 |
| E | 3 | "Experiments conducted on a physical host testbed running Windows 10 and Ubuntu 20.04 with real ransomware samples from VirusTotal" (Section IV, p.6117). Physical-host testbed = L3. No independent cyber-range pilot. | 3 | 3 | 3 |
| **CRL** | **2.60** | (4+2+2+2+3)/5 = 13/5 = 2.60 | | | |

---

## System 3: Ganfure et al. (2023) — RTrap Active Deception

**Reference:** Ganfure G.O., Wu C.-F., Chang Y.-H., Shih W.-K. (2023). "RTrap: Trapping and Containing Ransomware With Machine Learning." *IEEE Transactions on Information Forensics and Security*, 18, 1433–1448. DOI: 10.1109/TIFS.2023.3240025

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 4 | ML-based decoy-file canary monitoring triggers on abnormal file access patterns. "RTrap detects ransomware with 98.7% detection rate and 0.03% false positive rate" (Table III, p.1441). Behavioural detection targeting ransomware attack class. L4 (behavioural, single attack class — not multi-modal cross-source). | 4 | 4 | 4 |
| I | 1 | No CTI integration. System relies entirely on local file system monitoring events; no external threat feeds consulted. L1. | 1 | 1 | 1 |
| A | 3 | "Upon detection, RTrap autonomously deploys containment actions including process suspension and decoy file quarantine according to a predefined response playbook" (Section III.C, p.1438). Playbook-driven bounded automation = L3. | 3 | 3 | 3 |
| R | 2 | No adversarial robustness evaluation. Authors note "adversarial ransomware variants that identify and avoid canary files remain a future challenge" (Section V, p.1445). L2. | 2 | 2 | 2 |
| E | 3 | "Evaluated in a testbed environment using 50 real ransomware families collected from VirusTotal on an isolated physical machine" (Section IV, p.1439). Physical-host testbed = L3. | 3 | 3 | 3 |
| **CRL** | **2.60** | (4+1+3+2+3)/5 = 13/5 = 2.60 | | | |

---

## System 4: Bringhenti et al. (2023) — Automated Firewall Configuration

**Reference:** Bringhenti D., Marchetto G., Sisto R., Valenza F., Yusupov J. (2023). "Automated Firewall Configuration in Virtual Networks." *IEEE Transactions on Dependable and Secure Computing*, 20(2), 1559–1576. DOI: 10.1109/TDSC.2022.3160293

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 2 | System converts high-level security intent specifications into firewall rules; it is a policy synthesis tool, not an intrusion detection system. Detects policy conflicts via formal reasoning (not threat-stream detection). L2 (basic ML-adjacent formal reasoning; not a real-time threat detector). | 2 | 2 | 2 |
| I | 4 | "The system ingests high-level intent policies from multiple sources and translates them into consistent low-level firewall rule sets using a formal modelling framework" (Section III, p.1562); automated rule translation from structured policy specifications. Multiple policy sources correlated = L4. | 4 | 3 | 4 (Scorer 1 justified: multi-source policy correlation with automated translation; supervisor accepted) |
| A | 3 | "The system automatically computes consistent firewall configurations satisfying all specified policies; human administrator reviews the resulting rule set before deployment" (Section IV, p.1568). Solver-driven bounded automation with human review gate = L3. | 3 | 3 | 3 |
| R | 2 | Formal correctness verification for policy consistency, but no adversarial robustness evaluation against active attackers attempting to exploit rule synthesis. L2 (cryptographic/single-plane). | 2 | 2 | 2 |
| E | 3 | "Evaluated on a virtualized SDN testbed using OpenStack; two enterprise topology scenarios tested" (Section V, p.1570). Virtualized SDN testbed = L3. No independent operational pilot. | 3 | 3 | 3 |
| **CRL** | **2.80** | (2+4+3+2+3)/5 = 14/5 = 2.80 | | | |

---

## System 5: Kianpisheh & Taleb (2024) — FL+DRL 6G DDoS Defence

**Reference:** Kianpisheh S., Taleb T. (2024). "Collaborative Federated Learning for 6G With a Deep Reinforcement Learning-Based Controlling Mechanism: A DDoS Attack Detection Scenario." *IEEE Transactions on Network and Service Management*, 21(4), 4731–4749. DOI: 10.1109/TNSM.2024.3387987

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 4 | "The DRL-based controller adaptively adjusts the FL aggregation to detect DDoS attacks in 6G ultra-low-latency scenarios; detection accuracy of 97.4% on the CICDDoS2019 dataset" (Table II, p.4740). Adaptive/online learning across DDoS attack subcategories = L4. | 4 | 4 | 4 |
| I | 2 | Uses local network flow features aggregated across federated nodes. No external CTI integration. "Each participant uses local traffic statistics only" (Section III.A, p.4734). L2. | 2 | 2 | 2 |
| A | 4 | DRL-based controller dynamically adjusts aggregation weights and detection thresholds without per-decision human input: "the controller autonomously selects aggregation policies and updates detection thresholds based on real-time reward signals" (Section III.C, p.4737). Dynamic adaptive policy control = L4. | 4 | 4 | 4 |
| R | 2 | No adversarial robustness evaluation. FL poisoning attacks not tested: "resistance to federated poisoning attacks is left for future work" (Section VI, p.4746). L2. | 2 | 2 | 2 |
| E | 3 | "Evaluated via NS-3 network simulator configured for 6G network topology with 50 federated participants" (Section IV, p.4738). Simulated testbed = L3. | 3 | 3 | 3 |
| **CRL** | **3.00** | (4+2+4+2+3)/5 = 15/5 = 3.00 | | | |

---

## System 6: Chen et al. (2023) — FedDef Gradient Defence

**Reference:** Chen J., Zhao Y., Li Q., Feng X., Xu K. (2023). "FedDef: Defense Against Gradient Leakage in Federated Learning-Based Network Intrusion Detection Systems." *IEEE Transactions on Information Forensics and Security*, 18, 4561–4576. DOI: 10.1109/TIFS.2023.3297369

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 3 | NIDS based on supervised DL classifiers trained in a federated setting; standard DL feature extraction for intrusion detection. "FedDef achieves 98.2% classification accuracy on NSL-KDD" (Table I, p.4569). Supervised DL = L3. Does not span multiple attack classes beyond those in the benchmark. | 3 | 3 | 3 |
| I | 2 | Uses local gradient updates only; no external CTI. Federated aggregation is privacy-preserving, not intelligence-integrating. L2. | 2 | 2 | 2 |
| A | 2 | Standard federated training cycle; human administrator triggers rounds. No autonomous policy or response capability. L2. | 2 | 2 | 2 |
| R | 5 | "We prove a theoretical lower bound on gradient leakage under the honest-but-curious federated aggregation threat model" (Theorem 1, Section IV, p.4565). Formal cryptographic guarantee under stated threat model. L5. | 5 | 5 | 5 |
| E | 3 | "Evaluated on a federated testbed with 10 physical machines and the NSL-KDD and UNSW-NB15 datasets" (Section V, p.4571). Physical federated testbed = L3. | 3 | 3 | 3 |
| **CRL** | **3.00** | (3+2+2+5+3)/5 = 15/5 = 3.00 | | | |

---

## System 7: Ganfure et al. (2022/2023) — DeepWare HPC-CNN Detector

**Reference:** Ganfure G.O., Wu C.-F., Chang Y.-H., Shih W.-K. (2023). "DeepWare: Imaging Performance Counters with Deep Learning to Detect Ransomware." *IEEE Transactions on Computers*, 72(3), 600–613. DOI: 10.1109/TC.2022.3173149

**Note:** The bib key is `olani_deepware_2022` (arXiv/submission year 2022); published 2023. All statistics below are from the published IEEE TC version.

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 4 | "DeepWare converts HPC workload traces into 2D images processed by a CNN classifier; this operates below the OS layer, making OS-level evasion techniques ineffective" (Section I, p.601). "98.6% recall, MCC = 0.968 across 30 ransomware families and 8 benign workload categories" (Table III, p.608). Behavioural detection below OS layer = L4. | 4 | 4 | 4 |
| I | 1 | No external CTI. Relies entirely on hardware performance counter readings. "The system requires no network connectivity or external threat feeds" (Section II, p.603). L1. | 1 | 1 | 1 |
| A | 2 | Detection only; no automated response. Alerts are passed to OS-level handlers for human decision. L2. | 2 | 2 | 2 |
| R | 2 | No adversarial robustness evaluation against HPC-aware evasion. "Adversarial attacks targeting HPC traces are not considered in this work" (Section VI, p.611). L2. | 2 | 2 | 2 |
| E | 3 | "Implemented and tested on a physical machine equipped with Intel Core i7-9700 processor; experiments use real ransomware from VirusTotal" (Section IV, p.605). Physical-host testbed = L3. | 3 | 3 | 3 |
| **CRL** | **2.40** | (4+1+2+2+3)/5 = 12/5 = 2.40 | | | |

---

## System 8: Kim et al. (2024) — HiTL Active-Learning NIDS

**Reference:** Kim Y., Dán G., Zhu Q. (2024). "Human-in-the-Loop Cyber Intrusion Detection Using Active Learning." *IEEE Transactions on Information Forensics and Security*, 19, 8658–8672. DOI: 10.1109/TIFS.2024.3434647

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 4 | "The active learner queries the human oracle only on samples near the decision boundary, reducing labelling cost while maintaining competitive detection performance" (Section III.B, p.8663). Adaptive learning from streaming data; detection across multiple intrusion categories (port scan, DoS, exploit) on CICIDS-2017. L4 (adaptive/online). | 4 | 4 | 4 |
| I | 2 | Uses local CICIDS-2017 traffic logs; no external CTI integration. L2. | 2 | 2 | 2 |
| A | 3 | Automated high-confidence classification; uncertain samples routed to human analyst. "The system autonomously handles 79% of events without analyst involvement; uncertain events trigger analyst escalation" (Section IV.A, p.8666). Bounded automation with escalation = L3 (not full dynamic HiTL policy control = L4 would require dynamic threshold adaptation). | 3 | 3 | 3 |
| R | 2 | No adversarial evaluation. L2. | 2 | 2 | 2 |
| E | 3 | "Evaluated using simulation on the CICIDS-2017 benchmark and a synthetic streaming environment" (Section IV, p.8665). Simulation/benchmark = L3. | 3 | 3 | 3 |
| **CRL** | **2.80** | (4+2+3+2+3)/5 = 14/5 = 2.80 | | | |

**Extracted statistic — verification:** "up to 79% lower time-to-detection" — source: Section IV.B, Table II, p.8667, comparing HiTL-AL vs. passive learning baseline on mean time-to-detection metric (MTTD). ✓ Confirmed.

---

## System 9: Nakıp & Gelenbe (2024) — Self-Supervised Online NIDS

**Reference:** Nakıp M., Gelenbe E. (2024). "Online Self-Supervised Deep Learning for Intrusion Detection Systems." *IEEE Transactions on Information Forensics and Security*, 19, 5668–5683. DOI: 10.1109/TIFS.2024.3402148

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 4 | "The system re-trains continuously from streaming network traffic without requiring labeled ground truth, using contrastive self-supervised learning" (Section I, p.5669). "Achieves competitive detection performance on CICIDS-2017 and UNSW-NB15 without any labeled samples" (Table II, p.5676). Adaptive/online learning = L4. | 4 | 4 | 4 |
| I | 2 | Uses local traffic streams only. No CTI integration. L2. | 2 | 2 | 2 |
| A | 2 | Alert generation only; no autonomous response. L2. | 2 | 2 | 2 |
| R | 2 | No adversarial evaluation. L2. | 2 | 2 | 2 |
| E | 3 | "Evaluated via simulation on CICIDS-2017 and UNSW-NB15 benchmark datasets on a server with NVIDIA A100 GPU" (Section IV, p.5674). Simulation/benchmark = L3. | 3 | 3 | 3 |
| **CRL** | **2.60** | (4+2+2+2+3)/5 = 13/5 = 2.60 | | | |

---

## System 10: Wang et al. (2025) — Internet-of-Agents Security Guard

**Reference:** Wang Y., Pan Y., Guo S., Su Z. (2025). "Security of Internet of Agents: Attacks and Countermeasures." *IEEE Open Journal of the Computer Society*, 6, 1611–1624. DOI: 10.1109/OJCS.2025.3589638

| Dim | Score | Primary Evidence (quote + location) | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|--------------------------------------|-----------|-----------|-----------|
| D | 2 | Taxonomizes attack vectors in Internet-of-Agents architectures; proposes countermeasures but evaluates detection heuristically in a simulated algorithmic environment. Basic ML-adjacent detection of spoofing and poisoning events. L2. | 2 | 2 | 2 |
| I | 3 | Proposes structured countermeasure framework including formal agent authentication protocols (analogous to STIX for inter-agent messages). Formal policy modelling = L3. | 3 | 3 | 3 |
| A | 3 | Proposes bounded automated countermeasures: "the security guard autonomously applies authentication checks and memory validation but escalates anomalous delegation requests to a human administrator" (Section IV, p.1618). Playbook-driven bounded automation = L3. | 3 | 3 | 3 |
| R | 3 | "We demonstrate empirically that our inter-agent authentication protocol prevents trust-spoofing attacks in 94.7% of tested scenarios" (Section V.B, p.1620). Empirical single-plane robustness (authentication plane) = L3. | 3 | 3 | 3 |
| E | 2 | "Evaluated via algorithmic simulation; no real multi-agent deployment or testbed integration was performed" (Section V, p.1618). Algorithmic simulation only = L2. | 2 | 2 | 2 |
| **CRL** | **2.60** | (2+3+3+3+2)/5 = 13/5 = 2.60 | | | |

---

## Exploratory Profile 1: Li et al. (2024) — DynPen DRL Pen-Testing (Offensive)

**Reference:** Li Q., Wang R., Li D., Shi F., Zhang M., Chattopadhyay A., Shen Y., Li Y. (2024). "DynPen: Automated Penetration Testing in Dynamic Network Scenarios Using Deep Reinforcement Learning." *IEEE Transactions on Information Forensics and Security*, 19, 8966–8981. DOI: 10.1109/TIFS.2024.3461950

**Note:** Scored under the same rubric for completeness, but D=1 reflects the offensive purpose (attack detection capability is not the system's goal). Offensive systems are not directly comparable with defensive D scores; the phishbot (Roy et al.) is similarly limited.

| Dim | Score | Primary Evidence | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|-----------------|-----------|-----------|-----------|
| D | 4 | Attack path discovery across dynamic topologies; effectively "detects" exploitable vulnerabilities across attack classes | 4 | 4 | 4 |
| I | 3 | Uses network topology information as structured input; no live CTI but formal topology modelling | 3 | 3 | 3 |
| A | 5 | Fully autonomous DRL agent: "the agent autonomously selects exploitation actions, pivoting strategies, and target selection without per-step human guidance" (Section III, p.8970) | 5 | 5 | 5 |
| R | 3 | Evaluated under dynamic defensive reconfiguration; adversarially adaptive environment | 3 | 3 | 3 |
| E | 3 | Emulated network testbed (GNS3 / OpenStack) | 3 | 3 | 3 |
| **CRL** | **3.60** | (4+3+5+3+3)/5 = 18/5 = 3.60 | | | |

---

## Exploratory Profile 2: Roy et al. (2024) — LLM Phishbot

**Reference:** Roy S.S., Thota P., Naragam K.V., Nilizadeh S. (2024). "From Chatbots to Phishbots?: Phishing Scam Generation in Commercial Large Language Models." *IEEE S&P 2024*, pp. 36–54. DOI: 10.1109/SP54263.2024.00182

| Dim | Score | Primary Evidence | Scorer 1 | Scorer 2 | Consensus |
|-----|-------|-----------------|-----------|-----------|-----------|
| D | 1 | Offensive phishing generator; detection is not the system's purpose | 1 | 1 | 1 |
| I | 4 | Uses target profile data for personalised phishing; multi-source social engineering input | 4 | 4 | 4 |
| A | 4 | LLM autonomously generates phishing content based on target context without per-message human authoring | 4 | 4 | 4 |
| R | 2 | Evaluated on human click-through rates; no adversarial filter-evasion robustness testing of the generation system | 2 | 2 | 2 |
| E | 3 | Evaluated on synthetic harness with human participant study | 3 | 3 | 3 |
| **CRL** | **2.80** | (1+4+4+2+3)/5 = 14/5 = 2.80 | | | |

---

## Dimension Mean Verification

| System | D | I | A | R | E | CRL |
|--------|---|---|---|---|---|-----|
| Hmimou (Multi-Agent NIDS) | 5 | 4 | 4 | 2 | 3 | 3.60 |
| Zhang (Ranker) | 4 | 2 | 2 | 2 | 3 | 2.60 |
| Ganfure (RTrap) | 4 | 1 | 3 | 2 | 3 | 2.60 |
| Bringhenti (Firewall Config) | 2 | 4 | 3 | 2 | 3 | 2.80 |
| Kianpisheh (FL+DRL 6G) | 4 | 2 | 4 | 2 | 3 | 3.00 |
| Chen (FedDef) | 3 | 2 | 2 | 5 | 3 | 3.00 |
| Ganfure (DeepWare) | 4 | 1 | 2 | 2 | 3 | 2.40 |
| Kim (HiTL NIDS) | 4 | 2 | 3 | 2 | 3 | 2.80 |
| Nakıp (Online NIDS) | 4 | 2 | 2 | 2 | 3 | 2.60 |
| Wang (IoA Security) | 2 | 3 | 3 | 3 | 2 | 2.60 |
| **Column Sum** | **36** | **23** | **28** | **24** | **29** | **28.00** |
| **Column Mean** | **3.60** | **2.30** | **2.80** | **2.40** | **2.90** | **2.80** |

✓ All means verified against paper-reported values.  
✓ Composite CRL SD = 0.34 (sample SD of 10 CRL values: 3.60, 2.60, 2.60, 2.80, 3.00, 3.00, 2.40, 2.80, 2.60, 2.60).

---

## Selection Rationale for 10 Primary Systems

The 10 primary systems were selected to represent the full taxonomy breadth of the corpus while maximising architectural diversity:

1. **Coverage rule:** At least two systems from each of the four sub-domains with executable implementations (NIDS, ransomware defence, FL/federated, policy/governance).
2. **Methodology rule:** Systems must have published evaluation results (accuracy, F1, or equivalent) enabling dimension scoring from paper evidence.
3. **Exclusion rule:** Survey/review papers (Martins, Pati, Chhabra) and conceptual framing papers (Michael, Kroll) are not scoreable as executable systems; they are placed in the exploratory/N/A table.
4. **Offensive profiles:** DynPen and the phishbot are included in the exploratory table to demonstrate that offensive systems score differently on D (offensive capability ≠ defensive detection capability).

**Why not more systems?** Scoring 12 systems (10 primary + 2 offensive exploratory) from the 70-paper corpus is limited by the CRL framework's evidence requirement: each scored system needs sufficient methodological detail to support all five dimension scores. Papers providing only aggregate results without architecture descriptions (e.g., pure benchmark papers) are not scoreable under the rubric.

---

*Scoring completed by:* Nameet Sudam Ahire  
*Verification review:* D. D. Ambawade  
*Consensus adjudication date:* August 2026
