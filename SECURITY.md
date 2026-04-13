# Security Policy

## Scope

This repository contains the **A2A Commerce Specification** — a set of documents, not executable code. As such, the notion of "security vulnerabilities" is different from a typical software project.

We welcome reports in the following categories:

### ✅ What to Report

- **Security-relevant errors in the specification itself**
  — e.g., protocol flows that enable replay attacks, authentication patterns that weaken trust, economic incentive structures that reward malicious agents
- **Trust, safety, and privacy concerns** in the normative text
  — e.g., patterns that could leak Principal information to unintended parties
- **Threat models** we may have missed
  — scenarios where a compliant A2A Commerce implementation could be exploited by a sophisticated attacker

### ❌ Not in Scope Here

The following should **not** be reported via this channel:

- Bugs in implementations (those belong to the implementation project)
- Vulnerabilities in AgentShow's own platform (report to [agentshow.shop](https://agentshow.shop))
- Vulnerabilities in third-party agent frameworks (Google A2A, MCP, etc.) — report to those upstream projects
- General questions about security → use [GitHub Discussions](../../discussions)

## Reporting a Vulnerability

If you believe you have found a security-relevant flaw in the A2A Commerce Specification, please report it privately **before** opening a public issue.

**Contact**: security@agentshow.shop

**Please include**:

- A clear description of the issue and why it is security-relevant
- The specific section(s) of the specification affected
- A proposed mitigation or fix, if you have one
- Your name and affiliation (optional, for acknowledgment)

**What to expect**:

- We aim to respond within **5 business days**
- We will work with you to understand and validate the report
- If the issue is confirmed, we will plan a correction and coordinate disclosure
- If the issue is out of scope, we will explain why and suggest where to report it instead

## Disclosure Timeline

For confirmed security-relevant issues in the specification:

1. **Day 0**: Report received, acknowledgment sent
2. **Day 0–14**: Triage, investigation, validation
3. **Day 14–30**: Fix developed, reviewed, and prepared for publication
4. **Day 30**: Fix published in a new spec version (e.g., v1.0.1) with attribution

This timeline is a goal, not a guarantee. Severe issues may be handled faster; complex issues may require more time.

## Acknowledgment

We gratefully acknowledge security researchers who report issues in good faith. Reporters will be credited in the spec CHANGELOG (unless they prefer to remain anonymous).

## Safe Harbor

We consider security research conducted according to this policy to be:

- Authorized in view of any applicable anti-circumvention laws
- Exempt from restrictions in our terms of service that would interfere with good-faith security research
- Lawful, helpful to the overall security of the open internet, and conducted in good faith

We will not pursue legal action against researchers who report in good faith and within the scope described here.

## Questions

If you are unsure whether something qualifies as a security issue, err on the side of caution and send an email. We would rather receive a non-issue than miss a real one.
