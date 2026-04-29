---
title: Set up an Amazon Data Firehose \(MID-less\) integration for Health Log Analytics
description: Set up an integration to stream log data from Amazon Data Firehose directly to the ServiceNow datacenter, where it’s queued for Health Log Analytics processing. There’s no need to store AWS keys on your ServiceNow instance.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [AWS Firehose, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up an Amazon Data Firehose \(MID-less\) integration for Health Log Analytics

Set up an integration to stream log data from Amazon Data Firehose directly to the ServiceNow datacenter, where it’s queued for Health Log Analytics processing. There’s no need to store AWS keys on your ServiceNow instance.

## Before you begin

This integration doesn't run on a MID Server.

Role required: evt\_mgmt\_admin

## About this task

You set up integrations through the Integrations Launchpad in Service Operations Workspace, which you access from the ITOM AIOps configuration center. The AIOps configuration center is a centralized workspace for configuring and managing AIOps features from a single place. The integrations setup process reduces implementation time compared to manual data input setup in the classic interface in Health Log Analytics. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](../../service-operations-workspace-itom/concept/integrations-launchpad.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  From the Integrate section, under Integrations, select **Add integration**.

    The Integrations Launchpad appears.

4.  In the **Browse integrations** tab, enter `Firehose` in the search field.

5.  Select the Amazon Data Firehose \(MID-less\) integration tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can cancel the setup and complete the prior requirements first. Alternatively, you can continue in draft mode and complete the requirements later. Note that you can't activate the integration until you have completed all the prerequisites.

6.  On the **Provide details** form, fill in the fields.

    For a description of the fields, see [Amazon Data Firehose integration configuration fields](../reference/il-connector-hla-firehose-fields.md).

7.  Select **Next**.

8.  Follow one of the procedures provided on the **Set-up instruction** screen to install the integration in AWS.

    You can perform the installation procedure using either AWS CloudFormation or the AWS Management Console. Both methods require the same input. The appropriate choice depends on your requirements and the size of your deployment:

    -   Use AWS CloudFormation when you need automation, repeatability, and infrastructure-as-code benefits. It's best for deploying standardized configurations across multiple environments. AWS CloudFormation prompts for input automatically.
    -   Use the AWS Management Console when you need manual setups or quick configurations without automation.
    Before you perform either of these procedures, copy the access token, the ServiceNow endpoint URL, and the integration ID to the clipboard. You need these values during the installation process.

9.  Do one of the following:

    -   If you completed all the prerequisites before starting the configuration, activate the integration either with or without AI-powered capabilities. Select the appropriate option:
        -   **Activate with AI** enables AI-powered automatic mapping of log data. When the integration is activated successfully, the **Overview** tab is displayed and Now Assist collects and analyzes log data. An AI icon indicates that Now Assist auto-maps log data to service instances and components for contextual alert generation.
        -   **Activate** activates the integration without AI-powered mapping. The integration is activated and the **Overview** tab is displayed.
    -   If you didn't complete all the prior requirements, select **Save draft**.

        The system saves the integration as a draft in the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**. You can complete the prerequisites and activate the installation later. For more information, see [Activate a draft integration in Health Log Analytics](il-connector-hla-activate-draft.md).


## What to do next

On the **Overview** tab, do the following:

-   Use the displayed information to refine how Health Log Analytics reads the log data. For more information, see [Review log streaming data and adjust integration settings in Health Log Analytics](il-connector-overview-tab.md).
-   Use the More options menu \(![More options menu icon.](../image/more-options.png)\) to open the **Data Input Mapping**, **Source Type Structures**, or **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More options menu also provides direct access to the **Log Viewer**. Use the **Log Viewer** to review raw log messages ingested by the integration. For more information, see:
    -   [Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)
    -   [Source type structure adjustment](../concept/hla-source-type-structure-adjustment.md)
    -   [Review logs on the Log Viewer](../../health-log-analytics-operator/concept/hla-op-logs-log-viewer-concept-sow.md)

If you activated the integration with AI, verify that AI correctly auto-mapped log data to service instances and components. To do this, select **View mapping** under **Log context mapping**. You can override the AI mapping by selecting a different log field from each list. For more information, see [Map logs to service instances, components, and source types for contextual alerts in Health Log Analytics](il-connector-hla-map-business-context.md).

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

