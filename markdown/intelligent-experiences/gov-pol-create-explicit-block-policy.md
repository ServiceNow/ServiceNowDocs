---
title: Create an Explicit Block policy
description: Stop a user, group, department, or everyone in your organization from using a specific AI agent, model, or domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-pol-create-explicit-block-policy.html
release: australia
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Policies, Explicit Block, Control Framework, block]
breadcrumb: [Manage policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Create an Explicit Block policy

Stop a user, group, department, or everyone in your organization from using a specific AI agent, model, or domain.

## Before you begin

To enforce a block on an external system, confirm the corresponding connector is already configured. External systems include cloud AI agents and devices running Agent Client Collector \(ACC\). See [Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-security-connections.md).

Role required: sn\_ai\_governance.ai\_steward

## About this task

An Explicit Block policy stops a user, group, department, or everyone in your organization from using a specific AI agent, model, or domain. Once published, it stays in effect until you deactivate it; there's no pause or in-between state.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies**.

2.  Select **Create policy**.

3.  Enter a name and description of this policy.

4.  In the Policy type section, select **An explicit block**.

5.  In the Block section, define who's blocked.

    For example, select a type, such as **User**, then search for someone specific. Leave the search field empty to apply the block to everyone.

6.  In the Block section, define what they're blocked from using.

<table><thead><tr><th align="left" id="d322205e166">

Option

</th><th align="left" id="d322205e169">

Description

</th></tr></thead><tbody><tr><td id="d322205e175">

**AI agent**

</td><td>

1.  In the What field, select **AI agent**.
2.  Identify the AI agent that you want to block by building a condition using a field, an operator, and a value. For example, **Asset** \| **is** \| **ACME Agent**.
3.  Combine multiple conditions with **and** or **or**, or select **Add group** for another set of conditions.


</td></tr><tr><td id="d322205e217">

**Model**

</td><td>

1.  In the What field, select **Model**.
2.  Enter one or more models in a comma-separated list.


</td></tr><tr><td id="d322205e238">

**Domain**

</td><td>

1.  In the What field, select **Domain**.
2.  Enter one or more domains in a comma-separated list.


</td></tr></tbody>
</table>7.  In the Block section, add a follow-up action.

    A follow-up fires only when the policy actually blocks an attempt, not just because it's published.

    1.  Select **+Add follow-up**.

    2.  Select **Notify**.

    3.  Search or enter the user to notify.

8.  Review the policy, then select **Publish**.


## Result

The policy takes effect at every enforcement point it applies to. If enforcement depends on an agent installed on a device, such as ACC, the block takes effect when the policy syncs to that device.

## What to do next

Confirm the policy is working as expected by reviewing the policy enforcement activity. For details, see [Reviewing policy enforcement in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-reviewing-enforcement-activity.md).

You can't edit a policy once it's published. To change who or what it blocks, clone the policy, make your changes in the cloned policy, then deactivate the original once your clone is confirmed working, if you no longer need it. For details, see [Clone a policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-clone-policy.md).

