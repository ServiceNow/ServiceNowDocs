---
title: Change the number prefix for goals and targets
description: Change the prefix of the Number field for goals and targets, for example, from GOAL and TRGT to OBJ and KR when your organization uses objectives and key results, and apply the new prefix to existing records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/goal-framework/change-number-prefix-goals-targets.html
release: brazil
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [number prefix, OBJ, KR, objectives and key results]
breadcrumb: [Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Change the number prefix for goals and targets

Change the prefix of the Number field for goals and targets, for example, from GOAL and TRGT to OBJ and KR when your organization uses objectives and key results, and apply the new prefix to existing records.

## Before you begin

Role required: admin

## About this task

Each goal and target has a unique identifier in the **Number** field. By default, goal numbers start with GOAL and target numbers start with TRGT, for example, GOAL0001234 and TRGT0005678. You can change the prefixes, for example, to OBJ and KR, and then run a scheduled job that applies the new prefixes to existing goals and targets.

The scheduled job keeps the numeric part of each number. For example, GOAL0001234 becomes OBJ0001234. Records that already have the new prefix are skipped, so you can run the job again safely. The job does not run business rules or change the updated date of the records.

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

**Parent Topic:**[Configuring Goal Framework and Goal Framework for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/configuring-goal-framework.md)

