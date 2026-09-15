# ISO-06: NIST to ISO Framework Crosswalk
### Keystone Grants Management System (KGMS) | Family level mapping, and where the two frameworks genuinely diverge

> ### PORTFOLIO EXERCISE, SIMULATED SYSTEM
> **Keystone Grants Management System (KGMS) does not exist.** The Federal Workforce Development Agency (FWDA) is a fictional federal
> agency invented for this portfolio. Every organisation, person, system
> identifier, network address, finding, date and signature on this page is
> fabricated for training purposes, with one exception: the author, Nkeiru Sarah Adesida, is a real person. Where her name appears in a scenario role, that role is fictional, and she has never worked for this agency, which does not exist. Nothing here is drawn from any real
> employer, client or government system, and no real document, artifact or
> data has been reproduced. This file is coursework, not a government record.

---

**Document:** NIST SP 800-53 Rev 5 and FedRAMP to ISO/IEC 27001:2022 Crosswalk  
**Simulated system:** Keystone Grants Management System (KGMS) | `FWDA-KGMS-2026-MOD`  
**Framework and standards:** NIST SP 800-53 Rev 5, NIST SP 800-37 Rev 2, ISO/IEC 27001:2022  
**Author:** Nkeiru Sarah Adesida  
**Document date:** 28 August 2026  
**Status:** Complete. Representative family level crosswalk, not control by control

**Navigation:** [<- ISO-05: Internal Audit and Management Review](../iso-05-audit-management-review/README.md) &nbsp;|&nbsp; [Repository home](../README.md)

---

## Purpose

This document maps the federal framework used in the
[FedRAMP and NIST RMF repository](https://github.com/Nkee07/keystone-kgms-fedramp-rmf) to the
international framework used here, for the same system.

Plain language version: two rulebooks, one building. This is the translation table, plus
an honest account of where translation stops working.

**Scope statement, stated up front.** This is a **representative crosswalk at control
family level**. It maps 19 NIST SP 800-53 Rev 5 control families to Annex A controls. It
is **not** a control by control mapping of roughly a thousand individual NIST controls
and enhancements to 93 Annex A controls, and a reader should not treat it as one.
Overclaiming completeness on a crosswalk is easy and it is the first thing a reviewer
tests, usually by picking one control and asking where it went.

---

## Section 1: NIST control families to Annex A

| Family | Name | NIST controls | Annex A controls | Alignment |
|---|---|---|---|---|
| AC | Access Control | AC-1 to AC-25 | 5.15, 5.16, 5.17, 5.18, 8.2, 8.3, 8.5, 8.18 | Strong alignment. Both require role based access, strong authentication and periodic review |
| AT | Awareness and Training | AT-1 to AT-6 | 6.3 | Aligned. ISO places training in the People theme; NIST gives it a family of its own |
| AU | Audit and Accountability | AU-1 to AU-16 | 8.15, 8.16, 8.17, 5.28, 5.33 | Aligned. NIST is markedly more prescriptive on record content and retention |
| CA | Assessment, Authorization and Monitoring | CA-1 to CA-9 | 5.35, 5.36, 8.29, 9.2 and 9.3 clauses | Partial. NIST CA contains authorisation, which ISO has no direct equivalent for. This is the largest structural difference between the two |
| CM | Configuration Management | CM-1 to CM-14 | 8.9, 8.19, 8.32, 5.9 | Aligned |
| CP | Contingency Planning | CP-1 to CP-13 | 5.29, 5.30, 8.13, 8.14 | Aligned. ISO 27001 defers much of this to ISO 22301 for business continuity |
| IA | Identification and Authentication | IA-1 to IA-12 | 5.16, 5.17, 8.5 | Strong alignment |
| IR | Incident Response | IR-1 to IR-10 | 5.24, 5.25, 5.26, 5.27, 6.8 | Strong alignment. ISO 5.27, learning from incidents, maps to the NIST lessons learned requirement |
| MA | Maintenance | MA-1 to MA-7 | 7.13, 8.18 | Aligned. Mostly inherited from the provider in a cloud deployment |
| MP | Media Protection | MP-1 to MP-8 | 7.10, 7.14, 8.10, 8.12 | Aligned. 7.10 is excluded in this scope, so the NIST side is satisfied by the provider |
| PE | Physical and Environmental Protection | PE-1 to PE-23 | 7.1 to 7.5, 7.8, 7.11 | Aligned. Both largely inherited in a cloud deployment |
| PL | Planning | PL-1 to PL-11 | 5.1, 5.8, Clauses 4, 5, 6 | Partial. Much of NIST PL maps to ISO clauses rather than to Annex A controls |
| PS | Personnel Security | PS-1 to PS-9 | 6.1, 6.2, 6.4, 6.5, 6.6 | Strong alignment |
| PT | PII Processing and Transparency | PT-1 to PT-8 | 5.34 | Partial. ISO 27001 addresses privacy thinly. ISO 27701 is the privacy extension and would be the right companion |
| RA | Risk Assessment | RA-1 to RA-10 | Clause 6.1.2, 8.8, 5.7 | Aligned. ISO puts risk assessment in the clauses, which is architecturally significant: it is a management system requirement, not a control |
| SA | System and Services Acquisition | SA-1 to SA-23 | 8.25, 8.26, 8.27, 8.28, 8.29, 8.30, 8.31 | Aligned |
| SC | System and Communications Protection | SC-1 to SC-51 | 8.20, 8.21, 8.22, 8.23, 8.24, 8.1 | Aligned. NIST is considerably more granular |
| SI | System and Information Integrity | SI-1 to SI-23 | 8.7, 8.8, 8.16, 8.26 | Aligned |
| SR | Supply Chain Risk Management | SR-1 to SR-12 | 5.19, 5.20, 5.21, 5.22 | Strong alignment. Note the family: supply chain is SR in Revision 5. SA-12 was withdrawn |

---

## Section 2: RMF steps to the ISO management system

| RMF step | What it does | ISO equivalent | Notes |
|---|---|---|---|
| Step 0, Prepare | Readiness, roles, risk tolerance | Clauses 4 and 5, plus 6.1 risk criteria | Close alignment. Both start by establishing context and leadership |
| Step 1, Categorise | FIPS 199 impact rating drives the control baseline | Clause 6.1.2 risk assessment, 5.12 classification | **This is the biggest divergence.** NIST derives controls from a categorisation of the information. ISO derives them from a risk assessment. The NIST route is more repeatable across agencies; the ISO route fits the organisation better |
| Step 2, Select | Choose and tailor a baseline | Clause 6.1.3 and the Statement of Applicability | Close functional equivalence. The SoA is the ISO analogue of a tailored baseline, and it is arguably stronger because every exclusion carries a written justification |
| Step 3, Implement | Build and document controls | Clause 8 operation, plus Annex A implementation | Aligned |
| Step 4, Assess | Independent assessment against the plan | Clause 9.2 internal audit, plus certification audit | Aligned in purpose. NIST assessment is deeper on technical control testing; ISO audit is deeper on whether the management system functions |
| Step 5, Authorize | A named official accepts residual risk in writing | **No direct equivalent.** Nearest is Clause 9.3 management review | The most important structural difference and it is treated in Section 3 |
| Step 6, Monitor | Continuous monitoring, ongoing authorisation | Clauses 9.1, 9.3 and 10, plus 8.16 | Aligned in intent. ISO cadence is typically annual surveillance; federal continuous monitoring is monthly |

---

## Section 3: Where the two frameworks genuinely differ

Nine differences that matter in practice, not nine restatements of the same one.

| # | Difference | NIST and FedRAMP | ISO/IEC 27001:2022 |
|---|---|---|---|
| 1 | What drives control selection | Information impact categorisation under FIPS 199 | Risk assessment under Clause 6.1.2 |
| 2 | Who accepts risk | A named Authorizing Official signs a decision memorandum and owns it personally | Top management endorses through management review. No individual signature on a risk acceptance |
| 3 | Formal permission to operate | An Authorization to Operate with a termination date. Without it, the system may not run | No equivalent. Certification attests that a management system conforms, not that a system is permitted to operate |
| 4 | Who audits | A third party assessor or agency assessor, against SP 800-53A procedures | An accredited certification body, against the standard, on a three year cycle with annual surveillance |
| 5 | Prescription | Highly prescriptive. Roughly a thousand controls and enhancements with organisation defined parameters | Principle based. 93 controls, with implementation left to the organisation |
| 6 | Handling of exclusions | Tailoring out a control requires justification and assessor agreement | The Statement of Applicability requires a documented justification for every exclusion, all 93 controls addressed |
| 7 | Monitoring cadence | Monthly continuous monitoring reporting to the AO, with vulnerability service levels | Annual surveillance audit. Internal monitoring frequency set by the organisation |
| 8 | Privacy | A parallel control set, PT family, plus the Privacy Act and privacy impact assessments | Thin. ISO 27701 is the privacy extension and is the right companion standard |
| 9 | Scope definition | The authorization boundary, a technical construct | The ISMS scope, an organisational construct that can include people and processes outside any system boundary |

### The difference worth understanding above the others

Difference 3. Under the federal framework an unauthorised system is not permitted to
operate: the authorisation is permission, and it expires. Under ISO, certification says
that an organisation runs a conforming management system. Neither is stronger in the
abstract. The federal model forces a dated, individual, accountable decision, which is
its real contribution. The ISO model forces the organisation to prove the system keeps
working over time, which is its real contribution.

An organisation with a current ATO and no management system passes an inspection and
then decays. An organisation with a certificate and no authorisation decision has
nobody personally accountable for the residual risk. The pairing is complementary,
which is the practical argument for doing both.

---

## Section 4: Dual use of one evidence set

Where one artifact satisfies both frameworks, it should be produced once. Maintaining
two parallel evidence sets for one system is how compliance programmes become expensive
and then become inconsistent, which is worse than expensive.

| Artifact | Satisfies in NIST and FedRAMP | Satisfies in ISO | Produced once? |
|---|---|---|---|
| System Security Plan | PL-2, and the core of the authorisation package | Clause 7.5 documented information, and much of Annex A evidence | Yes |
| Risk register | RA-3 risk assessment | Clause 6.1.2 | Yes |
| Statement of Applicability | Control tailoring record | Clause 6.1.3 d, mandatory | Yes. The SoA and the tailoring log are the same analysis presented in two shapes |
| Vulnerability scan reports | RA-5, SI-2 | A 8.8 | Yes |
| Access review attestations | AC-2, AC-6 | A 5.18, 8.2 | Yes |
| Incident records | IR-4, IR-5, IR-6 | A 5.24 to 5.27 | Yes |
| Component inventory | CM-8 | A 5.9 | Yes |
| Training completion records | AT-2 | A 6.3 | Yes |
| Continuous monitoring report | CA-7 | Clause 9.1 | Yes |
| Internal audit report | CA-2 supporting | Clause 9.2, mandatory | Yes |
| Management review record | No direct equivalent | Clause 9.3, mandatory | ISO only |
| Authorization decision memorandum | Required, the point of the process | No equivalent | Federal only |

Ten of twelve artifacts serve both frameworks. Only two are framework specific, and they
are precisely the two that embody difference 2 and difference 3 above: the ISO
management review, and the federal authorisation decision.

---

## Section 5: What this crosswalk does not do

- It does not map individual NIST controls to individual Annex A controls. Family level
  only.
- It does not claim that satisfying one framework satisfies the other. A system with a
  FedRAMP Moderate ATO would still fail an ISO certification audit if it had no
  management review, no internal audit programme and no Statement of Applicability.
- It does not address ISO 27017 for cloud services or ISO 27701 for privacy, either of
  which would be the right next step for this system.

---

**Navigation:** [<- ISO-05: Internal Audit and Management Review](../iso-05-audit-management-review/README.md) &nbsp;|&nbsp; [Repository home](../README.md)

---

*Author: Nkeiru Sarah Adesida, Information System Security Officer (ISSO), portfolio scenario*  
*Simulated system: Keystone Grants Management System (KGMS) | FWDA-KGMS-2026-MOD*  
*This document is a portfolio exercise built on a fictional organisation. It is not a government record.*  
*[GitHub portfolio](https://github.com/Nkee07) | [LinkedIn](https://www.linkedin.com/in/nkeiru-adesida-grc)*
