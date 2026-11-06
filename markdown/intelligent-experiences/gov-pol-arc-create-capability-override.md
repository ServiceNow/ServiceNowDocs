---
title: Create a capability override for an Arc policy
description: Turn a ServiceNow Arc feature on or off, or change a limit, for the users a policy covers without changing the default for anyone else.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-arc-create-capability-override.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 3
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, capability override, auto mode, mcp lockdown, max task duration, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create a capability override for an Arc policy

Turn a ServiceNow Arc feature on or off, or change a limit, for the users a policy covers without changing the default for anyone else.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

Capabilities are feature switches and numeric limits with a default value. An override replaces that value for the users the policy covers. Unlike other rules, each override belongs to one policy.

When more than one policy overrides the same capability for a user, the policy with the lowest priority number wins. If those policies have the same priority, an on/off capability resolves to off, a number resolves to the lowest value, and a text value applies only when every policy sets the same value. Otherwise, the capability keeps its default.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy you want to update.

3.  Select **More**.

4.  Select **Capability overrides**.

5.  Select **Create capability overrides**.

    If the policy already has capability overrides, select **+ Add rule** instead.

6.  On the form, fill in the fields.

<table id="table_capability_override_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Policy**

</td><td>

Policy the override belongs to. The field starts empty, so search for and select the policy you're updating.

</td></tr><tr><td>

**Active**

</td><td>

Option to apply the override. Selected by default. When you clear it, the capability reverts to its default for the users this policy covers.

</td></tr><tr><td>

**Override Value**

</td><td>

Value that replaces the default. It must match the capability's type. Enter `true` or `false` for an on/off capability, a whole number for a limit, or text for a text capability.

</td></tr><tr><td>

**Capability**

</td><td>

Capability to override. Only capabilities that allow a policy override appear in the list.

 -   **__auto\_approval__**

Whether users can switch a chat to auto mode, where an AI safety classifier reviews calls to tools with an **Auto Approval** tool gate instead of asking the user. When off, those tools ask for approval the same way as **Require Approval**. Default is false.

-   **__sub\_agents__**

Whether the agent can start sub-agents to run parts of a task in parallel. Default is true.

-   **__mcp\_lockdown__**

Whether users are kept from adding custom MCP servers or changing the URL or transport of existing ones. Users can still update credentials and connect the MCP servers that ship with Arc. Default is false.

-   **__max\_task\_duration\_secs__**

How long one agent run can take, in seconds. When the limit is reached, the agent writes one summary and stops. Enter 0 to remove the limit. Doesn't apply to sub-agents. Default is 1200, which is 20 minutes.

-   **__feedback\_url__**

Link the desktop application's send feedback action opens, such as a Teams channel. Leave it empty to hide the action. Default is empty.

-   **__servicenow__, __microsoft365__, __github__**

Whether the connector is available to the users the policy covers. Default is true.

</td></tr><tr><td>

**Description**

</td><td>

Reason for the override, kept for your audit trail.

</td></tr><tr><td>

**Domain**

</td><td>

Domain that owns the override. Keep the default unless your instance uses domain separation.

</td></tr></tbody>
</table>7.  Select **Create**.


## Result

The override appears on the policy's **Capability overrides** tab, and the new value applies to the users the policy covers at their next policy sync.

## Pilot auto mode with one team

You want your support engineering team to try auto mode before it's offered to everyone. On a policy whose user criteria cover that team, create a capability override with the following values:

-   **Policy**: the team's policy
-   **Capability**: **auto\_approval**
-   **Override Value**: `true`
-   **Description**: `Auto mode pilot for support engineering.`

On/off capabilities take `true` or `false`.

The override makes auto mode available, but it has no effect until at least one tool gate that applies to the team is set to **Auto Approval**. Set the gates for the tools the team uses most, and leave hard gate approval patterns in place for actions that must wait for a person.

## What to do next

If you turned on **auto\_approval**, set at least one tool gate to **Auto Approval**. Auto mode is offered to users only when both are in place. For details, see [Create a tool gate for an Arc policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-tool-gate.md).

