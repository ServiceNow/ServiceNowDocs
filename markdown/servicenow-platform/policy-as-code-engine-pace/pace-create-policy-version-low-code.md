---
title: Create a PaCE policy version using low-code
description: Create a policy version using low-code for any of your existing PaCE policies.
locale: en-US
release: australia
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create PaCE policy versions, Manage PaCE policy versions, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Create a PaCE policy version using low-code

Create a policy version using low-code for any of your existing PaCE policies.

## Before you begin

Role required: sn\_pace.code\_editor

## About this task

The low-code function enables you to write policies using simple UI elements by defining conditions for the policy to determine if it’s compliant or non-compliant. If the **Is low code** check box is selected when you create a policy version, the **Policy Builder** and **Test Playground** tabs will automatically have the Policy logic page set to low-code.

You can switch to the Policy Script to create a policy using JavaScript by selecting the **Switch to code editor** button, but you’ll be unable to switch back to low-code. For more information on how to write PaCE policies using JavaScript, see [How to write and test PaCE policies](../concept/pace-write-test-policies.md).

**Note:** Policy Builder works best in Google Chrome and Firefox.

## Procedure

1.  Navigate to **Policies** &gt; **My Policies**.

2.  Select the policy name for the policy that you want to add a new version to.

3.  In the Policy Details page, select the **Versions** tab.

4.  Select **New**.

    The New version page appears.

5.  Select the New blank version tile or an existing policy template, then **Create**.

    Templates can be filtered by most used, alphabetically, state, and type. By default, inactive templates are hidden.

6.  Fill in the **Description** field.

    **Note:** By default, the **Is low code** check box is automatically selected.

7.  Select **Save**.


## Result

The policy version is saved with an assigned number according to the policy numbering and will enable you to set the conditions using low-code.

