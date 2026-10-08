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
reading_time_minutes: 2
breadcrumb: [Installing, Developer Sandboxes, Build, AI Workflow Factory, Building applications]
---

# Components installed with Developer Sandboxes

Several types of components are installed with activation of Developer Sandboxes, including tables and user roles.

## Roles installed with Developer Sandboxes

<table id="table_pzh_zsb_xhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sandbox license admin \[sn\_dsb\_commons.sandbox\_license\_admin\]

</td><td>

Assign sandbox licenses to non-production instances in App Engine Management Center \(AEMC\).**Note:** You must have the com.glide.dsb.licensing plugin installed for this role.

</td></tr><tr><td>

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

<table><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.dsb

</td><td>

Developer Sandboxes application plugin

</td></tr><tr><td>

com.glide.dsb.licensing

</td><td>

Enables self-serve sandbox license assignment from \(AEMC\). Install on your base or controller instance to distribute sandbox packs to non-production instances.**Note:** The com.glide.dsb.licensing plugin should be used from only one instance, the license management instance.

</td></tr><tr><td>

App Management Framework \(sn-app-amf\)

</td><td>

Required for sandbox pack license assignment. This app is available in the ServiceNow Store and must be installed separately. It is not a dependency of the `com.glide.dsb.licensing` plugin and is not installed automatically.**Important:** Install the App Management Framework app from the ServiceNow Store before using sandbox pack license assignment.

</td></tr></tbody>
</table>## Tables installed with Developer Sandboxes

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

Developer Sandboxes instance allocation table \[sys\_dsb\_instance\_allocation\]

</td><td>

Stores the sandbox pack allocation state for each non-production instance, including the number of packs assigned and the current allocation status.**Note:** This table is available only if the com.glide.dsb.licensing plugin is installed.

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
</table>**Parent Topic:**[Installing Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-installing.md)

