---
title: Configure Service Portal to send analytics data
description: Enable loading of the AI Search Analytics dashboard by configuring Service Portal to send analytics data.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AI Search analytics dashboard, Advanced AI Search Management Tools, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Service Portal to send analytics data

Enable loading of the AI Search Analytics dashboard by configuring Service Portal to send analytics data.

## Before you begin

The Platform Analytics Solution for Advanced AI Search Management Tools must be activated on your instance. For details on activating this solution, see [Activate the Platform Analytics Solution for Advanced AI Search Management Tools](install-adv-ais-mgmt-tools.md).

Role required: admin

## About this task

If the AI Search Analytics dashboard doesn't load, you must configure tracking of User Experience Analytics data in the Service Portal. This configuration is a prerequisite for the dashboard.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Edit the **Service Portal** record.

3.  Select **Create Analytics Settings**.

4.  On the User Experience Analytics Settings form, select the **Enable Unauthenticated User Tracking** option, then select **Update**.


## Result

The AI Search Analytics dashboard should now load correctly.

