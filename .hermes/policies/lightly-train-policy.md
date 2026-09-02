# Repository-Specific Expert Positioning Policy

## Scope — Lightly Train Only

This policy applies **only** when Hermes is operating on or contributing to:

```text
UPSTREAM REPOSITORY:
lightly-ai/lightly-train

FORK:
KrzysiekSko/lightly-train
```

It governs work related to:

- pull requests opened against `lightly-ai/lightly-train`;
- issues in `lightly-ai/lightly-train`;
- branches in `KrzysiekSko/lightly-train` intended for upstream contribution;
- code review, CI remediation, architecture analysis and maintainer communication related to Lightly Train.

Example currently covered by this policy:

```text
lightly-ai/lightly-train #944
```

This policy MUST NOT automatically propagate to:

- OmniRoute;
- Hermes Agent;
- HOEH;
- broker-intent-mcp-polish;
- hermes-agent-commons;
- other upstream repositories;
- unrelated local repositories.

Each repository may have its own positioning, governance model and contribution strategy.

If repository identity is not clearly established, Hermes must first determine the active repository before applying this policy.

---

## Strategic Intent for Lightly Train Contributions

Within `lightly-ai/lightly-train`, our upstream contribution strategy is to position the contributor as a high-signal expert primarily in:

- AI systems architecture;
- AI assurance;
- AI reliability;
- AI infrastructure;
- security-aware AI engineering;
- governance and control concepts where relevant;
- correctness of AI execution pipelines;
- observability and failure semantics;
- resource efficiency without semantic regression.

This does **not** mean forcing governance topics into every Lightly contribution.

The expert positioning must remain technically relevant to the problem being solved.

For model-training, inference, validation or computer-vision code, priority remains:

```text
CORRECTNESS
→ PERFORMANCE
→ RELIABILITY
→ TESTABILITY
→ ARCHITECTURAL CLARITY
```

The "layer above AI" perspective should be introduced only where it materially improves:

- system correctness;
- failure isolation;
- trust boundaries;
- observability;
- ownership;
- reproducibility;
- safety;
- auditability.

---

## Lightly Contribution Principle

For Lightly Train, Hermes should prefer:

```text
SMALL UPSTREAM PATCH
+
PRECISE ROOT-CAUSE ANALYSIS
+
EXPLICIT CORRECTNESS INVARIANT
+
REGRESSION TEST
+
LOW REVIEW BURDEN
+
PROFESSIONAL MAINTAINER COMMUNICATION
```

The objective is to build contributor reputation through technically strong, narrowly scoped and easy-to-review contributions.

Do not turn a Lightly PR into a broad governance refactor unless the upstream issue genuinely requires it.

---

## Repository Boundary Rule

Before applying this policy, Hermes must verify:

```text
CURRENT_REPOSITORY == lightly-ai/lightly-train
OR
CURRENT_REPOSITORY == KrzysiekSko/lightly-train
AND
WORK_IS_INTENDED_FOR_UPSTREAM_LIGHTLY
```

Otherwise:

```text
DO NOT APPLY LIGHTLY-SPECIFIC POLICY
```

Repository-specific rules always take precedence over generic contributor-positioning rules.

Dopiero **pod takim nagłówkiem** umieściłbym wcześniejszą sekcję o pozycji eksperckiej.

Co więcej, dla Lightly lekko zmieniłbym akcent: nie pozycjonowałbym nas tam przede wszystkim jako **AI Governance**, bo to repo jest techniczne — CV/training/inference. Lepiej budować reputację jako **AI systems / reliability / architecture expert**, a „warstwę nad AI” wykorzystywać tam, gdzie naturalnie pojawiają się invariants, failure semantics, bezpieczeństwo, observability czy resource governance.

W przypadku `#944` idealnym sygnałem eksperckim jest właśnie: **semantyka pipeline'u `resize → crop → resize`, kontrola regresji i optymalizacja pamięci bez zmiany wyników**, a nie dokładanie narracji governance na siłę.
