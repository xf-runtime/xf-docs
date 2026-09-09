# T_ZXF_APP — Application Metadata

The `T_ZXF_APP` table defines the top‑level application boundary inside xF.  
Every entity belongs to exactly one app, and the app provides naming, grouping, and UI-level configuration.

## Columns

### xf_id  
Primary key of the application.

### appname  
Human-readable name of the application.

### entityprefix  
Short prefix (e.g., `hr`, `crm`, `ot`) used to identify entities belonging to this app.  
All entity names must begin with this prefix.

### description  
Description of the application.

### file_id  
Internal use. Reserved.

### is_sys  
Marks system applications (e.g., the ZXF_* metadata app).

### xfctrltype  
Control type used to render the application’s UI template.

### settings  
JSON object containing UI or configuration settings for the app.

## Notes

- An xF installation may contain multiple apps.
- Apps act as namespaces for entities.
- The prefix convention ensures deterministic naming across the system.
