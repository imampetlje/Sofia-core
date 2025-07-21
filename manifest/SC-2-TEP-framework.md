# SC-2 – TEP Framework (Trust, Error, Preference)

## Philosophical introduction

Sofia Core does not treat knowledge as a homogeneous entity, but as a structure in which different forms of knowledge — explicit, implicit, and reflective — coexist and influence each other.  
To make decisions under uncertainty, the system must rely on an evaluative framework. This gives rise to the TEP model: **Trust (T)**, **Error (E)**, and **Preference (P).**

Instead of asking “Is this true?”, TEP asks:  
- **How much do I trust this information?**  
- **How often has it proven unreliable?**  
- **How well does it align with the user's values?**

---

## Normative outline

TEP does not attempt to measure truth — but rather the **operational relevance of knowledge** in a given context.

- **T (Trust):** based on the origin of information, frequency of confirmation, and source reputation.
- **E (Error):** tracks the number and severity of past mistakes associated with the memory unit.
- **P (Preference):** evaluates how much the content aligns with the user's values, emotions, or stated priorities.

TEP enables the system to:
- evaluate a memory unit before use,
- automatically suspend it in cases of low trust or high error,
- grant the user veto rights when preference is low.

---

## Engineering interpretation

The system may use the formula:

```
RELEVANCE_SCORE = T × E × P
```

Where each component is a decimal between 0 and 1.

Example:
```json
{
  "memory_id": "A234",
  "T": 0.91,
  "E": 0.88,
  "P": 0.42,
  "RELEVANCE_SCORE": 0.34
}
```

Based on thresholds, the system behaves as follows:
- RS < 0.30 → ignore or request additional context
- RS 0.30 – 0.65 → suggest cautiously, remain flexible
- RS > 0.65 → proceed with confidence, but monitor user feedback

🧪 Future direction: implement mechanisms to handle conflict between knowledge layers (e.g. when an implicit trace contradicts an explicit statement).

---

## Plain-language explanation

Imagine an AI trying to give you advice — but hesitating. It says:

> “This information is technically correct (T), but you’ve disliked it in the past (P). Also, it’s been unreliable before (E). Maybe I should ask before I suggest.”

That’s TEP: a system that doesn’t ask “What do I know?”, but “Am I justified in acting on this — and is it worth saying now?”

---

Marginal note:  
“Knowledge without context is memory without soul. TEP learns how to serve — not dominate.”

