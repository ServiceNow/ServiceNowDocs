---
title: Get started with AI search in upgraded instances
description: Enable intelligent query features that help agents to quickly find the required answers in ITSM Mobile Agent in upgraded instances.
locale: en-US
release: xanadu
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [AI Search in ITSM Mobile Agent, Explore, ITSM Mobile Agent, IT Service Management]
---

# Get started with AI search in upgraded instances

Enable intelligent query features that help agents to quickly find the required answers in ITSM Mobile Agent in upgraded instances.

## Before you begin

Role required: ais\_admin or admin

## About this task

You can get started with AI search in upgraded instances by using the AI search configuration in the base system.

## Procedure

1.  Enable AI search.

    1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Status**.

    2.  Click **Request AI Search**.

2.  Activate the AI Search Index Sources \(Id: com.glide.ais.index\_sources\) plugin.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

    2.  Search for the AI Search Index Sources \(Id: com.glide.ais.index\_sources\) plugin.

    3.  Click **Activate**.

3.  Index all search sources.

    1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

    2.  Select all data sources.

    3.  From the **Actions on selected rows** drop down, select **Index All Tables**.

4.  Publish the AI search-related search profile.

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

    2.  Click **ITSM Mobile Agent Search Profile**.

    3.  Click **Publish**.

5.  Select the AI search-related search application configuration for the global search record.

    1.  Navigate to **sys\_sg\_global\_search.list**.

    2.  From the list of search configurations, Click **ITSM Mobile Agent Search**.

    3.  For the **Search Application Configuration** field, select **\[AIS\] ITSM Mobile Agent Search Configuration**.

    4.  Click **Update**.

    **Note:** If you do not want to use the AI search configuration in the base system, migrate your search profiles and other configurations from zing search to AI search. Perform the steps mentioned in [Configure AI Search for mobile devices](https://www.servicenow.com/docs/access?context=advanced-text-search-config-now&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).


