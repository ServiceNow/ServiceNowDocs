---
title: Edit a rule in an Arc policy
description: Adjust how an existing ServiceNow Arc rule behaves, such as a gate mode, a pattern's priority, or a network destination, without recreating it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-edit-arc-policy-rule.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, edit arc policy rule, edit tool gate, edit approval pattern, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Edit a rule in an Arc policy

Adjust how an existing ServiceNow Arc rule behaves, such as a gate mode, a pattern's priority, or a network destination, without recreating it.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

Editing a shared rule changes it for every policy that links it. To change a shared rule for one policy only, create a rule on the policy instead, and then remove the shared one from it.

The **Active** and **Approval gate** options on a connector scope are the exception. They belong to the current policy only.

You can't edit rules in the default Arc policy.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy that contains the rule.

3.  Select the tab for the type of rule.

    To reach **Sandbox rules**, **Connector scopes**, or **Capability overrides**, select **More** first.

4.  Select the rule's name.

    The rule opens in a read-only side panel.

5.  Select **Edit**.

6.  Update the rule as needed.

7.  Select **Save**.


## Result

The updated rule reaches the users of every policy that links the rule at their next policy sync.

