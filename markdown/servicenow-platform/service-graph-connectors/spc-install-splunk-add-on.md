---
title: Install the add-on for the Service Graph Connector for Splunk
description: Install the Splunk add-on developed by ServiceNow engineering from splunkbase to search for Windows and Linux Assets.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-08-08"
reading_time_minutes: 1
breadcrumb: [Splunk, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Install the add-on for the Service Graph Connector for Splunk

Install the Splunk add-on developed by ServiceNow® engineering from splunkbase to search for Windows and Linux Assets.

## Before you begin

Role required: admin or security\_admin

## Procedure

1.  Navigate to **splunkbase** \([splunkbase](https://splunkbase.splunk.com/app/7355)\) and log in.

2.  In your Splunk console, select **Apps** &gt; **FInd More Apps**.

3.  Locate the **ServiceNow Add-on for Windows and Linux Assets** app and select **Install**.

    **Note:** You can upgrade from within the app.

4.  Follow the prompts.

5.  Navigate to **Settings** &gt; **Searches, reports and alerts** to view when searches are scheduled.

    **Note:**

    You can change the schedules, but since the schedules run in a specific order and require successful completion before the next search in the list is initiated, you might prefer to leave the settings in their defaults.

    After all the searches are completed, the data is grouped from each search into a few coalesced key-value parings \(kvstores\) for import into your instance: asset details, asset process details, asset service details, and asset software details.

6.  Select **App: Search and Reporting \(search\)** &gt; **ServiceNow Add-on for Windows and Linux Assets.**

    By default, search data is stored in the following key definitions:

    -   Asset\_index\_macro: Index=”internal”
    -   Asset\_linex\_Index\_macro: index=”main”
    -   Asset\_windows\_index=”main”
    If you are storing the search data for Linux and Windows in custom indexes, you must update your search macros.

7.  To update your search macros, navigate to **Settings** &gt; **Advanced search** &gt; **Search macros** &gt; **Search &amp; Reporting \(Search\)** &gt; **ServiceNow Add-on for Windows and Linux Assets ServiceNow\_TA\_windows\_linux\_assets**

8.  On the Search macros page, update the index as required in the Definition column.

9.  Adjust workloads to specify resources for search, indexing, and other workloads.

    1.  In Splunk Web, select **Settings** &gt; **Workload Management** &gt; **Workload Rules**.

    2.  In the Status column, select the toggle to activate or deactivate individual workload rules.

    See [Service Graph Connector for Splunk add-on](../concept/sgc-splunk-add-on.md) for more information about target workloads and supported deployments.


