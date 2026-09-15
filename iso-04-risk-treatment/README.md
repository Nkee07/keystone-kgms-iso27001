# ISO-04: Risk Treatment Plan
### Keystone Grants Management System (KGMS) | The five highest residual risks, selected on a published rule

> ### PORTFOLIO EXERCISE, SIMULATED SYSTEM
> **Keystone Grants Management System (KGMS) does not exist.** The Federal Workforce Development Agency (FWDA) is a fictional federal
> agency invented for this portfolio. Every organisation, person, system
> identifier, network address, finding, date and signature on this page is
> fabricated for training purposes, with one exception: the author, Nkeiru Sarah Adesida, is a real person. Where her name appears in a scenario role, that role is fictional, and she has never worked for this agency, which does not exist. Nothing here is drawn from any real
> employer, client or government system, and no real document, artifact or
> data has been reproduced. This file is coursework, not a government record.

---

**Document:** Risk Treatment Plan  
**Simulated system:** Keystone Grants Management System (KGMS) | `FWDA-KGMS-2026-MOD`  
**Framework and standards:** ISO/IEC 27001:2022 Clause 6.1.3, ISO/IEC 27005  
**Author:** Nkeiru Sarah Adesida  
**Document date:** 17 April 2026  
**Status:** Current. 5 of 12 risks under active treatment, 7 retained within tolerance

**Navigation:** [<- ISO-03: Information Security Risk Register](../iso-03-risk-register/README.md) &nbsp;|&nbsp; [Repository home](../README.md) &nbsp;|&nbsp; [ISO-05: Internal Audit and Management Review ->](../iso-05-audit-management-review/README.md)

---

## Purpose

A risk register lists problems. A risk treatment plan commits to doing something about
them, with names and dates.

Plain language version: the register is the diagnosis. This is the prescription: which
problems get worked on, what exactly gets done, who does it, by when, and how you will
know it worked.

---

## Section 1: Selection rule, stated before the selection

**The rule: this plan treats the five risks with the highest residual score.**

Residual, not inherent, because residual is what is actually still there after
everything already being done. Treating by inherent score sends effort at risks that
existing controls have already handled.

### The selection, shown so it can be checked

| Rank | ID | Residual | In this plan? |
|---|---|---|---|
| 1 | R-03 | 12 | **Yes** |
| 2 | R-06 | 12 | **Yes** |
| 3 | R-02 | 10 | **Yes** |
| 4 | R-04 | 10 | **Yes** |
| 5 | R-07 | 9 | **Yes** |
| 6 | R-01 | 8 | No |
| 7 | R-05 | 8 | No |
| 8 | R-08 | 6 | No |
| 9 | R-09 | 6 | No |
| 10 | R-10 | 6 | No |
| 11 | R-11 | 6 | No |
| 12 | R-12 | 4 | No |

Rank 5 scores 9. Rank 6 scores 8. No tie
crosses the cut, so the selection is unambiguous.

Note what this rule does **not** produce: it does not select R-01 through R-05 in
identifier order. R-01 and R-05 are not in this plan, despite low identifiers, because
their residual scores are 8 and
8, inside tolerance. R-06 and R-07 are
in it despite higher identifiers. Publishing the ranked list alongside the claim is the
only way a reader can tell the difference between a genuine top five and the first five
rows of a table, and that difference is exactly the kind of thing a reviewer checks.

### Treatment options used, per ISO/IEC 27005

| Option | Meaning | Used in this plan |
|---|---|---|
| Modify | Change the risk by adding or strengthening controls | Yes, all five |
| Retain | Accept the risk as within tolerance, with a documented decision | Yes, for the seven risks not in this plan |
| Avoid | Stop doing the activity that creates the risk | No |
| Share | Transfer or share the risk, for example through insurance or a supplier | Partly, through the cloud provider for physical and platform risk |

---

## Section 2: Treatment summary

| Risk | Title | Residual now | Band | Option | Owner | Target residual |
|---|---|---|---|---|---|---|
| R-03 | Exploitation of an unremediated software vulnerability in a syst... | 12 | Moderate | Modify | Samuel P. Hargrave | 9 (Moderate, at the lower edge) |
| R-06 | Compromise of a third party component introduced through the sof... | 12 | Moderate | Modify | Nkeiru Sarah Adesida | 8 (Low, within tolerance) |
| R-02 | Exploitation of an application input handling weakness to read o... | 10 | Moderate | Modify | Priya N. Raghunathan | 5 (Low, within tolerance) |
| R-04 | Misuse of privileged access by an authorised administrator | 10 | Moderate | Modify | Derrick A. Whitmore | 5 (Low, within tolerance) |
| R-07 | Extended service unavailability with an unverified recovery capa... | 9 | Moderate | Modify | Marcus T. Delacroix | 6 (Low, within tolerance) |

---

## Section 3: Treatment detail

### R-03: Exploitation of an unremediated software vulnerability in a system component or dependency

| Field | Detail |
|---|---|
| Risk owner | Samuel P. Hargrave |
| Inherent score | 16 (High) |
| Residual score now | 12 (Moderate) |
| Treatment option | Modify |
| Target residual score | 9 (Moderate, at the lower edge) |
| Estimated effort | Approximately 120 engineering hours, no new licence cost |

**Why this risk is being treated**

Residual score 12, the joint highest in the register, and the inherent to residual drop is only 16 to 12. Software vulnerabilities are the most frequently realised risk on this system: July 2026 scanning alone produced a 10.0 base score finding. Likelihood cannot realistically be reduced below possible, because new vulnerabilities are published continuously, so treatment targets the window of exposure rather than the event.

**Controls to implement**

| Control | What it does | Annex A reference | Owner | Target |
|---|---|---|---|---|
| Resolve the full dependency tree in scanning | Reconfigure the dependency scanner to resolve transitive dependencies, not direct ones only. This was the precise failure that let CVE-2021-44228 sit undetected in a bundled logging library inside a charting package. | 8.8 Management of technical vulnerabilities | Priya N. Raghunathan | 2026-08-30 |
| Close the scan scope gap | Bind the scan target group to the component inventory so a newly provisioned instance is added automatically rather than manually. | 8.8, 5.9 Inventory of information and other associated assets | Samuel P. Hargrave | 2026-08-14 |
| Reduce the patch window for internet reachable components | Move Critical and High remediation on internet reachable components from 30 days to 14 days. | 8.8 | Samuel P. Hargrave | 2026-09-30 |
| Automate image rebuild on base image update | Trigger a pipeline rebuild whenever the approved base image is updated, so instances do not drift behind the baseline between releases. | 8.9 Configuration management, 8.19 Installation of software on operational systems | Samuel P. Hargrave | 2026-10-31 |


### R-06: Compromise of a third party component introduced through the software supply chain

| Field | Detail |
|---|---|
| Risk owner | Nkeiru Sarah Adesida |
| Inherent score | 12 (Moderate) |
| Residual score now | 12 (Moderate) |
| Treatment option | Modify |
| Target residual score | 8 (Low, within tolerance) |
| Estimated effort | Approximately 90 engineering hours plus 20 ISSO hours |

**Why this risk is being treated**

Residual score 12, joint highest, and the only risk in the register where the residual equals the inherent: 12 to 12. The controls listed as in place, signed base images and checksum verification, address component authenticity but not the compromise of a legitimate dependency upstream, which is the actual threat. A supply chain procedure exists in draft and has not been approved, so there is no governed process at all. This is the weakest position of any risk here and it is first for that reason.

**Controls to implement**

| Control | What it does | Annex A reference | Owner | Target |
|---|---|---|---|---|
| Approve the supply chain risk management procedure | Finalise and obtain System Owner approval for the procedure covering base image provenance, dependency vetting and the criteria for accepting a new third party component. | 5.21 Managing information security in the ICT supply chain, 5.19 Information security in supplier relationships | Nkeiru Sarah Adesida | 2026-08-31 |
| Generate and retain a software bill of materials per build | Produce a complete component manifest on every build and retain it, so that when the next widely exploited dependency is published the question 'are we affected' is answered by query rather than by investigation. | 5.21, 5.9 | Priya N. Raghunathan | 2026-09-30 |
| Pin and verify dependencies | Pin dependency versions with integrity hashes so a compromised upstream release cannot be pulled silently into a build. | 5.21, 8.19 | Priya N. Raghunathan | 2026-09-30 |
| Vet the third party merit scoring library | Formal review of the one third party component that processes in-scope data, covering maintainer provenance, release signing and update cadence. Its removal is the alternative if the review is not satisfactory. | 5.21, 5.20 Addressing information security within supplier agreements | Nkeiru Sarah Adesida | 2026-10-31 |


### R-02: Exploitation of an application input handling weakness to read or alter grant records

| Field | Detail |
|---|---|
| Risk owner | Priya N. Raghunathan |
| Inherent score | 20 (High) |
| Residual score now | 10 (Moderate) |
| Treatment option | Modify |
| Target residual score | 5 (Low, within tolerance) |
| Estimated effort | Approximately 60 engineering hours plus an estimated independent test engagement |

**Why this risk is being treated**

Residual score 10. Impact is the maximum, 5, because this risk reaches grant records directly, and the threat population is anyone on the internet who can start an application. The assessment demonstrated the risk was real rather than theoretical: a stored cross site scripting payload executed in a reviewer's browser. That has been remediated, which is why likelihood is now 2, but a single application layer weakness remains the shortest path to the data.

**Controls to implement**

| Control | What it does | Annex A reference | Owner | Target |
|---|---|---|---|---|
| Annual penetration test by an independent tester | Move from assessment only testing to an annual dedicated application penetration test, with the scope explicitly including all 31 input fields and the file upload path. | 8.29 Security testing in development and acceptance | Nkeiru Sarah Adesida | 2026-11-30 |
| Add interactive application security testing to the pipeline | Automated security testing in the build pipeline so an injection regression fails the build rather than reaching production. | 8.28 Secure coding, 8.29 | Priya N. Raghunathan | 2026-10-31 |
| Tune web application firewall rules to the application | Replace the generic managed rule set with rules tuned to the application's own routes and parameter shapes, and enable blocking rather than counting. | 8.20 Networks security, 8.26 Application security requirements | Samuel P. Hargrave | 2026-09-30 |


### R-04: Misuse of privileged access by an authorised administrator

| Field | Detail |
|---|---|
| Risk owner | Derrick A. Whitmore |
| Inherent score | 15 (Moderate-High) |
| Residual score now | 10 (Moderate) |
| Treatment option | Modify |
| Target residual score | 5 (Low, within tolerance) |
| Estimated effort | Approximately 160 engineering hours plus analytics licensing |

**Why this risk is being treated**

Residual score 10. Impact is the maximum, 5, because a privileged administrator can reach every record and can also alter the audit trail that would evidence it. Likelihood is already low at 2, given a population of 16 accounts under quarterly full population review with session recording. Treatment therefore targets detection and the integrity of the record rather than further restricting access, which is already tight.

**Controls to implement**

| Control | What it does | Annex A reference | Owner | Target |
|---|---|---|---|---|
| Implement behavioural analytics on privileged activity | Baseline normal privileged behaviour and alert on deviation: access from a new location, activity outside working hours, bulk record retrieval, or one administrator acting across all three planes in a single session. | 8.16 Monitoring activities, 8.15 Logging | Derrick A. Whitmore | 2026-11-30 |
| Move to just in time privileged access | Replace standing group membership with time bound elevation requested per task, so the standing privileged population approaches zero between tasks. | 8.2 Privileged access rights, 5.18 Access rights | Samuel P. Hargrave | 2026-12-31 |
| Write audit records to append only storage | Ship audit records to storage an administrator cannot alter or delete, so the record survives the administrator. | 8.15, 5.33 Protection of records | Derrick A. Whitmore | 2026-10-31 |
| Complete the weekly correlated review automation | Close the evidence gap that is also tracked as POA-004, so the detective control produces an artifact whether or not anything is found. | 8.16 | Derrick A. Whitmore | 2026-08-31 |


### R-07: Extended service unavailability with an unverified recovery capability

| Field | Detail |
|---|---|
| Risk owner | Marcus T. Delacroix |
| Inherent score | 12 (Moderate) |
| Residual score now | 9 (Moderate) |
| Treatment option | Modify |
| Target residual score | 6 (Low, within tolerance) |
| Estimated effort | Approximately 40 engineering hours plus one scheduled outage window |

**Why this risk is being treated**

Residual score 9, the lowest of the five treated and still in the Moderate band. The inherent to residual drop, 12 to 9, is small, and the reason is specific: the backups exist and are replicated, but nobody has ever restored from them. An untested backup is a belief, not a control. The documented four hour recovery time objective is currently unverified.

**Controls to implement**

| Control | What it does | Annex A reference | Owner | Target |
|---|---|---|---|---|
| Perform a functional restore test of the database tier | Restore from backup into an isolated subnet, verify data integrity against a known checkpoint, and measure the actual elapsed time against the four hour objective. This is also tracked as POA-005. | 5.29 Information security during disruption, 8.13 Information backup | Marcus T. Delacroix | 2026-09-15 |
| Publish the measured recovery time | Replace the stated objective with the measured result, or revise the objective if the measurement does not support it. A recovery time objective nobody has measured should not be published as a commitment. | 5.30 ICT readiness for business continuity | Marcus T. Delacroix | 2026-09-30 |
| Schedule the restore test annually with automated verification | Make the test recurring rather than a one off, with automated integrity verification so the cost of repeating it is low enough that it actually gets repeated. | 5.29, 8.13 | Samuel P. Hargrave | 2026-10-31 |


---

## Section 4: Timeline

| Target date | Actions due |
|---|---|
| 2026-08-14 | 1 |
| 2026-08-30 | 1 |
| 2026-08-31 | 2 |
| 2026-09-15 | 1 |
| 2026-09-30 | 5 |
| 2026-10-31 | 5 |
| 2026-11-30 | 2 |
| 2026-12-31 | 1 |

Earliest commitment 14 August 2026, latest 31 December 2026. Three actions fall in
August, which is deliberate: they are the ones that also appear as open items in the
federal POA&M, so the two frameworks share a deadline rather than setting two.

---

## Section 5: Success criteria

Treatment is complete when the evidence exists, not when the work is believed done.

| Risk | Success criterion | Evidence required |
|---|---|---|
| R-03 | Scanner resolves transitive dependencies and scan scope matches inventory | A scan report demonstrating detection of a known transitive vulnerability in a test build, plus a report showing scan targets equal to inventory with no gap |
| R-06 | Approved supply chain procedure and a software bill of materials per build | Signed procedure, and the component manifest from three consecutive builds |
| R-02 | Independent penetration test with no High or Critical findings in the application layer | Penetration test report, and pipeline configuration showing the security test as a blocking gate |
| R-04 | Behavioural alerting live, standing privileged population reduced, audit records immutable | Alert configuration and one triaged true positive or tuned false positive, elevation records showing time bound access, and storage policy showing append only |
| R-07 | Measured recovery time published, and it meets or revises the objective | Restore test after action report with the elapsed time, and an integrity verification result against a known checkpoint |

### The line that matters

For R-07 the criterion is that the measured recovery time is published **or the
objective is revised**. If the restore takes six hours against a four hour objective,
the honest outcome is a revised objective, not a quietly repeated test until a good
number appears. A treatment plan that only permits the flattering result is not a plan.

---

## Section 6: Residual position after treatment

|  | Now | Projected after treatment |
|---|---|---|
| Risks in the Moderate band | 5 | 1 |
| Risks in the Low band | 7 | 11 |
| Risks above the Moderate band | 0 | 0 |

Projected, not achieved. R-03 is expected to remain at the lower edge of the Moderate
band even after treatment, because the likelihood of a new software vulnerability being
published cannot be driven below possible. Claiming it will reach Low would be claiming
that this system will stop having dependencies.

Approved by Marcus T. Delacroix, System Owner, and noted by Patricia L. Ambrose, Authorizing Official, on
17 April 2026.

---

**Navigation:** [<- ISO-03: Information Security Risk Register](../iso-03-risk-register/README.md) &nbsp;|&nbsp; [Repository home](../README.md) &nbsp;|&nbsp; [ISO-05: Internal Audit and Management Review ->](../iso-05-audit-management-review/README.md)

---

*Author: Nkeiru Sarah Adesida, Information System Security Officer (ISSO), portfolio scenario*  
*Simulated system: Keystone Grants Management System (KGMS) | FWDA-KGMS-2026-MOD*  
*This document is a portfolio exercise built on a fictional organisation. It is not a government record.*  
*[GitHub portfolio](https://github.com/Nkee07) | [LinkedIn](https://www.linkedin.com/in/nkeiru-adesida-grc)*
