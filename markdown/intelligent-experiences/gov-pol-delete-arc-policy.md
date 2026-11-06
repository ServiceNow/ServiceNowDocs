---
title: Delete an Arc policy
description: Return a group of users to the behavior of their remaining ServiceNow Arc policies, such as the default Arc policy, by deleting a policy you no longer need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-delete-arc-policy.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, delete arc policy, arc policies]
breadcrumb: [Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Delete an Arc policy

Return a group of users to the behavior of their remaining ServiceNow Arc policies, such as the default Arc policy, by deleting a policy you no longer need.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

Deleting a policy also removes its links to rules and deletes its capability overrides. Rules that other policies link to stay available to those policies. You can't undo a deletion, and you can't delete the default Arc policy.

To stop enforcing a policy but keep it for later, clear its **Active** option instead. For details, see [Edit an Arc policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-edit-arc-policy.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy you want to delete.

3.  Select **Delete**.

4.  In the confirmation dialog box, select **Delete**.


## Result

The policy is deleted. At their next policy sync, the users it covered get the rules from their remaining policies.

