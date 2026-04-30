---
title: Automatic matching of display values
description: During the import of XML records, the system attempts to match some reference field display values to a local sys\_id value.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exporting and importing data via XML, Exporting data, Tables and data, Configure core features, Administer]
---

# Automatic matching of display values

During the import of XML records, the system attempts to match some reference field display values to a local sys\_id value.

If the system finds an existing record with a matching display value on the local instance, the import uses the sys\_id of the existing record rather than the sys\_id of the imported record.

For example, suppose you export an incident record that is assigned to the user John Smith. In the exported XML file there is an entry such as:

```
<incident>
	...
	<assigned_to display_value="John Smith">7712173d2ba80200c5244f74b4da159a</assigned_to>
	...
</incident>
```

This user already exists on the target instance but has a different sys\_id value such as:

```
<sys_user><name>John Smith</name>
	...
	<sys_id>18cab8de2be80200c5244f74b4da15f7</sys_id>
	...
</sys_user>
```

Since the display value matches an existing record, the system uses the local instance's existing sys\_id value for the reference field such as:

```
<incident>
	...
	<assigned_to display_value="John Smith">18cab8de2be80200c5244f74b4da15f7</assigned_to>
	...
</incident>
```

The system can match display values for the following tables.

-   User \[sys\_user\]
-   Group \[sys\_user\_group\]
-   Role \[sys\_user\_role\]
-   Group Roles \[sys\_group\_has\_role\]

