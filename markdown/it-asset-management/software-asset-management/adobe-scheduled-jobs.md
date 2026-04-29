---
title: Scheduled jobs for Adobe
description: Your Adobe integration profile is set to fetch subscription and usage information automatically from the Adobe portal on a scheduled basis. If needed, you can also run the following scheduled jobs manually to get this information. Each job must be complete before starting the next one.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Scheduled jobs for Adobe

Your Adobe integration profile is set to fetch subscription and usage information automatically from the Adobe portal on a scheduled basis. If needed, you can also run the following scheduled jobs manually to get this information. Each job must be complete before starting the next one.

|Scheduled job|Run frequency|Description|
|-------------|-------------|-----------|
|SAM - Import Adobe User Subscriptions|Weekly|Imports and updates the Adobe Cloud application subscription data into the Software Asset Management application from the Adobe Admin Console. This data provides visibility into all Adobe user subscriptions and the users to whom the subscriptions are assigned in the Adobe portal. The user subscription data can be viewed in the Software Asset Workspace.|
|SAM - Optimize Adobe Subscriptions|Monthly|Adobe subscription data is pulled into the Software Asset Management application when the SAM - Import Adobe User Subscriptions scheduled job runs. When the subscription data is pulled, the SAM - Optimize Adobe Subscriptions scheduled job optimizes the Adobe Creative Cloud subscriptions based on usage.|

**Parent Topic:**[Software Asset Management references](references.md)

