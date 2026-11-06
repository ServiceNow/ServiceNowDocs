---
title: Relink an auto-complete suggestion type to an AI Search application configuration
description: Re-enable the display of auto-complete suggestions of a selected type in your search application's input field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/relink-auto-complete-srch-app-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Auto-complete suggestions, Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Relink an auto-complete suggestion type to an AI Search application configuration

Re-enable the display of auto-complete suggestions of a selected type in your search application's input field.

## Before you begin

Role required: search\_application\_admin

## About this task

When you define a search application configuration, AI Search automatically populates it with auto-complete suggestion types. If you removed one of these auto-complete suggestion types from the search application configuration, you can relink it.

**Note:** A search application configuration can't link to multiple search suggestion types that include the same reader and have the same click-in mode. If you try to link a second suggestion type with the same reader and click-in mode to a search application configuration, the system displays an error message.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Open the search application configuration that you want to relink the auto-complete suggestion type to.

3.  In the Autocomplete Suggestions related list, select **Add Existing**.

4.  In the Suggestion Reader Groups list, open the auto-complete suggestion type that you want to relink to your search application configuration.

5.  On the Suggestion Reader Group form, enter or look up the search application configuration by name in the **Search Application** field.

    For a description of the field values, see [Suggestion Reader Group form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/sugg-reader-group-form-ais.md).

6.  Select **Update**.


## Result

The selected auto-complete suggestion type appears in the search application configuration's Autocomplete Suggestions related list.

**Parent Topic:**[Auto-complete suggestions in AI Search applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/auto-complete-ais.md)

