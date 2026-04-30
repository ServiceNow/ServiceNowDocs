---
title: Install and configure the CrowdStrike integrations for mitigation controls monitoring
description: The CrowdStrike Service Graph Connector and API integrations require separate configuration steps. You configure the CrowdStrike Service Graph Connector to import asset details. You configure the CrowdStrike API Integration to gather mitigation data about the assets that are monitored by CrowdStrike.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Policies for Exploit Protection \(EDR\), Use mitigation controls, Security Posture Control, Security Operations]
---

# Install and configure the CrowdStrike integrations for mitigation controls monitoring

The CrowdStrike Service Graph Connector and API integrations require separate configuration steps. You configure the CrowdStrike Service Graph Connector to import asset details. You configure the CrowdStrike API Integration to gather mitigation data about the assets that are monitored by CrowdStrike.

## Before you begin

-   Verify you have installed and activated the Security Posture Control and the Mitigation Controls Monitoring applications in your instance. These applications are available in the ServiceNow Store.
-   The CrowdStrike Service Graph Connector must be installed and configured before you configure the CrowdStrike API integration.

Roles required: admin for installation of plugins, and SPC Admin Group and SPC Analyst Group for configuration of integrations in the workspace.

## Procedure

1.  To install and configure the CrowdStrike Service Graph Connector integration, follow these steps:

    **Note:** If you have installed the Service Graph Connector for CrowdStrike, proceed to step 2 for how to configure the CrowdStrike API Integration.

    1.  Navigate to **Connectors and use cases setup** &gt; **Service graph connectors tab**.

    2.  Locate the CrowdStrike Endpoint Protection service graph connector.

    3.  Select the link that takes you app listing for the Service Graph Connector for CrowdStrike in the ServiceNow® Store.

    4.  Follow the prompts to install the application.

    5.  Download the installation guide from the Supporting Links and Docs section on the app listing before you exit to help you with configuration and activation.

    6.  Navigate to **CrowdStrike** &gt; **Setup** in your instance.

    7.  Follow the prompts in the guided setup and refer to the documentation to configure and activate the SGC.

2.  Navigate to **Connectors and use cases setup** &gt; **SPC API Integrations**.

    This tab lists the mitigation controls sources \(CrowdStrike, F5 Big Ip, and SCCM\), and the tab is displayed in the workspace only if you have installed the Mitigation Controls Monitoring application.

    On the source cards, you can view the status of the mitigation source \(`Active` or `Inactive`\) and the number of mitigation controls and their associated policies that are monitored by CrowdStrike \(6\). You can select the number to view the list.

    Note the Active column in Sources displays, `Active`. This indicates the source \(CrowdStrike SGC\) is active, but you must configure the CrowdStrike API Integration before you can monitor mitigation controls.

3.  Select **Next**.

4.  Select CrowdStrike in the Name column.

5.  Select Edit and fill out the fields.

    **Note:** Enter the same CrowdStrike account information and server details for the API Integration that you provided for the CrowdStrike Service Graph connector. This information ensures that you import mitigation data that matches the asset data that you imported with the service graph connector.

    |Field|Description|
    |-----|-----------|
    |Name|Instance name. You can change this name to help you save credentials without testing them. If you change any fields under the Name field, you must test the connection prior to saving and exiting.|
    |Asset Size Limit|Number of assets monitored.|
    |Client ID|CrowdStrike ID|
    |Client Secret|CrowdStrike Secret|
    |API URL|API URL, for example, https://api.crowdstrike.com|

6.  When you are ready, select **Test connection**.

    A message is displayed if the connection is successful.

7.  Select **Save and exit**.

8.  Select **View details** on the CrowdStrike card on the SPC API Integrations tab and note the source and API are activated, and the configuration progress bar is completed.

9.  If the credential test is not successful, you can select **Revert to previous credentials** to insert credentials you've previously validated.

10. Follow these steps to run the CrowdStrike integrations.

    1.  Navigate to **CrowdStrike Mitigation Control** &gt; **Integrations**.

        There are three integrations:

        -   CrowdStrike Prevention Policy Integration
        -   CrowdStrike Device Control Policy Integration
        -   CrowdStrike Asset Insight Integration
        The integrations are chained and run in a specific order. Successful completion of one integration initiates the next.

    2.  Select the CrowdStrike Prevention Policy Integration in the Name column to initiate the integration runs.

    3.  On the record, select the **Active** check box and select **Execute Now**.

        You can view the integration run status on the Integration Run tab from the integration records.

        The integration is scheduled to run daily by default.

        The CrowdStrike Asset Insight Integration imports only information about assets that have changed since the last integration run. The CrowdStrike Device Control Policy Integration and the CrowdStrike Prevention Policy Integration import all data for each run.


