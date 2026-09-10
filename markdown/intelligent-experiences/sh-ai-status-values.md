---
title: Shadow AI status values
description: Understand what triggers each status a detected AI service can have, and what to expect from each.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sh-ai-status-values.html
release: australia
topic_type: reference
last_updated: "2026-08-20"
reading_time_minutes: 1
keywords: [status, Shadow AI]
breadcrumb: [Reference, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Shadow AI status values

Understand what triggers each status a detected AI service can have, and what to expect from each.

|Status|Description|
|------|-----------|
|**New**|The default status for any service with traffic in the last 30 days.|
|**Limited details**|Only aggregate detail is available for the service, once it has had no traffic for 30 days. See [Detected AI service details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-service-details.md). Returns to **New** automatically once new traffic arrives.|
|**Snoozed**|Deprioritizes the record for a fixed 7-day window. Set by selecting **Snooze for 7 days**, and reverts automatically once that window closes.|
|**Dismissed**|Mutes the record until new traffic arrives, rather than for a fixed window like **Snoozed**. Set by selecting **Dismiss**, and returns to **New** automatically once traffic resumes.|
|**Not Shadow AI**|Marks the finding as a misclassification rather than a real risk. Linked to the domain's entry in the registry, so changing one changes the other, which is what stops the domain from being flagged again. Set by selecting **This is not Shadow AI** on the service, or by marking the domain **Not Shadow AI** directly in the registry.|

**Parent Topic:**[AI Control Tower Shadow AI reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-reference.md)

