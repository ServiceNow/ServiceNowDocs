---
title: Managing ServiceNow Arc policies in AI Control Tower
description: Create and manage ServiceNow Arc policies that control what Arc can do, which actions need approval, and which actions are blocked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-managing-arc-policies.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, arc policies, manage arc policies]
breadcrumb: [Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Managing ServiceNow Arc policies in AI Control Tower

Create and manage ServiceNow Arc policies that control what Arc can do, which actions need approval, and which actions are blocked.

## Managing Arc policies workflow

Every Arc user starts with the rules in the default Arc policy. To give a group different behavior, create a policy for that group and add only the rules that differ from the default.

## Default Arc policy

ServiceNow Arc includes the default Arc policy, which applies to every Arc user at priority 999. You can't edit, delete, or deactivate it, or add rules to it.

New policies start at priority 100, so a policy you create outranks the default wherever their rules conflict. Anything your policy doesn't define continues to come from the default Arc policy. For how priorities and conflicting rules interact, see [Policy stacking and precedence in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-policy-stacking-precedence.md).

## Important considerations

-   The **Arc policies** tab appears only for users with the Arc admin \[sn\_app\_arc.admin\] role, and only on instances where ServiceNow Arc is installed.
-   Changes reach the users a policy covers at their next policy sync. For how policies reach the Arc application, see .
-   Pausing a policy keeps it and its rules for later. Deleting a policy can't be undone, and it also deletes the policy's capability overrides.

