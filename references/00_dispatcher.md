# Affirmative Logic Formulator — Technical Operational Dispatcher

**Framework Author**: William Fitzpatrick (*Writer Science*)  
**Source Lecture**: [How to Articulate Your Thoughts More Clearly than 99% of Writers](https://www.youtube.com/watch?v=nsa44tXal7A)  
**Parent Collection**: [Master Collection](../../kirby-fitzpatrick-writers-collection/SKILL.md) | [Global Help](../../../kirby-help/SKILL.md)  

---

## 1. Cognitive Foundation: Cognitive Inversion Penalty

Human cognition processes affirmative assertions faster and with lower error rates than negative or inverted assertions. When technical documentation, code comments, or RFCs state conditions using double negatives or exclusionary framing, readers must perform two cognitive operations:
1. Construct the hypothetical negative scenario.
2. Invert the truth value to find the real operational invariant.

The **Affirmative Logic Formulator** rewrites convoluted exclusions into direct, affirmative technical requirements.

```text
[Double-Negative Inversion: High Cognitive Friction]
"The daemon does not fail to terminate child processes unless the kill signal is not delivered."
     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

[Direct Affirmative Logic: Zero Friction]
"The daemon terminates all child processes when it receives the kill signal."
```

---

## 2. Core Transformation Protocols

### Protocol 1: Double-Negative Elimination
Replace hedging double negatives with affirmative equivalents:

| Negative Framing | Direct Affirmative Assertion |
|---|---|
| `not uncommon` | `frequent`, `common` |
| `not unable to` | `able to`, `can` |
| `does not fail to` | `always`, `consistently` |
| `not inconsistent with` | `consistent with`, `matches` |
| `not insignificant` | `significant`, `material` |
| `not invalid` | `valid` |
| `not disallow` | `allow`, `permit` |

### Protocol 2: Affirmative Guardrail Formulation
State security boundaries and validation constraints in terms of **what is required or allowed** rather than what is forbidden:

* **Negative Slop**: *"Users are not permitted to submit requests without providing an Authorization header."*
* **Affirmative**: *"Requests require an Authorization header."*

### Protocol 3: Conditional Logic Normalization
Eliminate *"unless... not"* and nested negative conditionals in documentation:
* **Convoluted**: *"Do not execute the migration unless the replica is not lagging."*
* **Affirmative**: *"Execute the migration only when the replica is fully caught up."*

---

## 3. Engineering Application Scenarios

### 3.1 Security Policies & Auth Documentation
* **Negative**: *"Access is not denied unless the token has not been verified."*
* **Affirmative**: *"Grant access only to verified tokens."*

### 3.2 Code Invariants & Function Docstrings
* **Negative**: `// Ensures that the buffer does not contain non-printable characters.`
* **Affirmative**: `// Validates that all buffer characters are printable.`

### 3.3 Pull Request Descriptions & RFCs
* **Negative**: *"This patch ensures that background workers will not fail to clean up temporary scratch files upon unexpected shutdown."*
* **Affirmative**: *"This patch guarantees that background workers clean up scratch files upon shutdown."*

---

## 4. Verification Checklist

- [ ] Are all double negatives (*"not uncommon"*, *"does not fail to"*) replaced by direct positives?
- [ ] Are preconditions formulated as requirements (*"Must be X"*) rather than exclusions (*"Cannot be not-X"*)?
- [ ] Have *"unless... not"* constructions been eliminated?
- [ ] Can a software engineer immediately code the boolean condition from the sentence without truth-table algebra?
