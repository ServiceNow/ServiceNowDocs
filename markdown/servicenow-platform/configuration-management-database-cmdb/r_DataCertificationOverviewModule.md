---
title: Data Certification Overview module
description: The Data Certification Overview module displays various data certification-related reports on the Data Certification Console homepage.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data Certification Overview module

The Data Certification Overview module displays various data certification-related reports on the Data Certification Console homepage.

The Overview module is a type of homepage.

The different levels of access are:

<table id="table_zmb_mmj_wt"><thead><tr><th>

Role

</th><th>

Access

</th></tr></thead><tbody><tr><td>

certification

</td><td>

-   View \(view overview page and refresh reports\)
-   Review, certify, and fail certifications

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
</table>## Data Certification Overview Module

The Overview module includes the following reports:

|report|Description|Table|
|------|-----------|-----|
|30/60/90 Day Aging|Groups tasks by the number of days \(30, 60, 90, and 90 and over\) since the task was opened.|Certification Task|
|Certification Instances|Lists all certification instances.|Certification Instance|
|Certification Progress Report|Groups tasks by task owner, indicating task progress as a percentage.|Certification Task|
|Certification Task Completed Report|Groups tasks by task owner, indicating tasks that are complete.|Certification Task|
|Exceptions To Date|Lists all task elements that have comments added and a state of Failed or In Progress.|Certification Element|
|Functional Roll Up|Lists the managers that have groups with assigned certification tasks. The report is a horizontal bar chart, grouped by status, with each bar representing a manager of an assignment group.|Certification Task|
|Hierarchical Roll Up|Shows the managers that have employees with assigned certification tasks \(task owners\). The report is a horizontal bar chart, grouped by status, with each bar representing a manager of a task owner \(identified in the **Assigned to** field\).|Certification Task|
|Upcoming Schedules|Lists all schedules that are scheduled to run within the next 30 days.|Certification Schedule|

**Related topics**  


[Use the Data Certification Overview module](../task/t_UsingDataCertOverviewMod.md)

