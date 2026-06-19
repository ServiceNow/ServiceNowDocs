---
title: Resolve an out-of-sync principal class state in the Data Foundations advisor
description: Resolve a principal class sync discrepancy by reviewing and updating the Data Foundations advisor scope in the Set principal classes dialog box.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-resolve-class-sync.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
keywords: [out-of-sync principal class]
breadcrumb: [Manage advisor scope, Advisor setup, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Resolve an out-of-sync principal class state in the Data Foundations advisor

Resolve a principal class sync discrepancy by reviewing and updating the Data Foundations advisor scope in the **Set principal classes** dialog box.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

When other tools or processes change principal class designations outside the advisor, the Data Foundations advisor scope and the principal class state in the CMDB can diverge. An out-of-sync notification appears on the dashboard when this occurs. For more information, see [Principal class sync in Data Foundations advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-sync.md).

## Procedure

1.  Navigate to the Data Foundations advisor dashboard.

    See [Access CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-access.md).

2.  Open the **Set principal classes** dialog box.

    -   From the out-of-sync notification banner on the dashboard, select **Manage principal classes**.
    -   From the Data Foundations advisor dashboard, select **Manage principal classes**.
3.  Review the current scope against the classes listed in the inline alert.

    Select **Show more** to expand the alert and see the full list of classes that other tools added or removed outside the advisor.

4.  Update the scope to reflect the intended set of principal classes.

5.  Select **Done**.


## Result

The advisor scope is updated, and the out-of-sync notification no longer appears on the dashboard. For more information about selecting and managing principal classes, see [Get started with Data Foundations advisor dashboard setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-get-started.md).

