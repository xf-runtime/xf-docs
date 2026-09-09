# AI Workflow in xF

xF enables a deterministic, low‑risk AI workflow by constraining LLMs to produce metadata rather than imperative code.  
This eliminates arbitrary control flow, reduces hallucination risk, and ensures that AI-generated output remains safe, interpretable, and maintainable.

The AI workflow consists of three bounded transformations:

1. **Model the Application**
2. **Model the Logic**
3. **Design and Iterate the Frontend**

Each step has a narrow, well-defined target, allowing AI systems to operate with high precision.

---

## 1. Model the Application

The AI produces:

- Applications (`T_ZXF_APP`)
- Entities (`T_ZXF_ENTITY`)
- Attributes (`T_ZXF_ATTRIBUTE`)
- Relationships (FKs)
- UI sections
- Basic validation rules

This replaces traditional schema design, DTO creation, and controller scaffolding.

### Deterministic Constraints

- All output must be declarative.
- No imperative code.
- No loops, branches, or arbitrary logic.
- No external dependencies.

The runtime interprets metadata, guaranteeing correctness.

---

## 2. Model the Logic

The AI produces:

- Validation SQL (`validationsql`)
- Computed SQL (`computesql`)
- Composite uniqueness rules
- Search definitions
- Workflow intervals (`setinterval`)
- Routing metadata (`T_ZXF_ROUTER`)

Logic is expressed declaratively, not as code.

### Deterministic Constraints

- SQL only.
- No dynamic code generation.
- No arbitrary branching.
- No side effects.

The runtime executes logic deterministically.

---

## 3. Design and Iterate the Frontend

The AI produces:

- UI sections
- Control types
- Templates
- Grid definitions
- Dashboard layouts

The no-build frontend renders UI directly from metadata.

### Deterministic Constraints

- HTML/JS only.
- No bundlers.
- No frameworks.
- No build pipeline.

---

## Why This Workflow Works

Traditional AI app builders generate imperative code, which:

- Is hard to maintain
- Is prone to vulnerabilities
- Is difficult for LLMs to reason about
- Creates long-term technical debt

xF avoids this entirely by constraining AI to metadata.

The result is:

- Low hallucination
- High determinism
- High interpretability
- Zero rebuilds
- Zero migrations

AI becomes a safe, high-leverage tool for enterprise system generation.
