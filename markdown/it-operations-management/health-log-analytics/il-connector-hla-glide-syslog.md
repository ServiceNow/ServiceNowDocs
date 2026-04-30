---
title: Configure a ServiceNow System Logs connector
description: Configure a push connector for streaming log data from the ServiceNow System Log table to the Health Log Analytics AI engine. Integrating with a connector is an essential step in setting up the Health Log Analytics \(HLA\) application.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-26"
reading_time_minutes: 3
breadcrumb: [Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure a ServiceNow System Logs connector

Configure a push connector for streaming log data from the ServiceNow System Log table to the Health Log Analytics AI engine. Integrating with a connector is an essential step in setting up the Health Log Analytics \(HLA\) application.

## Before you begin

**Note:** This integration doesn't run on a MID Server. Only a single ServiceNow System Logs Retriever integration or data input can exist in the system.

-   Ensure that the Health Log Analytics application is installed and provisioned on your instance. For more information, see [Health Log Analytics \(HLA\) installation](install-health-log-analytics.md).
-   Ensure that a service instance is available.
-   Ensure that the HLA Engine is up and running.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon \(![Integration Launchpad icon](../../service-operations-workspace-itom/image/integrations-launchpad.png)\)

3.  In the **Browse integrations** tab, enter `System Logs` in the search field.

4.  Select the ServiceNow System Logs tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can either cancel the setup and complete the prior requirements first, or continue in draft mode and complete them later. Note that you can't activate the integration until all prerequisites are met.

5.  On the **Provide details** form, fill in the fields.

    These fields are auto-populated, because only one ServiceNow System Logs Retriever integration or data input can exist in the system. For a description of the fields, see the **Provide details** table in [ServiceNow System Logs Retriever integration configuration fields](../reference/il-connector-hla-glidesyslog-fields.md).

6.  Select **Next**.

7.  On the **Set data retrieval method** page, build conditions for filtering log data from the System Log table before it is streamed to the HLA engine.

    This page helps you focus on the specific logs you want to monitor. For example, you might want to look at Discovery logs or exclude email logs. By default, all logs are included.

8.  Do one of the following:

    -   If you completed all the prerequisites before starting the configuration, select **Activate**.

        The integration is activated and the **Overview** tab is displayed. On the Integrations Launchpad, the integration tile is available in the **Installed integrations** tab.

    -   If you didn't complete all the prior requirements, select **Save draft**.

        The system saves the integration as a draft in the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**. You can complete the prerequisites and activate the installation later. For more information, see the **What to do next** section.


## Result

Log data starts streaming from the ServiceNow System Log table to the Health Log Analytics AI engine, based on the configured filters.

## What to do next

Leverage the information in the **Overview** tab to refine how HLA reads the log data by adjusting your integration configuration. For more information, see [Review log data streaming status and sources of an integration](il-connector-overview-tab.md).

The MID Server streaming status and the **Log streaming sources** table do not appear on the **Overview** tab for this integration, because it doesn't run on a MID Server. When the integration is first configured, it may take up to 24 hours for the first alerts to appear. Once the data is populated, you can refresh the screen to see real-time metrics.

**Tip:** Use the View menu to go directly from the **Overview** tab to the **Data Input Mapping**, **Source Type Structures**, and **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the View menu also provides direct access to the **Log Viewer**, where you can see the raw logs that the integration ingests.

If you saved the integration as a draft, perform these steps to activate it later:

1.  Complete all the prior requirements.
2.  In the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**, locate and select the integration tile.
3.  On the configuration screen, select **Activate**.

    The integration is activated and the **Overview** tab is displayed. The integration tile is available in the **Installed integrations** tab on the Integrations Launchpad.


-   **[ServiceNow System Logs Retriever integration configuration fields](../reference/il-connector-hla-glidesyslog-fields.md)**  
Description of the fields on the ServiceNow System Logs Retriever integration configuration form for Health Log Analytics.

**Parent Topic:**[Set up integrations from Integrations Launchpad](../concept/hla-data-input-setup-integrations.md)

