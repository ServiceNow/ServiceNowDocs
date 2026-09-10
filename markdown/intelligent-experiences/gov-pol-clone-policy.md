---
title: Clone a policy
description: Start a new policy using an existing policy as a template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-pol-clone-policy.html
release: australia
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Policies, Explicit Block, Threat Response, clone]
breadcrumb: [Manage policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Clone a policy

Start a new policy using an existing policy as a template.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

Clone a policy when you want to start a new version from an existing one, without changing what's already published. The clone is a separate, independent policy; the original keeps running until you deactivate it.

For example:

-   Clone an Explicit Block policy when you want to scope the same block to a different set of users or models. You can't edit an Explicit Block policy once it's published, so cloning is the only way to change one. Once your clone is confirmed working, deactivate the original if you no longer need it.
-   Clone a Threat Response policy when you want to test a variant of its threat type, scope, or sensitivity without changing the original. You can also edit a Threat Response policy directly; see [Edit a Threat Response policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-edit-threat-response-policy.md). Once your clone is confirmed working, deactivate the original if you no longer need it.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies**.

2.  Find the policy that you want to clone.

3.  In the More actions menu, select **Clone**.

4.  Update the cloned policy's conditions.

5.  Select **Publish**.


## Result

The policy is cloned with any optional updates that you added. The original policy stays in force.

## What to do next

Once the clone is confirmed working as expected, you can deactivate the original if it's no longer needed. For details, see [Deactivate a policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-deactivate-policy.md).

