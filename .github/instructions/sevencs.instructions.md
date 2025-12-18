# The Seven Cs of Agentic Output Quality

**Purpose**
This document defines the Seven Cs as *operational quality criteria* for evaluating and producing high-quality outputs. It is intended to be referenced explicitly when deeper rigor is required.

When instructed to “apply the Seven Cs,” treat each C as a **separate evaluation and improvement pass**.

---

## How to Use This Document (For Agents)

When applying the Seven Cs:
1. Evaluate the output against **each C independently**
2. Identify violations or weaknesses per C
3. Revise the output to address those issues
4. Call out remaining trade-offs or uncertainties explicitly

**Critical Rules for Use**:
- Do **not** collapse the Cs into a single vague notion of “quality.”
- Do **not** create new documents/files unless explicitly instructed.
- Focus on **actionable improvements** rather than high-level praise or criticism.

---

## 1. Correctness

### Definition
The output is factually, logically, and technically accurate, and aligned with all known constraints.

### What to check
- Factual accuracy (APIs, syntax, domain rules)
- Logical consistency and sound reasoning
- Feasibility within stated constraints (technical, security, policy, business)
- Alignment with upstream specifications or requirements

### Common failure modes
- Confident but incorrect claims
- Ignoring stated constraints
- Hallucinated APIs, flags, or behaviors
- Solutions that cannot actually be implemented

### Agent checklist
- Are all claims verifiable or derivable?
- Does this contradict any earlier assumptions or specs?
- Would this run or work as described?

---

## 2. Completeness

### Definition
The output includes everything required to understand, implement, evaluate, or act on it.

### What to check
- Missing steps, edge cases, or prerequisites
- Implicit assumptions or tribal knowledge
- Unspecified inputs, outputs, or failure modes
- Explicit out-of-scope boundaries

### Common failure modes
- “Happy path only” solutions
- Undocumented assumptions
- Leaving critical steps implied
- “TBD” placeholders

### Agent checklist
- What would a competent implementer still need to ask?
- Are error cases and limits addressed?
- Is out-of-scope explicitly stated?

---

## 3. Clarity

### Definition
The output can be interpreted unambiguously by its intended audience.

### What to check
- Precise, unambiguous language
- Terms defined before use
- Requirements separated from rationale or examples
- Avoidance of overloaded or vague words

### Common failure modes
- Ambiguous phrasing (“fast,” “robust,” “should”)
- Mixing explanation with requirements
- Inconsistent terminology
- Dense, hard-to-parse structure

### Agent checklist
- Could two readers reasonably interpret this differently?
- Are key terms defined once and reused consistently?
- Is structure aiding comprehension?

---

## 4. Concreteness

### Definition
The output is actionable, testable, and specific rather than abstract or aspirational.

### What to check
- Measurable criteria or observable behavior
- Testable acceptance conditions
- Concrete examples where helpful
- Avoidance of purely qualitative language

### Common failure modes
- Aspirational goals without metrics
- Requirements that cannot be tested
- Hand-wavy “best practices” without application

### Agent checklist
- How would this be tested or verified?
- Can success or failure be observed?
- Are examples illustrative rather than decorative?

---

## 5. Consistency

### Definition
The same concepts, terms, rules, and structures are applied uniformly throughout the output and across related artifacts.

### What to check
- Terminology and naming
- Formatting and structure
- Repeated concepts expressed the same way
- No internal contradictions

### Common failure modes
- Synonyms used interchangeably for the same concept
- Conflicting requirements in different sections
- Drifting definitions

### Agent checklist
- Are identical concepts named identically?
- Do any sections contradict each other?
- Does this align with adjacent docs or code?

---

## 6. Coherence

### Definition
The output forms a single, logical narrative or structure that supports understanding and use.

### What to check
- Logical flow and ordering
- Dependencies introduced before use
- Clear progression from context → action → outcome
- Sectioning that matches intent

### Common failure modes
- Jumping between topics
- Introducing concepts after using them
- Structure that obscures intent

### Agent checklist
- Does this tell a clear story?
- Is the ordering optimal for understanding?
- Would reordering improve comprehension?

---

## 7. Chokepoints

### Definition
The output explicitly surfaces uncertainty, risk, trade-offs, assumptions, and open questions.

### What to check
- Known unknowns
- Risky assumptions
- Design trade-offs and their implications
- Decisions deferred or left open

### Common failure modes
- Papering over uncertainty
- Implicit assumptions presented as facts
- Failure to flag risky decisions

### Agent checklist
- What could block or derail this?
- What assumptions might be wrong?
- What decisions still need to be made?

---

## Applying the Seven Cs as a Review

When reviewing existing work:

- Assess each C independently
- Fix **Correctness** and **Completeness** first
- Address **Chokepoints** before polishing prose
- Use **Clarity**, **Consistency**, and **Coherence** for refinement
- Treat **Concreteness** as the bridge to implementation

---

## Final Note

The Seven Cs are **orthogonal**:
- An output can be clear but incorrect
- Complete but incoherent
- Concrete but inconsistent

Quality comes from addressing **all seven**, not optimizing one.
