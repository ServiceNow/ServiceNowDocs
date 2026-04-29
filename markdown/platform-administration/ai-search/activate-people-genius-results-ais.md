---
title: Activate People Genius Results
description: Enable AI Search's People default Genius Result configuration for use in your search profiles.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [People Genius Results, Genius Result configurations in the base system, Genius Results, Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate People Genius Results

Enable AI Search's People default Genius Result configuration for use in your search profiles.

## Before you begin

Role required: ais\_admin

**Warning:** Don't activate the People Genius Result configuration if your instance has more than 100,000 records in any of the following tables:

-   Catalog Item \[sc\_cat\_item\]
-   Department \[cmn\_department\]
-   Location \[cmn\_location\]
-   User \[sys\_user\]

These tables are configured as vocabulary sources in the Default AI Search Genius Results Model specified in the People configuration's NLU trigger condition. If your instance has more than 100,000 records in any of the listed tables, training will fail for the NLU model and the People Genius Result configuration won't operate correctly.

## About this task

The People default Genius Result configuration is inactive in the base system. To use this Genius Result configuration in your search profiles, you must activate it.

**Note:** If you upgraded from the Quebec release, this Genius Result configuration is already activated. You don't need to perform the steps from this task.

As part of activation, you need to run a scheduled job that trains and publishes the Default AI Search Genius Results Model. This **NLU** model contains intents used by the People configuration's **NLU** trigger.

For more information on the People default Genius Result configuration, see [People Genius Results](../concept/genius-result-people-ais.md).

## Procedure

1.  Train and publish the Default AI Search Genius Results Model.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Open the **AI Search Create Train Model** job.

    3.  Select **Execute Now**.

    4.  Check the publication status of the NLU model by navigating to **All** &gt; **AI Search** &gt; **Search Query Settings** &gt; **Search Intents**.

        When a **Last Published** field value is displayed, the NLU model is trained and published. You can now activate the People default Genius Result configuration.

2.  Activate the People default Genius Result configuration.

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Query Settings** &gt; **Genius Results**.

    2.  Open the People Genius Result configuration.

    3.  On the AI Search Genius Result Configuration form, select **Change Active State**.

        For a description of the field values, see [AI Search Genius Result Configuration form](../reference/genius-result-cfg-form-ais.md).

        The Genius Result configuration's **Active** field value changes to **true**.


## Result

The People Genius Result configuration is available for use in search profiles.

**Parent Topic:**[People Genius Results](../concept/genius-result-people-ais.md)

