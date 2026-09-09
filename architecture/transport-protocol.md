# xF Transport Protocol

The xF Transport Protocol defines how intent, state, data, and workflow instructions move between client and server.

It is the backbone of xF’s deterministic execution model.

## Transport Isomorphism

Persistent entities and transient workflows share the same transport schema:

- Same routing structure  
- Same state representation  
- Same payload format  

This keeps API complexity O(1) regardless of domain size.

## Payload Structure

An xF payload contains:

### 1. Intent
What the client wants to do:
- GET entity
- SET entity
- Execute workflow step
- Load dashboard
- Run xt query

### 2. State
The complete execution state machine:
- Current step
- Next step
- Continuation tokens
- Temporal recursion intervals

### 3. Data
Entity attributes or workflow parameters.

### 4. Metadata References
Entity ID, attribute IDs, control types, sections.

### 5. Transport Segment (y)
The server’s response:
- UI schema
- Data tables
- Validation results
- Workflow continuation

## xt Segment

If an attribute contains SQL in `xt`, the runtime executes it and returns:

- A single table  
- Or multiple tables if `{{dataset}}` is present
  For example
    xy.bookings.t[0]
    xy.bookings.t[1]

## Statelessness

All workflow state is carried inside the payload.  
The server stores nothing between requests.

This enables:
- Infinite horizontal scaling  
- Zero session management
- Zero orchestration middleware  

