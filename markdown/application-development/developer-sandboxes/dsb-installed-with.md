---
title: Components installed with Developer Sandboxes
description: Several types of components are installed with activation of Developer Sandboxes, including tables and user roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/developer-sandboxes/dsb-installed-with.html
release: brazil
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Installing, Developer Sandboxes, Developing your application, Building applications]
---

# Components installed with Developer Sandboxes

Several types of components are installed with activation of Developer Sandboxes, including tables and user roles.

## Roles installed with Developer Sandboxes

<table id="table_pzh_zsb_xhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sandbox manager

 \[sandbox\_manager\]

</td><td>

Manage the lifecycle of all sandboxes.

</td></tr><tr><td>

Sandbox user

 \[sandbox\_user\]

</td><td>

Request and view sandboxes.

</td></tr></tbody>
</table>## Plugins for Developer Sandboxes

|Plugin|Description|
|------|-----------|
|com.glide.dsb|Developer Sandboxes application plugin|

## Tables installed with Developer Sandboxes

**Note:**

-   Tables that aren't explicitly mentioned in table config are shared across all sandboxes instead of copied separately.
-   If you make a schema change to a shared table, the table becomes an isolated table on the sandbox that initiated the schema change. For example, adding a column to a shared table isolates it in the sandbox.

<table id="table_tzh_zsb_xhc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Main Developer Sandboxes table

 \[sys\_dsb\]

</td><td>

Ensures controlled access to critical sandbox data and prevents unauthorized modifications.

 Only the admin or sandbox\_manager role can read or report\_view.

</td></tr><tr><td>

Developer Sandboxes alias table

 \[sys\_dsb\_table\_alias\]

</td><td>

-   Stores table alias data for sandbox operations.
-   Prevents unauthorized changes to alias records.
-   Ensures secure management of critical sandbox-related configurations.

 Only the admin or sandbox\_manager role can read or report\_view.

</td></tr><tr><td>

Developer Sandboxes configuration table

 \[sys\_dsb\_table\_config\]

</td><td>

-   Stores configuration data for sandbox tables.
-   Ensures secure management of sandbox table configurations.
-   Prevents unauthorized access or modifications.

 Only the admin or sandbox\_manager role can read or report\_view.

</td></tr><tr><td>

Developer Sandboxes message table

 \[sys\_dsb\_message\]

</td><td>

Stores messages for sandboxes.

</td></tr><tr><td>

\[sys\_dsb\_lifecycle\_log\]

</td><td>

Stores all lifecycle-related events for sandboxes along with context describing the events.

</td></tr><tr><td>

\[sys\_dsb\_lifecycle\_assign\_log\]

</td><td>

Stores lifecycle events describing sandbox node assignment.

</td></tr><tr><td>

\[sys\_dsb\_lifecycle\_create\_log\]

</td><td>

Stores lifecycle events describing the creation of a sandbox.

</td></tr><tr><td>

\[sys\_dsb\_lifecycle\_destroy\_log\]

</td><td>

Stores lifecycle events describing the deletion of a sandbox.

</td></tr><tr><td>

\[sys\_dsb\_query\_condition\]

</td><td>

Stores rules for partial copy tables.

</td></tr></tbody>
</table>