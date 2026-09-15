# ISO-05: Internal Audit and Management Review
### Keystone Grants Management System (KGMS) | ISO/IEC 27001:2022 Clauses 9 and 10

> ### PORTFOLIO EXERCISE, SIMULATED SYSTEM
> **Keystone Grants Management System (KGMS) does not exist.** The Federal Workforce Development Agency (FWDA) is a fictional federal
> agency invented for this portfolio. Every organisation, person, system
> identifier, network address, finding, date and signature on this page is
> fabricated for training purposes, with one exception: the author, Nkeiru Sarah Adesida, is a real person. Where her name appears in a scenario role, that role is fictional, and she has never worked for this agency, which does not exist. Nothing here is drawn from any real
> employer, client or government system, and no real document, artifact or
> data has been reproduced. This file is coursework, not a government record.

---

**Document:** Internal Audit Report and Management Review Record  
**Simulated system:** Keystone Grants Management System (KGMS) | `FWDA-KGMS-2026-MOD`  
**Framework and standards:** ISO/IEC 27001:2022 Clauses 9.2, 9.3 and 10  
**Author:** Nkeiru Sarah Adesida  
**Document date:** 9 July 2026  
**Status:** Complete. 0 major, 3 minor nonconformities, 1 observation

**Navigation:** [<- ISO-04: Risk Treatment Plan](../iso-04-risk-treatment/README.md) &nbsp;|&nbsp; [Repository home](../README.md) &nbsp;|&nbsp; [ISO-06: NIST to ISO Framework Crosswalk ->](../iso-06-crosswalk/README.md)

---

## Purpose

Clause 9 asks whether the management system actually works, and Clause 10 asks what was
done about it when the answer was no. Part A is the internal audit. Part B is the
management review.

Plain language version: Part A is marking your own homework, honestly, before the
external examiner arrives. Part B is the meeting where the people in charge read the
marks and decide what to change.

---

# PART A: INTERNAL AUDIT

| Field | Detail |
|---|---|
| Audit scope | The full ISMS for Keystone Grants Management System (KGMS), Clauses 4 to 10 and the Annex A controls |
| Audit criteria | ISO/IEC 27001:2022, the ISMS documented information, and applicable federal requirements |
| Audit type | Internal audit under Clause 9.2 |
| Auditor | Agency internal audit function |
| Impartiality | The internal audit function reports to the agency Audit Committee, not to the System Owner or the ISSO. The ISSO was auditee, not auditor |
| Fieldwork | 8 to 18 June 2026 |
| Report issued | 26 June 2026 |
| Previous audit | None. This is the first internal audit of this ISMS |

## A1: Audit checklist and results

| Clause | Audit question | Evidence examined | Finding | Result |
|---|---|---|---|---|
| 4.1 | Is the ISMS scope documented, and are exclusions justified? | ISMS Scope Document ISO-01, section 1 | Scope documented with five exclusions, each with a reason. The exclusion of the end user computing estate is stated as a limitation rather than glossed | Conformant |
| 4.2 | Are interested parties and their requirements identified? | ISO-01 section 1, 4.2 | Ten parties identified with requirements | Conformant |
| 5.1 | Is top management commitment demonstrable through decisions, not statements? | Authorization decision memorandum 15 May 2026; AO direction on the reconciliation control | Three specific decisions evidenced, including a binding condition on the authorisation | Conformant |
| 5.3 | Are roles, responsibilities and authorities assigned, with adequate segregation? | ISO-01 section 2, 5.3; authorisation package | Eleven roles assigned. The Authorizing Official and the CISO are separate individuals, which satisfies segregation of the recommend and accept decisions | Conformant |
| 6.1.2 | Is there a documented risk assessment process, applied consistently? | Risk Register ISO-03 | Twelve risks, each scored inherent and residual on a documented 1 to 5 scale. Method applied consistently across all rows | Conformant |
| 6.1.3 | Is a Statement of Applicability produced, current, and does it reconcile? | Statement of Applicability ISO-02 | All 93 controls addressed. 4 exclusions with testable justifications. Auditor recounted the rows: applicable 89, excluded 4, matching the summary table exactly | Conformant |
| 6.1.3 | Does the risk treatment plan treat the risks it claims to treat? | Risk Treatment Plan ISO-04 | The plan claims to treat the five highest residual risks. Auditor sorted the register independently and confirmed the five selected are ranks 1 to 5 by residual score, with no tie across the cut | Conformant |
| 6.2 | Are information security objectives measurable, and measured honestly? | ISO-01 section 3, 6.2 | Six objectives with measures and results. Two recorded as not met. Auditor notes that recording a failure is itself evidence the measurement is real | Conformant |
| 7.2 | Is competence determined and evidenced? | Training records; ISSO certifications | ISSO holds CISA and CompTIA Security+. Assessor competence is a contract requirement | Conformant |
| 7.3 | Are personnel aware of the policy and their contribution? | Training completion report | 418 of 420 agency users current, the remaining two inside grace | Conformant |
| 7.5 | Is documented information controlled and available? | Repository version history; RSA Archer evidence store | Version controlled with a change history. SSP shows three versions with the reason for each | Conformant |
| 8.1 | Is the ISMS operated as planned, with records? | Continuous monitoring report July 2026 | Monthly report produced on schedule, 12 August, inside the 15th of month requirement | Conformant |
| 8.2 | Are risk assessments performed at planned intervals and on change? | Risk register review log; significant change records | Quarterly review evidenced. Four July changes each have an impact analysis record | Conformant |
| 8.3 | Is the risk treatment plan implemented? | ISO-04; POA&M status | Implementation in progress with committed dates. Two treatment actions already complete ahead of milestone | Conformant |
| 9.1 | Is ISMS performance monitored and evaluated? | Objectives table; monthly reports | Six objectives measured monthly. Results reported including failures | Conformant |
| 9.2 | Is internal audit conducted at planned intervals by competent, impartial auditors? | This audit; audit programme | Audit performed June 2026 by the agency internal audit function, which does not report to the System Owner | Conformant |
| 9.3 | Is management review conducted with the required inputs? | Management review record, Part B below | Review held 9 July 2026 with all Clause 9.3 inputs present | Conformant |
| 10.1 | Is continual improvement demonstrable? | POA&M closure record; control changes | Four POA&M items closed in July. Drift detection and validation approach both strengthened beyond the minimum the finding required | Conformant |
| 10.2 | Are nonconformities corrected, with root cause addressed? | Assessment findings and remediation records | Root cause recorded for each finding, not just the correction. Two findings, SAR-006 and SAR-013, share a root cause of controls performed without leaving a record, which was addressed as a pattern | Conformant |
| 8.8 / A | Is technical vulnerability management effective? | July 2026 scan reports; POA-011, POA-012 | **Minor nonconformity.** Two instances were outside scan scope and the dependency scanner resolved direct dependencies only, which allowed a 10.0 base score vulnerability to remain undetected in a transitive dependency | Minor nonconformity |
| 8.16 / A | Is monitoring evidenced at the defined frequency? | Weekly review records, July 2026 | **Minor nonconformity.** Two of four weekly correlated privileged activity reviews were evidenced. Tracked as POA-004 with automation due 31 August 2026 | Minor nonconformity |
| 5.21 / A | Is ICT supply chain security managed under an approved process? | Draft supply chain procedure | **Minor nonconformity.** The procedure remains in draft and unapproved. Tracked as risk R-06 and POA-006 | Minor nonconformity |
| 5.29 / A | Is continuity capability verified rather than assumed? | Continuity plan v2.0; backup records | **Observation.** Backups run and replicate. No functional restore has ever been performed, so the four hour recovery objective is unverified. Not raised as a nonconformity because the control is documented and a test is scheduled | Observation |

## A2: Audit summary

| Result | Count |
|---|---|
| Conformant | 19 |
| Minor nonconformity | 3 |
| Observation | 1 |
| **Total questions** | **23** |

| Measure | Result |
|---|---|
| Major nonconformities | 0 |
| Minor nonconformities | 3 |
| Observations | 1 |
| Recommendation | The ISMS is operating as documented. No major nonconformity. Suitable for progression toward certification once the three minor nonconformities are closed |

## A3: What the auditor checked rather than accepted

Three verifications are recorded explicitly, because in each case the auditor recounted
a number rather than reading a summary. This is the difference between an audit and a
review of paperwork.

1. **The Statement of Applicability was recounted row by row.** Applicability values
   across all 93 rows were tallied independently and compared against the
   summary table. They matched: 89 applicable, 4 excluded. An SoA whose summary
   does not reconcile with its own rows is the most common defect in this document type,
   and it is detectable in under a minute, so it is checked first.
2. **The risk register was re-sorted independently.** The treatment plan claims to treat
   the five highest residual risks. The auditor sorted the twelve register rows by
   residual score and confirmed the five treated are genuinely ranks 1 to 5, with no tie
   across the boundary. Selecting the first five rows and describing them as the highest
   five is a common substitution and it is trivially checkable.
3. **POA&M movement arithmetic was verified.** Opening balance 10, closed
   4, new 2, closing
   balance 8. The
   arithmetic reconciles.

## A4: Nonconformities and corrective action

| Ref | Nonconformity | Clause / control | Root cause | Corrective action | Owner | Due |
|---|---|---|---|---|---|---|
| NC-01 | A 10.0 base score vulnerability remained undetected in a transitive dependency, and two instances were outside scan scope | A 8.8 | Two distinct causes: the dependency scanner was configured for direct dependencies only, and scan scope was maintained manually rather than bound to the inventory | Reconfigure the scanner to resolve the full dependency tree; bind scan targets to the component inventory; produce a software bill of materials per build | Priya N. Raghunathan | 2026-08-30 |
| NC-02 | Weekly correlated privileged activity review evidenced for 2 of 4 weeks | A 8.16 | The review was performed from a live dashboard, so a week with no anomaly produced no artifact and was indistinguishable from a week with no review | Automated weekly report generated on a schedule, recording queries run, period, reviewer, volume examined, and an explicit no anomalies identified statement where that is the outcome | Derrick A. Whitmore | 2026-08-31 |
| NC-03 | ICT supply chain procedure remains in draft and unapproved | A 5.21 | No owner was assigned to obtain approval after the draft was produced, so it stalled at 90 percent complete | Finalise and obtain System Owner approval; brief the development team; add the approval to the ISMS document register with a review date | Nkeiru Sarah Adesida | 2026-08-31 |

### On the root cause of NC-02

NC-02 and assessment finding SAR-013, the missing separation checklists, have the same
root cause: a control performed by a person without a system forcing an artifact leaves
no artifact when nothing interesting happens. Treating them as two unrelated paperwork
lapses would produce two reminders and no change. Treating them as one pattern produces
the correct fix, which is automating the artifact. The auditor recorded this as the most
useful finding of the audit even though neither individual item is severe.

---

# PART B: MANAGEMENT REVIEW

Held 9 July 2026. This record was written on the day of the meeting.

**A note on dates, deliberately.** This record covers only what was known on 9 July
2026. It does not report the July closure of POA-001, which happened on 24 July, and it
does not report the July monthly figures, because the period had not closed. A
management review that minutes events occurring after its own meeting date is a
document nobody checked, and it is one of the easiest defects for a reader to spot.

## B1: Attendance

| Role | Name | Present |
|---|---|---|
| Authorizing Official | Patricia L. Ambrose | Yes, chair |
| Chief Information Security Officer | Daniel K. Osei | Yes |
| System Owner | Marcus T. Delacroix | Yes |
| Information System Security Officer | Nkeiru Sarah Adesida | Yes, presenting |
| Senior Agency Official for Privacy | Helen M. Barragan | Yes |
| Security Operations Manager | Derrick A. Whitmore | Yes |
| Cloud Operations Lead | Samuel P. Hargrave | Apologies, represented by the System Owner |

The Senior Agency Official for Privacy attended. Clause 9.3 inputs include compliance
obligations, and for a system holding information on individuals under the Privacy Act
the privacy function has to be in the room rather than consulted afterwards.

## B2: Clause 9.3 inputs

| Required input | What was presented |
|---|---|
| Status of actions from previous management reviews | None. This is the first management review of this ISMS |
| Changes in external and internal issues | Reviewer population confirmed stable at 65. No change to the interconnections. Cloud provider certification confirmed current |
| Changes in interested party needs | The AO restated the condition attached to the authorisation: SAR-001 closed by 31 July 2026 |
| Performance and effectiveness: nonconformities | Three minor nonconformities from the June internal audit, no major. All three with owners and dates |
| Performance and effectiveness: monitoring results | Ten POA&M items open at authorisation. As at 9 July, two closed, POA-002 on 26 June and POA-008 on 15 July is not yet due. Reported as two closed and eight open at the meeting date |
| Performance and effectiveness: audit results | Internal audit June 2026, independent assessment March 2026 |
| Performance and effectiveness: objectives | Six objectives. Four on track, two at risk: evidence of the weekly review, and inventory accuracy |
| Feedback from interested parties | No applicant or grantee complaints relating to security or privacy in the period |
| Results of risk assessment and treatment status | Twelve risks. Five under active treatment, seven retained within tolerance. No risk above the Moderate band at residual |
| Opportunities for continual improvement | Bind scan scope to inventory; automate evidence generation rather than reminding people to produce it; consider just in time privileged access |

## B3: Discussion recorded

**On the one open High risk item.** The ISSO reported the reviewer portal federation on
track for July, with the identity provider licences procured on 5 June and a pilot
completed with eight reviewers on 26 June. The AO stated that the condition stands and
that no further extension would be granted.

**On the evidence nonconformity.** The CISO argued NC-02 should be treated as more
significant than a minor nonconformity, on the grounds that an unevidenced monitoring
control is the control the agency would most need after an incident. The AO agreed with
the reasoning, and accepted the auditor's classification on the basis that the control
does appear to be performed and the corrective action is already scoped. Recorded
because the disagreement is part of the record.

**On the reconciliation dependency.** The AO asked whether anyone outside the security
function understood that the system's integrity categorisation depends on the daily
payment reconciliation. The System Owner confirmed it is recorded in the System Security
Plan and in the change control checklist. The AO directed that the finance function be
briefed as well, since they operate the reconciliation and could change its cadence for
reasons that have nothing to do with security.

**On the restore test.** The System Owner reported difficulty securing an outage window
before the September award cycle. The AO declined to accept a tabletop as a substitute.

## B4: Decisions

| # | Decision | Owner | Due |
|---|---|---|---|
| 1 | The authorisation condition on SAR-001 stands. Closure by 31 July 2026, no extension | Samuel P. Hargrave | 2026-07-31 |
| 2 | All three minor nonconformities closed by 31 August 2026 | Nkeiru Sarah Adesida | 2026-08-31 |
| 3 | Brief the finance function on the reconciliation control dependency and add it to their change checklist | Marcus T. Delacroix | 2026-07-31 |
| 4 | Functional restore test scheduled and confirmed. A tabletop is not an acceptable substitute | Marcus T. Delacroix | 2026-09-15 |
| 5 | Bind vulnerability scan scope to the component inventory rather than maintaining it manually | Samuel P. Hargrave | 2026-08-14 |
| 6 | Produce a software bill of materials on every build | Priya N. Raghunathan | 2026-09-30 |
| 7 | Bring a just in time privileged access proposal with costs to the next review | Samuel P. Hargrave | 2026-10-08 |
| 8 | ISMS scope, policy and risk tolerance confirmed unchanged and remain adequate | Patricia L. Ambrose | Noted |

## B5: Resources

No additional funding requested. Two items carry cost beyond existing budget and were
noted for the next planning cycle: behavioural analytics licensing under risk R-04, and
an independent application penetration test under risk R-02.

## B6: Next review

**8 October 2026**, quarterly cadence.

---

## Continual improvement, Clause 10

| Improvement | Triggered by | Beyond the minimum required? |
|---|---|---|
| Continuous configuration compliance evaluation | Assessment finding SAR-005 | Yes. The finding required the four drifted instances be corrected. The agency added automated detection so the condition cannot recur undetected |
| Allow list input validation plus output encoding | Assessment finding SAR-002 | Yes. Either layer alone would have satisfied the finding. Both were implemented because either alone is a single point of failure |
| Reviewer account expiry set at creation | Readiness gap R-01 | Yes. Not required by any finding. Added because a reviewer account outliving its panel was the most likely stale account on the system |
| Automated evidence generation for monitoring | Audit nonconformity NC-02 | Yes. Addresses the root cause pattern shared with SAR-013 rather than the individual lapse |
| Scan scope bound to inventory | Audit nonconformity NC-01 | Yes. Removes the manual step rather than adding a reminder to perform it |


---

**Navigation:** [<- ISO-04: Risk Treatment Plan](../iso-04-risk-treatment/README.md) &nbsp;|&nbsp; [Repository home](../README.md) &nbsp;|&nbsp; [ISO-06: NIST to ISO Framework Crosswalk ->](../iso-06-crosswalk/README.md)

---

*Author: Nkeiru Sarah Adesida, Information System Security Officer (ISSO), portfolio scenario*  
*Simulated system: Keystone Grants Management System (KGMS) | FWDA-KGMS-2026-MOD*  
*This document is a portfolio exercise built on a fictional organisation. It is not a government record.*  
*[GitHub portfolio](https://github.com/Nkee07) | [LinkedIn](https://www.linkedin.com/in/nkeiru-adesida-grc)*
