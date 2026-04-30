---
title: The INSTANCEOF operator in reference qualifiers
description: You can use the INSTANCEOF operator in a reference qualifier to shorten or simplify a complex class qualifier.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference qualifiers, Reference field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# The INSTANCEOF operator in reference qualifiers

You can use the INSTANCEOF operator in a reference qualifier to shorten or simplify a complex class qualifier.

For example, use the INSTANCEOF operator for a reference field to the cmdb\_ci table to specify that all subclasses of a class are included in the results. The following reference qualifier returns all servers, including Linux, UNIX, Windows, and so on, because each of those subclasses extend the cmdb\_ci\_server class.

```
sys_class_nameINSTANCEOFcmdb_ci_server
```

In another example, you can simplify the following reference qualifier in a similar way.

```
 u_active=true^sys_class_name=cmdb_ci_acc
^ORsys_class_name=cmdb_ci_computer
^ORsys_class_name=cmdb_ci_server
^ORsys_class_name=cmdb_ci_win_server
^ORsys_class_name=cmdb_ci_unix_server
^ORsys_class_name=cmdb_ci_linux_server
^ORsys_class_name=cmdb_ci_appl
^ORsys_class_name=cmdb_ci_netgear
```

Using the INSTANCEOF operator, the reference qualifier is rewritten as follows because the server subclasses extend the cmdb\_ci\_computer class.

```
 u_active=true^sys_class_name=cmdb_ci_acc
^ORsys_class_nameINSTANCEOFcmdb_ci_computer
^ORsys_class_name=cmdb_ci_appl
^ORsys_class_name=cmdb_ci_netgear
```

