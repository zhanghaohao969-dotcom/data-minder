# Data Minder · Stay Evidence-Aware

English | [简体中文](README.zh-CN.md)

**No data retrieval. No calculations. No reports. Just a gentle nudge when you make a decision, write a review or draw a conclusion: what would help validate this claim?**

Data Minder is an instruction-only Agent Skill. It is not a data analysis tool. It adds a layer of data awareness to AI conversations: helping you choose relevant metrics, find appropriate comparisons, consider confounders and notice experience or quality trade-offs.

> Data navigation, not autopilot.

## What It Looks Like

You say:

> The new detail page has an 8% click-through rate. Pretty good, right?

Instead of agreeing automatically or launching into a full statistical analysis, it asks a gentle question:

> 8% alone isn't enough to judge. What are you comparing it with? If there isn't a reference yet, that's fine; we can keep it as an observation.

You say:

> Conversion rose after I changed the copy. The copy clearly worked.

It helps separate a change from an attribution:

> The change may be related to the copy; let's start with an easy confounder check. What was the overall trend during the same period? If that's unavailable, we can describe the copy's effect as a hypothesis to validate.

These numbers and conversations are illustrative examples, not measured performance or industry benchmarks.

## Four-Step Data Navigation

1. **Starting point · Choose a metric**: Identify the behavior to observe without setting a numerical target for you.
2. **Coordinates · Choose a reference**: Decide what to compare the number with, and align measurement definitions first.
3. **Route · Examine attribution**: Consider factors that may coexist and start with the easiest checks.
4. **Stay on track · Watch guardrails**: Avoid improving one metric at the expense of another important experience.

Seven disciplines support these steps: keeping an eye on evidence, the reference reflex, ruling out alternatives first, checking vanity metrics, small-sample caution, guardrail awareness and reconciling conflicting signals.

## When to Use It

- **Planning and product or design changes**: Leave baselines and validation directions before launch.
- **OKRs and goals**: Discuss metrics and references without choosing someone else's target number.
- **Reviews, status updates, retrospectives and promotion cases**: Separate verified conclusions, preliminary observations and hypotheses to validate.
- **Outcome reviews, trade-off decisions and attribution discussions**: Avoid isolated numbers, vanity metrics and single-cause explanations.

It should intervene only when a judgment needs evidence or an outcome needs later validation. Questions such as "blue or green for this button" or "make this sentence smoother" should not trigger data follow-ups.

## The Core Experience Rule: Nudge, Do Not Interrogate

The first intervention has just three parts: **a hint, one question and an exit ramp**.

- Ask one subquestion at a time; do not hide several questions behind one question mark.
- Go deeper only if the user wants to engage.
- If the user does not take up the question, do not pursue it.
- If the user says "leave the data aside for now," return to the original task.

The Skill should not turn every conversation into a metrics review or make gathering data a prerequisite for writing a plan.

## Installation and Usage

### Install in a Skill-Compatible Agent Client

1. Download or clone this repository.
2. Locate the `skills/data-minder/` folder.
3. Import that folder according to your client's instructions, or place it in the client's supported Skill directory. Preserve the `data-minder/SKILL.md` structure.
4. Reload Skills as your client requires, then try the examples below.

Directories and installation mechanisms vary across clients. This repository provides no automatic installer and does not claim verified compatibility with every client. A GitHub repository location is not the same thing as a client's Skill installation directory.

**Language support**: The default `README.md` and `SKILL.md` are in English. A [Chinese README](README.zh-CN.md) and [Chinese reading version of the instructions](docs/data-minder.zh-CN.md) are available. The Skill still responds in the user's language; English instructions do not force English replies. Install only `skills/data-minder/`, not the Chinese reading document as a second Skill.

### Try It Without Native Skill Support

You can give the body of `skills/data-minder/SKILL.md` to an AI as conversation guidance or custom instructions. This is a convenient way to try it, but it is not equivalent to native Skill discovery and on-demand loading.

### Try These Prompts

```text
Use data-minder to discuss this with me: I want to shorten the sign-up flow from 5 steps to 3.
```

```text
Help me draft a redesign retrospective with the tentative conclusion "the experience improved significantly." Gently flag evidence gaps; do not invent data.
```

```text
Clicks increased after I moved the entry point. Help me think through possible confounders to check first.
```

You can opt out just as directly:

```text
Leave the data aside for now and help me finish the plan.
```

The Agent should then stop data follow-ups and continue the original task.

## Dependencies and Privacy

- The Skill itself contains only Markdown instructions, with no executable scripts, SDKs, API keys, browser dependency or Feishu/Lark dependency.
- No network access is needed when the user's inputs are sufficient for a methodological discussion.
- Public external benchmarks are optional, require an explicit user request and are handled by the host Agent's own search capability. The core nudges work without search.
- This Skill does not proactively connect to internal data platforms, request data permissions or ask for passwords or credentials.
- **No data retrieval does not mean data stays on your device**: numbers, screenshots or materials you give an AI may still be processed under the host product's rules. Follow your organization's policies and prefer necessary, de-identified aggregate information.

## What It Does Not Do

- Query internal business data, perform calculations or produce reports.
- Calculate statistical significance or confidence intervals.
- Set numerical targets for users.
- Turn before-and-after changes, correlation or partial elimination of confounders into causal conclusions.
- Declare a project successful simply because a primary metric rose and a guardrail did not fall.
- Replace professional statistical analysis, valid experiment design or final business judgment.

Separate, explicit requests for data retrieval or calculation should be handled by the host Agent under its own authorization and tool rules. This Skill does not expand authorization.

## Repository Structure

```text
data-minder/
├── README.md
├── README.zh-CN.md
├── LICENSE
├── .gitignore
├── docs/
│   └── data-minder.zh-CN.md
└── skills/
    └── data-minder/
        └── SKILL.md
```

`README.md` is for people; `SKILL.md` is for Agent execution. Import only `skills/data-minder/` to install.

## Validation Notes

This version has undergone static checks for file structure, metadata and content consistency. Cross-client automatic triggering has not been tested, and no quantitative effectiveness results are available. Do not treat the examples as performance promises.

Before relying on it in your client, check:

1. Planning and retrospective scenarios trigger naturally, rather than from keywords alone.
2. The first nudge asks only one subquestion and lets the original task continue.
3. Follow-ups stop when the user declines a deeper discussion.
4. Aesthetic choices and copy polishing do not cause false triggers.
5. The Agent avoids unauthorized retrieval, invented numbers, target setting and unverified causal conclusions.

To evaluate whether it helps, compare the same inputs with and without the Skill. Look at relevance, follow-up burden, respect for opting out and unsupported conclusions. Those comparisons are not currently available, so effectiveness is not claimed to be established.

## Sharing and Redistribution

This repository shares only Skill instructions and usage guidance, not real business data or user conversations.

Retain the MIT License and copyright notice when redistributing. De-identify submitted examples; do not upload credentials, personal-level records or materials you are not authorized to share.

## Contributing

Issues with concrete examples of false triggers, excessive questioning, follow-ups after opting out or unsupported conclusions are welcome. Remove sensitive information before submitting an example.

Prioritize three qualities when making changes: **gentle nudges, respect for opting out and no false certainty**. New examples should cover both situations that should trigger the Skill and situations that should not. Keep the English and Chinese versions aligned when changing behavior or examples.

## License

This project is licensed under the [MIT License](LICENSE).
