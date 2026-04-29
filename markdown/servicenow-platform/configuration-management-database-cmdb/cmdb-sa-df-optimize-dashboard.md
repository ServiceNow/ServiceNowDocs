---
title: Manage Data Foundations advisor scope in CMDB success advisor
description: Manage the scope of your advisor for Data Foundations by editing principal classes in CMDB success advisor to support your targeted Data Foundations outcomes.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up advisor, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage Data Foundations advisor scope in CMDB success advisor

Manage the scope of your advisor for Data Foundations by editing principal classes in CMDB success advisor to support your targeted Data Foundations outcomes.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

Control which principal classes are included in your Data Foundations advisor dashboard in CMDB success advisor. You can add or remove entire CI class group or fine-tune the selection by including or excluding specific classes within a group.

For guidance on choosing the right classes, see the [Guidance on designating principal classes in the CMDB \[KB2707240\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2707240) article in the Now Support Knowledge Base.

**Note:** Principal classes that are currently in use by CMDB success advisor for HAM can't be edited here. To edit those classes in Data Foundations, you must first remove them from the HAM advisor. See [Manage HAM advisor scope in CMDB success advisor](cmdb-sa-ham-optimize-dashboard.md).

## Procedure

1.  On the CMDB success advisor landing page, select **Edit principal classes** within the Data Foundations card.

    See [Viewing the CMDB success advisor landing page](../concept/cmdb-sa-landing-page.md).

2.  In the Edit principal classes dialog box, add or remove CI classes to update your principal class selection.

    |Purpose|Action|Data coverage|
    |-------|------|-------------|
    |Add a CI class group|Select the check box for the group to include all its CI classes.|Includes all CI classes associated with the selected group.|
    |Expand CI class selection|Select **&gt;** to expand a group, then select check boxes for specific CI classes.|Includes only the selected CI classes associated with a group.|
    |Narrow down CI class selection|Select **&gt;** to expand a group, then clear check boxes for specific CI classes.|Excludes only the CI classes cleared from a group.|
    |Remove a CI class group|Clear the check box for the CI class group.|Excludes all CI classes associated with the removed group.|
    |Remove a selected CI class|Select the X icon next to the category in the **Selected classes** column.|CI class is removed from scope.|

3.  Select **Save** to apply the changes.


## Result

The CMDB success advisor for Data Foundations dashboard is updated to reflect the data based on the principal class selection.

