---
title: Configure AI Search Assist for a record producer
description: Configure AI Search Assist settings for a record producer to help users view related Catalog Item and knowledge article search results.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-02-19"
reading_time_minutes: 2
breadcrumb: [AI Search record producer for Service Portal, Integrate, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure AI Search Assist for a record producer

Configure AI Search Assist settings for a record producer to help users view related Catalog Item and knowledge article search results.

## Before you begin

Role required: aisa\_admin or admin

## About this task

AI Search Assist is a Service Portal widget that displays relevant Catalog Item and knowledge article search results within a record producer configuration.

**Note:** If both AI Search Assist and Contextual Search are configured for the same record producer, see **Results** at the end of this task for how to control which one is displayed.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Assist** &gt; **Record Producer Configuration**.

2.  Select **New** and fill in the form to create a configuration for Catalog Item and knowledge article search results.

3.  On the **Search application information** tab, select a Search application configuration.

    You can choose from a list of pre-defined configurations for specific features. For example, **\[AI Search Assist\] - Incident Deflection**.

    ![Search Application Configurations.](../image/search-application-configurations.png)

4.  On the **Record producer information** tab, select a Record producer and Search variable.

    For example, **Service Category Request** as a record producer can have a search variable of **Category name**.

    ![Record Producer Information.](../image/record-producer-information.png)

5.  To adjust the visibility of your card or detail view, select **Show UI Actions** under the new Record Producer Configuration record's related links.

    AI Search Assist **UI actions** can hide from view using a simple condition or advanced condition via a script.

6.  Select **Submit**.


## Result

AI Search Assist is active.

**Note:** AI Search Assist doesn't support external users. If an external user tries to use an Assist UI action, the system returns an error.

If Contextual Search has been configured for the same record producer, and is showing results instead of AI Search Assist, check the following conditions:

-   The **Enable AI Search** flag on the Portal \(sp\_portal\) is active
-   The AI Search Assist record configuration is active
-   The AI Search Profile is active and published
-   The record producer variable for AI Search Assist is created for the associated record producer and the variable is active

If these conditions aren't all met, then Contextual Search is the fallback for the same record producer to make sure you see related search results.

**Parent Topic:**[AI Search Assist record producer integration for Service Portal](../concept/ai-search-assist.md)

