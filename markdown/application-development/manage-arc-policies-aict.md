---
title: Manage Arc agent policies in AI Control Tower
description: Create and manage Arc agent policies and their rules in AI Control Tower, so you govern Arc in the same place as the rest of your AI systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/manage-arc-policies-aict.html
release: australia
topic_type: concept
last_updated: "2026-10-29"
reading_time_minutes: 1
keywords: [AI Control Tower, agent policy, Arc policies, policy authoring]
breadcrumb: [Configure, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Manage Arc agent policies in AI Control Tower

Create and manage Arc agent policies and their rules in AI Control Tower, so you govern Arc in the same place as the rest of your AI systems.

You manage Arc agent policies on the **Arc policies** tab in AI Control Tower, under **Govern** &gt; **Policies**.

## Policies

A policy controls what Arc can do for the users it covers. You create, edit, and delete policies, and set each one's priority. When more than one policy covers a user, priority decides which policy's rules take effect. You can't edit or delete the **Default Policy**, or add rules to it, but a policy with a lower priority number can override it.

For more information, see [Managing Arc policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-managing-arc-policies.md).

## Policy rules

Each policy holds its rules in seven groups: tool gates, approval patterns, network rules, file type rules, sandbox rules, connector scopes, and capability overrides. Tool gates and approval patterns decide whether an action runs, waits for approval, or is blocked. The other rules limit what an action can reach once it runs. Rules can be shared across policies, so removing a rule from one policy doesn't affect the others.

For more information, see [Working with Arc policy rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-working-with-arc-policy-rules.md).

**Parent Topic:**[Configuring ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-configuring.md)

