---
title: Edit an Explicit Block policy
description: Change who an Explicit Block policy blocks, what they're blocked from using, or its follow-up actions, without recreating the policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-pol-edit-explicit-block-policy.html
release: brazil
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, Policies, Explicit Block, edit]
breadcrumb: [Manage policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Edit an Explicit Block policy

Change who an Explicit Block policy blocks, what they're blocked from using, or its follow-up actions, without recreating the policy.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

Narrow or widen an existing block by editing the policy instead of replacing it. Editing keeps the same policy record, along with its enforcement history.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies**.

2.  Select the Explicit Block policy you want to edit.

3.  Select **Edit**.

4.  Update the policy name or description.

5.  In the Block section, update who's blocked.

    Change the type between **User** and **Department**, remove a selection, or search for another one. Leave the search field empty to apply the block to everyone.

6.  In the Block section, update what they are blocked from using.

    For an AI agent, adjust the field, operator, or value of each condition, or add and remove conditions. For a model or a domain, update the comma-separated list.

7.  In the Block section, add, remove, or update follow-up actions.

8.  Review the policy summary, then select **Publish**.


## Result

The policy takes effect with your changes at every enforcement point it applies to. Enforcement activity from before the edit stays available in the **Enforcement activity** tab.

## What to do next

Confirm the policy is working as expected by reviewing policy enforcement activity. For details, see [Reviewing policy enforcement in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-pol-reviewing-enforcement-activity.md).

To try a variant of a policy without changing what's already published, clone it instead of editing it. For details, see [Clone a policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-pol-clone-policy.md).

