---
title: Activate a draft integration in Health Log Analytics
description: Activate an integration that was configured and saved as a draft in Health Log Analytics \(HLA\).
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, draft, integration, activation]
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Activate a draft integration in Health Log Analytics

Activate an integration that was configured and saved as a draft in Health Log Analytics \(HLA\).

## Before you begin

Configure an integration in draft mode through the Integrations Launchpad and save it.

Role required: evt\_mgmt\_admin

## Procedure

1.  Complete all the prior requirements for the integration.

2.  In the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**, locate and select the integration tile.

3.  On the configuration page, select **Activate**.

    -   For Push integrations: The integration is activated and the **Overview** tab is displayed. The integration tile is available in the **Installed integrations** tab on the Integrations Launchpad.
    -   For all other integrations: Continue with the following steps.
4.  In the pop-up window, select **Test &amp; Save** to save the integration to the database and test connectivity.

    If an error is returned, adjust the configuration as suggested in the error message and then try to activate the integration again.

5.  When the test is successful, select the appropriate activation option.

    -   **Activate**

        The integration is activated and the **Overview** tab is displayed.

        **Note:** If your integration supports activation with AI capabilities, you can select this option to activate the integration without enabling these capabilities.

    -   **Activate with AI**

        **Note:** This option is only available if your integration supports activation with AI capabilities.

        The integration is activated with AI capabilities enabled and the **Overview** tab is displayed. Now Assist collects and analyzes log data, and an icon indicates that it auto-maps log data to service instances and components for contextual alert generation.

    The integration tile is available in the **Installed integrations** tab on the Integrations Launchpad


**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

