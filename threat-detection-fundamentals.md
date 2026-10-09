# Threat Detection Fundamentals

## 1. Introduction

Threat detection is the process of identifying activity that may indicate a cybersecurity threat. Security analysts examine system events, network traffic, logs, and alerts to identify suspicious behavior.

The goal is to detect potential threats early, investigate the evidence, and support an appropriate response.

## 2. What Is a Cybersecurity Threat?

A cybersecurity threat is a potential cause of harm to systems, networks, applications, or data.

Examples include:

- Unauthorized access
- Malware activity
- Credential theft
- Data exfiltration
- Exploitation of software vulnerabilities
- Denial-of-service activity

## 3. Threat Detection vs. Threat Prevention

- **Threat detection:** Identifies suspicious or malicious activity.
- **Threat prevention:** Uses controls to stop or reduce the likelihood of an attack.
- **Incident response:** Investigates and manages a security incident.

These functions work together but have different objectives.

## 4. Common Detection Methods

### Signature-Based Detection

Identifies activity matching known patterns, rules, or indicators.

**Advantage:** Effective for recognized threats.

**Limitation:** May miss new threats or attacks that change their patterns.

### Anomaly-Based Detection

Identifies activity that differs from an established baseline.

**Advantage:** Can reveal previously unknown or unusual behavior.

**Limitation:** Legitimate changes can trigger false positives.

### Behavior-Based Detection

Examines actions and sequences of events to identify suspicious behavior.

For example, an unexpected privilege change followed by unusual access to sensitive files may warrant investigation.

### Rule-Based Detection

Uses defined conditions to generate alerts when particular events or combinations of events occur.

Rules need regular review to maintain accuracy and relevance.

## 5. Indicators of Compromise

An Indicator of Compromise (IOC) is an observable artifact that may suggest a system has been compromised.

Examples include:

- A known malicious IP address
- A suspicious domain
- A file hash associated with known malware
- An unexpected persistence mechanism
- An unusual process or connection

An IOC is evidence to investigate, not automatic proof of malicious activity. Context and validation are important.

## 6. The Security Operations Center

A Security Operations Center (SOC) monitors systems and investigates potential security incidents.

Typical SOC activities include:

1. Monitoring alerts.
2. Reviewing logs and supporting evidence.
3. Prioritizing alerts based on risk.
4. Investigating suspicious activity.
5. Escalating confirmed or high-risk incidents.
6. Documenting findings and supporting response actions.

## 7. False Positives and False Negatives

- **False positive:** Benign activity is incorrectly identified as malicious.
- **False negative:** Malicious activity is not detected.

Effective detection requires balancing coverage, alert quality, and investigation workload.

## 8. Detection and Response Workflow

A typical workflow is:

1. Collect telemetry from relevant systems.
2. Analyze events using rules or behavioral techniques.
3. Generate an alert when detection criteria are met.
4. Validate the alert using additional evidence.
5. Assess severity and potential impact.
6. Escalate or respond according to approved procedures.
7. Document the investigation and improve detection rules.

Automated response actions should have safeguards, logging, and a way to review unintended consequences.

## 9. Threat Intelligence

Cyber Threat Intelligence (CTI) is analyzed information about threats, threat actors, their capabilities, and their observed activities.

CTI can help analysts understand the significance of alerts and prioritize investigations.

Useful concepts include:

- **IOC:** An observable artifact associated with possible malicious activity.
- **TTPs:** Tactics, techniques, and procedures used by threat actors.
- **Context:** Information that helps determine whether an indicator is relevant to an environment.
- **Enrichment:** Adding useful information to an event or indicator to support investigation.

## 10. Safe Practical Exercise

Use a sample log file you created yourself or an authorized training dataset.

1. Identify unusual login failures.
2. Compare the timestamps and source information available.
3. Determine whether related events provide additional context.
4. Record a hypothesis and the evidence supporting it.
5. Explain what additional evidence would be needed before confirming a threat.

Do not label an event malicious based on a single indicator without adequate context.

## 11. Key Takeaways

- Threat detection identifies potentially malicious activity.
- Signature-based, anomaly-based, behavior-based, and rule-based methods have different strengths.
- IOCs support investigation but require context.
- SOC analysts validate, prioritize, investigate, and document alerts.
- False positives and false negatives affect detection quality.
- Threat intelligence provides context for interpreting security events.
- Automated responses should be tested and controlled.

## Learning Progress

**Status:** Threat detection fundamentals notes drafted.

**Next goal:** Practice investigating sample alerts and document the evidence, reasoning, and conclusions.

---

*Original educational study notes. This document is not a walkthrough of a specific TryHackMe room.*
