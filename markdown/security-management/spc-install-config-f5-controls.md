---
title: Configure the F5 BIG-IP integrations for mitigation controls monitoring
description: The ITOM IP-based Discovery application and the F5 BIG-IP API integrations require separate configuration steps. You configure the ITOM IP-based Discovery application to import asset details. You configure the F5 BIG-IP API Integration to gather mitigation data about the assets that are monitored by ITOM IP-based Discovery.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Exploit protection \(WAF\), Use mitigation controls, Security Posture Control, Security Operations]
---

# Configure the F5 BIG-IP integrations for mitigation controls monitoring

The ITOM IP-based Discovery application and the F5 BIG-IP API integrations require separate configuration steps. You configure the ITOM IP-based Discovery application to import asset details. You configure the F5 BIG-IP API Integration to gather mitigation data about the assets that are monitored by ITOM IP-based Discovery.

## Before you begin

-   ITOM IP-based discovery must be up and running in the environment where F5 BIG-IP and any associated application servers are setup.
-   For on-premise assets, you must provide a MID Server.
-   Activate the source \(ITOM\) to gather data about the assets being monitored.
-   Activate the API Integration to gather mitigation data about the assets.

Roles required: admin for installation of plugins and creating system properties, and SPC Admin Group and SPC Analyst Group for configuration of integrations in the workspace.

## Procedure

1.  To install and configure the integration, follow these steps:

    **Note:** If you have installed and activated ITOM, proceed to step 2 for how to configure the F5 BIG-IP \(F5\) API Integration.

    1.  Navigate to **Connectors and use cases setup** &gt; **Service graph connectors tab**.

    2.  Select the F5 BIG-IP card.

    3.  Select the **ITOM Plugin** link to activate the ITOM plugin.

    4.  Follow the prompts.

2.  Navigate to **Connectors and use cases setup** &gt; **SPC API Integrations**.

    This tab lists the mitigation controls sources \(CrowdStrike and F5 Big Ip, and SCCM\), and the tab is displayed in the workspace only if you have installed the Mitigation Controls Monitoring application.

    On the source cards, you can view the status of the mitigation source \(`Active` or `Inactive`.

3.  Select **Next**.

    Note that the source \(ITOM\) is active, but you must configure and activate the F5 BIG-IP API Integration before you can monitor mitigation controls.

4.  Select F5 BIG-IP in the Name column.

5.  Select Edit and fill out the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Instance name. You can change this name to help you save credentials without testing them. If you change any fields under the Name field, you must test the connection prior to saving and exiting.|
    |Username|F5 BIG-IP username|
    |Password|F5 BIG-IP password.|
    |MID Server|Select a MID Server from the list.|
    |API URL|API URL with port 8443, for example, https://bigip.example.com:8443.|

6.  When you are ready, select **Test connection**.

    A message is displayed if the connection is successful.

    If the following error results from testing the connection during the configuration steps, `Session contains no certificates - Untrusted: Session contains no certificates - Untrusted`, set the following system properties to `false`:

    -   com.glide.communications.httpclient.verify\_hostname
    -   com.glide.communications.httpclient.verify\_revoked\_certificate
    A user with the admin role must create these system properties in the global scope if they are not listed on the System Property \[sys\_properties\] table. The system properties is Type, True/False \(Boolean\).

7.  Select **Save and exit**.

8.  On the F5 BIG-IP card on the SPC API Integrations tab and note the source and API are activated, and the configuration progress bar is completed.

9.  If the credential test is not successful, you can select **Revert to previous credentials** to insert credentials you've previously validated.

10. To run the API integrations, follow these steps:

    1.  Navigate to **F5 Big Ip Mitigation Control** &gt; **Integrations**

        There are Five integrations. The integrations are chained and run in a specific order. Successful completion of one integration initiates the next one:

        -   F5 Big IP Device Integration
        -   F5 Big IP Policy Integration
        -   F5 Big IP Attack Signature Integration
        -   F5 Big IP Virtual Server Integration
        -   F5 Big IP Pool Member Integration
    2.  To initiate the integration chain, select the **F5 Big IP Device Integration** in the Name column.

    3.  On the record, select the **Active** check box and select **Execute Now**.

    4.  View the status of the integration runs on the Integration Run tab from the integration records.

        The integration is scheduled to run daily by default.


