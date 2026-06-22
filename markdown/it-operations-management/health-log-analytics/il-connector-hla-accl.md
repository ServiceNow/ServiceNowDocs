---
title: Set up an ACC Log Analytics integration for Health Log Analytics
description: Set up an ACC Log Analytics \(ACC-L\) integration for streaming log messages to your ServiceNow instance. This integration can be used when agent-less log collection is impractical, for example because of security requirements or host accessibility.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/il-connector-hla-accl.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [ServiceNow, Health Log Analytics, HLA, Agent Client Collector, ACC-L, Log Analytics, agent, integration, configuration, setup]
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up an ACC Log Analytics integration for Health Log Analytics

Set up an ACC Log Analytics \(ACC-L\) integration for streaming log messages to your ServiceNow instance. This integration can be used when agent-less log collection is impractical, for example because of security requirements or host accessibility.

## Before you begin

-   Verify you're using the latest release version of the Health Log Analytics plugin to enable ACC Log Analytics integration setupfrom the Integrations Launchpad.
-   Verify that a MID Server is installed and configured. For more information, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).
-   The MID Server must support the Agent Client Collector Listener. The ACC Listener can be enabled during ACC Log Analytics integration setup from the Integrations Launchpad.
-   The Agent Client Collector Log Analytics application has a dependency on the following ServiceNow applications, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home):
    -   Health Log Analytics, Version 22.0.12 - December 2021 and later releases.
    -   Agent Client Collector - Framework, Version 2.7.0 - December 2021 and later releases.

**Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

**Note:** Currently, this setup only supports basic authentication with the MID Server. mTLS is not supported.

Role required: evt\_mgmt\_admin

## About this task

Set up an integration from the Integrations Launchpad in Service Operations Workspace, which you access from the ITOM AIOps configuration center. The AIOps configuration center is a centralized workspace for configuring and managing AIOps features from a single place. The integrations setup process reduces implementation time compared to manual data input setup in the classic interface in Health Log Analytics. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/integrations-launchpad.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon \[Omitted image "icon-itom-aiops-config.png"\] Alt text: ITOM AIOps configuration center icon.

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  From the Integrate section, under Integrations, select **Add integration**.

    The Integrations Launchpad appears.

4.  In the **Browse integrations** tab, search for `Agent Log Analytics`.

5.  Select the Agent Log Analytics integration tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can cancel the setup and complete the prior requirements first. Alternatively, you can continue in draft mode and complete the requirements later. Note that you can't activate the integration until you have completed all the prerequisites.

6.  On the **Provide details** form, complete the fields.

    For a description of the fields, see the **Provide details** table in [ACC Log Analytics \(ACC-L\) integration configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-accl-fields.md).

7.  Select **Advanced settings** and complete the advanced configuration fields.

    For a description of the fields, see the **Advanced settings** table in [ACC Log Analytics \(ACC-L\) integration configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-accl-fields.md).

8.  Select **Next** to save your settings and proceed to the **Setup instructions** tab.

9.  Enable Agent Client Collector Log Analytics to stream logs from your IT infrastructure to Health Log Analytics by creating log collection policies for your configuration items \(CIs\).

    For more information, see [Create an Agent Client Collector log policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/hla-acc-log-policies.md).

10. Do one of the following:

    -   If you completed all the prerequisites before starting the configuration, select **Activate**.

        The integration is activated and the **Overview** tab is displayed. On the Integrations Launchpad, the integration tile is available in the **Installed integrations** tab.

    -   If you didn't complete all the prerequisites, select **Save draft**.

        The system saves the integration as a draft in the Integrations Launchpad. It appears in the **Installed integrations** tab, under **Waiting for your action**. You can complete the prerequisites and activate the integration later. For more information, see [Activate a draft integration in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-activate-draft.md).


## What to do next

On the **Overview** tab, do the following:

-   Use the displayed information to refine how Health Log Analytics reads the log data. For more information, see [Review log streaming data and adjust integration settings in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-overview-tab.md).
-   Use the More options menu \(\[Omitted image "more-options.png"\] Alt text: More options menu icon.\) to open the **Data Input Mapping**, **Source Type Structures**, or **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More options menu also provides direct access to the **Log Viewer**. Use the **Log Viewer** to review raw log messages ingested by the integration. For more information, see:
    -   [Log data auto-mapping and mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-automapping.md)
    -   [Source type structure adjustment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-source-type-structure-adjustment.md)
    -   [Reviewing the logs for an alert on the Log Viewer in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-logs-log-viewer-concept-sow.md)

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-implement.md)

