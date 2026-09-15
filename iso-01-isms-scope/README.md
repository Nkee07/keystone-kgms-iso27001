# ISO-01: ISMS Scope, Context and Leadership
### Keystone Grants Management System (KGMS) | ISO/IEC 27001:2022 Clauses 4 to 7

> ### PORTFOLIO EXERCISE, SIMULATED SYSTEM
> **Keystone Grants Management System (KGMS) does not exist.** The Federal Workforce Development Agency (FWDA) is a fictional federal
> agency invented for this portfolio. Every organisation, person, system
> identifier, network address, finding, date and signature on this page is
> fabricated for training purposes, with one exception: the author, Nkeiru Sarah Adesida, is a real person. Where her name appears in a scenario role, that role is fictional, and she has never worked for this agency, which does not exist. Nothing here is drawn from any real
> employer, client or government system, and no real document, artifact or
> data has been reproduced. This file is coursework, not a government record.

---

**Document:** ISMS Scope, Context and Leadership Document  
**Simulated system:** Keystone Grants Management System (KGMS) | `FWDA-KGMS-2026-MOD`  
**Framework and standards:** ISO/IEC 27001:2022 Clauses 4, 5, 6 and 7  
**Author:** Nkeiru Sarah Adesida  
**Document date:** 20 February 2026  
**Status:** Complete

**Navigation:** [Repository home](../README.md) &nbsp;|&nbsp; [ISO-02: Statement of Applicability ->](../iso-02-soa/README.md)

---

## Purpose

Clause 4 of ISO/IEC 27001 asks a question that sounds trivial and is not: what exactly
are you protecting, and who cares about it? Getting the scope wrong is the most
expensive mistake available in an ISMS, because everything else is measured against it.

Plain language version: before you promise to keep something safe, you have to draw a
line around what "something" is. If the line is too big you will fail your own audit.
If it is too small the certificate is worthless because it covers nothing anyone cares
about.

---

## Section 1: Context of the organisation, Clause 4

### 4.1 The scope statement

**In scope.** The Keystone Grants Management System (KGMS), comprising the application, its supporting cloud
infrastructure inside the authorisation boundary, the information it processes, and
the agency functions that operate and govern it: grants technology operations,
information security operations, privacy, and the human capital processes that
control access.

**Out of scope, and why each one is out.**

| Excluded | Reason |
|---|---|
| The provider's physical data centre operations | Operated by Keystone Digital Services LLC under its own certification. Managed as a supplier under Annex A 5.19 to 5.22, not as an internal control |
| The agency wide area network and end user computing estate | A separate certified scope. In-scope information traverses it, so the interface is controlled, but the estate itself is not this ISMS |
| The nine regional offices as physical locations | No in-scope processing or storage occurs there. Staff use the service as ordinary users |
| The federal payment processing service | A separately authorised external system. The interface is in scope; the system is not |
| Other agency programme systems | No shared components or data with KGMS |

### The honest risk in this scope

The scope excludes the end user computing estate, which means an ISMS certificate over
this scope says nothing about whether an agency laptop is patched. That is a real
limitation and it is stated rather than glossed, because an auditor will find it and a
reader should not have to.

### 4.2 Interested parties and their requirements

| Interested party | Relationship | What they require |
|---|---|---|
| Grant applicants and grantee organisations | Data subjects and service users | That their information is protected and the award process is fair and available |
| Contracted peer reviewers | External users | Access to what they need to review, and protection of their own identity and conflict of interest declarations |
| Agency programme staff | Internal users | A service that is available during award cycles and does not obstruct the mission |
| The Authorizing Official | Accountable executive | Evidence sufficient to accept residual risk, and honest reporting when something changes |
| The Senior Agency Official for Privacy | Regulatory function | Compliance with the Privacy Act and the E-Government Act, and minimal collection |
| Agency Office of the Inspector General | Oversight | Auditable records and demonstrable internal control |
| Congressional oversight and the public | External accountability | Proper stewardship of appropriated funds |
| Keystone Digital Services LLC (fictional) | Cloud service provider | A clear responsibility split and accurate customer side configuration |
| Ardent Assurance Group LLC (fictional) | Independent assessor | Accurate documentation to assess against |
| Certification body | External auditor of this ISMS | A management system that operates as documented, with records to prove it |

### 4.3 and 4.4 The management system

The ISMS covers the scope above and is documented across this repository and the
federal authorisation package. The two are deliberately not separate management
systems: they are one set of controls reported against two frameworks, which is the
point of the crosswalk in [ISO-06](../iso-06-crosswalk/README.md).

---

## Section 2: Leadership, Clause 5

### 5.1 Leadership and commitment

Commitment is demonstrated by decisions, not by a signed statement. Three that count in
this scenario:

1. The Authorizing Official attached a **binding condition** to the authorisation
   rather than accepting an open High risk indefinitely, and stated that missing the
   date would trigger reconsideration.
2. The AO **declined to adjust a risk rating down** for convenience on the audit
   evidence finding, and asked to review that evidence personally rather than accept a
   closure report.
3. The AO **directed that any change to the payment reconciliation control be brought
   for approval before implementation**, because the system's impact categorisation
   depends on it.

### 5.2 Policy

The information security policy commits the agency to protect the confidentiality,
integrity and availability of grant information, to comply with FISMA, the Privacy Act
and the E-Government Act, to manage risk through a documented process, and to improve
the ISMS continually. Reviewed annually and on significant change.

### 5.3 Roles, responsibilities and authorities

| Role | Name | Authority in the ISMS |
|---|---|---|
| Authorizing Official (AO) | Patricia L. Ambrose | Accepts residual risk and signs the authorization decision |
| Chief Information Security Officer (CISO) | Daniel K. Osei | Advises the AO; does not sign the authorization decision |
| System Owner | Marcus T. Delacroix | Owns the mission function and the system budget |
| Information System Security Officer (ISSO) | Nkeiru Sarah Adesida | Day to day security posture, evidence, POA&M upkeep |
| Senior Agency Official for Privacy (SAOP) | Helen M. Barragan | Privacy threshold analysis and privacy impact assessment |
| Security Control Assessor, lead | Rebecca J. Tran | Independent assessment; authored the SAR |
| Cloud Service Provider representative | Alicia R. Vandermeer | CSP control implementation and inheritance |
| Cloud Operations Lead | Samuel P. Hargrave | Infrastructure, patching, configuration baselines |
| Application Development Lead | Priya N. Raghunathan | Application code, secure development, input validation |
| Security Operations Manager | Derrick A. Whitmore | Monitoring, detection, incident response |
| Human Capital Liaison | Yvonne C. Castellanos | Screening, onboarding, separation notifications, training records |

### The separation that matters most here

The Authorizing Official and the Chief Information Security Officer are two people.
The CISO recommends; the AO decides and accepts. A single person doing both is a
segregation of duties failure under Annex A 5.3, and it means nobody independent ever
challenged the risk decision. This is worth naming because collapsing the two is the
most common shortcut in practice scenarios and it quietly removes the control the
whole framework is built around.

---

## Section 3: Planning, Clause 6

### 6.1.1 General

Risks and opportunities are identified through the risk assessment process in
[ISO-03](../iso-03-risk-register/README.md), which follows ISO/IEC 27005.

### 6.1.2 Risk assessment

Method: asset and threat based. Likelihood and impact each rated 1 to 5, multiplied to
give a score from 1 to 25, banded as follows.

| Score | Band |
|---|---|
| 16 to 25 | High |
| 13 to 15 | Moderate-High |
| 9 to 12 | Moderate |
| 1 to 8 | Low |

Every risk is scored twice: **inherent**, before the controls currently in place, and
**residual**, after them. Scoring only once is the most common shortcut and it destroys
the value of the register, because you can no longer tell which controls are earning
their keep.

### 6.1.3 Risk treatment and the Statement of Applicability

Treatment options follow ISO/IEC 27005: **Modify** the risk by adding or strengthening
controls, **Retain** it as within tolerance, **Avoid** the activity, or **Share** it
with another party. These are the current terms. The older accept, reduce, avoid,
transfer wording belongs to a superseded revision and using it signals the current
edition was never opened.

The Statement of Applicability in [ISO-02](../iso-02-soa/README.md) records, for all
93 Annex A controls, whether the control applies and why, with
4 exclusions each carrying a justification an auditor can test.

### 6.2 Objectives

| Objective | Measure | Target | Result at 31 July 2026 |
|---|---|---|---|
| Close High risk weaknesses inside the authorised window | Days from finding to closure for High items | Within 30 days of the agreed date | Met. The single open High item closed 7 days early |
| Remediate vulnerabilities inside service levels | Percentage closed within the service level | 95 percent | Met. 100 percent of items closed in July closed inside service level |
| Evidence the weekly privileged activity review | Weeks with a retained review record | 4 of 4 per month | Not met. 2 of 4 in July. Tracked as POA-004 |
| Maintain security awareness currency | Agency users current on annual training | 98 percent | Met. 418 of 420, 99.5 percent |
| Verify the reconciliation control the categorisation depends on | Business days the daily reconciliation ran | 100 percent | Met. 22 of 22 business days in July |
| Maintain inventory accuracy | Components in inventory as a percentage of components discovered by scanning | 100 percent | Not met. Container images and two database instances were missing. Tracked as POA-010 and POA-011 |

Two of six objectives were not met, and both are recorded as not met rather than
softened. An ISMS whose objectives are all green every period is not being measured.

---

## Section 4: Support, Clause 7

| Requirement | How it is met |
|---|---|
| 7.1 Resources | Grants technology operations team, agency security operations centre, contracted assessor, GRC tooling in ServiceNow and RSA Archer |
| 7.2 Competence | The ISSO holds CISA and CompTIA Security+. Assessor competence is a contractual requirement |
| 7.3 Awareness | Annual security literacy and awareness training, tracked monthly, plus role specific briefings for privileged users |
| 7.4 Communication | Monthly continuous monitoring report to the AO; immediate escalation paths defined for incidents and for failure of the reconciliation control |
| 7.5 Documented information | This repository and the authorisation package. Version controlled, with evidence retained in RSA Archer for the retention period |


---

**Navigation:** [Repository home](../README.md) &nbsp;|&nbsp; [ISO-02: Statement of Applicability ->](../iso-02-soa/README.md)

---

*Author: Nkeiru Sarah Adesida, Information System Security Officer (ISSO), portfolio scenario*  
*Simulated system: Keystone Grants Management System (KGMS) | FWDA-KGMS-2026-MOD*  
*This document is a portfolio exercise built on a fictional organisation. It is not a government record.*  
*[GitHub portfolio](https://github.com/Nkee07) | [LinkedIn](https://www.linkedin.com/in/nkeiru-adesida-grc)*
