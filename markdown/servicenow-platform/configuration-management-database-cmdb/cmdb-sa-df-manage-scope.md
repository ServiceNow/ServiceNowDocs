---
title: Manage principal classes in the Data Foundations advisor
description: Add or remove CI classes from the Data Foundations advisor scope to keep it aligned with your organization's current goals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-manage-scope.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [manage principal classes, Data Foundations advisor scope, add or remove CI classes, Set principal classes dialog box, principal class selection]
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
    |Find a specific CI class|Enter a class name in the **Search** box.|Matches any non-excluded CI class in the CMDB, not only the classes already shown in the **Available classes** column groups. Selecting a matched class adds it to your principal class selection.|

    **Note:** CI classes on the exclusion list aren't shown in the **Available classes** column.

3.  If a confirmation check box appears under **Review and confirm changes**, select the check box.

    The check box appears only when the **com.snc.task.principal\_class\_filter** system property is set and your selection has an unsaved change.

    The check box label states how many principal classes you're adding and removing. It also notes a possible effect on CI filtering for incident, problem, and change \(IPC\) tasks.

    **Done** stays disabled until you select the check box. Changing your selection again clears the check box and disables **Done** until you select it again.

    Selecting the check box enables **Done**.

4.  Select **Done** to apply the changes.


## Result

The Data Foundations advisor dashboard updates to reflect the data based on the new principal class selection. Dashboard metrics refresh once daily when the **CMDB Advisor - DF Daily Data Collection** scheduled job runs. The scheduled job invokes the **CMDB success advisor data collection for Data Foundation** Performance Analytics job to recalculate the pre-aggregated indicators used throughout the dashboard. For more information about Performance Analytics jobs, see [Collecting indicator scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/c_ClctData.md). Changes to your principal class selection appear in the dashboard metrics after this job's next run, not immediately. For the full list of CMDB success advisor scheduled jobs, see [Components installed with CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-components-installed.md).

