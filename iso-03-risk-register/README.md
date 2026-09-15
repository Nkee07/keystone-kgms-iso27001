# ISO-03: Information Security Risk Register
### Keystone Grants Management System (KGMS) | 12 risks, scored inherent and residual

> ### PORTFOLIO EXERCISE, SIMULATED SYSTEM
> **Keystone Grants Management System (KGMS) does not exist.** The Federal Workforce Development Agency (FWDA) is a fictional federal
> agency invented for this portfolio. Every organisation, person, system
> identifier, network address, finding, date and signature on this page is
> fabricated for training purposes, with one exception: the author, Nkeiru Sarah Adesida, is a real person. Where her name appears in a scenario role, that role is fictional, and she has never worked for this agency, which does not exist. Nothing here is drawn from any real
> employer, client or government system, and no real document, artifact or
> data has been reproduced. This file is coursework, not a government record.

---

**Document:** Information Security Risk Register  
**Simulated system:** Keystone Grants Management System (KGMS) | `FWDA-KGMS-2026-MOD`  
**Framework and standards:** ISO/IEC 27001:2022 Clause 6.1.2, ISO/IEC 27005  
**Author:** Nkeiru Sarah Adesida  
**Document date:** 12 August 2026  
**Status:** Current. 12 risks. First issued 20 March 2026, this is the quarterly review revision. A risk register is a living document, so the controls in place column reflects the position at the review date, not at first issue

**Navigation:** [<- ISO-02: Statement of Applicability](../iso-02-soa/README.md) &nbsp;|&nbsp; [Repository home](../README.md) &nbsp;|&nbsp; [ISO-04: Risk Treatment Plan ->](../iso-04-risk-treatment/README.md)

---

## Purpose

The risk register is the engine of an ISMS. Clause 6.1.2 requires a documented risk
assessment process, and Annex A exists to serve it: controls are selected because a
risk requires them, not because a list mentioned them.

Plain language version: write down everything that could go wrong, how likely each one
is, how bad it would be, what you already do about it, and how bad it still is after
what you already do. The last number is the one that decides what you work on next.

---

## Section 1: Method

| Element | Approach |
|---|---|
| Standard | ISO/IEC 27005, risk management guidance supporting ISO/IEC 27001 Clause 6.1.2 |
| Identification | Asset and threat based. Assets from the component inventory; threats from the agency threat profile, the assessment findings and vulnerability scan history |
| Likelihood | 1 to 5. 1 rare, 2 unlikely, 3 possible, 4 likely, 5 almost certain |
| Impact | 1 to 5, judged against mission delivery, harm to individuals, financial loss and statutory compliance |
| Score | Likelihood multiplied by impact, 1 to 25 |
| Inherent score | Before the controls currently in place |
| Residual score | After the controls currently in place |
| Risk tolerance | Residual scores in the Low band are within tolerance. Moderate requires active treatment or a documented retention decision. Moderate-High and High are outside tolerance and must be treated |
| Treatment options | Modify, Retain, Avoid, Share, per ISO/IEC 27005 |
| Review | Quarterly, and on any significant change |

### Bands

| Score | Band | Meaning |
|---|---|---|
| 16 to 25 | High | Outside tolerance. Treat immediately |
| 13 to 15 | Moderate-High | Outside tolerance. Treat |
| 9 to 12 | Moderate | Treat, or retain with a documented decision |
| 1 to 8 | Low | Within tolerance. Monitor |

### Why every risk is scored twice

An inherent score alone tells you what the world looks like with no controls, which is
not a decision. A residual score alone tells you where you are but not which control is
holding the weight. Both together tell you where control investment is actually
earning: R-08, cloud misconfiguration, drops from 15
to 6, which is the strongest control
effect in this register. R-06, supply chain, drops from
12 to
12, that is, not at all, which is exactly
why it is first in the treatment plan.

---

## Section 2: Risk register, 12 risks

| ID | Risk | Threat source | Affected asset | L | I | Inherent | Band | Controls currently in place | rL | rI | Residual | Band | Treatment |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R-01 | Compromise of an external reviewer credential exposing applicant PII and unpublished merit scores | External attacker, credential phishing | Reviewer portal, merit review records | 4 | 4 | 16 | High | Multifactor authentication enforced for all 65 reviewer accounts since 24 July 2026; accounts expire at panel end plus 14 days; session timeout 30 minutes | 2 | 4 | 8 | Low | Modify |
| R-02 | Exploitation of an application input handling weakness to read or alter grant records | External attacker, any member of the public able to start an application | Application tier, grant records | 4 | 5 | 20 | High | Allow list input validation on all 31 fields; context aware output encoding; parameterised queries; monthly authenticated web application scanning; annual penetration test | 2 | 5 | 10 | Moderate | Modify |
| R-03 | Exploitation of an unremediated software vulnerability in a system component or dependency | External attacker; automated exploitation of a published vulnerability | All tiers, third party dependencies | 4 | 4 | 16 | High | Weekly authenticated scanning; per build container scanning; service levels of 30 days for Critical and High; monthly patch cycle with an emergency path | 3 | 4 | 12 | Moderate | Modify |
| R-04 | Misuse of privileged access by an authorised administrator | Insider, malicious or negligent | Application, database and cloud control plane | 3 | 5 | 15 | Moderate-High | 16 privileged accounts across 3 groups; documented approval required; role assumed per task with logged justification; quarterly full population review; session recording on all brokered access | 2 | 5 | 10 | Moderate | Modify |
| R-05 | Undetected alteration of an award or disbursement record misdirecting federal funds | Insider; external attacker; processing error | Award records, payment instruction records | 3 | 5 | 15 | Moderate-High | Daily two way reconciliation against the payment service confirmation and the obligation balance; segregation of duties between award approval and disbursement; immutable audit trail | 2 | 4 | 8 | Low | Modify |
| R-06 | Compromise of a third party component introduced through the software supply chain | Upstream compromise of a dependency or base image | Build pipeline, container images, application dependencies | 3 | 4 | 12 | Moderate | Signed base images; checksum verification in the pipeline; dependency scanning. Supply chain procedure drafted but not approved, and the scanner resolved direct dependencies only until August 2026 | 3 | 4 | 12 | Moderate | Modify |
| R-07 | Extended service unavailability with an unverified recovery capability | Infrastructure failure; regional outage; destructive incident | Whole service | 3 | 4 | 12 | Moderate | Nightly backup with 35 day retention; cross region snapshot replication; multi availability zone deployment; continuity plan documented. The functional restore test has never been performed | 3 | 3 | 9 | Moderate | Modify |
| R-08 | Cloud misconfiguration exposing a data store to unauthorised access | Human error in configuration change | Document store, database | 3 | 5 | 15 | Moderate-High | Infrastructure defined as code with peer review; continuous compliance rules evaluating every resource; public access blocked at the account level; data subnet has no internet route | 2 | 3 | 6 | Low | Retain |
| R-09 | Compromise of an agency user account through phishing | External attacker | Agency accounts, application data | 4 | 3 | 12 | Moderate | PIV card authentication for all 420 agency accounts, which defeats credential replay; annual training with monthly tracking; email filtering; reporting path to the security operations centre | 2 | 3 | 6 | Low | Retain |
| R-10 | Mishandling of personal information in breach of the Privacy Act | Process failure; excessive collection or retention | Applicant and reviewer personal information | 2 | 4 | 8 | Low | Privacy impact assessment; collection limited to what the grant process requires; retention schedule enforced; access restricted by role; privacy officer review of any new data element | 2 | 3 | 6 | Low | Retain |
| R-11 | Insufficient audit evidence to support an investigation after an incident | Control performed without leaving a record; retention misconfiguration | Audit records across seven log groups | 3 | 3 | 9 | Moderate | Seven log groups with one year online and two years archived; retention corrected March 2026; daily triage evidenced. The weekly correlated review record is still being automated | 3 | 2 | 6 | Low | Modify |
| R-12 | Weak key governance over the secondary region copy of system data | Loss of agency control over key policy and key usage visibility | Replicated snapshots in the secondary region | 2 | 4 | 8 | Low | All data encrypted at rest. Primary region uses a customer managed key with agency controlled policy, rotation and usage logging. Secondary region key created 30 July 2026, re-encryption of existing snapshots pending | 2 | 2 | 4 | Low | Modify |

---

## Section 3: Distribution

| Band | Inherent count | Residual count |
|---|---|---|
| High (16 to 25) | 3 | 0 |
| Moderate-High (13 to 15) | 3 | 0 |
| Moderate (9 to 12) | 4 | 5 |
| Low (1 to 8) | 2 | 7 |
| **Total** | **12** | **12** |

Both columns are computed from the register rows. No risk is scored outside the
1 to 25 range, no residual score exceeds its own inherent score, and both columns sum
to 12. Those three checks run as a script before publication.

### Reading the shift honestly

Inherent: 3 High, 3 Moderate-High,
4 Moderate, 2 Low.
Residual: 0 High, 0 Moderate-High,
5 Moderate, 7 Low.

The controls in place move every risk out of the High and Moderate-High bands.
**5 risks remain in the Moderate band and are therefore outside
the Low tolerance threshold.** They are not described as acceptable, because by the
tolerance statement in Section 1 they are not. They are the subject of
[ISO-04](../iso-04-risk-treatment/README.md).

Stating that plainly matters. The tempting sentence here is "all residual risks are
within tolerance", and it would be false against this register's own threshold
definition.

---

## Section 4: Risks ranked by residual score

This ordering is what drives the treatment plan. It is published so a reader can check
the selection rather than take it on trust.

| Rank | ID | Residual score | Band | Treated in ISO-04? |
|---|---|---|---|---|
| 1 | R-03 | 12 | Moderate | Yes |
| 2 | R-06 | 12 | Moderate | Yes |
| 3 | R-02 | 10 | Moderate | Yes |
| 4 | R-04 | 10 | Moderate | Yes |
| 5 | R-07 | 9 | Moderate | Yes |
| 6 | R-01 | 8 | Low | No, within tolerance and monitored |
| 7 | R-05 | 8 | Low | No, within tolerance and monitored |
| 8 | R-08 | 6 | Low | No, within tolerance and monitored |
| 9 | R-09 | 6 | Low | No, within tolerance and monitored |
| 10 | R-10 | 6 | Low | No, within tolerance and monitored |
| 11 | R-11 | 6 | Low | No, within tolerance and monitored |
| 12 | R-12 | 4 | Low | No, within tolerance and monitored |

The boundary is unambiguous: rank 5 scores 9 and rank 6 scores
8. There is no tie across the cut, so the five treated risks are
genuinely the five highest by residual score and not simply the first five by
identifier.

---

## Section 5: Risk owners

A risk owner is the person accountable for the risk, which is not always the person who
implements the control.

| ID | Risk | Owner |
|---|---|---|
| R-01 | Compromise of an external reviewer credential exposing applicant PII a... | Samuel P. Hargrave |
| R-02 | Exploitation of an application input handling weakness to read or alte... | Priya N. Raghunathan |
| R-03 | Exploitation of an unremediated software vulnerability in a system com... | Samuel P. Hargrave |
| R-04 | Misuse of privileged access by an authorised administrator | Derrick A. Whitmore |
| R-05 | Undetected alteration of an award or disbursement record misdirecting ... | Marcus T. Delacroix |
| R-06 | Compromise of a third party component introduced through the software ... | Nkeiru Sarah Adesida |
| R-07 | Extended service unavailability with an unverified recovery capability | Marcus T. Delacroix |
| R-08 | Cloud misconfiguration exposing a data store to unauthorised access | Samuel P. Hargrave |
| R-09 | Compromise of an agency user account through phishing | Derrick A. Whitmore |
| R-10 | Mishandling of personal information in breach of the Privacy Act | Helen M. Barragan |
| R-11 | Insufficient audit evidence to support an investigation after an incid... | Derrick A. Whitmore |
| R-12 | Weak key governance over the secondary region copy of system data | Samuel P. Hargrave |

---

## Machine readable version

[artifacts/kgms-risk-register.csv](../artifacts/kgms-risk-register.csv).

---

**Navigation:** [<- ISO-02: Statement of Applicability](../iso-02-soa/README.md) &nbsp;|&nbsp; [Repository home](../README.md) &nbsp;|&nbsp; [ISO-04: Risk Treatment Plan ->](../iso-04-risk-treatment/README.md)

---

*Author: Nkeiru Sarah Adesida, Information System Security Officer (ISSO), portfolio scenario*  
*Simulated system: Keystone Grants Management System (KGMS) | FWDA-KGMS-2026-MOD*  
*This document is a portfolio exercise built on a fictional organisation. It is not a government record.*  
*[GitHub portfolio](https://github.com/Nkee07) | [LinkedIn](https://www.linkedin.com/in/nkeiru-adesida-grc)*
