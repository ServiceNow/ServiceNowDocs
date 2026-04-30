---
title: Configure Amazon Data Firehose integrations
description: Configure an integration to stream log data from Amazon Data Firehose directly to the ServiceNow data center, where it’s queued for Health Log Analytics processing. There’s no need to store AWS keys on your ServiceNow instance.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-04-08"
reading_time_minutes: 3
keywords: [AWS Firehose, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure Amazon Data Firehose integrations

Configure an integration to stream log data from Amazon Data Firehose directly to the ServiceNow data center, where it’s queued for Health Log Analytics processing. There’s no need to store AWS keys on your ServiceNow instance.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

This integration doesn't run on a MID Server.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon \(![Integration Launchpad icon](../../service-operations-workspace-itom/image/integrations-launchpad.png)\)

3.  In the **Browse integrations** tab, enter `Firehose` in the search field.

4.  Select the Amazon Data Firehose \(MID-less\) integration tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can either cancel the setup and complete the prior requirements first, or continue in draft mode and complete them later. Note that you can't activate the integration until all prerequisites are met.

5.  On the **Provide details** form, fill in the fields.

    For a description of the fields, see [AWS Firehose integration configuration fields](../reference/il-connector-hla-firehose-fields.md).

6.  Select **Next**.

7.  Follow one of the procedures provided on the **Set-up instruction** screen to install the integration in AWS.

    You can perform the installation procedure using either AWS CloudFormation or the AWS Management Console. Both methods require the same input. The appropriate choice depends on your requirements and the size of your deployment:

    -   AWS CloudFormation is best for deploying standardized configurations across multiple environments. Use it when you need automation, repeatability, and infrastructure-as-code benefits. AWS CloudFormation prompts for input automatically.
    -   The AWS Management Console is best for manual setups and quick configurations where you don't need automation.
    Before you perform either of these procedures, copy the access token, the ServiceNow endpoint URL, and the integration ID to the clipboard. You need these values during the installation process.

8.  Select **Save draft**.

9.  Select **Activate** to activate the integration.


## Result

The integration is activated and the **Overview** tab is displayed. The tile for the integration is available in the **Installed integrations** tab on the Integrations Launchpad.

## What to do next

Leverage the information on the **Overview** tab to refine how HLA reads the log data. For more information, see [Review log data streaming status and sources of an integration](il-connector-overview-tab.md).

**Tip:** Use the More options menu \(![](../image/more-options.png)\) to open the **Data Input Mapping**, **Source Type Structures**, or **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More options menu also provides direct access to the **Log Viewer**, where you can review raw log messages ingested by the integration.

For more information, see:

-   [Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)
-   [Source type structure adjustment](../concept/hla-source-type-structure-adjustment.md)
-   [Review logs on the Log Viewer](../../health-log-analytics-operator/concept/hla-op-logs-log-viewer-concept-sow.md)

-   **[AWS Firehose integration configuration fields](../reference/il-connector-hla-firehose-fields.md)**  
Description of the fields on the AWS Firehose integration configuration forms for Health Log Analytics.

**Parent Topic:**[Set up integrations from Integrations Launchpad](../concept/hla-data-input-setup-integrations.md)

