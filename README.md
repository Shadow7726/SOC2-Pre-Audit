# SOC 2 Trust Services Criteria — Complete Reference

> A single-source study and pre-audit reference covering the full SOC 2 framework: every Trust Services Criterion across all five categories, plus dedicated **Type 1** and **Type 2** guides.

**Framework basis:** AICPA *TSP Section 100 — Trust Services Criteria* (2017, with 2022 revised points of focus), derived from the COSO *Internal Control–Integrated Framework* (2013). SOC 2 examinations are performed under the AICPA attestation standards (AT-C 205).

> [!NOTE]
> Criterion names, COSO mappings, and the category structure in this document were verified against the primary AICPA TSP Section 100 source text. The external links referenced by practitioners interpret these criteria; for any formal audit record, cite the AICPA criteria themselves.

> [!WARNING]
> This is an internal study and pre-audit preparation aid. It does **not** constitute an audit opinion, certification, or legal advice. Only a licensed CPA firm can perform a SOC 2 examination and issue a report.

---

## Table of Contents

- [1. How SOC 2 is Structured](#1-how-soc-2-is-structured)
  - [The five Trust Services Categories](#the-five-trust-services-categories)
  - [Type 1 vs Type 2](#type-1-vs-type-2)
- [2. Complete Trust Services Criteria](#2-complete-trust-services-criteria)
  - [Security — Common Criteria (CC1–CC9)](#security--common-criteria-cc1cc9)
  - [Availability (A1)](#availability-a1)
  - [Confidentiality (C1)](#confidentiality-c1)
  - [Processing Integrity (PI1)](#processing-integrity-pi1)
  - [Privacy (P1–P8)](#privacy-p1p8)
- [3. SOC 2 Type 1 — Point-in-Time](#3-soc-2-type-1--point-in-time)
- [4. SOC 2 Type 2 — Observation Period](#4-soc-2-type-2--observation-period)
- [5. Building an Evidence Package](#5-building-an-evidence-package)
- [6. Where Audits Most Often Fail](#6-where-audits-most-often-fail)
- [Sources](#sources)

---

## 1. How SOC 2 is Structured

SOC 2 defines **criteria** you must meet; **you design the controls** that satisfy them and produce the evidence an auditor tests. SOC 2 does not prescribe specific algorithms, key lengths, or password rules — controls must be **risk-based, documented, implemented, and (for Type 2) shown to operate across the whole observation period.**

### The five Trust Services Categories

| Category | Criteria | Focus — the question the auditor is answering |
|---|---|---|
| **Security** *(mandatory)* | CC1–CC9 (33) | Is information and are systems protected against unauthorized access, disclosure, and damage? The Common Criteria — required in every SOC 2 report. |
| **Availability** | A1.1–A1.3 | Are systems available for operation and use as committed in contracts / SLAs (capacity, backup, recovery)? |
| **Confidentiality** | C1.1–C1.2 | Is information designated confidential protected throughout its lifecycle, including secure disposal? |
| **Processing Integrity** | PI1.1–PI1.5 | Is system processing complete, valid, accurate, timely, and authorized? |
| **Privacy** | P1–P8 | Is personal information collected, used, retained, disclosed, and disposed of in line with commitments (GDPR / CCPA-aligned)? |

**Criterion counts:** 33 Common (CC1–CC9) + Availability (3) + Confidentiality (2) + Processing Integrity (5) + Privacy (8 series) = **51**.

> [!NOTE]
> The Privacy figure counts each P-series as one. At the individual sub-criterion level (P1.1, P3.1–3.2, P4.1–4.3, P5.1–5.2, P6.1–6.7, etc.) the granular Privacy count is ~18, bringing the full criterion total to roughly **61**.

### Type 1 vs Type 2

| Dimension | Type 1 | Type 2 |
|---|---|---|
| **Question answered** | Are controls suitably **designed & implemented** as of a date? | Did controls **operate effectively** across a period? |
| **Time coverage** | Point-in-time ("as of [date]") | Observation period (commonly 3–12 months) |
| **What's tested** | Design suitability + implementation | Design + operating effectiveness over time |
| **Evidence needed** | Current-state snapshot per control | Recurring evidence spanning the whole period |
| **Auditor methods** | Inquiry, observation, inspection, walkthroughs | All of Type 1 **plus** sampling & reperformance |
| **Report Section IV** | Lists controls tested — no test results | Controls **plus** auditor tests, results, exceptions |
| **Typical timeline** | ~3–6 months | ~6–15 months (includes the observation period) |
| **Best when** | Controls newly implemented; prove design quickly | Buyers require sustained assurance; renewals |

> **Type 1 → Type 2.** A Type 1 proves the design is sound on day one; a Type 2 then proves those same controls *operated* across the following months. Many teams issue a Type 1 just before the Type 2 observation period begins.

---

## 2. Complete Trust Services Criteria

### Security — Common Criteria (CC1–CC9)

Mandatory in every SOC 2 report. CC1–CC5 map to the 17 COSO principles; CC6–CC9 add technology-specific criteria.

#### CC1 — Control Environment

*The governance foundation: integrity, board oversight, structure, competence, and accountability. Maps to COSO Principles 1–5.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| CC1.1 | Integrity & ethical values | Demonstrate commitment to integrity and ethics; set tone at the top; address deviations promptly. | Code of conduct; ethics policy; signed acknowledgements; disciplinary process. |
| CC1.2 | Board oversight | Board / governing body operates independently and oversees internal control. | Board charter; meeting minutes; independence documentation. |
| CC1.3 | Structure & authority | Management establishes structures, reporting lines, authorities, and responsibilities. | Org chart; roles & responsibilities; RACI; job descriptions. |
| CC1.4 | Commitment to competence | Attract, develop, and retain competent individuals; provide security training; plan succession. | Training policy & curriculum; per-person completion records; hiring criteria. |
| CC1.5 | Accountability | Hold individuals accountable for internal-control responsibilities, with consequences for failures. | Performance reviews; accountability in job descriptions; policy acknowledgements. |

#### CC2 — Communication & Information

*How quality information is generated and communicated. Maps to COSO Principles 13–15.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| CC2.1 | Quality information | Obtain / generate and use relevant, quality information to support control operation. *(System-boundary communication points of focus sit under CC2.2 / CC2.3; the diagram artifact is primarily governed by the Description Criteria.)* | System description; network / data-flow diagrams; asset inventory. |
| CC2.2 | Internal communication | Communicate objectives and control responsibilities internally, including security policies and how to report issues. | Published policies; training; intranet; internal reporting / whistleblower channel. |
| CC2.3 | External communication | Communicate with external parties (customers, vendors) about objectives and responsibilities, including a channel to report concerns. | Customer security / trust page; contact & escalation process; ToS / DPA. |

#### CC3 — Risk Assessment

*Setting objectives and identifying, analyzing, and responding to risk. Maps to COSO Principles 6–9.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| CC3.1 | Specify objectives | Specify objectives clearly enough to enable identification and assessment of risks. | Documented business / security objectives; risk-assessment scope. |
| CC3.2 | Identify & analyze risk | Identify risks to objectives across the entity and analyze how they should be managed. | Risk assessment; risk register with likelihood / impact scoring; treatment plans. |
| CC3.3 | Fraud risk | Consider the potential for fraud in assessing risks. | Fraud-risk review; documented fraud scenarios in the risk register. |
| CC3.4 | Changes affecting controls | Identify and assess changes that could significantly impact the system of internal control. | Change-triggered risk reviews; re-assessment on major system / org changes. |

#### CC4 — Monitoring Activities

*Ongoing and separate evaluations. Maps to COSO Principles 16–17.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| CC4.1 | Ongoing / separate evaluations | Perform ongoing and/or separate evaluations to ascertain whether controls are present and functioning. | Internal audits; control self-assessments; vulnerability scans; penetration tests. |
| CC4.2 | Evaluate & communicate deficiencies | Evaluate and communicate control deficiencies timely to those responsible for corrective action. | Findings tracker; remediation tickets with owners & dates; management reporting. |

#### CC5 — Control Activities

*Selecting and deploying control activities through policy. Maps to COSO Principles 10–12.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| CC5.1 | Select control activities | Select and develop control activities (preventive / detective, manual / automated) that mitigate risks. | Control matrix mapping risks to controls; policy set. |
| CC5.2 | Technology general controls | Select and develop general control activities over technology. | Access, change, and operations control documentation; IT general controls. |
| CC5.3 | Deploy via policy | Deploy control activities through policies and procedures that put them into action. | Approved policies & procedures; review / version history; acknowledgements. |

#### CC6 — Logical & Physical Access Controls

*The largest CC series — where most audit hours land.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| CC6.1 | Logical access security | Implement logical access software, infrastructure, and architectures over protected assets; includes authentication, segmentation, **encryption, and key management**. | Access-control policy; SSO/IdP config; MFA; encryption config; firewall rules; asset inventory. |
| CC6.2 | User registration & deprovisioning | Register and authorize new users before granting access; remove access when no longer authorized; review access periodically. | Onboarding / offboarding tickets; dated access reviews with approvers. |
| CC6.3 | Role-based access | Authorize, modify, or remove access based on roles, responsibilities, and least privilege. | RBAC export; role definitions; access-change approvals. |
| CC6.4 | Physical access | Restrict physical access to facilities and protected information assets. | Badge logs; visitor logs; data-center provider SOC 2; server-room access list. |
| CC6.5 | Secure decommissioning | Discontinue logical & physical protections over assets only after data has been rendered unrecoverable. | Media-sanitization / destruction records; asset-retirement logs; certificates of destruction. |
| CC6.6 | Boundary protection | Implement measures against threats from outside the system boundary; **additional authentication (MFA) for external access**; firewalls / IDS. | MFA-enforcement proof per external system; VPN / zero-trust config; firewall & IDS configs. |
| CC6.7 | Data transmission & movement | Restrict and protect information during transmission, movement, and removal (**encryption in transit**, DLP, removable-media controls). | TLS scan; DLP config & alerts; removable-media policy; transfer logs. |
| CC6.8 | Malicious software | Prevent or detect and act upon unauthorized or malicious software. | EDR / antivirus config; file-integrity monitoring; allowlisting; patch evidence. |

#### CC7 — System Operations

*Vulnerability detection, monitoring, and the full incident lifecycle.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| CC7.1 | Vulnerability detection | Detect config changes introducing vulnerabilities and susceptibilities to newly discovered ones; **conduct vulnerability scans**. | Scan schedule & reports; config baselines (CIS); remediation tracking within SLA. |
| CC7.2 | Security event monitoring | Monitor system components for anomalies and indicators of security events. | SIEM / log monitoring; alerting rules; log-coverage evidence. |
| CC7.3 | Evaluate security events | Evaluate security events to determine whether they constitute incidents. | Triage records; incident-classification criteria; event review logs. |
| CC7.4 | Incident response | Respond to identified incidents through a defined program (contain, remediate, communicate). | Incident-response plan; incident tickets; post-incident reviews; breach-notification process. |
| CC7.5 | Recovery | Identify, develop, and implement activities to recover from identified incidents. | Recovery procedures; root-cause analyses; tabletop-exercise records. |

#### CC8 — Change Management

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| CC8.1 | Change management | Authorize, design, develop / acquire, configure, document, test, approve, and implement changes to infrastructure, data, software, and procedures. *(Segregation of duties and environment separation are accepted implementation controls mapped here, not named sub-criteria.)* | Change-mgmt policy; PRs with reviewer approvals; CI test evidence; release notes; IaC history; env-separation config. |

#### CC9 — Risk Mitigation

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| CC9.1 | Business disruption mitigation | Identify, select, and develop risk-mitigation activities for disruptions (BC/DR, insurance). | BC/DR plan; insurance (cyber / E&O); tabletop-exercise records. |
| CC9.2 | Vendor & partner risk | Assess and manage risks associated with vendors and business partners. | Vendor inventory; security reviews / SOC 2s of critical vendors; DPAs; periodic re-assessment. |

### Availability (A1)

*Optional category — ensures systems are available for operation and use as committed.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| A1.1 | Capacity management | Maintain, monitor, and evaluate current processing capacity and use of resources. | Capacity / performance dashboards; autoscaling config; forecasting. |
| A1.2 | Environmental & backup protections | Provide environmental protections, backups, and recovery infrastructure. | Backup policy & logs; offsite / geo-redundant storage; redundancy / failover config. |
| A1.3 | Recovery testing | Test recovery-plan procedures supporting system recovery (RTO / RPO). | Dated restore-test results; DR tabletop / failover drill records; RTO/RPO definitions. |

### Confidentiality (C1)

*Optional category — protects information designated confidential throughout its lifecycle.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| C1.1 | Identify & protect | Identify and maintain confidential information (classification, access restriction, encryption). | Data-classification policy; encryption at rest / in transit; access restrictions; NDAs. |
| C1.2 | Disposal | Dispose of confidential information when no longer needed (retention limits + secure disposal). | Retention schedule; deletion / disposal logs; sub-processor deletion attestations. |

### Processing Integrity (PI1)

*Optional category — ensures processing is complete, valid, accurate, timely, and authorized.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| PI1.1 | Processing definitions | Use information about processing objectives and specifications. | Data-processing specs; data-quality definitions; product / API documentation. |
| PI1.2 | Input controls | Inputs are complete, accurate, and timely. | Input validation rules; error handling; rejected-record logs. |
| PI1.3 | Processing controls | Processing is complete, valid, accurate, timely, and authorized. | Processing logs; job-completion monitoring; authorization checks. |
| PI1.4 | Output controls | Outputs are complete, accurate, timely, and delivered to authorized parties. | Output reconciliation reports; delivery / distribution logs. |
| PI1.5 | Storage controls | Store inputs and outputs completely, accurately, and timely. | Storage integrity checks; checksums / hashing; backup-integrity evidence. |

### Privacy (P1–P8)

*Optional category — governs the full lifecycle of personal information; aligns closely with GDPR and CCPA.*

| ID | Criterion | What it requires | Typical evidence |
|---|---|---|---|
| P1 | Notice | Provide notice about privacy practices — how PII is collected, used, retained, and disclosed. | Privacy notice with version control; publication records. |
| P2 | Choice & consent | Give individuals choice regarding collection, use, and disclosure, and obtain consent. | Consent-capture mechanism; consent logs; preference center. |
| P3 | Collection | Collect PII only for identified purposes, limited to what is necessary. | Data-collection inventory; data-minimization records; lawful-basis mapping. |
| P4 | Use, retention & disposal | Limit use to stated purposes; retain only as long as needed; dispose securely. | Retention schedule; deletion logs; purpose-limitation controls. |
| P5 | Access | Enable individuals to access, review, and correct their PII (data-subject requests). | DSAR workflow with SLA tracking; access / correction request logs. |
| P6 | Disclosure & notification | Disclose PII to third parties only for identified purposes and with consent; notify of unauthorized disclosure. | Third-party / sub-processor register; DPAs; breach-notification procedure. |
| P7 | Quality | Maintain accurate, complete, and relevant PII for its intended use. | Data-accuracy / correction processes; quality-check records. |
| P8 | Monitoring & enforcement | Monitor compliance with privacy policies and address inquiries, complaints, and disputes. | Privacy-complaint log; compliance monitoring; enforcement / remediation records. |

---

## 3. SOC 2 Type 1 — Point-in-Time

A Type 1 report evaluates the **suitability of design and implementation** of controls **as of a single specified date**. It answers: *"Are the right controls in place and properly designed today?"* It does **not** test operating effectiveness over a period.

> [!IMPORTANT]
> Because Type 1 is a snapshot, **point-in-time evidence is sufficient** — a current policy, a configuration screenshot, today's access list. You do **not** need to prove a control fired repeatedly across months.

### What the auditor tests (design & implementation)

| Method | What the auditor does | Example |
|---|---|---|
| Inquiry | Asks personnel to explain how a control is designed and who operates it. | Interview the IAM lead on access provisioning. |
| Observation | Witnesses a control in action or a configuration in its current state. | Watch an MFA challenge on the production console. |
| Inspection | Reviews documents, policies, and artifacts as they exist on the date. | Inspect the encryption policy and a current TLS scan. |
| Walkthrough | Traces a control end-to-end once to confirm it is designed and in place. | Walk a single change from PR → review → approval → deploy. |

> [!WARNING]
> **"Implemented," not just "documented."** A written policy alone is not enough. The auditor confirms the control actually exists and is in place on the report date (e.g. MFA genuinely enforced, encryption genuinely on). A control that is documented but not yet operating is a **design/implementation gap**.

### The report (four sections)

| § | Section | Type 1 contents |
|---|---|---|
| I | Independent auditor's opinion | Opinion that, as of the date, the description is fairly presented and controls are suitably designed & implemented. Opinion may be *unqualified, qualified, adverse,* or a *disclaimer*. |
| II | Management's assertion | Management's assertion that the description is accurate and controls suitably designed as of the date. |
| III | System description | Scope, boundaries, infrastructure, software, people, data, policies. |
| IV | Applicable criteria & controls | The in-scope criteria and mapped controls — **list of controls only**, no test procedures/results. |

### Type 1 roadmap (~3–6 months)

1. **Readiness & prep (1–3 months)** — define scope & the "as of" date, implement controls, write policies, assign owners, run a gap self-assessment, select a CPA firm.
2. **Fieldwork (2–5 weeks)** — auditor reviews control design, runs walkthroughs, inspects current-state evidence.
3. **Report (2–6 weeks)** — auditor drafts and issues the report.

### Design-suitability self-check (per control)

1. **Exists** — Is there a defined control addressing the risk (not just an intention)?
2. **Documented** — Is it written into a policy / procedure with an owner?
3. **Implemented** — Is it actually in place and operating on the "as of" date (config proves it, not just the policy)?
4. **Mapped** — Does it clearly satisfy one or more in-scope Trust Services Criteria?

### Common Type 1 pitfalls

- **Documented but not implemented** — a policy exists but the control isn't live on the date (MFA in advisory mode, encryption not switched on).
- **System description doesn't match reality** — the diagram/boundary differs from the live environment the auditor walks through.
- **Orphan controls** — a control that doesn't map to an in-scope criterion, or an in-scope criterion with no control.
- **Scope drift** — including optional categories whose criteria don't apply, forcing "not applicable" entries and extra cost.
- **Stale snapshot** — evidence captured too far from the "as of" date.

---

## 4. SOC 2 Type 2 — Observation Period

A Type 2 report evaluates both the **suitability of design** and the **operating effectiveness** of controls **across an observation period** (commonly 3–12 months). It answers: *"Did the controls operate effectively, every time they were supposed to, throughout the window?"*

> [!IMPORTANT]
> A single point-in-time snapshot is **not** enough. The auditor samples evidence drawn from **across the whole period** to confirm each control operated **consistently** — not just at the start or end.

### The observation period

| Decision | Guidance |
|---|---|
| **How long** | Typically 3–12 months. A first Type 2 is often **3–6 months**; renewals move to a **rolling 12-month** window for continuous coverage. |
| **When to start the clock** | Only **after** controls are genuinely live and producing evidence. Starting early means the auditor samples from a window when controls were not operating consistently. |
| **Choosing the window** | Avoid ending during holidays, fiscal year-end, or peak cycles. Leave 1–2 weeks between period end and audit kickoff. |
| **Report validity** | The clock starts aging the day the window **closes**. Plan the renewal before the first report is delivered. |

### How the auditor tests operating effectiveness

On top of the Type 1 methods (inquiry, observation, inspection), a Type 2 adds **reperformance** and **sampling** across the period.

**Sampling.** Auditors do not test every transaction; they select a representative sample from across the period. Sample size depends on the control's **frequency** and **risk** and is the auditor's judgment. Illustratively:

- A control running **monthly** across a 6-month window → typically **2–4 months** sampled.
- A **daily** control → a handful of days.
- A **quarterly** access review across 12 months → the auditor expects to see **all four** reviews, with dates, reviewers, and outcomes.

**Exceptions & opinion.**

| Concept | Meaning |
|---|---|
| Exception / deviation | Recorded when a control did not operate effectively for some portion of the period. |
| Impact on opinion | A **small** number of isolated exceptions may not cause a qualified opinion; **significant or pervasive** exceptions can. |
| Opinion types | **Unqualified** (clean), **Qualified**, **Adverse**, or **Disclaimer**. |

### The report (four sections)

Same four sections as Type 1, but **Section IV** adds the auditor's **test procedures, results, and any exceptions** for every control — the section that differs most from a Type 1.

### Type 2 roadmap (~6–15 months)

1. **Readiness (1–3 months)** — scope, implement controls, write policies, assign owners, close gaps. Optionally issue a Type 1.
2. **Observation period (3–12 months)** — controls run; recurring evidence is collected continuously.
3. **Fieldwork (3–6 weeks)** — auditor samples evidence across the period, reperforms, evaluates effectiveness.
4. **Report (2–6 weeks)** — auditor issues the report with opinion, tests, results, and exceptions.

> [!TIP]
> **The cadence rule:** every recurring control needs an **owner**, a **calendar entry**, and a **default evidence destination** (a folder, ticket queue, or tagged channel). If the artifact does not land somewhere consistent as it is produced, the last month of the window becomes a scramble to reconstruct it.

### Recurring evidence — by Trust Services Criteria

Each item must be produced **repeatedly across the period** and is what the auditor samples.

| Criteria series | Typical cadence | Recurring evidence the auditor samples |
|---|---|---|
| CC1 — Control Environment | Annual / per-hire | Training completions for staff onboarded / refreshed in the period; policy acknowledgements for new hires. |
| CC2 — Communication & Info | Ongoing | Evidence policies were communicated; system description kept current; reports issued in the period. |
| CC3 — Risk Assessment | Annual / on change | Risk assessment(s) performed and dated within the period; register updates on significant changes. |
| CC4 — Monitoring | Periodic | Internal reviews; each vulnerability scan / pen test in the period; deficiency-tracker updates. |
| CC5 — Control Activities | Ongoing / annual | Evidence control activities operated; policy reviews / re-approvals dated in the period. |
| CC6 — Logical & Physical Access | Per-event / quarterly | Provisioning & **deprovisioning tickets** per joiner/leaver (auditor samples terminations for timely removal); every **periodic access review** with dates & reviewers; MFA enforced throughout; physical-access logs. |
| CC7 — System Operations | Continuous / per-event | Monitoring & alerting active throughout; scan reports each cycle; incident tickets; incident-response exercise. |
| CC8 — Change Management | Per-change | Full population of production changes; auditor samples changes for approval, testing, and review. |
| CC9 — Risk Mitigation | Annual / periodic | BC/DR test in the period; vendor reviews / re-assessments dated in the period; current insurance. |
| A1 — Availability *(if in scope)* | Continuous / per-run | Capacity monitoring throughout; backup success logs sampled across the period; restore / DR test record. |
| C1 — Confidentiality *(if in scope)* | Per-event | Secure-disposal / deletion records for the period; sample of retention-driven disposals. |
| PI1 — Processing Integrity *(if in scope)* | Continuous / per-run | Input / processing / output / storage controls operating; reconciliations (auditor samples transactions). |
| P1–P8 — Privacy *(if in scope)* | Per-event / ongoing | Consent records; DSARs handled in the period with SLA tracking; complaint / disclosure logs. |

### Bridge letters & renewal

- **Bridge (gap) letter** — a short, **management-signed** statement (typically CEO / CTO / CISO) affirming **no material changes** to the control environment between the report's period-end and the next report. Covers the interim gap, usually accepted for **3–6 months**. It is **not audited**, and the audit firm will **not** issue it — their responsibility ends when the period closes. Not a substitute for a current Type 2.
- **Renewal cadence** — most organizations move to a **rolling 12-month** window after the first report so a current report is always available. Plan the renewal **before** the first report is delivered.

### Common Type 2 pitfalls

- **Starting the period too early** — opening the window before controls are consistently live guarantees the auditor samples a gap.
- **Controls implemented mid-period** — evidence won't exist before a control went live; the auditor records a deviation.
- **Reconstructed evidence** — artifacts assembled at the last minute rather than captured as produced.
- **High-frequency exception areas** — quarterly access reviews (all must be present), timely deprovisioning, change approvals, and untested DR / incident-response exercises.
- **Letting the report age out** — the window closes with no renewal planned, leaving a coverage gap.

---

## 5. Building an Evidence Package

For each control, assemble a package in this shape — it mirrors how an auditor tests: confirm a documented control exists, verify implementation, inspect objective evidence that it operated during the period, and evaluate any exceptions.

| Package item | What to include |
|---|---|
| Control name | The control being tested. |
| Criteria mapping | The TSC criterion / criteria it satisfies (e.g. CC6.1, CC6.3, CC8.1). |
| Policy | The governing policy document(s). |
| Technical verification | The concrete configuration state proving the control is live. |
| Evidence | Dated, objective artifacts — reports, screenshots, logs, exports, tickets. |
| Control owner | The accountable role. |
| Evidence date | Capture date — must fall within the observation period for Type 2. |
| Status | Pass / Gap. |
| Findings & remediation | Any exception, plus owner and due date to close it. |

---

## 6. Where Audits Most Often Fail

- **Logical access (CC6)** and **change management (CC8)** are the most heavily tested and the most common sources of qualified opinions.
- **Undated access reviews (CC6.2 / CC6.3)** — reviews happen informally with no artifact showing who was reviewed, who approved, and what changed.
- **Advisory-mode MFA (CC6.6)** — if a user can skip or disable MFA, the control is treated as not in place.
- **Untested DR (A1.3)** — a backup policy with no documented restore test is the single most common Availability gap.
- **Unapproved / retro-approved changes (CC8.1)** — any change reaching production outside the review workflow is a hard-to-explain exception.
- **Incomplete training records (CC1.4)** — no per-employee completion evidence for the full period, or contractors / late-period hires excluded.
- **Vulnerability closure (CC7.1)** — teams fix issues but can't prove closure with a dated re-scan tied to the original finding.
- **Processing Integrity (PI1.4)** — missing end-to-end reconciliation proving output matches input.
- **Confidentiality disposal (C1.2)** — unverified de-identification / deletion claims.

---

## Sources

- **Authoritative:** AICPA *TSP Section 100 — Trust Services Criteria for Security, Availability, Processing Integrity, Confidentiality, and Privacy* (2017, with 2022 revised points of focus), derived from the COSO *Internal Control–Integrated Framework* (2013).
- **Examination standard:** AICPA attestation standards (AT-C 205).
- Criterion names, COSO mappings, and category structure in this document were verified against the primary AICPA TSP Section 100 source text. Practitioner and audit-firm guidance was used to describe typical evidence and audit practice.

---

<sub>This document is an internal study and pre-audit preparation aid. It does not constitute an audit opinion, certification, or legal advice. Only a licensed CPA firm can perform a SOC 2 examination and issue a report. Last updated: 2026-07-30.</sub>
