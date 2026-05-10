---
title: Data catalog roles
description: Assign roles to specify what different users can see and do.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Data Catalog, Workflow Data Fabric]
---

# Data catalog roles

Assign roles to specify what different users can see and do.

## Roles

For more information about managing and assigning roles, see [Managing roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/ua-creating-roles.md).

<table id="table_qpl_rqy_j3c"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Role inherited

</th></tr></thead><tbody><tr><td>

Connection Admin \(connection\_admin\)

</td><td>

Configures and manages metadata collectors that import data from external systems. Schedules data collection, monitors integration health, and verifies collected assets. Cannot create or edit catalog assets directly.

</td><td>

-   df\_data\_steward
-   external\_app\_install\_admin
-   agent\_admin
-   wdf\_operator
-   credential\_admin
-   web\_service\_admin
-   sn\_nowassist\_wdf.creator\_admin
-   df\_connection\_admin

</td></tr><tr><td>

Data Steward\[df\_data\_steward\]

</td><td>

Creates and manages catalog assets, business glossary terms, tags, domains, and metadata. Has full edit permissions for organizing and enriching catalog content. Can perform bulk operations and manage asset lifecycle.

</td><td>

-   sn\_nowassist\_wdf.creator\_admin
-   wdf\_consumer

</td></tr><tr><td>

WDF Consumer\[wdf\_consumer\]

</td><td>

Searches and views catalog assets, explores relationships and lineage, and connects to data sources for analysis. Has read-only access to catalog content.

</td><td>

sn\_nowassist\_wdf.creator\_admin

</td></tr></tbody>
</table>**Parent Topic:**[Data catalog reference](data-catalog-reference.md)

