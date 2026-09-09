# Deterministic AI in xF

xF is designed for deterministic AI-assisted system generation.  
The runtime ensures that AI output cannot introduce instability, arbitrary control flow, or unpredictable behaviour.

This document explains how determinism is achieved.

---

# 1. Declarative Metadata Only

AI produces metadata, not code.

Metadata is:

- Finite
- Structured
- Validated
- Interpreted deterministically

This eliminates the risk of:

- Infinite loops
- Arbitrary branching
- Side effects
- Hidden logic

---

# 2. Constrained Output Domains

Each metadata field has a defined domain:

- `valuetype` → fixed set of types  
- `property_type` → fixed enumeration  
- `xfctrltype` → registered control types  
- `querymode` → fixed search modes  
- `setinterval` → integer milliseconds  
- `validationsql` → SQL only  
- `computesql` → SQL only  

AI cannot invent new behaviours outside these domains.

---

# 3. Runtime Interpretation

The xF Runtime:

- Loads metadata
- Validates structure
- Executes deterministically
- Rejects invalid metadata
- Enforces constraints

AI output is never executed directly.  
It is interpreted by a stable virtual machine.

---

# 4. No Arbitrary Code Execution

AI cannot:

- Generate C#
- Generate JavaScript
- Generate backend logic
- Modify routing
- Modify transport protocol

All logic must be expressed as:

- SQL
- Metadata fields
- Declarative UI definitions

---

# 5. Deterministic Pipelines

GET and SET pipelines are fixed:

- No dynamic branching
- No dynamic code paths
- No runtime mutation
- No uncontrolled side effects

AI output flows through a deterministic engine.

---

# 6. Safety Guarantees

- No code injection
- No routing injection
- No workflow drift
- No session state corruption
- No uncontrolled API exposure

The Unified Dispatch Model ensures the client never sees endpoint addresses.

---

# Summary

xF provides a deterministic execution environment where AI can safely generate enterprise systems without producing imperative code.

This is the structural advantage xF has over all AI app builders.
