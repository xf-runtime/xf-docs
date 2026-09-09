# xF Runtime Overview

The xF Runtime is a deterministic, metadata‑interpreted execution engine for enterprise systems.  
It replaces controllers, DTOs, workflow engines, and UI binding layers with a single unified Meta‑Model stored in ZXF_* tables.

The runtime is stateless, horizontally scalable, and driven entirely by declarative metadata.  
No code generation, no build pipelines, no migrations.

## Core Principles

### 1. Deterministic Execution
All behaviour is derived from metadata.  
Given the same metadata and the same input, the runtime always produces the same output.

### 2. Stateless Operation
Workflow state is carried inside the payload itself, not stored on the server.  
This enables infinite horizontal scaling.

### 3. Unified Model
One metadata registry drives:
- Database schema
- API payloads
- UI forms
- Validation rules
- Workflow logic

### 4. Transport Isomorphism
Persistent entities and transient workflows share the same wire format.

### 5. No-Build Frontend
UI is rendered from metadata at runtime using standard HTML/JS.

## Runtime Components

- Metadata Loader  
- Registry Layer  
- Execution Pipeline (GET/SET)  
- Validation Engine  
- Composite Uniqueness Engine  
- Workflow Engine  
- Search Engine  
- Router Engine  
- Dynamic Function Compiler  
- Transport Layer (xy, y-segment, xt)

## What the Runtime Is Not

- It is not a low-code platform.  
- It is not a code generator.  
- It is not a DSL compiler.  
- It is not a workflow orchestrator.  

It is a **virtual machine for enterprise semantics**.
