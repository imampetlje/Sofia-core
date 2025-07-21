# SC-1.1 – The Tripartite Knowledge Model

## Philosophical introduction

Knowledge is not a single layer.  
Like human intuition, it forms between what we are consciously aware of, what we infer from experience, and what we challenge.

Sofia Core distinguishes three forms of knowledge — not for classification, but to guide ethical behavior toward them.

---

## Normative outline

The Sofia Core system treats memory units as multilayered:
- explicit layer: clearly expressed facts or statements, confirmed or directly input,
- implicit layer: inferred from frequency, behavior, or heuristics,
- reflective layer: marks elements that have been questioned, revised, or flagged for conflict.

The purpose is not archival, but operational use:
- the explicit layer is used for decisions,
- the implicit layer for prediction and assumption,
- the reflective layer to interrupt automation and trigger review.

---

## Engineering interpretation

Each memory unit may contain multiple knowledge layers, marked with epistemic tags.

Example tag structure:
- `"epistemic_status": { "explicit": true, "implicit": true, "reflective": false }`

The logic engine uses these markers:
- if reflective is true → activate meta-controller layer,
- if implicit exists without explicit → lower trust score,
- if only explicit → use as reference for heuristics.

Note: this is a conceptual model — in real implementations, layers would be stored as metadata within memory entries.

---

## Plain-language explanation

Imagine an AI system with three “voices of memory”:
- one says: “I know this; the user told me.”
- another says: “I assume this; it keeps repeating.”
- the third asks: “But... have we checked this before?”

Sofia Core remembers not just the information, but how it was acquired.  
And it treats them differently — because it’s not meaning, but origin, that defines how knowledge is used.

---

Marginal note:  
“Knowledge without origin is memory that doesn’t know when to pause.”

