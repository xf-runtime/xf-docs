# xF Execution Pipeline

The execution pipeline is the deterministic process the runtime uses to interpret metadata and execute operations.

It consists of two major flows: GET and SET.

---

# GET Pipeline

The GET pipeline retrieves an entity instance and prepares the UI.

## Steps

1. Load entity metadata  
2. Load attribute metadata  
3. Execute `stridsql` if present  
4. Execute `xt` queries  
5. Apply FK display columns  
6. Apply UI sections  
7. Build y-segment  
8. Return metadata + data to frontend

The frontend renders the UI from metadata without build steps.

---

# SET Pipeline

The SET pipeline processes incoming values, validates them, and persists changes.

## Steps

1. Parse incoming values  
2. Apply `setsequence` ordering  
3. Validate mandatory fields  
4. Validate uniqueness  
5. Validate FK constraints  
6. Execute `validationsql`  
7. Execute `computesql`  
8. Execute `deny_set`  
9. Morph aggregates if `set_entity` is defined  
10. Save to DB or stored procedure  
11. Return updated state

---

# Composite Uniqueness Engine

If `hascompositeuniquecheck = 1`, the runtime executes:

  `compositeuniqueproparray`

  
This SQL determines whether a combination of values is unique.

---

# Save Modes

Entities may define:

- Stored procedure (`storeprocforupdate`)
- Save algorithm (`savemode`)
- Standard SQL persistence

---

# Deterministic Guarantees

- No arbitrary control flow  
- No imperative code paths  
- No side effects outside metadata  


