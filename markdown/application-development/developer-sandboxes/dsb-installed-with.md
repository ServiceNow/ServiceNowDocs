---
title: Tables installed with Developer Sandboxes
description: Several types of components are installed with activation of Developer Sandboxes, including tables and user roles.
locale: en-US
release: zurich
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: reference
last_updated: "2026-01-08"
reading_time_minutes: 1
breadcrumb: [Installing, Developer Sandboxes, Developing your application, Building applications]
---

# Tables installed with Developer Sandboxes

Several types of components are installed with activation of Developer Sandboxes, including tables and user roles.

## Tables installed with Developer Sandboxes

<table id="table_tzh_zsb_xhc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Main Developer Sandboxes table

 \[sys\_dsb\]

</td><td>

Ensures controlled access to critical sandbox data and prevents unauthorized modifications.

 Only the admin role can read or report\_view.

</td></tr><tr><td>

Developer Sandboxes alias table

 \[sys\_dsb\_table\_alias\]

</td><td>

-   Stores table alias data for sandbox operations.
-   Prevents unauthorized changes to alias records.
-   Ensures secure management of critical sandbox-related configurations.

 Only the admin role can read or report\_view.

</td></tr><tr><td>

Developer Sandboxes configuration table

 \[sys\_dsb\_table\_config\]

</td><td>

-   Stores configuration data for sandbox tables.
-   Ensures secure management of sandbox table configurations.
-   Prevents unauthorized access or modifications.

 Only the admin role can read or report\_view.

</td></tr><tr><td>

Developer Sandboxes template configuration table

 \[sys\_dsb\_template\_repository\]

</td><td>

-   Stores sandbox template repository configurations and records.
-   Ensures secure handling of repository data.
-   Prevents unauthorized modifications or access.

 Admins can create, read, update, delete, and report\_view.

</td></tr><tr><td>

Developer Sandboxes template management table

 \[sys\_dsb\_template\]

</td><td>

Manages sandbox templates used for configuration and allocation.Depending on conditions, admins can create, read, update, delete, and report\_view.

</td></tr><tr><td>

Developer Sandboxes message table

 \[sys\_dsb\_message\]

</td><td>

Stores messages for sandboxes.

</td></tr><tr><td>

\[sys\_dsb\_query\_condition\]

</td><td>

 

</td></tr></tbody>
</table>