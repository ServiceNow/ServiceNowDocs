---
title: Manage principal classes in the Data Foundations advisor
description: Add or remove CI classes from the Data Foundations advisor scope to keep it aligned with your organization's current goals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-manage-scope.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Manage advisor scope, Advisor setup, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage principal classes in the Data Foundations advisor

Add or remove CI classes from the Data Foundations advisor scope to keep it aligned with your organization's current goals.

## Before you begin

Role required: sn\_cmdb\_admin

## Procedure

1.  On the Data Foundations advisor dashboard, select **Manage principal classes**.

2.  In the Set principal classes dialog box, add or remove CI classes to update your principal class selection.

    |Purpose|Action|Data coverage|
    |-------|------|-------------|
    |Add a CI class group|Select the check box for the group to include all its CI classes.|Includes all CI classes associated with the selected group.|
    |Expand CI class selection|Select **&gt;** to expand a group, then select check boxes for specific CI classes.|Includes only the selected CI classes associated with a group.|
    |Narrow down CI class selection|Select **&gt;** to expand a group, then clear check boxes for specific CI classes.|Excludes only the CI classes cleared from a group.|
    |Remove a CI class group|Clear the check box for the CI class group.|Excludes all CI classes associated with the removed group.|
    |Remove a selected CI class|Select X icon next to the category in the **Selected classes** column.|CI class is removed from scope.|

3.  Select **Done** to apply the changes.


## Result

The Data Foundations advisor dashboard updates to reflect the data based on the new principal class selection.

