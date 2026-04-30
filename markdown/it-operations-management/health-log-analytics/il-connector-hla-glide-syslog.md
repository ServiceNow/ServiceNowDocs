---
title: Set up a ServiceNow System Logs Retriever integration for Health Log Analytics
description: Set up an integration for streaming log data from your ServiceNow platform's System Log table to the HLA engine.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [System Logs Retriever, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up a ServiceNow System Logs Retriever integration for Health Log Analytics

Set up an integration for streaming log data from your ServiceNow platform's System Log table to the HLA engine.

## Before you begin

**Note:**

-   This integration doesn't run on a MID Server.
-   Only a single ServiceNow System Logs Retriever integration or data input can exist in the system.

-   Verify that the Health Log Analytics application is installed and provisioned on your instance. For more information, see [Install Health Log Analytics \(HLA\)](install-health-log-analytics.md).
-   Verify that a service instance is available.
-   Verify that the HLA Engine is up and running.

Role required: evt\_mgmt\_admin

## About this task

You set up integrations through the Integrations Launchpad in Service Operations Workspace, which you access from the ITOM AIOps configuration center. The AIOps configuration center is a centralized workspace for configuring and managing AIOps features from a single place. The integrations setup process reduces implementation time compared to manual data input setup in the classic interface in Health Log Analytics. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](../../service-operations-workspace-itom/concept/integrations-launchpad.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  From the Integrate section, under Integrations, select **Add integration**.

    The Integrations Launchpad appears.

4.  In the **Browse integrations** tab, enter `System Logs` in the search field.

5.  Select the ServiceNow System logs tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can cancel the setup and complete the prior requirements first. Alternatively, you can continue in draft mode and complete the requirements later. Note that you can't activate the integration until you have completed all the prerequisites.

6.  The **Provide details** form is displayed.

    These fields are auto-populated, because only one ServiceNow System Logs Retriever integration or data input can exist in the system. For a description of the fields, see the **Provide details** table in [ServiceNow System Logs Retriever integration configuration fields](../reference/il-connector-hla-glidesyslog-fields.md).

7.  Select **Next**.

8.  On the **Set data retrieval method** page, build conditions for filtering log data from the System Log table before it is streamed to the HLA engine.

    This page helps you focus on the specific logs you want to monitor. For example, you might want to look at Discovery logs or exclude email logs. By default, all logs are included.

9.  Do one of the following:

    -   If you completed all the prerequisites before starting the configuration, select **Activate**.

        The integration is activated and the **Overview** tab is displayed. On the Integrations Launchpad, the integration tile is available in the **Installed integrations** tab.

    -   If you didn't complete all the prior requirements, select **Save draft**.

        The system saves the integration as a draft in the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**. You can complete the prerequisites and activate the installation later. For more information, see [Activate a draft integration in Health Log Analytics](il-connector-hla-activate-draft.md).


## Result

Log data starts streaming from the ServiceNow System Log table to the Health Log Analytics AI engine, based on the configured filters. The dedicated HLA engine for your instance starts analyzing your system logs in real-time.

**Note:** Starting with Health Log Analytics version 37.0.15, you can use the ServiceNow System Logs Retriever integration to automatically detect errors and anomalies in your ServiceNow instance's system log. By combining HLA's anomaly detection with Now Assist's GenAI capabilities, you can identify and resolve platform issues more effectively for a better user experience. For more information, see [Use Case: Proactive monitoring of your ServiceNow instance in Health Log Analytics](../../health-log-analytics-operator/reference/hla-use-case-syslogs.md).

## What to do next

Use the information in the **Overview** tab to refine how HLA reads the log data by adjusting your integration configuration. For more information, see [Review log data streaming status and sources of an integration](il-connector-overview-tab.md).

**Note:**

-   The MID Server streaming status and the **Log streaming sources** table do not appear on the **Overview** tab for this integration, because it doesn't run on a MID Server.
-   When the integration is first configured, it may take up to 24 hours for the first alerts to appear. Once the data is populated, you can refresh the screen to see real-time metrics.

Use the More menu to go directly from the **Overview** tab to the **Data Input Mapping**, **Source Type Structures**, and **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More menu also provides direct access to the **Log Viewer**, where you can see the raw logs that the integration ingests.

**Parent Topic:**[Setting up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

