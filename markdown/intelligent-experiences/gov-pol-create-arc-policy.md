---
title: Create an Arc policy
description: Give a team its own ServiceNow Arc rules by creating a policy that applies to the users you choose and takes precedence over the default Arc policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-create-arc-policy.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, create arc policy, arc policies, user criteria, policy priority]
breadcrumb: [Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create an Arc policy

Give a team its own ServiceNow Arc rules by creating a policy that applies to the users you choose and takes precedence over the default Arc policy.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

A policy sets who it applies to and how much weight its rules carry. You add rules, such as tool gates and network rules, after you create the policy.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select **+ Create policy**.

3.  On the form, fill in the fields.

<table id="table_create_arc_policy_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Policy Name**

</td><td>

Name that identifies the policy. Name it for the audience and intent, for example, Service desk analysts standard.

</td></tr><tr><td>

**User Criteria**

</td><td>

User criteria record that decides which users the policy applies to. If you leave this field empty, the policy applies to every Arc user.

</td></tr><tr><td>

**Priority**

</td><td>

Weight of this policy when more than one policy applies to the same user. A lower value indicates higher priority. New policies start at 100.

 Enter a whole number from 0 through 9999. For how priority works, see [Policy stacking and precedence in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-policy-stacking-precedence.md).

</td></tr><tr><td>

**Active**

</td><td>

Option to enforce the policy. Selected by default. An inactive policy doesn't apply to any users.

</td></tr><tr><td>

**Description**

</td><td>

Purpose of the policy, for other administrators who review it later.

</td></tr></tbody>
</table>4.  Select **Create policy**.


## Result

An active policy takes effect for matching users at their next policy sync. Wherever this policy has no rule of its own, those users keep the rule from the default Arc policy.

## Example: Give contractors stricter rules than your engineers

Your engineering policy, at priority 100, covers every engineer, including contractors. You want contractors to get stricter rules wherever the two policies conflict. Create a policy with the following values:

-   **Policy Name**: `Contractors restricted`
-   **User Criteria**: the user criteria record that matches your contractor group
-   **Priority**: `50`
-   **Description**: `Stricter rules for contractors than the engineering policy.`

Because 50 is lower than 100, the contractor policy wins wherever its rules conflict with the engineering policy, and both policies outrank the default Arc policy at 999. For anything the contractor policy doesn't define, contractors keep the engineering policy's rules.

## What to do next

Configure the policy by adding one or more rules. For details, see [Working with Arc policy rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-working-with-arc-policy-rules.md).

