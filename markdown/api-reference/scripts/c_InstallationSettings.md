---
title: Installation settings
description: Installation settings are global business rules with calculated names. Installation settings are calculated just before a record is displayed and facilitate dynamic determination of access and roles. Installation Settings permit the programmatic determination of a setting.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Installation settings

Installation settings are global business rules with calculated names. Installation settings are calculated just before a record is displayed and facilitate dynamic determination of access and roles. Installation Settings permit the programmatic determination of a setting.

Installation settings controlling access to fields and records are:

-   CanRead\(\)
-   CanWrite\(\)
-   CanCreate\(\)
-   CanDelete\(\)

Functions can return true if access is permitted, false if not. No return value uses the permission calculated using roles. The function has access to the current record through the variable current code.

The name of the function checking the permission on a record is formed by prefixing the setting name with the record name:

```
*record\_name*CanRead()
```

Similarly, the permission on a field in a record is formed by prefixing the function name with the record name, underscore, and field name:

```
*record\_name\_field\_name*CanRead()
```

Naming examples:

```
function incidentCanWrite() {} //  can user write to this record?
 function incident_numberCanWrite() {}  // can user write to the number field?
```

This sample business rule restricts the writing of the name field in the sys\_dictionary file when the entry exists:

```
  // the element name cannot be written unless this is a new record (not yet in database)
  function sys_dictionary_nameCanWrite() {
    if (current.isNewRecord())
      return; 

    return false;
  }

```

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

