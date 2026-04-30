---
title: Populate search suggestions in the mobile apps
description: If you are upgrading from a previous release, run a script to populate search suggestions with data from a platform search table to provide search suggestions to your users. Alternatively, you can wait until users search for keywords instead of running this script.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enable global search, Global search, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Populate search suggestions in the mobile apps

If you are upgrading from a previous release, run a script to populate search suggestions with data from a platform search table to provide search suggestions to your users. Alternatively, you can wait until users search for keywords instead of running this script.

## Before you begin

Role required: admin

In new instances, the search suggestions are enabled by default. In upgraded instances, you must enable the search suggestions. For more information, see [Enable search suggestions](https://www.servicenow.com/docs/access?context=enable-search-suggestions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## About this task

The ServiceNow AI Platform collects search data and analytics that generate search suggestions. If you are upgrading from a previous release, the search analytics do not contain any data yet. To immediately provide suggestions to your users, you can populate the search suggestions using knowledge, catalog, and user search records from the Text Searches \[text\_search\] table.

Search suggestions improve over time as more people use the app. Search Suggestions is a ServiceNow AI Platform feature. For more information, see [Search Suggestions](https://www.servicenow.com/docs/access?context=search-suggestions-overview&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Warning:** Populating search suggestions can be a resource-intensive task that may take a while to complete. Do not run this script during peak hours. Populating search suggestions is not supported on domain-separated instances.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the **Populate Suggestions to avoid Cold Start - NowMobile App** scheduled job.

3.  Activate the record and select **Execute Now**.

    Running this scheduled job populates the Search Events \[sys\_search\_event\], Search Source Events \[sys\_search\_source\_event\], and Search Suggestions \[sys\_search\_suggestion\] tables with records from the Text Searches \[text\_search\] table.


## Result

Users see suggestions when they start typing in a search field in the Now Mobile app.

