---
title: Populate search suggestions in Service Portal
description: If you are upgrading from a previous release, run a script to populate search suggestions with data from a platform search table to provide search suggestions to your users. Alternatively, you can wait until users search for keywords instead of running this script.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Populate search suggestions in Service Portal

If you are upgrading from a previous release, run a script to populate search suggestions with data from a platform search table to provide search suggestions to your users. Alternatively, you can wait until users search for keywords instead of running this script.

## Before you begin

Role required: admin

In new instances, the search suggestions are enabled by default. In upgraded instances, you must enable the search suggestions. For more information, see [Enable search suggestions](https://www.servicenow.com/docs/access?context=enable-search-suggestions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## About this task

The ServiceNow AI Platform collects search data and analytics that generate search suggestions. If you are upgrading from a previous release, the search analytics do not contain any data yet. To immediately provide suggestions to your users, you can populate the search suggestions using data from either the Text Searches \[text\_search\] table or the Service Portal Log Entries \[sp\_log\] table. The Service Portal Log Entries table includes search data from Service Portal only and may take less time to populate search suggestions. The Text Search table includes search data from the entire platform.

Search suggestions improve over time as more people use Service Portal. Search Suggestions is a ServiceNow AI Platform feature. For more information, see [Search Suggestions](https://www.servicenow.com/docs/access?context=search-suggestions-overview&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Warning:** Populating search suggestions can be a resource-intensive task that may take a while to complete. Do not run this script during peak hours. Populating search suggestions is not supported on domain-separated instances.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the **Populate Suggestions to avoid Cold Start - Portals** scheduled job.

3.  Modify the script for your search implementation.

    1.  Define which portals the suggestions apply to.

        By default, the script populates suggestions in the base system service portal, but you can add as many as you want to the array.

        ```
        var portals = ["Service Portal"];
        ```

    2.  Change where the data comes from

        By default, the script imports data from the Text Searches \[text\_search\] table, but you can change the source table to the Service Portal Log Entries \[sp\_log\] table. The Service Portal Log Entries only saves records from the last 90 days.

        ```
        var searchLogTable = "text_search";
        ```

    3.  Push data to any custom search sources in your instance.

        Suggestions are not enabled for external search sources. You must push data to both the search source name and the Sys ID.

        For example, push text searches from the Incident table to your custom Incident search source. For more information about custom search sources, see [Define a search source](add-table-search-source.md). By default, the system pushes text searches from the Catalog and Knowledge tables to the respective search sources.

        Add the following code after line 11 in the script for each of your custom search sources.

        ```
        searchSources.push("<search-source-table-name>");
        searchSourceIds.push("<search-source-sys-id>");
        ```

        If the search source table does not exist, the system does not push suggestions to that search source.

    4.  Save the record.

        Make sure that the script includes the configuration you need. You can only run the script once.

4.  Activate the record and select **Execute Now**.

    Running this scheduled job populates the Search Events \[sys\_search\_event\], Search Source Events \[sys\_search\_source\_event\], and Search Suggestions \[sys\_search\_suggestion\] tables.


## Result

Users see suggestions when they start typing in a Service Portal search widget.

**Parent Topic:**[Zing search in Service Portal](../concept/zing-search-service-portal.md)

