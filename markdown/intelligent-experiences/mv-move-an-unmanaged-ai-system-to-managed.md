---
title: Move an unmanaged AI system to managed
description: When an AI system is unmanaged, its value data stops appearing on the value dashboard and its value templates are unpublished. Move it back to managed in AI Control Tower to restore value tracking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mv-move-an-unmanaged-ai-system-to-managed.html
release: brazil
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [AI Control Tower, move to managed, unmanaged AI system, AI asset inventory]
breadcrumb: [Value, Configure, Measure AI system, Measure AI systems, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Move an unmanaged AI system to managed

When an AI system is unmanaged, its value data stops appearing on the value dashboard and its value templates are unpublished. Move it back to managed in AI Control Tower to restore value tracking.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

The value dashboard shows insights only for managed AI systems. Move an unmanaged AI system to managed when you want to track its value again.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**.

2.  Navigate to **Inventory** &gt; **Assets**.

    All AI assets are listed.

3.  Select the check box for the AI system that you want to move to managed.

    To find an AI system, filter the list by **Display name**.

4.  From the **Action** list, select **Move to Managed**.

    \[Omitted image "mv-move-to-managed.png"\] Alt text: Action menu in AI Control Tower with the Move to Managed option highlighted.

    A confirmation message appears, confirming the AI system is now managed.


## Result

The AI system moves to the managed AI asset inventory. Its value templates return to the **Published** state, and its value data starts appearing on the value dashboard again.

The template mappings of the AI system appear in the **Templates mapping** list.

**Related topics**  


[Value tracking for managed and unmanaged AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mv-value-tracking-for-managed-and-unmanaged-ai-systems.md)

