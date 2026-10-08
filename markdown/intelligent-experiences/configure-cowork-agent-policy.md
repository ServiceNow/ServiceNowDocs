---
title: Configure a ServiceNow Cowork agent policy
description: Add tool gates, approval patterns, network rules, sandbox rules, capability overrides, connector scopes, and file type rules to a policy to control what Cowork can do for the users the policy applies to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/configure-cowork-agent-policy.html
release: brazil
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [policy, tool gates, approval patterns, network rules, sandbox rules, capability overrides, connector scopes, file type rules]
breadcrumb: [Configure, ServiceNow Cowork, Extending AI with external systems and providers, Enable AI Experiences]
---

# Configure a ServiceNow Cowork agent policy

Add tool gates, approval patterns, network rules, sandbox rules, capability overrides, connector scopes, and file type rules to a policy to control what Cowork can do for the users the policy applies to.

## Before you begin

Create the policy. For more information, see [Create a ServiceNow Cowork agent policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-cowork-agent-policy.md).

Role required: sn\_app\_cowork.admin

## About this task

Each tab on a policy record links existing rule records to the policy. Add only the components you need. The number on each tab shows how many records are linked to the policy.

You can't edit or remove the predefined rules in the **Default Policy**, but you can add new ones.

When you use a policy to override the **Default Policy**, add only the rules you want to change. Anything you don't add keeps coming from the **Default Policy**.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Cowork** &gt; **Policies** &gt; **Cowork Agent Policy**.

2.  Open the policy you want to configure.

3.  Add a tool gate.

    1.  Select the **Policy Tool Gates** tab, and then select **New**.

    2.  In the **Tool Gate** field, select the tool gate.

    3.  In the **Domain** field, select the domain.

    4.  Select **Submit**.

4.  Add an approval pattern.

    1.  Select the **Policy Patterns** tab, and then select **New**.

    2.  In the **Approval Pattern** field, select the approval pattern.

    3.  In the **Domain** field, select the domain.

    4.  Select **Submit**.

5.  Add a network rule.

    1.  Select the **Policy Network Rules** tab, and then select **New**.

    2.  In the **Network Rule** field, select the network rule.

    3.  In the **Domain** field, select the domain.

    4.  Select **Submit**.

6.  Add a sandbox rule.

    1.  Select the **Policy Sandbox Rules** tab, and then select **New**.

    2.  In the **Sandbox Rule** field, select the sandbox rule.

    3.  In the **Domain** field, select the domain.

    4.  Select **Submit**.

7.  Add a capability override.

    1.  Select the **Capability Overrides** tab, and then select **New**.

    2.  In the **Capability** field, select the capability.

    3.  In the **Override Value** field, enter the value for the capability.

    4.  In the **Description** field, enter a description of the override.

    5.  In the **Domain** field, select the domain.

    6.  Confirm that **Active** is selected.

    7.  Select **Submit**.

8.  Add a connector scope.

    1.  Select the **Policy Connector Scopes** tab, and then select **New**.

    2.  In the **Connector Scope** field, select the connector scope.

    3.  Select **Active**.

        The **Active** check box is cleared by default. If you don't select it, the connector scope doesn't take effect.

    4.  In the **Domain** field, select the domain.

    5.  Select **Submit**.

9.  Add a file type rule.

    1.  Select the **Policy File Type Rules** tab, and then select **New**.

    2.  In the **File Type Rule** field, select the file type rule.

    3.  In the **Domain** field, select the domain.

    4.  Select **Submit**.

10. Select **Update**.


## Result

The policy includes the components you added, and Cowork enforces them for every user that the policy's user criteria covers.

**Parent Topic:**[Configuring ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-cowork-configuring.md)

