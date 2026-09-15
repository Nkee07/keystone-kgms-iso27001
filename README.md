# Keystone Grants Management System (KGMS): ISO/IEC 27001:2022 Information Security Management System
### The same simulated system, assessed against the international standard

> ### PORTFOLIO EXERCISE, SIMULATED SYSTEM
> **Keystone Grants Management System (KGMS) does not exist.** The Federal Workforce Development Agency (FWDA) is a fictional federal
> agency invented for this portfolio. Every organisation, person, system
> identifier, network address, finding, date and signature on this page is
> fabricated for training purposes, with one exception: the author, Nkeiru Sarah Adesida, is a real person. Where her name appears in a scenario role, that role is fictional, and she has never worked for this agency, which does not exist. Nothing here is drawn from any real
> employer, client or government system, and no real document, artifact or
> data has been reproduced. This file is coursework, not a government record.

![Standard](https://img.shields.io/badge/Standard-ISO%2FIEC%2027001%3A2022-C8102E?style=flat-square)
![Risk](https://img.shields.io/badge/Risk-ISO%2FIEC%2027005-C8102E?style=flat-square)
![Annex A](https://img.shields.io/badge/Annex%20A-93%20of%2093%20controls-0F766E?style=flat-square)
![Simulated](https://img.shields.io/badge/Simulated-Fictional%20System-6B7280?style=flat-square)
![Author](https://img.shields.io/badge/Author-Nkeiru%20Sarah%20Adesida-00C853?style=flat-square)

---

## What this repository is

The same fictional system that appears in the
[FedRAMP and NIST RMF repository](https://github.com/Nkee07/keystone-kgms-fedramp-rmf), documented
again from scratch under ISO/IEC 27001:2022 and ISO/IEC 27005.

Plain language version: the American federal government has its own rulebook for
proving a computer system is safe. Most of the rest of the world uses a different
rulebook, published by the International Organization for Standardization (ISO). The
two rulebooks want most of the same things, but they organise them differently and
they argue about different points. Doing the same system twice, once under each,
shows which parts are the framework and which parts are the actual security.

Why that is worth doing rather than picking three unrelated projects: an employer is
not buying knowledge of one framework, they are buying the ability to pick up a
framework. Two frameworks on one system demonstrates that. Three frameworks on three
systems demonstrates three tutorials.

---

## The two standards, in one sentence each

- **ISO/IEC 27001:2022** is the certifiable standard. Clauses 4 to 10 describe the
  management system: context, leadership, planning, support, operation, performance
  evaluation and improvement. Annex A lists 93 controls in 4 themes.
- **ISO/IEC 27005** is the guidance for how to do the risk management that Clause 6
  requires. It is not certifiable on its own.

A frequent error is describing the 2022 edition with the 2013 numbers. The 2013
edition had 114 controls in 14 domains. The 2022 edition reorganised them into **93
controls in 4 themes**: Organizational 37, People 8, Physical 14, Technological 34,
and introduced 11 controls that did not previously exist, including threat
intelligence, information security for use of cloud services, data masking, data
leakage prevention, monitoring activities, web filtering and secure coding.

---

## Contents

| Module | Document | Clause or standard | Date |
|---|---|---|---|
| [ISO-01](iso-01-isms-scope/README.md) | ISMS Scope, Context and Leadership | Clauses 4, 5, 6, 7 | 20 February 2026 |
| [ISO-02](iso-02-soa/README.md) | Statement of Applicability, all 93 Annex A controls | Clause 6.1.3, Annex A | 13 March 2026 |
| [ISO-03](iso-03-risk-register/README.md) | Information Security Risk Register, 12 risks | Clause 6.1.2, ISO/IEC 27005 | 12 August 2026 |
| [ISO-04](iso-04-risk-treatment/README.md) | Risk Treatment Plan | Clause 6.1.3, ISO/IEC 27005 | 17 April 2026 |
| [ISO-05](iso-05-audit-management-review/README.md) | Internal Audit and Management Review | Clauses 9, 10 | 9 July 2026 |
| [ISO-06](iso-06-crosswalk/README.md) | NIST to ISO Framework Crosswalk | Both | 28 August 2026 |

### Machine readable artifacts

| File | What it is |
|---|---|
| [artifacts/kgms-statement-of-applicability.csv](artifacts/kgms-statement-of-applicability.csv) | All 93 controls as a spreadsheet, which is how an SoA is actually maintained |
| [artifacts/kgms-risk-register.csv](artifacts/kgms-risk-register.csv) | The 12 risk register with inherent and residual scoring |

---

## Statement of Applicability at a glance

| Theme | Controls in theme | Applicable | Excluded |
|---|---|---|---|
| 5. Organizational controls | 37 | 37 | 0 |
| 6. People controls | 8 | 8 | 0 |
| 7. Physical controls | 14 | 11 | 3 |
| 8. Technological controls | 34 | 33 | 1 |
| **Total** | **93** | **89** | **4** |

Implementation status is tracked in a **separate column** from applicability, because
they answer different questions. "Does this control apply to us" is Yes or No.
"Have we finished implementing it" is a different axis, and collapsing the two is why
Statement of Applicability summaries so often fail to add up.

| Implementation status | Count |
|---|---|
| Implemented | 72 |
| Implemented by supplier | 9 |
| Partially implemented | 8 |
| Not applicable | 4 |
| **Total** | **93** |

Every number on this page is computed from the 93 control rows in ISO-02.
None of them is typed.

---

## The simulated system

| Field | Detail |
|---|---|
| System | Keystone Grants Management System (KGMS) |
| Identifier | `FWDA-KGMS-2026-MOD` |
| Operator | Federal Workforce Development Agency (FWDA), fictional |
| Hosting | AWS GovCloud (US-East), provided by Keystone Digital Services LLC, fictional |
| ISMS scope | The KGMS service and the agency functions that support it |
| Users | ~8,400 external grant applicants and grantee staff, 420 agency users, 65 contracted peer reviewers, 9 regional offices |
| Federal parallel | Authorised to operate under a FedRAMP Moderate agency ATO, 15 May 2026 |

---

## Related repositories

| Repository | What it covers |
|---|---|
| [keystone-kgms-fedramp-rmf](https://github.com/Nkee07/keystone-kgms-fedramp-rmf) | The federal authorisation of the same system: RMF Steps 0 to 6, 16 assessment findings, 10 POA&M items |
| [keystone-kgms-conmon-vulnmgmt](https://github.com/Nkee07/keystone-kgms-conmon-vulnmgmt) | Continuous monitoring, vulnerability management and control assessment in Tenable Nessus, ServiceNow and RSA Archer |

---

## About the author

**Nkeiru Sarah Adesida**
Cybersecurity Governance, Risk and Compliance analyst. Certified Information Systems
Auditor (CISA), CompTIA Security+, and a Master of Science in Cybersecurity Management
and Policy from University of Maryland Global Campus.

[GitHub](https://github.com/Nkee07) | [LinkedIn](https://www.linkedin.com/in/nkeiru-adesida-grc) | [nkiru_sarah@yahoo.com](mailto:nkiru_sarah@yahoo.com)

---

*Author: Nkeiru Sarah Adesida, Information System Security Officer (ISSO), portfolio scenario*  
*Simulated system: Keystone Grants Management System (KGMS) | FWDA-KGMS-2026-MOD*  
*This document is a portfolio exercise built on a fictional organisation. It is not a government record.*  
*[GitHub portfolio](https://github.com/Nkee07) | [LinkedIn](https://www.linkedin.com/in/nkeiru-adesida-grc)*
