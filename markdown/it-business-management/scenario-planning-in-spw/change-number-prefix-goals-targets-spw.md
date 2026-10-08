---
title: Change the number prefix for goals and targets
description: Change the Number field prefixes for goals and targets, for example, to OBJ and KR for objectives and key results, and update existing records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/change-number-prefix-goals-targets-spw.html
release: brazil
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [number prefix, OBJ, KR, objectives and key results]
breadcrumb: [Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Change the number prefix for goals and targets

Change the Number field prefixes for goals and targets, for example, to OBJ and KR for objectives and key results, and update existing records.

## Before you begin

Role required: admin

## About this task

Each goal and target has a unique identifier in the **Number** field. By default, goal numbers start with GOAL and target numbers start with TRGT, for example, GOAL0001234 and TRGT0005678. A scheduled job applies changed prefixes to existing goals and targets.

If you renamed the Goal and Target table labels, for example, to Objective and Key Result, you can change the prefixes to match. For information about renaming the labels, see [Customize label for Goal and Target tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/customize-labels-for-goal-and-target-tables.md).

The scheduled job keeps the numeric part of each number. For example, GOAL0001234 becomes OBJ0001234. Records that already have the new prefix are skipped, so you can run the job again safely. The job doesn't run business rules or change the updated date of the records.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Number Maintenance**.

2.  Open the number record for the Goal Core \[sn\_gf\_core\_goal\] table.

3.  In the **Prefix** field, enter the new prefix for goals, for example, `OBJ`, and then select **Update**.

4.  Open the number record for the Target \[sn\_gf\_goal\_target\] table, enter the new prefix for targets in the **Prefix** field, for example, `KR`, and then select **Update**.

5.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

6.  Open the **GF - Override Goal and Target Number fields with customized prefixes** scheduled job.

7.  Select **Execute Now**.


## Result

Existing goals and targets show the new prefix in the **Number** field, and new goals and targets are numbered with the new prefix.

**Parent Topic:**[Configuring goals in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/configuring-goal-framework-apw.md)

**Related topics**  


[Customize label for Goal and Target tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/customize-labels-for-goal-and-target-tables.md)

