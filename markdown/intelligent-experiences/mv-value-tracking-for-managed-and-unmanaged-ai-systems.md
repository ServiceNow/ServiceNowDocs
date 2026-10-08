---
title: Value tracking for managed and unmanaged AI systems
description: The AI Control Tower value dashboard shows value and usage only for AI systems that were managed during the reporting period. Value realized while an AI system was managed stays on the dashboard, even after the AI system becomes unmanaged.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mv-value-tracking-for-managed-and-unmanaged-ai-systems.html
release: brazil
topic_type: concept
last_updated: "2026-09-23"
reading_time_minutes: 3
keywords: [managed AI system, unmanaged AI system, value dashboard, value template]
breadcrumb: [Value, Explore, Measure AI system, Measure AI systems, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Value tracking for managed and unmanaged AI systems

The AI Control Tower value dashboard shows value and usage only for AI systems that were managed during the reporting period. Value realized while an AI system was managed stays on the dashboard, even after the AI system becomes unmanaged.

## Value data for unmanaged AI systems

An AI system that changes from managed to unmanaged continues to appear on the value dashboard. AI Control Tower counts its value and usage only for the dates when the AI system was managed. Data from after the AI system became unmanaged isn't included in the total value.

For the date range when the AI system was managed, the AI system name on the value dashboard is a link that opens the AI system record.

Unmanaged AI system example.

Incident Summarization is a managed AI system that an AI steward marks as unmanaged on January 15. When you view the value dashboard for the 30 days of January, the dashboard shows the following.

-   All managed AI systems, including Incident Summarization.
-   Value and usage data for Incident Summarization from January 1 through January 15 only.
-   A link to Incident Summarization for its managed period.

**Important:**

If your organization uses a ServiceNow SKU and you upgrade AI Control Tower, review your AI systems and mark those you would like to track as managed. For more information, see [Move an unmanaged AI system to managed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mv-move-an-unmanaged-ai-system-to-managed.md).

## Value template tab

When an AI system is unmanaged, the **Value template** tab shows its value templates as unmapped. Actions that change the AI system or its value templates aren't available.

|Field|Value for an unmanaged AI system|
|-----|--------------------------------|
|**Lifecycle status**|**Unmanaged**|
|**Value template status**|**Unmapped**. Applies to all templates that were previously mapped, including published and draft templates.|

## Value templates for unmanaged AI system

When an AI system is set to unmanaged, AI Control Tower automatically unmaps the AI system from all of its value templates. Templates that were previously mapped, whether published or draft, show the **Unmapped** status. The lifecycle status of the AI system changes to **Unmanaged**. Value and usage for the period when the AI system was unmanaged aren't calculated.

While the AI system is unmanaged, you can't add, edit, reject, or delete value templates or the AI system from the **Value template** tab.

## Value data when an AI system is managed again

When an AI steward changes an unmanaged AI system back to managed, AI Control Tower does the following.

-   Maps the AI system to the same value templates that it was mapped to before.
-   Restores each template to its previous status.

    **Important:** Mappings that were in draft status when the AI system was set to unmanaged aren't restored.

-   Resumes value and usage calculations from the date the AI system is set to managed again.

For ServiceNow SKUs, when you mark an AI system as managed again, AI Control Tower resumes value and usage calculation. It fills in the value data for the time the AI system was unmanaged. By default, it fills in up to 30 days. To fill in a longer period, change the date range of the historical job. For more information, see [Set look back date range for unmanaged AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mv-set-date-range-for-historical-job.md).

Value data isn't filled in for enterprise AI systems. When an enterprise AI system is marked as unmanaged, its connectors are disabled and no usage data is collected for that period.

**Related topics**  


[Move an unmanaged AI system to managed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mv-move-an-unmanaged-ai-system-to-managed.md)

