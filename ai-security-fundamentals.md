# AI Security Fundamentals

## 1. Introduction

Artificial Intelligence (AI) enables computer systems to perform tasks such as classification, prediction, language processing, and content generation.

AI security focuses on protecting AI systems, their data, models, and users from attacks, misuse, and unintended behavior.

## 2. Common AI Security Risks

- **Prompt injection:** Untrusted input attempts to manipulate an AI system into ignoring its intended instructions or performing unintended actions.
- **Sensitive data exposure:** Private information may be disclosed through prompts, outputs, logs, or improperly configured systems.
- **Data poisoning:** Training or feedback data is manipulated to influence model behavior.
- **Model theft:** An attacker attempts to reproduce or obtain a model through unauthorized access or excessive querying.
- **Insecure output handling:** AI-generated output is trusted or executed without appropriate validation.
- **Excessive agency:** An AI system is given more permissions or autonomy than its task requires.
- **Supply-chain risks:** Compromised models, datasets, libraries, or other dependencies introduce security problems.

## 3. Prompt Injection

Prompt injection occurs when instructions embedded in user input or external content attempt to influence an AI system in unintended ways.

Potential consequences include inappropriate data disclosure, misuse of connected tools, or violations of application rules.

### Defensive Practices

- Treat user input and retrieved content as untrusted.
- Keep system instructions separate from untrusted data where possible.
- Do not rely on prompts alone to enforce access control.
- Restrict tool permissions and available actions.
- Require authorization checks before sensitive operations.
- Test applications against direct and indirect prompt-injection attempts.

## 4. Data Privacy

AI systems may process personal, confidential, or business-sensitive information.

Security practices include:

- Collect only the data necessary for the task.
- Avoid submitting secrets or confidential information to unapproved services.
- Restrict access to datasets and logs.
- Apply appropriate retention and deletion policies.
- Protect data during storage and transmission.
- Review what information may appear in model outputs.

## 5. AI Model Security

AI models can be exposed to attacks involving training data, model behavior, inference interfaces, and dependencies.

Important controls include:

- Protect model files and access credentials.
- Validate and document data sources.
- Monitor model endpoints for unusual usage.
- Apply rate limits and access controls.
- Keep dependencies updated.
- Evaluate models before deployment and after significant changes.

## 6. Secure AI Application Design

AI applications should use the same foundational security principles as other software systems.

- **Least privilege:** Give models and tools only the permissions they need.
- **Input validation:** Check input formats and enforce limits.
- **Output validation:** Treat generated output as untrusted until checked.
- **Human oversight:** Require appropriate review for high-impact actions.
- **Logging and monitoring:** Record relevant events while protecting sensitive data.
- **Defense in depth:** Use multiple complementary security controls.

## 7. AI Security Testing

Authorized AI security testing can examine:

- Resistance to prompt injection.
- Protection of sensitive information.
- Access-control enforcement.
- Unsafe tool execution.
- Output validation.
- Reliability under unexpected inputs.
- Monitoring and incident-response readiness.

Testing should use controlled environments and clearly defined permissions.

## 8. AI Security vs. Traditional Cybersecurity

Traditional cybersecurity protects systems, networks, applications, and data.

AI security also considers model-specific risks, including prompt injection, training-data manipulation, model behavior, and interactions between AI systems and external tools.

Both areas rely on secure design, access controls, monitoring, testing, and incident response.

## 9. Safe Practical Exercise

Use a local or authorized AI application with non-sensitive test data.

1. Create a harmless test prompt.
2. Observe how the application handles unexpected or conflicting instructions.
3. Check whether its access controls remain effective.
4. Verify that generated output is validated before sensitive actions.
5. Record observations and identify possible defensive improvements.

Do not test systems or attempt to access data without authorization.

## 10. Key Takeaways

- AI systems introduce security risks involving models, data, prompts, and connected tools.
- Prompt injection can influence model behavior but should not bypass properly enforced authorization controls.
- Sensitive information must be protected throughout its lifecycle.
- AI-generated output should not automatically be treated as safe.
- Least privilege, monitoring, testing, and human oversight are important defensive measures.
- AI security complements rather than replaces traditional cybersecurity.

## Learning Progress

**Status:** AI security fundamentals notes drafted.

**Next goal:** Practice evaluating an authorized AI application and document the risks, evidence, and mitigations.

---

*Original educational study notes. This document is not a walkthrough of a specific TryHackMe room.*
