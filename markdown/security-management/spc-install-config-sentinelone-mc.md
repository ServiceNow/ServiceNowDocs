---
title: Install and configure the Service Graph Connector for SentinelOne and the SentinelOne Mitigation Control Integration
description: The Service Graph Connector for SentinelOne and the SentinelOne Integration for Mitigation Control Integration require separate configuration steps. You install and configure the Service Graph Connector for SentinelOne to import asset details. You configure the SentinelOne Integration for Mitigation Control Integration to gather mitigation data about the assets that are monitored by the Service Graph Connector for SentinelOne.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Policies for Exploit Protection \(EDR\), Use mitigation controls, Security Posture Control, Security Operations]
---

# Install and configure the Service Graph Connector for SentinelOne and the SentinelOne Mitigation Control Integration

The Service Graph Connector for SentinelOne and the SentinelOne Integration for Mitigation Control Integration require separate configuration steps. You install and configure the Service Graph Connector for SentinelOne to import asset details. You configure the SentinelOne Integration for Mitigation Control Integration to gather mitigation data about the assets that are monitored by the Service Graph Connector for SentinelOne.

## Before you begin

Roles required:

-   admin for installation and activation of plugins.
-   SPC Admin Group and SPC Analyst Group for configuration of integrations in the workspace.
-   SentinelOne credentials.

## Procedure

1.  To install and configure the Service Graph Connector for SentinelOne integration, follow these steps:

    **Note:** If you have installed the Service Graph Connector for SentinelOne, proceed to step 2 to configure the SentinelOne Integration for Mitigation Control Integration.

    1.  Navigate to **Connectors and use cases setup** &gt; **Service graph connectors tab**.

    2.  Locate the Service Graph Connector for SentinelOne integration.

    3.  Select the link that takes you to the app listing for the application in the ServiceNow® Store.

    4.  Follow the prompts to install the application.

    5.  Download the installation guide from the Supporting Links and Docs section on the app listing before you exit to help you with configuration and activation.

    6.  Navigate to **Setup** in your instance.

    7.  Follow the prompts in the guided setup and refer to the documentation to configure and activate the SGC.

2.  Navigate to **Connectors and use cases setup** &gt; **SPC API Integrations** to configure the SentinelOne Integration for Mitigation Control Integration.

    This tab lists the mitigation controls sources: CrowdStrike, F5 Big Ip, Defender, SentinelOne. The tab is displayed in the workspace only if you have installed the Mitigation Controls Monitoring application.

    On the source cards, you can view the status of the mitigation source \(`Active` or `Inactive`\).

    Note the Active column in Sources displays, `Active`. This indicates the source, in this case, the Service Graph Connector for SentinelOne, is active to retrieve asset data, but you must configure the SentinelOne Integration for Mitigation Control Integration before you can monitor mitigation controls on the imported assets.

3.  Select **Next**.

    The SentinelOne Configuration page is displayed with one SentinelOne Integration for Mitigation Control instance link.

4.  Select the instance link that is provided in the Name column.

5.  Fill out the fields for the SentinelOne Integration for Mitigation Control Integration.

    **Note:**

    Enter the same SentinelOne account information and server details for the SentinelOne Integration for Mitigation Control Integration that you provided for the Service Graph Connector for SentinelOne. This information ensures that you import mitigation data that matches the asset data that you imported with the service graph connector.

    Select the pen icon if you need to edit the fields.

    |Field|Description|
    |-----|-----------|
    |Instance name|Field is populated automatically with the instance name.|
    |API Key|Field populated automatically with the API key information.|
    |API URL|Host name for the SentinelOne server, for example: https//usea1-na.sentinelone.net|

6.  Select **Save and Test Credentials**.

    A `Valid` response for a successful connection is required to proceed to the next step.

7.  Select **Save and Exit**.

8.  Select **View details** on the SentinelOne card on the SPC API Integrations tab.

    Note that the source and API are activated, and the configuration progress bar is completed.

9.  Select **Revert to previous credentials** to insert credentials that you've previously validated.

10. Follow these steps to run the SentinelOne Asset Import Integration.

    1.  Navigate to **SentinelOne Mitigation Control** &gt; **Integrations**.

        There is one integration: SGC SentinelOne Asset Import.

    2.  Select the **SentinelOne Prevention Policy Integration** in the Name column to initiate the integration.

    3.  On the record, select the **Active** check box and select **Execute Now**.

        You can view the integration run status on the **Integration Run** tab from the integration records.

        The integration is scheduled to run daily by default.

        The SentinelOne Asset Import Integration imports only information about assets that have changed since the last integration run.


