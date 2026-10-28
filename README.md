# Threat-modelling workshop exercise

This repository contains my notes and diagrams from a DevSecOps training exercise. The case study uses a **fictional healthcare application**, Solaris Care Connect 360, to work through possible attack paths and control gaps.

The exercise came from a [DevSecOps bootcamp workshop](https://cyberagoge.thinkific.com/courses/take/devsecops-bootcamp/texts/55130887-part-1-introduction-to-the-course). It should not be read as an assessment of a real client system or as a claim that I led a commercial threat-modelling engagement.

## Scenario

The workshop material covers four threats:

1. Phishing an administrator for access to the application environment.
2. Attacking machine processes and the data lake.
3. SQL injection against a public-facing component.
4. An insider accessing sensitive algorithms.

The exercises combine STRIDE, MITRE ATT&CK and attack-sequence diagrams to identify missing controls and discuss risk. The source scenario reports four high risks and one medium risk; those are **exercise ratings**, not measured findings from a production environment.

## Controls considered

- MFA and least-privilege access for administrators.
- Regular patching and application security testing.
- Phishing awareness and secure credential handling.
- Restricted network access, logging and event review.
- Role-based access to sensitive healthcare records.
- WAF rules as one layer of protection, not a replacement for application fixes.

## What's in this repo

- `Application Summary/` — application diagrams and initial risk notes.
- `Attack Scenario 1/` — phishing scenario, attack flow and STRIDE worksheet.
- `Attack Scenario 2–4/` — placeholders for the remaining workshop scenarios.
- `Risks Summary.md` — scenario risk summary.

These are learning artifacts. Any templates or scenario material drawn from the workshop remain attributable to the course; the notes here should not be reused as a finished assessment without validating the application and assumptions.

# Threat Modelling Process Summary

```mermaid
mindmap
  root((Attack Begins))
    STRIDE/MITRE ATT&CK/Kill Chain
      Conduct Inherent Risk Assesment
      ::icon(fa fa-book)
      Create Critical Asset List
        Schedule and Scope Threat Modelling Workshop
    Controls Required
      Risks<br/>Mitigations
      Risk Summary
        Redmeiation workflow
            Slack
            JIRA 
    Attack Scenarios
      Attack 1
      Attack 2
      Attack 3
      Attack 4

