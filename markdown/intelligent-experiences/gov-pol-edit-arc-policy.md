---
title: Edit an Arc policy
description: Change who an ServiceNow Arc policy applies to, how much weight it carries, or whether it's enforced, without rebuilding its rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-edit-arc-policy.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, edit arc policy, arc policies, user criteria, policy priority]
breadcrumb: [Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Edit an Arc policy

Change who an ServiceNow Arc policy applies to, how much weight it carries, or whether it's enforced, without rebuilding its rules.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

Editing a policy changes its settings, such as its user criteria and priority. To change the rules inside the policy, edit them from the policy's tabs instead. For details, see [Edit a rule in an Arc policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-edit-arc-policy-rule.md).

You can't edit the default Arc policy. To pause a policy without deleting it, clear its **Active** option.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy you want to edit.

3.  Select **Edit**.

4.  Change the policy's **Policy Name**, **User Criteria**, **Priority**, **Active**, or **Description** values.

    A change to **User Criteria** or **Priority** changes which users get this policy's rules and which rules win conflicts. For what each field does, see [Create an Arc policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-create-arc-policy.md).

5.  Select **Save**.


## Result

The policy page shows the updated settings, and the change reaches the users the policy covers at their next policy sync.

