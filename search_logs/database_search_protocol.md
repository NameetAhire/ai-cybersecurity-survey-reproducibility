# Database Search Protocol — AI-Driven Cybersecurity Survey

**Paper:** AI-Driven Cybersecurity: A Structured Survey of Defense, Offense, Autonomy, and Emerging Security Challenges  
**Authors:** Nameet Sudam Ahire, Dayanand D. Ambawade  
**Target journal:** Journal of Information Security and Applications (JISA), Elsevier  
**Search execution period:** January 2026 – August 2026  
**Corpus date range:** January 2019 – August 2026  

---

## 1. Boolean Search Query

The primary Boolean query was executed verbatim in each database. Minor syntax adaptations were required by individual platform query parsers (noted per database):

```
("Artificial Intelligence" OR "Machine Learning" OR "Deep Learning"
 OR "LLM" OR "Large Language Model" OR "Agentic AI"
 OR "Federated Learning" OR "Generative AI")
AND
("Intrusion Detection" OR "Ransomware" OR "Zero Trust"
 OR "Penetration Testing" OR "Prompt Injection"
 OR "Adversarial Machine Learning" OR "Security Operations"
 OR "Cyber Threat Intelligence" OR "Autonomous Cyber Defense"
 OR "Deepfake Detection" OR "Smart Contract Security"
 OR "Supply Chain Security" OR "Digital Twin Security"
 OR "Exploit Generation" OR "Adversarial Robustness")
```

**Rationale for extended term set:** The Boolean query deliberately includes topic terms beyond the most common fields (IDS, ransomware) because the four-dimensional taxonomy (Defense / Offense / AI-Attack-Surface / Governance) required coverage of offensive tools (penetration testing, exploit generation), AI-specific threats (prompt injection, adversarial ML, deepfakes), and governance/supply-chain dimensions. All retained papers must map to at least one of the five Research Questions (RQ1–RQ5).

---

## 2. Per-Database Search Execution Log

### 2.1 IEEE Xplore

| Parameter | Value |
|-----------|-------|
| Database | IEEE Xplore Digital Library |
| URL | https://ieeexplore.ieee.org/search/searchresult.jsp |
| Search fields | Full text and metadata |
| Date filter | 2019-01-01 to 2026-08-31 |
| Publication types | Journals, Magazines, Conference Proceedings |
| Execution date | 2026-06-10 |
| **Raw hits** | **387** |
| After dedup (within DB) | 374 |

**Platform note:** IEEE Xplore uses proximity operators; `"LLM"` was also searched as `"large language model"` via OR to catch non-abbreviated titles.

---

### 2.2 ScienceDirect (Elsevier)

| Parameter | Value |
|-----------|-------|
| Database | ScienceDirect |
| URL | https://www.sciencedirect.com/search |
| Search fields | Title, Abstract, Keywords |
| Date filter | 2019 to 2026 |
| Publication types | Journal articles |
| Execution date | 2026-06-12 |
| **Raw hits** | **89** |
| After dedup (within DB) | 86 |

**Platform note:** ScienceDirect Advanced Search was used. The query was split into two runs (AI terms AND cybersecurity terms) combined via OR union of result sets. Elsevier journals targeted: *JISA*, *Computers & Security*, *Computer Networks*, *JNCA*.

---

### 2.3 Scopus

| Parameter | Value |
|-----------|-------|
| Database | Scopus (Elsevier) |
| URL | https://www.scopus.com/search/form.uri |
| Search fields | TITLE-ABS-KEY |
| Date filter | PUBYEAR > 2018 AND PUBYEAR < 2027 |
| Publication types | Article, Conference paper, Review |
| Execution date | 2026-06-14 |
| **Raw hits** | **62** |
| After dedup (within DB) | 58 |

**Platform note:** Scopus overlap with IEEE Xplore is high for IEEE journal papers; cross-database deduplication removed most overlaps at Stage 1 screening.

---

### 2.4 Google Scholar

| Parameter | Value |
|-----------|-------|
| Database | Google Scholar |
| URL | https://scholar.google.com |
| Search fields | Full text |
| Date filter | Custom range 2019–2026 |
| Execution date | 2026-06-18 |
| **Raw hits (first 10 pages)** | **68** |
| After dedup (within DB) | 61 |

**Platform note:** Google Scholar does not provide exact hit counts for complex Boolean queries. Search was executed across five targeted sub-queries (one per taxonomy domain) and results pooled. Only the first 10 pages (100 results) per sub-query were examined, as recall drops sharply beyond this threshold for well-specified queries. Google Scholar was used primarily to surface papers in ACM DL and SpringerOpen venues not well indexed by IEEE Xplore.

---

### 2.5 SpringerLink

| Parameter | Value |
|-----------|-------|
| Database | SpringerLink |
| URL | https://link.springer.com/search |
| Search fields | Full text |
| Date filter | 2019 to 2026 |
| Publication types | Journal article |
| Execution date | 2026-06-20 |
| **Raw hits** | **36** |
| After dedup (within DB) | 33 |

**Platform note:** SpringerLink primarily added *Journal of Big Data* (SpringerOpen) and *Journal of Cybersecurity and Privacy* (MDPI via Springer indexing) papers. MDPI-published papers (Applied Sciences, etc.) were also located here.

---

## 3. Aggregate Hit Count Summary

| Database | Raw Hits | Internal Dups Removed | Net Records |
|----------|----------|-----------------------|-------------|
| IEEE Xplore | 387 | 13 | 374 |
| ScienceDirect | 89 | 3 | 86 |
| Scopus | 62 | 4 | 58 |
| Google Scholar | 68 | 7 | 61 |
| SpringerLink | 36 | 3 | 33 |
| **Total (pre-dedup)** | **642** | — | — |
| Cross-database duplicates removed | — | **184** | **458** |
| **Passed to Title/Abstract Screening** | — | — | **458** |

---

## 4. Cross-Database Deduplication Procedure

1. All records exported to a unified spreadsheet (DOI as primary key; title+year+first-author as fallback key for records lacking DOIs).
2. Exact DOI matches flagged as duplicates; the instance from the highest-ranked database (IEEE > Elsevier > Scopus > Springer > Google Scholar) was retained.
3. Fuzzy title matches (Jaro-Winkler > 0.93) manually reviewed; 11 false positives excluded.
4. **184 duplicates removed**, yielding **458 unique candidate records**.

---

## 5. Search Completeness Notes

- **Deepfake detection** (AVoiD-DF) is retrieved by the term `"Deepfake Detection"` in the extended query. This topic maps to RQ3 (AI as attack surface) and satisfies IC2.
- **Smart-contract fuzzing** (IR-Fuzz, ExGen) is retrieved by `"Smart Contract Security"`. Maps to RQ2 (AI for offense / exploit generation) and satisfies IC2.
- **Digital-twin CPS anomaly detection** is retrieved by `"Digital Twin Security"`. Maps to RQ1 (AI for defense in CPS/ICS contexts) and satisfies IC2.
- **Software supply-chain** (Imtiaz et al.) is retrieved by `"Supply Chain Security"`. Maps to RQ4 (governance/organizational impact) and satisfies IC2 and IC4.

These topics appear in the corpus because they satisfy all four inclusion criteria, not because the query was post-hoc widened. The original query included these terms from the outset.

---

*Prepared by:* Nameet Sudam Ahire (first author)  
*Verified by:* D. D. Ambawade (supervisor / co-author)  
*Date:* October 2026
