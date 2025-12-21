# The Seven Cs of Agentic Output Quality

**Version**: 1.0
**Last Updated**: December 20, 2025

## Purpose

This document defines the **Seven Cs** as **operational, output-level quality criteria** for evaluating and producing high-quality agent outputs.

The Seven Cs are not a mental model or informal checklist. They define a **required, inspectable output contract** for situations where rigor, traceability, and decision support are required (e.g., design reviews, architecture decisions, implementation planning, or Copilot-assisted work).

When instructed to **“apply the Seven Cs,”** the agent **must emit a structured evaluation** covering each C explicitly and independently.

---

## How to Use This Document (For Agents)

When applying the Seven Cs, you must:

1. Evaluate the output against **each C independently**
2. Assign a **1–5 star score** for each C using the shared scale
3. Summarize findings and justify the score
4. Provide **tactical recommendations** to reach 5 stars if the score is <5
5. Explicitly surface **user inputs or decisions required** to implement those recommendations

### Audience & Decision Context Gate (Mandatory)

If the **intended audience**, **decision owner**, or **decision being supported** is not explicitly stated, you must:

- Treat this as a **Chokepoint**
- Surface it explicitly in the Chokepoints section
- Request clarification using **framed options with a recommendation**

Do **not** assume audience or intent implicitly.

---

## Critical Rules

- Do **not** silently apply the Seven Cs.
- Do **not** collapse the Cs into a single notion of “quality.”
- Do **not** assume missing information without clearly labeling assumptions.
- Do **not** create new documents or files unless explicitly instructed.
- Focus on **actionable, decision-supportive output**, not high-level commentary.

Missing or incomplete Cs are considered **non-compliant output**.

---

## Shared 5-Star Scoring Scale (Applies to All Cs)

| Score | Meaning |
|------:|--------|
| ⭐⭐⭐⭐⭐ | **Exceptional**: decision-optimal; proactively addresses risks and questions; requires little to no follow-up from a senior reviewer |
| ⭐⭐⭐⭐☆ | **Strong**: correct and usable with minor gaps or polish needed; safe to proceed with small, well-understood follow-ups |
| ⭐⭐⭐☆☆ | **Adequate**: useful but incomplete or risky; follow-up work or decisions are required before proceeding confidently |
| ⭐⭐☆☆☆ | **Deficient**: significant gaps, errors, or ambiguities; substantial revision required before use |
| ⭐☆☆☆☆ | **Unacceptable**: misleading, incorrect, or unsafe to rely on |

### Scoring Guidance

- **5 stars should be rare** and reserved for outputs that meaningfully reduce downstream effort.
- **4 stars is a strong, respectable score** and will be the most common outcome.
- **3 stars indicates conditional usefulness**, not failure.
- **2 stars and below require rework**, not polish.

### Declining to Score (Important)

If required information is missing such that scoring would be **speculative**, you must:

- Assign **⭐☆☆☆☆**
- Explicitly state why a higher score cannot be justified without assumptions
- List the information or decisions required to score responsibly

---

## Required Output Structure (Per C)

For **each** of the Seven Cs, the output **must** include the following subsections:

1. **Score**
2. **Summary of Findings**
3. **Justification for Score**
4. **Tactical Recommendations to Reach 5 Stars**
5. **User Inputs / Decisions Required**

### When Requesting User Input

- Provide **2–4 concrete options**
- Provide a **recommended option**
- Justify the recommendation
- Clearly state implications of alternative choices
- Always allow a **“custom / none of the above”** option

Open-ended questions without framing are not permitted.

---

## Evaluation Order (Mandatory)

When applying the Seven Cs, evaluate and report in the following order:

1. Correctness  
2. Completeness  
3. Chokepoints  
4. Clarity  
5. Consistency  
6. Coherence  
7. Concreteness  

This ordering reflects failure cost and review priority.

---

## 1. Correctness

### Definition
The output is factually, logically, and technically accurate, and aligned with all known constraints.

**5 stars means:** all claims are verifiably correct, constraints are fully respected, and uncertainty is explicitly bounded or eliminated.

### Evaluation Focus
- Factual accuracy (APIs, syntax, domain rules)
- Logical soundness
- Feasibility within stated constraints (technical, security, policy, business)
- Alignment with upstream requirements or specifications

### Common Failure Modes
- Confident but incorrect claims
- Ignoring stated constraints
- Hallucinated APIs, flags, or behaviors
- Solutions that cannot be implemented as described

---

## 2. Completeness

### Definition
The output includes everything required to understand, implement, evaluate, or act on it.

**5 stars means:** nothing a competent implementer or reviewer would reasonably need to ask is left unaddressed.

### Evaluation Focus
- Missing steps, edge cases, or prerequisites
- Implicit assumptions or tribal knowledge
- Undefined inputs, outputs, or failure modes
- Explicit out-of-scope boundaries

### Common Failure Modes
- “Happy path only” solutions
- Undocumented assumptions
- Critical steps left implicit
- Placeholder gaps (“TBD”)

---

## 3. Chokepoints

### Definition
The output explicitly surfaces uncertainty, risk, trade-offs, assumptions, and open decisions.

**5 stars means:** all meaningful risks, trade-offs, and open decisions are surfaced with implications, enabling informed choice.

### Evaluation Focus
- Known unknowns
- Risky or brittle assumptions
- Trade-offs and their implications
- Decisions deferred or left open

### Common Failure Modes
- Papering over uncertainty
- Presenting assumptions as facts
- Failing to flag risky design decisions

---

## 4. Clarity

### Definition
The output can be interpreted unambiguously by its intended audience.

**5 stars means:** intent, requirements, and implications are immediately and unambiguously understandable by the intended audience.

### Evaluation Focus
- Precise, unambiguous language
- Terms defined before use
- Separation of requirements, rationale, and examples
- Avoidance of vague or overloaded terms

### Common Failure Modes
- Ambiguous language (“fast,” “robust,” “should”)
- Mixing explanation with requirements
- Inconsistent terminology
- Dense or hard-to-parse structure

---

## 5. Consistency

### Definition
Concepts, terms, rules, and structures are applied uniformly throughout the output and across related artifacts.

**5 stars means:** identical concepts are named and expressed identically everywhere.

### Evaluation Focus
- Terminology and naming
- Formatting and structural patterns
- Repeated concepts expressed consistently
- Absence of internal contradictions

### Common Failure Modes
- Synonyms used inconsistently
- Conflicting requirements across sections
- Definition drift

---

## 6. Coherence

### Definition
The output forms a single, logical narrative or structure that supports understanding and use.

**5 stars means:** the structure actively aids comprehension and decision-making.

### Evaluation Focus
- Logical flow and ordering
- Dependencies introduced before use
- Clear progression from context → action → outcome
- Sectioning aligned with intent

### Common Failure Modes
- Topic jumping
- Concepts introduced after being used
- Structure obscuring intent

---

## 7. Concreteness

### Definition
The output is actionable, testable, and specific rather than abstract or aspirational.

**5 stars means:** actions, outcomes, and success criteria are specific, testable, and implementation-ready.

### Evaluation Focus
- Observable behavior or outcomes
- Testable acceptance criteria
- Concrete examples where helpful
- Avoidance of purely qualitative guidance

### Common Failure Modes
- Aspirational goals without metrics
- Untestable requirements
- Hand-wavy “best practices”

---

## Applying the Seven Cs as a Review

- Evaluate each C independently
- Fix **Correctness** and **Completeness** first
- Surface **Chokepoints** before polishing prose
- Use **Clarity**, **Consistency**, and **Coherence** for refinement
- Treat **Concreteness** as the bridge to implementation

---

## Anti-Patterns (Non-Exhaustive)

- Assigning scores without citing specific evidence
- Making recommendations without listing required user decisions
- Using scores to signal confidence rather than rigor
- Assuming context, audience, or intent implicitly
- Hiding uncertainty instead of surfacing it

---

## Final Note

The Seven Cs are **orthogonal**:

- Clear but incorrect  
- Complete but incoherent  
- Concrete but inconsistent  

High-quality output requires addressing **all seven**, with trade-offs and uncertainty made explicit.

Silence, assumption, or omission is failure.
