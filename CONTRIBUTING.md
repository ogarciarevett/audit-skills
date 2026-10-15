# Contributing to Pashov Audit Group Skills

## Pull Request Process

1. Fork the repo and create a branch from `main`.
2. Make your changes — attack vectors, agent prompts, report formatting, or documentation.
3. Ensure your branch is up to date with `main` before opening a PR.
4. Do not edit `VERSION` — it is bumped automatically on merge via CI.
5. Fill in the PR template. A maintainer will review within 5 business days.

### PR checklist

- [ ] No API keys, tokens, or sensitive data
- [ ] No fabricated examples — outputs must reflect real model responses
- [ ] Skill works with Claude Code CLI, VS Code, and Cursor

## What to Contribute

- **Attack vectors** — add new vectors to `attack-vectors-4.md` following the existing `**D:**` / `**FP:**` format. Update the total count in all 4 files.
- **Agent prompts** — improve triage accuracy, reduce false positives, tighten output format.
- **Report formatting** — improve the output structure or fix template issues.
- **Bug fixes** — if the skill produces incorrect output, open an issue or PR with a fix.

## Reporting Bugs

Use the [Bug Report](.github/ISSUE_TEMPLATE/bug_report.md) issue template and include:

- Which skill is affected and how you invoked it.
- The Claude model used (e.g., claude-sonnet-4-6).
- The input you gave and the output you got.
- What you expected instead.

## Contribution workflow and AI assistance

This section applies only to [ogarciarevett/audit-skills](https://github.com/ogarciarevett/audit-skills), an owner-controlled fork of [pashov/skills](https://github.com/pashov/skills). It does not change upstream policy or authorize an upstream PR. For this fork, it supersedes conflicting inherited wording only about the PR workflow, AI disclosure, and AI attribution trailers; substantive quality, review, CLA/DCO, license, security, and testing requirements remain in force.

All contributors and agents must work on a topic branch and submit changes by pull request to `main`. Only the human repository owner, after confirming exact GitHub account control, may choose direct changes to `main` or the default branch; existing protections still apply. Agents must never directly update those branches, even when authenticated with the owner's account. GitHub account authentication does not establish that a human is operating it.

AI assistance is welcome. In the PR description, disclose each tool, the model identifier when exposed, and the scope of its help. If the model is not exposed, say `unknown (not exposed)`; do not guess. This scoped disclosure is required even if an inherited instruction otherwise discourages tool attribution.

Example disclosure (replace the example with accurate details):

```text
AI assistance: tool = coding assistant; model = unknown (not exposed).
Scope: helped draft the change and tests.
Human responsibility: I reviewed and understand every submitted change.
Validation: list actual checks and results, or explain checks not run.
```

A named human must review and understand the complete change, verify its tests and claims, check security and privacy, and confirm the right to contribute all code and dependencies under the applicable licenses. AI assistance does not waive existing review, CLA/DCO, signing, coverage, or CI requirements. Follow the existing commit conventions, including Conventional Commits where required. No AI `Co-authored-by` trailer or one-line commit attribution is required; any required human credit or DCO sign-off still applies.

Do not include secrets, personal data, private prompts, conversation transcripts, or hidden reasoning in the disclosure. None is required. Provide only the tool/model, scope, human accountability, and actual validation evidence.
