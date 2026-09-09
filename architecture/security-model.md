# xF Security Model

Security in xF is declarative and metadata-driven.  
It applies uniformly across API, UI, and workflow layers.

## Components

### 1. deny_get
SQL expression returning 1 to deny GET.

### 2. deny_set
SQL expression returning 1 to deny POST.

### 3. RBAC Tables
- `T_ZXF_USER`
- `T_ZXF_USERROLE`
- `T_ZXF_USERRIGHT`
- `T_ZXF_USERGROUP`
- `T_ZXF_USER_USERGROUP`

### 4. Domain Partitioning
`T_ZXF_DOMAIN` defines multi-tenancy boundaries.

### 5. Field-Level Security
Rules like “only HR can see salary” are declared once and enforced everywhere.

### 6. Unified Dispatch Model
The client never sees endpoint addresses.  
Routing is resolved server-side.

## Deterministic Guarantees

- No imperative security logic  
- No per-endpoint ACLs  
- No client-side routing  
- No accidental exposure  
