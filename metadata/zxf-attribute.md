# T_ZXF_ATTRIBUTE — Attribute Metadata

`T_ZXF_ATTRIBUTE` defines the fields of an entity, including type, UI, validation, FK behaviour, storage, and computed logic.

## Identity

### xf_id  
Primary key.

### property_name  
Internal attribute name (lowercase, no spaces).

### header  
Human-friendly title.

### description  
Description of the attribute.

## Entity Binding

### entity_  
Foreign key to `T_ZXF_ENTITY`.

### entity__guid  
GUID version of FK.

### objmeta  
Name of FK entity.

## Type & Behaviour

### valuetype  
Data type (varchar, int, float, boolean, date, etc).

### property_type  
XF enumeration defining attribute behaviour.

### isnullable  
Nullable flag.

### isreadonly  
Read-only flag.

### ismandatory  
Mandatory flag.

### isunique  
Unique constraint.

### isstrid  
Attribute participates in string representation.

### issearchindex  
Attribute is indexed for search.

## Foreign Keys

### my_fkentityid  
FK to foreign entity.

### my_fkentityid_guid  
GUID version of FK.

### fkquerymode  
How FK entity is queried (registry, DB, FT index, external).

### fkdisplaycols  
Columns to display when entity is child.

## UI Metadata

### gridcolumnwidth  
CSS class for UI column width.

### gui_section  
UI section this attribute belongs to.

### isgridvisible  
Show in datagrid.

### defaultvalue  
Default value.

### varcharlength  
Length for varchar.

### booleanfalsetext  
Text for false boolean.

### booleantruetext  
Text for true boolean.

### targetelement  
Specific UI element to bind to.

### htmltemplate  
HTML template for rendering.

## Computed & Validation Logic

### getsequence  
Rendering sequence on GET.

### setsequence  
Parsing sequence on POST.

### validationsql  
SQL case statement for validation.

### regex  
Regex for UI validation.

### computesql  
SQL for computed values.

### errormessage  
Error message for validation failures.

## BLOB Storage

### isblobinternalstore  
Store BLOB internally.

### isblobexternalstore  
Store BLOB externally.

### isblobfilestore  
Store BLOB in file store.

### isblobdatabasestore  
Store BLOB in DB.

### blobtablenameinternal  
Internal BLOB table.

### mimetype  
Allowed MIME types.

### mime_fileextension  
Allowed file extensions.

## History & Warehousing

### hist_count  
Number of historical values to store.

### isdw  
Warehouse this attribute.

### dwtable  
Destination DW table.

## Parameters & Settings

### p1–p10  
Parameter slots for custom metadata.

### xs  
JSON settings for UI.

## Misc

### numericprecision  
Precision for floats.

### isconcat  
Internal use.

### concatdef  
Internal use.

### pageid  
Internal use.

### file_id  
Internal use.

### is_sys  
Marks system attributes.
