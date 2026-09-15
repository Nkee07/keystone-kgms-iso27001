# ISO-02: Statement of Applicability
### Keystone Grants Management System (KGMS) | All 93 Annex A controls, 89 applicable, 4 excluded

> ### PORTFOLIO EXERCISE, SIMULATED SYSTEM
> **Keystone Grants Management System (KGMS) does not exist.** The Federal Workforce Development Agency (FWDA) is a fictional federal
> agency invented for this portfolio. Every organisation, person, system
> identifier, network address, finding, date and signature on this page is
> fabricated for training purposes, with one exception: the author, Nkeiru Sarah Adesida, is a real person. Where her name appears in a scenario role, that role is fictional, and she has never worked for this agency, which does not exist. Nothing here is drawn from any real
> employer, client or government system, and no real document, artifact or
> data has been reproduced. This file is coursework, not a government record.

---

**Document:** Statement of Applicability  
**Simulated system:** Keystone Grants Management System (KGMS) | `FWDA-KGMS-2026-MOD`  
**Framework and standards:** ISO/IEC 27001:2022 Clause 6.1.3 d and Annex A  
**Author:** Nkeiru Sarah Adesida  
**Document date:** 13 March 2026  
**Status:** Complete

**Navigation:** [<- ISO-01: ISMS Scope, Context and Leadership](../iso-01-isms-scope/README.md) &nbsp;|&nbsp; [Repository home](../README.md) &nbsp;|&nbsp; [ISO-03: Information Security Risk Register ->](../iso-03-risk-register/README.md)

---

## Purpose

The Statement of Applicability is the document a certification auditor opens first. For
every control in Annex A it records whether the control applies, and if not, why not.

Plain language version: Annex A is a list of 93 safety measures. For each one
you have to say "yes we do this" or "no, and here is the reason it does not apply to
us". You cannot skip any. An auditor reads the reasons, not the yeses.

---

## Two design decisions in this document

**1. Applicability and implementation status are separate columns.**

These answer different questions. "Does this control apply to us" is Yes or No, and
nothing else. "Have we finished implementing it" is a separate axis with several
possible answers. Putting a value like "partially" into the applicability column is
what makes a Statement of Applicability summary unable to reconcile with its own rows,
because "partially" is neither applicable nor excluded and the totals stop adding up.

**2. Every count in this document is computed from the 93 rows below.**

Nothing is typed. The summary cannot drift from the detail, because the summary is
generated from the detail. This was a deliberate engineering choice, and it is the
single most valuable habit in compliance documentation: a summary table that disagrees
with the rows underneath it destroys a reader's trust in every other number in the
package, and it takes a reviewer about sixty seconds to find.

---

## Section 1: Summary

### By theme

| Theme | Controls in theme | Applicable | Excluded |
|---|---|---|---|
| 5. Organizational controls | 37 | 37 | 0 |
| 6. People controls | 8 | 8 | 0 |
| 7. Physical controls | 14 | 11 | 3 |
| 8. Technological controls | 34 | 33 | 1 |
| **Total** | **93** | **89** | **4** |

### By implementation status

| Status | Count | Meaning |
|---|---|---|
| Implemented | 72 | Control is in place and evidence exists |
| Implemented by supplier | 9 | Satisfied by Keystone Digital Services LLC under its own certification, managed as a supplier control and reviewed annually |
| Partially implemented | 8 | In place but with a known gap, each one tracked as an open item |
| Not applicable | 4 | Excluded, with a justification below |
| **Total** | **93** |  |

### The 2022 edition, stated correctly

|  | 2013 edition | 2022 edition |
|---|---|---|
| Controls | 114 | 93 |
| Grouping | 14 domains | 4 themes |
| New controls |  | 11 added, including threat intelligence, information security for use of cloud services, data masking, data leakage prevention, monitoring activities, web filtering and secure coding |

Organizational 37, People 8, Physical 14, Technological 34. That is
37 + 8 + 14 + 34 = 93.

---

## Section 2: The 4 exclusions

Exclusions are where an auditor spends their time, so each one states the reason and,
where relevant, **the condition that would make it applicable again**. An exclusion
without a reversal condition is an exclusion nobody intends to revisit.

**7.6 Working in secure areas**

No secure area as defined by the standard is operated by the agency within the ISMS scope. All in-scope processing occurs in the cloud provider's facility, which is addressed through supplier controls 5.19 to 5.22 and the provider's own certification.

**7.10 Storage media**

Removable storage media is prohibited by policy and blocked technically on all endpoints through device control. No in-scope information is held on physical media at any point in its lifecycle. Verified by the internal audit in June 2026.

**7.12 Cabling security**

The agency controls no cabling that carries in-scope information. Agency offices connect over the agency wide area network, which is a separate certified scope; in-scope processing cabling is inside the provider facility and addressed through supplier controls.

**8.30 Outsourced development**

All development is performed by agency staff and by provider staff working under direct agency technical direction. There is no outsourced development contract in scope. This exclusion is void if development work is contracted out.

Four exclusions from 93 controls. Excluding a large number of controls,
particularly the physical ones, is a common way to make an SoA look easy, and it does
not survive an audit. The nine physical controls satisfied inside the provider's
facility are recorded here as **applicable and implemented by the supplier**, not
excluded, because the agency still has to evidence that it reviewed the provider's
certification. "The cloud handles it" is not evidence.

---

## Section 3: The 8 partially implemented controls

Each one is tied to a specific open item in the federal
[POA&M](https://github.com/Nkee07/keystone-kgms-fedramp-rmf/blob/main/step-05-authorization/README.md),
so the two frameworks report the same truth rather than two different optimistic
versions of it.

| Control | Control name | Gap and where it is tracked |
|---|---|---|
| 5.9 | Inventory of information and other associated assets | Asset inventory is maintained. Three container images were omitted until July 2026 and two database instances were absent from the scan target group. Build pipeline automation to register components automatically is in design. Tracked as POA-010. |
| 5.21 | Managing information security in the ICT supply chain | Supply chain procedure for the container base image pipeline and the third party charting library is drafted but not yet approved by the System Owner. Tracked as risk R-06 and as POA-006 in the FedRAMP repository. Target 31 August 2026. |
| 5.29 | Information security during disruption | Continuity plan documented and updated 31 July 2026. The functional restore test that would verify the four hour recovery objective has not yet been performed. Tracked as risk R-07 and POA-005. Target 15 September 2026. |
| 5.30 | ICT readiness for business continuity | ICT readiness documented; recovery time objective unverified pending the functional test. Same dependency as 5.29. |
| 6.5 | Responsibilities after termination or change of employment | Accounts are disabled within one business day of separation, verified on all nine separations in the sample period. The signed separation checklist was on file for seven of nine. Tracked as POA-009. |
| 8.8 | Management of technical vulnerabilities | Weekly authenticated scanning, per build container scanning and defined service levels are in place. Two gaps in July 2026: two database instances outside scan scope, and a transitive dependency vulnerability the scanner was not configured to resolve. Tracked as POA-011 and POA-012. |
| 8.16 | Monitoring activities | Daily alert triage is evidenced. The weekly correlated review of privileged activity produced evidence for 2 of 4 weeks in July 2026. Automation in build. Tracked as POA-004. |
| 8.24 | Use of cryptography | Cryptography is applied throughout. One gap remains: snapshots replicated to the secondary region are not yet encrypted under a customer managed key. Tracked as risk R-12 and POA-007. Target 30 September 2026. |

---

## Section 4: Statement of Applicability, all 93 controls

### Theme 5: Organizational controls, 37 controls (37 applicable, 0 excluded)

| Control | Control name | Applicable | Implementation status | Justification |
|---|---|---|---|---|
| 5.1 | Policies for information security | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.2 | Information security roles and responsibilities | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.3 | Segregation of duties | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.4 | Management responsibilities | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.5 | Contact with authorities | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.6 | Contact with special interest groups | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.7 | Threat intelligence | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.8 | Information security in project management | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.9 | Inventory of information and other associated assets | Yes | Partially implemented | Asset inventory is maintained. Three container images were omitted until July 2026 and two database instances were absent from the scan target group. Build pipeline automation to register components automatically is in design. Tracked as POA-010. |
| 5.10 | Acceptable use of information and other associated assets | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.11 | Return of assets | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.12 | Classification of information | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.13 | Labelling of information | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.14 | Information transfer | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.15 | Access control | Yes | Implemented | Role based access control with nine application roles enforced server side, least privilege reviewed quarterly with line by line supervisor attestation retained in RSA Archer. |
| 5.16 | Identity management | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.17 | Authentication information | Yes | Implemented | Minimum 16 characters, screened against a breached password list, no forced rotation. Policy corrected in July 2026 to match the configured behaviour of the identity provider. |
| 5.18 | Access rights | Yes | Implemented | Quarterly access review. Reviewer accounts carry an expiry set at creation to panel end plus 14 days. |
| 5.19 | Information security in supplier relationships | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.20 | Addressing information security within supplier agreements | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.21 | Managing information security in the ICT supply chain | Yes | Partially implemented | Supply chain procedure for the container base image pipeline and the third party charting library is drafted but not yet approved by the System Owner. Tracked as risk R-06 and as POA-006 in the FedRAMP repository. Target 31 August 2026. |
| 5.22 | Monitoring, review and change management of supplier services | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.23 | Information security for use of cloud services | Yes | Implemented | Cloud service use governed by the provider agreement, the shared responsibility split recorded in the control responsibility matrix, and annual review of the provider's certification. |
| 5.24 | Information security incident management planning and preparation | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.25 | Assessment and decision on information security events | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.26 | Response to information security incidents | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.27 | Learning from information security incidents | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.28 | Collection of evidence | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.29 | Information security during disruption | Yes | Partially implemented | Continuity plan documented and updated 31 July 2026. The functional restore test that would verify the four hour recovery objective has not yet been performed. Tracked as risk R-07 and POA-005. Target 15 September 2026. |
| 5.30 | ICT readiness for business continuity | Yes | Partially implemented | ICT readiness documented; recovery time objective unverified pending the functional test. Same dependency as 5.29. |
| 5.31 | Legal, statutory, regulatory and contractual requirements | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.32 | Intellectual property rights | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.33 | Protection of records | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.34 | Privacy and protection of PII | Yes | Implemented | Privacy threshold analysis and privacy impact assessment completed by the Senior Agency Official for Privacy. Personal information limited to what the grant process requires. |
| 5.35 | Independent review of information security | Yes | Implemented | Independent assessment by a third party assessor reporting to the CISO, completed March 2026, plus the ISMS internal audit completed June 2026. |
| 5.36 | Compliance with policies, rules and standards for information security | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 5.37 | Documented operating procedures | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |

### Theme 6: People controls, 8 controls (8 applicable, 0 excluded)

| Control | Control name | Applicable | Implementation status | Justification |
|---|---|---|---|---|
| 6.1 | Screening | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 6.2 | Terms and conditions of employment | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 6.3 | Information security awareness, education and training | Yes | Implemented | Annual security literacy and awareness training, tracked monthly. 418 of 420 agency users current at 31 July 2026, the remaining two inside their grace period. |
| 6.4 | Disciplinary process | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 6.5 | Responsibilities after termination or change of employment | Yes | Partially implemented | Accounts are disabled within one business day of separation, verified on all nine separations in the sample period. The signed separation checklist was on file for seven of nine. Tracked as POA-009. |
| 6.6 | Confidentiality or non-disclosure agreements | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 6.7 | Remote working | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 6.8 | Information security event reporting | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |

### Theme 7: Physical controls, 14 controls (11 applicable, 3 excluded)

| Control | Control name | Applicable | Implementation status | Justification |
|---|---|---|---|---|
| 7.1 | Physical security perimeters | Yes | Implemented by supplier | Provider data centre perimeter. Evidence: the provider's current certification and authorisation package, reviewed annually under 5.22. |
| 7.2 | Physical entry | Yes | Implemented by supplier | Provider controls physical entry to the facility. |
| 7.3 | Securing offices, rooms and facilities | Yes | Implemented by supplier | Provider facility. Agency offices hold no in-scope processing. |
| 7.4 | Physical security monitoring | Yes | Implemented by supplier | Provider surveillance and intrusion detection. |
| 7.5 | Protecting against physical and environmental threats | Yes | Implemented by supplier | Provider fire suppression, flood and environmental protection. |
| 7.6 | Working in secure areas | No | Not applicable | No secure area as defined by the standard is operated by the agency within the ISMS scope. All in-scope processing occurs in the cloud provider's facility, which is addressed through supplier controls 5.19 to 5.22 and the provider's own certification. |
| 7.7 | Clear desk and clear screen | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 7.8 | Equipment siting and protection | Yes | Implemented by supplier | Equipment siting inside the provider facility. |
| 7.9 | Security of assets off-premises | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 7.10 | Storage media | No | Not applicable | Removable storage media is prohibited by policy and blocked technically on all endpoints through device control. No in-scope information is held on physical media at any point in its lifecycle. Verified by the internal audit in June 2026. |
| 7.11 | Supporting utilities | Yes | Implemented by supplier | Provider power, cooling and redundancy. |
| 7.12 | Cabling security | No | Not applicable | The agency controls no cabling that carries in-scope information. Agency offices connect over the agency wide area network, which is a separate certified scope; in-scope processing cabling is inside the provider facility and addressed through supplier controls. |
| 7.13 | Equipment maintenance | Yes | Implemented by supplier | Provider hardware maintenance. Agency endpoints are covered separately under 8.1. |
| 7.14 | Secure disposal or re-use of equipment | Yes | Implemented by supplier | Provider media sanitisation on decommissioning. Certificate of destruction available on request. |

### Theme 8: Technological controls, 34 controls (33 applicable, 1 excluded)

| Control | Control name | Applicable | Implementation status | Justification |
|---|---|---|---|---|
| 8.1 | User endpoint devices | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.2 | Privileged access rights | Yes | Implemented | Three privileged groups, 16 members, full population reviewed quarterly. Privileged actions performed from a role assumed for the task with a justification string logged. |
| 8.3 | Information access restriction | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.4 | Access to source code | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.5 | Secure authentication | Yes | Implemented | Federated authentication. PIV card for 420 agency users; authenticator application multifactor for 65 external reviewers since 24 July 2026. |
| 8.6 | Capacity management | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.7 | Protection against malware | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.8 | Management of technical vulnerabilities | Yes | Partially implemented | Weekly authenticated scanning, per build container scanning and defined service levels are in place. Two gaps in July 2026: two database instances outside scan scope, and a transitive dependency vulnerability the scanner was not configured to resolve. Tracked as POA-011 and POA-012. |
| 8.9 | Configuration management | Yes | Implemented | Hardened baseline images per tier. Continuous compliance evaluation active since July 2026, which closed the drift detection gap found at assessment. |
| 8.10 | Information deletion | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.11 | Data masking | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.12 | Data leakage prevention | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.13 | Information backup | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.14 | Redundancy of information processing facilities | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.15 | Logging | Yes | Implemented | Seven log groups, one year online and two years archived, retention corrected on all groups in March 2026. |
| 8.16 | Monitoring activities | Yes | Partially implemented | Daily alert triage is evidenced. The weekly correlated review of privileged activity produced evidence for 2 of 4 weeks in July 2026. Automation in build. Tracked as POA-004. |
| 8.17 | Clock synchronization | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.18 | Use of privileged utility programs | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.19 | Installation of software on operational systems | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.20 | Networks security | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.21 | Security of network services | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.22 | Segregation of networks | Yes | Implemented | Three tier subnet model. The data subnet has no route to the internet. |
| 8.23 | Web filtering | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.24 | Use of cryptography | Yes | Partially implemented | Cryptography is applied throughout. One gap remains: snapshots replicated to the secondary region are not yet encrypted under a customer managed key. Tracked as risk R-12 and POA-007. Target 30 September 2026. |
| 8.25 | Secure development life cycle | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.26 | Application security requirements | Yes | Implemented | Input validation on all 31 user supplied fields, allow list based, with context aware output encoding as a second layer. |
| 8.27 | Secure system architecture and engineering principles | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.28 | Secure coding | Yes | Implemented | Peer review required before merge, dependency scanning in the pipeline, parameterised queries throughout. |
| 8.29 | Security testing in development and acceptance | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.30 | Outsourced development | No | Not applicable | All development is performed by agency staff and by provider staff working under direct agency technical direction. There is no outsourced development contract in scope. This exclusion is void if development work is contracted out. |
| 8.31 | Separation of development, test and production environments | Yes | Implemented | Development, test and production are separate accounts with no shared credentials and no production data in lower environments. |
| 8.32 | Change management | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |
| 8.33 | Test information | Yes | Implemented | Test data is synthetic. Production data is never copied into a lower environment. |
| 8.34 | Protection of information systems during audit testing | Yes | Implemented | Implemented as part of the ISMS. Evidence retained in RSA Archer and sampled at internal audit. |

---

## Machine readable version

[artifacts/kgms-statement-of-applicability.csv](../artifacts/kgms-statement-of-applicability.csv).
A Statement of Applicability is maintained as a spreadsheet in practice, because it is
filtered, sorted and handed to auditors as a working document.

---

**Navigation:** [<- ISO-01: ISMS Scope, Context and Leadership](../iso-01-isms-scope/README.md) &nbsp;|&nbsp; [Repository home](../README.md) &nbsp;|&nbsp; [ISO-03: Information Security Risk Register ->](../iso-03-risk-register/README.md)

---

*Author: Nkeiru Sarah Adesida, Information System Security Officer (ISSO), portfolio scenario*  
*Simulated system: Keystone Grants Management System (KGMS) | FWDA-KGMS-2026-MOD*  
*This document is a portfolio exercise built on a fictional organisation. It is not a government record.*  
*[GitHub portfolio](https://github.com/Nkee07) | [LinkedIn](https://www.linkedin.com/in/nkeiru-adesida-grc)*
