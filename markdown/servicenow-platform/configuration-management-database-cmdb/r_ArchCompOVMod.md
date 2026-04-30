---
title: Architecture Compliance Overview module
description: The Architecture Compliance Overview module displays various architecture compliance reports. The Overview module is a type of homepage.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Architecture Compliance, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Architecture Compliance Overview module

The Architecture Compliance Overview module displays various architecture compliance reports. The Overview module is a type of homepage.

Only compliance users with certain roles can access the Overview module. The different levels of access are:

<table id="table_kbt_zr5_vt"><thead><tr><th>

Role

</th><th>

Access

</th></tr></thead><tbody><tr><td>

certification

</td><td>

View \(view overview page and refresh reports\)

</td></tr><tr><td>

certification\_admin

</td><td>

-   View \(view overview page and refresh reports\)
-   Customize \(refresh, add, delete, and rearrange reports\)

View, customize

</td></tr><tr><td>

admin

</td><td>

-   View \(view overview page and refresh reports\)
-   Customize \(refresh, add, delete, and rearrange reports\)
-   Edit \(can edit reports\)

</td></tr></tbody>
</table>## Using the Architecture Compliance Overview module

To use the Architecture Compliance Overview module, navigate to **Compliance** &gt; **Architecture Compliance** &gt; **Overview** and click elements within the gauges to obtain more information.

The available reports are:

|Report|Description|Table|
|------|-----------|-----|
|30/60/90 Day Task Aging|All outstanding follow-on tasks grouped by age in 30-day increments|Certification Task|
|Architecture Compliance Discrepancies|All audited attribute discrepancies|Audit Results|
|Hierarchical Task Roll Up|All follow-on tasks grouped by **Assigned to** user|Follow On Task|
|Outstanding Architecture Compliance Tasks|All follow-on tasks in the **Pending**, **Open**, or **Work in Progress** state|Follow On Task|
|Upcoming Architecture Compliance Audits|All scheduled audits|Audit|

![Architecture compliance module graphics.](../../../administer/assessments/images/ArchitectureComplianceOverview.png "Architecture Compliance module")

