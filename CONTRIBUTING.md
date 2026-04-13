# Contributing to A2A Commerce Specification

Thank you for your interest in contributing to the **A2A Commerce Specification**. This document explains how you can help improve the spec, what kinds of contributions we welcome, and the process we follow.

## What This Repository Is

This repository hosts the **A2A Commerce Specification** — an open, vendor-neutral definition of the fifth paradigm of electronic commerce. It is authored by [AgentShow](https://agentshow.shop) and released under the [CC BY 4.0](./LICENSE) license.

**This is a specification project, not a code project.** We do not accept implementation code in this repository. However, we welcome references to implementations you build elsewhere.

## Ways to Contribute

### 📝 Editorial Improvements (low barrier, always welcome)

- Fix typos, grammar, or unclear phrasing
- Improve cross-references and citations
- Clarify definitions and examples
- Translate the spec or README into additional languages

**Process**: Open a pull request directly. For translations, create a new file named `SPEC.{lang-code}.md` (e.g. `SPEC.fr.md` for French).

### 💡 Substantive Proposals (structured review)

- Propose new principles or properties
- Argue for changes to existing definitions
- Suggest additions to the ACML (AI Commerce Maturity Ladder)
- Propose extensions to the negotiation protocol

**Process**:
1. Open an **issue** first using the "Specification Proposal" template
2. Describe the problem you see and your proposed change
3. Wait for discussion and maintainer response before opening a PR
4. If accepted in principle, open a PR referencing the issue

Proposals that would materially change the spec require consensus from the maintainers and will be tracked in a future version (v1.1, v2.0, etc.), not merged into v1.0.

### 🌍 Implementation Reports

If you are building something that implements A2A Commerce concepts, we'd love to hear about it.

- Open a **Discussion** under the "Show and Tell" category
- Share what you built, which ACML level you target, and any lessons learned
- Implementation references help the specification evolve with real-world feedback

### 🐞 Reporting Issues

- **Errors in the spec** (factual, logical, editorial): Use "Specification Error" issue template
- **Questions about the spec**: Use GitHub Discussions, not issues
- **Security issues**: See [SECURITY.md](./SECURITY.md)

## What We Don't Accept

- **Implementation code** — this is a spec repo, implementations belong in separate projects
- **Vendor-specific extensions** — the spec must remain neutral across agent providers
- **Commercial terms, pricing, or negotiation algorithms** — these are intentionally outside the spec
- **Changes that dilute the three essential properties** (Agent-Native, Bilateral Autonomy, Delegated Authority)
- **Promotional content** for unrelated projects or services

## Specification Style Guide

When writing or editing spec content:

- **Normative language**: use MUST / SHOULD / MAY per [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119)
- **Defined terms**: capitalize on first use (e.g., Buyer Agent, Seller Agent, Principal)
- **Examples**: use code blocks with `json`, `http`, or `yaml` language hints
- **References to other sections**: use relative links `[Section Name](#section-anchor)`
- **External references**: prefer permanent links (DOI, arXiv, IETF RFCs) over blog posts

## Pull Request Process

1. Fork the repository and create a feature branch from `main`
2. Make your changes, keeping commits focused and well-described
3. Ensure Markdown renders correctly (use a preview tool)
4. Open a PR filling out the PR template
5. Reference any related issues or discussions
6. Respond to review feedback promptly

PRs for editorial fixes (typos, grammar) are typically merged within a few days. Substantive proposals go through longer review.

## Governance

The A2A Commerce Specification is currently stewarded by **AgentShow** as the sole maintainer. This is a deliberate choice for v1.0 to preserve coherence during the initial definition phase.

We plan to transition to a broader governance model as the community grows. The intended path is:

1. **v1.x (now)**: Single-steward maintenance by AgentShow
2. **v2.x**: Multi-maintainer working group with invited external contributors
3. **v3.x+**: Independent governance structure (foundation, working group, or standards body)

Contributors who make substantial editorial or conceptual contributions to v1.x will be first in line for maintainer invitations when we open up.

## Code of Conduct

All contributors are expected to follow our [Code of Conduct](./CODE_OF_CONDUCT.md). Be kind, stay on topic, and assume good faith.

## Recognition

Contributors are acknowledged in the project CHANGELOG and, for substantial contributions, in the spec's Acknowledgments section. We do not currently issue CLAs — by contributing, you agree that your contribution is released under the same CC BY 4.0 license as the rest of the spec.

## Questions?

- **Technical questions about the spec**: [GitHub Discussions](../../discussions)
- **General inquiries**: [agentshow.shop](https://agentshow.shop)
- **Security issues**: See [SECURITY.md](./SECURITY.md)

Thank you for helping make A2A Commerce a shared language for the future of AI-native trading.
