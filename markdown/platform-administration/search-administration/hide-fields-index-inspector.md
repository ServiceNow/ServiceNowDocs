---
title: Hide fields in the index inspector
description: Suppress display of fields on documents in the index inspector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/hide-fields-index-inspector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-08-21"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Review content item indexing status, Review, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Hide fields in the index inspector

Suppress display of fields on documents in the index inspector.

## Before you begin

Role required: admin

## About this task

By default, the index inspector displays fields found on indexed documents that match your search. Administrators can hide sensitive fields in the index inspector by setting the value of the **glide.ais.externalcontent.query\_api\_denied\_fields** system property. Hidden fields don't appear in index inspector search results.

To learn about the index inspector, see [Review indexing status for individual content items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/review-indexing-status-content-items.md).

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Search for the **glide.ais.externalcontent.query\_api\_denied\_fields** system property.

    -   If the system property already exists, open it.
    -   If the system property doesn't exist, select **New**, then enter the following field values on the System Property form.
    |Field|Value|
    |-----|-----|
    |Name|glide.ais.externalcontent.query\_api\_denied\_fields|
    |Type|string|

3.  In the system property record's **Value** field, enter a comma-separated list of names for fields that you want to hide in the index inspector.

    As an example, you might enter `title,url` to hide the **Title** and **URL** fields for indexed records.

    The default value is empty, meaning that no fields are hidden.

    **Note:** Field names are case sensitive and all in lowercase. Don't capitalize field names when entering them.

4.  To save your changes, select **Save** or **Update**.


## Result

The specified fields are hidden when viewing indexed documents in the index inspector.

**Parent Topic:**[Review indexing status for individual content items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/review-indexing-status-content-items.md)

