---
title: Enable search-based auto-complete suggestions in AI Search for Next Experience
description: Run a scheduled job to make search-based auto-complete suggestions available in AI Search for Next Experience.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-03"
reading_time_minutes: 2
breadcrumb: [Configuring AI Search for Next Experience, AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable search-based auto-complete suggestions in AI Search for Next Experience

Run a scheduled job to make search-based auto-complete suggestions available in AI Search for Next Experience.

## Before you begin

The AI Search for Next Experience ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install AI Search for Next Experience](install-ais-next-experience-app.md).

You only need to perform this task if you installed AI Search for Next Experience 3.x on a San Diego instance that you then upgraded to Tokyo or a later release.

Role required: admin

## About this task

If you install AI Search for Next Experience 3.x on a San Diego instance and then upgrade to Tokyo or a later release, the new search-based auto-complete suggestion types introduced in Tokyo aren't automatically enabled in the **\[AIS\] Next Experience Search Configuration** search application configuration used by global search.

To enable the new search-based auto-complete suggestion types in AI Search for Next Experience and remove the legacy suggestion types that they replace, administrators can run a scheduled job.

Running the scheduled job adds these auto-complete suggestion types to the **\[AIS\] Next Experience Search Configuration** search application configuration, making them available for global search:

-   Search-based Suggested Results Reader Group for \[AIS\] Next Experience Search Configuration
-   User History Reader Group for \[AIS\] Next Experience Search Configuration

The scheduled job removes these two legacy auto-complete suggestion types from the **\[AIS\] Next Experience Search Configuration** search application configuration, making them unavailable for global search:

-   Suggested Query Reader Group for \[AIS\] Next Experience Search Configuration
-   Suggested Result Reader Group for \[AIS\] Next Experience Search Configuration

To learn more about auto-complete suggestion types in AIS applications, see [Auto-complete suggestions in AI Search applications](../concept/auto-complete-ais.md#).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the **Enable search-based suggestions** scheduled job record.

3.  Select **Execute Now**.


## Result

The scheduled job adds these auto-complete suggestion types to the **\[AIS\] Next Experience Search Configuration** search application configuration:

-   Search-based Suggested Results Reader Group for \[AIS\] Next Experience Search Configuration
-   User History Reader Group for \[AIS\] Next Experience Search Configuration

The scheduled job removes these auto-complete suggestion types from the **\[AIS\] Next Experience Search Configuration** search application configuration:

-   Suggested Query Reader Group for \[AIS\] Next Experience Search Configuration
-   Suggested Result Reader Group for \[AIS\] Next Experience Search Configuration

Global search uses the updated set of auto-complete suggestion types.

**Parent Topic:**[Configuring AI Search for Next Experience](../concept/configuring-ais-next-experience.md)

