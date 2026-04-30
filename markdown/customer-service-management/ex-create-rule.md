---
title: Create a rule from the Case context record
description: Create a rule to show recommendations for active cases that meet the condition specified in this rule.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Example: Link the similar major case to the current case, Example configurations of recommended actions, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a rule from the Case context record

Create a rule to show recommendations for active cases that meet the condition specified in this rule.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, admin

## About this task

New rules can only be created from context records.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.

2.  Select the Case context.

    The Case context is available by default.

3.  In the Rules related list, select **New**.

4.  In the **Name** field, enter `Active rule`.

5.  In the **Roles** field, select the Edit User Roles ![Edit User Roles icon](../image/icon-pencil-ac.png) icon and then select Customer service agent \[sn\_customerservice\_agent\] and Consumer service agent \[sn\_customerservice.consumer\_agent\].

    The selected user roles can see recommendations for this rule.

6.  Select **Done** on the Roles pop-up window.

7.  In the **Condition** field, use the condition builder to add the condition "Active \| is \| true".

    Agents can see recommendations for the records in the context table that meet this criteria.

8.  In the **Field affecting this rule** field, select Short description from the slush bucket.

9.  Select **Submit**.


