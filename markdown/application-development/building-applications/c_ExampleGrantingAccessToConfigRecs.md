---
title: Example allowing configuration records for a table
description: You can permit other application scopes to create configuration records on application data tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/building-applications/c\_ExampleGrantingAccessToConfigRecs.html
release: zurich
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Design-time access to application tables, Table design and runtime settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Example allowing configuration records for a table

You can permit other application scopes to create configuration records on application data tables.

You can grant access to the following configuration records with these settings.

<table id="table_j4n_xjc_br"><thead><tr><th>

Configuration record

</th><th>

Setting required to grant access

</th></tr></thead><tbody><tr><td>

Access controls

</td><td rowspan="2">

-   **Accessible from** set to **All application scopes**
-   **Can read** is selected

</td></tr><tr><td>

Business rules

</td></tr><tr><td>

Client scripts

</td><td rowspan="3">

-   **Accessible from** set to **All application scopes**
-   **Can read** is selected
-   **Allow configuration** is selected

</td></tr><tr><td>

Dictionary entry \(new field only\)

</td></tr><tr><td>

UI actions

</td></tr></tbody>
</table>\[Omitted image "GrantingAllDesignTimeAccess.png"\] Alt text: Granting other application scopes design access permission

The following diagram illustrates the effect of granting other application scopes the ability to create configuration records.

\[Omitted image "EffectsOfGrantAllDesignTimeAccess.png"\] Alt text: Granting access to configuration records

**Parent Topic:**[Design-time access to application tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/c_DesignTimeAccessToAppTables.md)

