---
title: Add external search sources
description: Add external search sources to include non-ServiceNow content in Employee Slate conversational search.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
keywords: [external search sources, Employee Slate, Now Assist]
breadcrumb: [Search sources for Employee Slate, Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# Add external search sources

Add external search sources to include non-ServiceNow content in Employee Slate conversational search.

## Before you begin

The Employee Slate for Now Assist product is installed and configured through the Product Configuration console.

You have network and credential details for the external source.

Role required: admin

## About this task

No external source is linked out of the box for Employee Slate for Now Assist. Add an existing external connector or create a new connector to surface content from third-party systems in the conversational assistant.

## Procedure

1.  In the **Data Sources** module of the Product Configuration console, open the **External Sources** configuration.

2.  Select **Create New**.

    To reuse an existing external connector, select **Add existing** and select the connector from the list.

3.  Select the connector type.

    The connector type determines the subsequent steps. For web content, select the **Web crawler** connector.

4.  Select a predefined web source or enter a custom web source, then validate the connection.

5.  Select the crawl settings, then select **Next**.

6.  Select the crawl options, then select **Save**.

7.  Create a search source for the connector.

    Enter a search source name and select the filters that apply to the connector. The new search source automatically links to the search profile for Employee Slate for Now Assist.

8.  Add more search sources for the same connector.

    If the connector supports multiple search sources, add them from this step.

9.  Select **Next** to start the initial crawl.

    After the crawl completes, results from the external source appear in the conversational assistant response for relevant queries.

10. Select **Manage External Content Connectors** to open the External Content admin home.

    Use the External Content admin home to manage crawl schedules, crawl history, analytics, and other advanced connector settings.


## Result

The external search source links to the Employee Slate for Now Assist search profile. The conversational assistant returns results from the external source after the initial crawl completes.

