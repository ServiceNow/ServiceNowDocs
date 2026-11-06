---
title: Get started with AI search in upgraded instances
description: Enable intelligent query features that help agents find answers quickly in ITSM Mobile Agent in upgraded instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/get-started-ais-upgrade-itsm-mobile-agent.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [AI Search in ITSM Mobile Agent, Exploring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Get started with AI search in upgraded instances

Enable intelligent query features that help agents find answers quickly in ITSM Mobile Agent in upgraded instances.

## Before you begin

Role required: ais\_admin or admin

## About this task

You can get started with AI search in upgraded instances by using the AI search configuration in the base system.

## Procedure

1.  Enable AI search.

    1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Status**.

    2.  Select **Request AI Search**.

2.  Activate the AI Search Index Sources plugin \(com.glide.ais.index\_sources\).

    1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

    2.  Search for the AI Search Index Sources plugin \(com.glide.ais.index\_sources\).

    3.  Select **Activate**.

3.  Index all search sources.

    1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

    2.  Select all data sources.

    3.  From the **Actions on selected rows** drop-down list, select **Index All Tables**.

4.  Publish the AI search-related search profile.

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

    2.  Select **ITSM Mobile Agent Search Profile**.

    3.  Select **Publish**.

5.  Select the AI search-related search application configuration for the global search record.

    1.  Enter `sys_sg_global_search.list` in the navigation filter.

    2.  From the list of search configurations, select **ITSM Mobile Agent Search**.

    3.  For the **Search Application Configuration** field, select **\[AIS\] ITSM Mobile Agent Search Configuration**.

    4.  Select **Update**.

    **Note:** To use your own search profiles and configurations instead of the AI search configuration in the base system, migrate them from Zing search to AI search. For instructions, see [Configure AI Search for mobile devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/advanced-text-search-config-now.md).


