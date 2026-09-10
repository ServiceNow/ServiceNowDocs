---
title: Create a Threat Response policy
description: Automatically contain an AI agent when a specific threat is detected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-pol-create-threat-response-policy.html
release: australia
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Policies, Threat Response, Control Framework, containment]
breadcrumb: [Manage policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Create a Threat Response policy

Automatically contain an AI agent when a specific threat is detected.

## Before you begin

Confirm the connector for each AI agent runtime platform you want to cover is active. See [Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-security-connections.md).

Role required: sn\_ai\_governance.ai\_steward

## About this task

A Threat Response policy watches for a specific threat type. Once conditions matching that type are detected, it automatically contains the affected agent instead of waiting for someone to notice and act.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies**.

2.  Select **Create policy**.

3.  Enter a name and description of this policy.

4.  In the Policy type section, select **A threat response**.

5.  In the On threat section, select the threat type the policy watches for, such as **Prompt Injection**.

    For the full list, see [Threat types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-threat-categories.md).

6.  In the On threat section, define which agents the policy covers.

    Build a condition from a field, an operator, and a value, such as a specific agent or a platform vendor. Combine multiple conditions with **and** or **or**, or select **Add group** for another set of conditions.

7.  In the On threat section, set the sensitivity.

    For example, trigger the policy **on every detection**, or only once detections cross a threshold you define.

8.  In the Do this section, add one or more follow-up actions.

    A follow-up fires only when the policy actually blocks an attempt, not just because it's published.

<table id="choicetable_tqh_bxr_jkc"><thead><tr><th align="left" id="d162968e206">

Follow-up action

</th><th align="left" id="d162968e209">

Description

</th></tr></thead><tbody><tr><td id="d162968e215">

**Create a ticket**

</td><td>

1.  Select **+Add follow-up**.
2.  Select **Create a ticket**.
3.  Select the assignment group that will receive the ticket.


</td></tr><tr><td id="d162968e242">

**Notify**

</td><td>

1.  Select **+Add follow-up**.
2.  Select **Notify**.
3.  Search or enter the user to notify.


</td></tr></tbody>
</table>9.  Review the policy summary, then select **Publish**.


## Result

The policy runs as soon as a matching threat is detected. The affected agent is taken offline and stays offline until it's reinstated from Security. For details, see [Contain AI agents manually using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md).

## What to do next

Confirm the policy is working as expected by reviewing policy enforcement activity. For details, see [Reviewing policy enforcement in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-reviewing-enforcement-activity.md).

You can edit a Threat Response policy directly to change its threat type, scope, sensitivity, or follow-up actions. For details, see [Edit a Threat Response policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-edit-threat-response-policy.md). Alternatively, clone the policy to test a variant without changing the original, then deactivate the original once your clone is confirmed working, if you no longer need it. For details, see [Clone a policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-clone-policy.md).

