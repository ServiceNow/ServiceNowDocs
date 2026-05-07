---
title: Add internal search sources
description: Add internal search sources to include ServiceNow table content in Employee Slate conversational search.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
keywords: [internal search sources, Employee Slate, Now Assist]
breadcrumb: [Search sources for Employee Slate, Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# Add internal search sources

Add internal search sources to include ServiceNow table content in Employee Slate conversational search.

## Before you begin

The Employee Slate for Now Assist product is installed and configured through the Product Configuration console.

You have identified the table that you want to index as a search source.

Role required: admin

## About this task

Internal search sources contribute results to the conversational assistant from ServiceNow tables. Use **Create New** only when the required source isn't already available in the instance. To reuse an existing source that isn't yet linked to the search profile, use **Add existing**.

## Procedure

1.  In the **Data Sources** module of the Product Configuration console, open the **Internal Sources** configuration.

2.  Select **Create New**.

3.  Enter a search source name and select the table to index as the source.

4.  Select the filter conditions that apply to the source, then select **Continue**.

    Filter conditions scope the records from the selected table that the search source exposes to the assistant.

5.  If the selected table doesn't have an existing index source, set the field mapping attributes.

    Field mapping governs how the system indexes and displays records in the search results. Select fields to exclude from the search if the table contains fields that shouldn't appear.

6.  Save the configuration.

    The new internal source associates with the search profile for Employee Slate for Now Assist and appears in the internal sources list.

7.  Select **Manage Search Profile** to open the AI Search Admin Console.

    Use the AI Search Admin Console to manage advanced configurations such as synonyms, dictionaries, and stop words.


## Result

The internal search source links to the Employee Slate for Now Assist search profile. The conversational assistant returns results from the configured table within the filter conditions that you set.

