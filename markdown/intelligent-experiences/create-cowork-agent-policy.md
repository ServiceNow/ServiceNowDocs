---
title: Create a ServiceNow Cowork agent policy
description: Create a policy to define what ServiceNow Cowork can do, which actions need human approval, and which actions are blocked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-cowork-agent-policy.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [policy, agent policy, user criteria, priority]
breadcrumb: [Configure, ServiceNow Cowork, Extending AI with external systems and providers, Enable AI Experiences]
---

# Create a ServiceNow Cowork agent policy

Create a policy to define what ServiceNow Cowork can do, which actions need human approval, and which actions are blocked.

## Before you begin

Role required: sn\_app\_cowork.admin

## About this task

A policy record sets which users the policy applies to and its priority. After you create the policy, you add components to it, such as tool gates, network rules, and sandbox rules.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Cowork** &gt; **Policies** &gt; **Cowork Agent Policy**.

2.  Select **New**.

3.  In the **Domain** field, select the domain.

4.  In the **User Criteria** field, select the user criteria record.

    The user criteria decide which users the policy applies to.

5.  In the **Description** field, enter a description of the policy.

6.  Confirm that **Active** is selected.

    An inactive policy doesn't apply to any users.

7.  In the **Priority** field, enter a value.

    When more than one policy applies to a user, the policy with the lowest priority number takes precedence. The **Default Policy** has priority 999, and new policies default to 1,000. To override the **Default Policy**, enter a number lower than 999.

8.  In the **Policy Name** field, enter the policy name.

9.  Select **Submit**.


## Result

The policy is created and applies to the users that its user criteria cover.

## What to do next

Add components to the policy. For more information, see [Configure a ServiceNow Cowork agent policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-cowork-agent-policy.md).

**Parent Topic:**[Configuring ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-cowork-configuring.md)

