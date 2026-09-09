# xF Workflow Engine

The workflow engine allows multi-step processes to run without client-side state machines or external orchestration middleware.

Workflows are self-orchestrating and stateless.

## Key Concepts

### 1. Temporal Recursion
Workflows can request the server to re-run themselves after a defined interval (`setinterval`).

### 2. Continuation Tokens
The payload carries the next step of the workflow.

### 3. Self-Hydration
The runtime reconstructs workflow state from the payload.

### 4. No Orchestration Middleware
Multi-system workflows run natively inside xF.

## Workflow Steps

1. Client sends intent + state  
2. Runtime executes step  
3. Runtime returns next state  
4. Client resends payload  
5. Repeat until workflow completes

## Use Cases

- Dashboards  
- Polling  
- Approval chains  
- Multi-step forms  
- Background processes  
- External system coordination

## Deterministic Behaviour

Workflows cannot drift because:
- All logic is metadata-defined  
- All state is payload-defined  
- No server memory is used  
