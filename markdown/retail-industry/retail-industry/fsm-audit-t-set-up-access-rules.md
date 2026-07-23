---
title: Set up custom access rules
description: The Audit Admin configures a custom access rule to control which audit tasks Auditors in a specific product or business unit can see.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 2
---

# Set up custom access rules

The Audit Admin configures a custom access rule to control which audit tasks Auditors in a specific product or business unit can see.

## Before you begin

The Audit Admin performing this task must have administrator access and must work within the scope of the consuming product. Field Service for Audit must be installed.

Before starting, identify:

-   Which audit tasks the rule should apply to — for example, tasks linked to cases owned by the consuming product.
-   What determines an Auditor's access — for example, whether the Auditor has access to the related case.

## About this task

Custom access rules are scoped to the consuming product. The Audit Admin can update or remove rules at any time without affecting Field Service for Audit or other products. To also restrict access at the field level for custom fields, complete the optional steps at the end of this procedure.

## Procedure

1.  In the consuming product's scope, navigate to **System Definition &gt; Extension Instances**.

2.  Click **New**.

3.  Set **Extension Point** to the Field Service for Audit access-control extension point.

4.  Set **Order** to a unique number. Rules with lower numbers are evaluated first.

5.  Define which audit tasks the rule applies to and what access decision it returns for matching tasks.

6.  Click **Submit**.

7.  Test the rule: open a matching audit task as an Auditor who meets the criteria and confirm access, then repeat as an Auditor who does not meet the criteria and confirm the task is not visible.

8.  To restrict access to custom fields, open the access rule, update it to specify which fields it covers and what access decision to return for each, then click **Update**.

9.  Test field-level access by opening the audit task as an Auditor who should and should not see the custom field.


## Result

The Audit Admin's access rule is active. When an Auditor tries to view or update a matching audit task, the rule determines whether access is granted. Auditors who do not meet the criteria cannot see those tasks.

**Related topics**  


[How access to audit tasks works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Custom access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

