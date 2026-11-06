---
title: Remove an auto-complete suggestion type from an AI Search application configuration
description: Disable the display of auto-complete suggestions of a selected type in your search application's input field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/remove-auto-complete-srch-app-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Auto-complete suggestions, Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Remove an auto-complete suggestion type from an AI Search application configuration

Disable the display of auto-complete suggestions of a selected type in your search application's input field.

## Before you begin

Role required: search\_application\_admin

## About this task

When you define a search application configuration, AI Search automatically populates it with auto-complete suggestion types. You can remove unwanted auto-complete suggestion types from the search application configuration.

**Note:** Removing an auto-complete suggestion type from your search application configuration doesn't delete it. To relink the removed suggestion type to your search application configuration, see [Relink an auto-complete suggestion type to an AI Search application configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/relink-auto-complete-srch-app-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Open the search application configuration that contains the auto-complete suggestion type you want to remove.

3.  In the Autocomplete Suggestions related list, open the auto-complete suggestion type that you want to remove.

4.  On the Suggestion Reader Group form, select **Remove from Search Application**.

    For a description of the field values, see [Suggestion Reader Group form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/sugg-reader-group-form-ais.md).


## Result

The selected auto-complete suggestion type no longer appears in the search application configuration's Autocomplete Suggestions related list.

**Parent Topic:**[Auto-complete suggestions in AI Search applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/auto-complete-ais.md)

