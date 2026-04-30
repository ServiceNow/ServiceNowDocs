---
title: Define email configuration for contextual search
description: Define email configurations to allow the system to include search results with an email notifications.
locale: en-US
release: yokohama
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define email configuration for contextual search

Define email configurations to allow the system to include search results with an email notifications.

## Before you begin

Role required: admin

## About this task

When Knowledge articles are associated with a record, those search results can be included in email notifications. For example, email notifications sent when an incident is created can include Knowledge search results. An article in the search results may help the user who raised the incident to resolve the issue independently.

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Table Configuration**.

2.  In the Email Configurations related list, click **New**.

3.  In the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Email notification|Lookup icon ![Lookup icon to select a searcher](../image/look-up-icon.png) to select an email notification to attach the search results. You can select only from the notifications that are on the same table as the table configuration record.|
    |User field|A reference field that helps to narrow down on the search results. For example, if you select **Opened by**, the search results include only the articles that the **Opened by** user can access based on user criteria.|
    |Application|Application scope of the email configuration. The configuration is available for all applications or for scoped applications.|
    |Limit|Maximum number of search results returned.|

4.  Click **Submit**.


-   **[Provide knowledge in incident email notification](t_ProvideKnowledgeIEN.md)**  
Contextual search results are included in email notifications that are sent to users who create a new incident.

**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

