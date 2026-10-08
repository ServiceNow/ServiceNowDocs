---
title: View abandoned draft catalog request rates
description: Monitor the abandonment rate of unsubmitted draft catalog requests created by the L1 IT Service Desk AI Specialist but not submitted by requesters within a specified retention period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/catalog-cleanup-abandoned-cart-l1-sd-ai-spec.html
release: brazil
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 1
keywords: [abandoned, draft, catalog, cleanup, cart]
breadcrumb: [Use, L1 IT Service Desk AI Specialist, IT Service Management]
---

# View abandoned draft catalog request rates

Monitor the abandonment rate of unsubmitted draft catalog requests created by the L1 IT Service Desk AI Specialist but not submitted by requesters within a specified retention period.

## Before you begin

Role required: sn\_itsm\_common.sn\_service\_desk\_manager or admin

## About this task

Cart clean-up runs automatically. A scheduled job runs daily and checks for unsubmitted draft catalog requests created by the L1 IT Service Desk AI Specialist. It removes a draft when its source incident is closed, cancelled, or no longer exists. A draft whose source incident is still active is left alone, so the requester can still complete it. There's no retention period or schedule to configure — use the following step to monitor how often drafts go unsubmitted.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace**.

2.  On the Homepage, in the **L1 Service Desk AI Specialist** card, select **View details**.

3.  Select **Performance** and review the abandonment rate.

    The abandonment rate shows how many draft requests the L1 IT Service Desk AI Specialist created that requesters never submitted. If the rate is high, consider reviewing your L1 IT Service Desk AI Specialist catalog matching configuration to ensure the AI specialist is drafting requests for the correct catalog items.


