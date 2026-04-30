---
title: Using search scripted post-processors in AI Search application configurations
description: Use scripted post-processors to modify search result records for display in a search application.Define a script to post-process AI Search search results before displaying them to the user.Link a search scripted post-processor to an AI Search search application configuration. The search application executes the linked script for each search result before displaying it to the user.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-16"
reading_time_minutes: 2
breadcrumb: [Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Using search scripted post-processors in AI Search application configurations

Use scripted post-processors to modify search result records for display in a search application.

For example, a search scripted post-processor can modify search result date or currency field values to display in the user's regional formats.

**Parent Topic:**[Search application configurations](defining-search-app-cfgs-ais.md)

## Create a search scripted post-processor

Define a script to post-process AI Search search results before displaying them to the user.

### Before you begin

Role required: search\_application\_admin

### Procedure

1.  Copy code from an existing post-processor script to use as a starting point for your own script.

    1.  Select **All**.

    2.  In the Filter field, enter `sys_search_scripted_processor.list`.

    3.  Press Enter.

    4.  Open a post-processor script of your choice.

    5.  Copy the code from the **Post processing script** field.

2.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

3.  Open the search application configuration that you want to configure a scripted post-processor for.

4.  In the Search Scripted Post-processors related list, select **New**.

5.  On the Search Scripted Post-processors form, fill in the fields.

    For a description of the field values, see [Search Scripted Post-processors form](../reference/search-script-postprocess-form-ais.md). If you copied code from an existing post-processor script in step [1.e](script-post-process-ais.md#copy-search-script-processor-code), paste it into the new script's **Post processing script** field and modify it as needed.

6.  Select **Submit**.


### Result

The new search scripted post-processor appears in the search application configuration's Search Scripted Post-processors related list.

### What to do next

To make your new search scripted post-processor take effect, link it to the search application configuration for the application whose results you want to post-process.

## Link a search scripted post-processor to an AI Search application configuration

Link a search scripted post-processor to an AI Search search application configuration. The search application executes the linked script for each search result before displaying it to the user.

### Before you begin

Role required: search\_application\_admin

You must have already created the search script post-processor that you want to link to the search application configuration.

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Open the search application configuration that you want to link a search scripted post-processor to.

3.  In the Search Scripted Post-processors related list, select **New**.

4.  On the Search Scripted Post-processors form, select the reference lookup icon ![](../../navigation-and-ui/image/IconReferencelookup.png) for the **Search scripted processor** field and select the search scripted post-processor that you want to link to the search application configuration.

    For a description of the field values, see [Search Scripted Post-processors form](../reference/search-script-postprocess-form-ais.md).

5.  Select **Submit**.


### Result

The new search scripted post-processor appears in the Search Scripted Post-processors related list.

