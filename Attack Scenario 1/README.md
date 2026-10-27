# Scenario 1 — Phishing an administrator

This is a **hypothetical attack path** from the Solaris Care Connect 360 workshop exercise. It is not a report of an incident or a validated exploit.

The attacker's objective is access to the application environment through a privileged user. The stages below are used to decide where controls and monitoring would matter.

## Attack sequence

1. **Reconnaissance:** identify staff with administrative access and gather public information about the application.
2. **Preparation:** draft a phishing message intended to make the recipient disclose credentials or run an attachment.
3. **Delivery:** send the message to a targeted user.
4. **Credential compromise:** if the user responds and the credentials are usable, the attacker may obtain a foothold. This step depends on factors such as MFA and device protections.
5. **Persistence and movement:** the attacker may attempt to retain access and reach systems holding sensitive data, subject to their actual permissions.
6. **Impact:** possible outcomes include unauthorized access to patient records or service disruption.

The important questions for the exercise are where MFA, conditional access, monitoring, segmentation and review could interrupt the sequence. A successful compromise is **not assumed** simply because the message was delivered.

## Diagram from the training exercise

```mermaid
flowchart LR


    A[GitHub Repos] --> B{CI/CD Pipeline GH Actions}
    A[Reconnaissance] -->|Identify target| B
    B[Reconnaissance] -->|Gather information| B
    B[Weaponization] -->|Craft malicious payload| D
    D[Delivery] -->|Send phishing email| D
    D[Delivery] -->|Trick user to download payload| D
    D[Exploitation] -->|Execute payload| D
    D[Exploitation] -->|Gain access to web server| H
    H[Installation] -->|Install backdoor| H
    H[Installation] -->|Establish persistence| H
    H[Command and Control] -->|Communicate with C&C server| H
    H[Command and Control] -->|Issue commands| L
    H[Actions on Objectives] -->|Steal sensitive data| M

