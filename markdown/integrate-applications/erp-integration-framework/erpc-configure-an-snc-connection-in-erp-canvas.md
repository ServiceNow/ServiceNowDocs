---
title: Configure an SNC connection in Zero Copy Connector for ERP
description: Learn how to set up an SNC connection, including preparing the environment, configuring the SAP system, and testing the configuration.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, snc, configure, test, connection, kerberos, security, sn\_erp\_integration.ERP\_Canvas\_RFC]
breadcrumb: [Use an SNC connection, Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Configure an SNC connection in Zero Copy Connector for ERP

Learn how to set up an SNC connection, including preparing the environment, configuring the SAP system, and testing the configuration.

## Before you begin

Role required: admin

Confirm that you have the following:

-   An SNC-compatible security library, such as SAP Secure Login Library or a Kerberos-based library.
-   Administrative access to the SAP system and the server where it's hosted.

## Procedure

1.  Install the required security library on the MID Server by navigating to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Search for and open the **Zero Copy Connector for ERP RFC** alias with the ID sn\_erp\_integration.ERP\_Canvas\_RFC.

3.  In **Related Links**, select **Create New Connection &amp; Credential**.

    ![Alias record with name, ID, and related link option highlighted.](../image/erpc-snc-connection1.png)

4.  Complete the form.

    For information about the fields, see [Configure the Zero Copy Connector for ERP credentials and connection](set-up-erp-integration-connection.md).

5.  Restart the MID Server to apply the changes.

    For more information, see Manually start, stop, and restart a MID Server.

6.  Verify that the SNC configuration is working correctly.

    1.  Go to **All** &gt; **Workflow Studio**.

    2.  On the home page, select **Actions**.

    3.  Hover over the **Name** column and select the filter icon.

        ![Workflow Studio actions tab with name column filter icon highlighted.](../image/erpc-snc-connection2.png)

    4.  Filter for **contains** and type `heartbeat`.

    5.  Select **Apply**.

    6.  Select **HeartBeat**.

    7.  Select **Test**.

    8.  Specify a **system** and then select **Run Test**.

        ![Test action window with system field and run test button highlighted.](../image/erpc-snc-connection3.png)

    9.  When the test is complete, select the link **Your test has finished running. View the Action execution details**.

    10. Verify that the connection properties set are passed as input.

    11. Verify that **isAlive** is true, and if it's false, validate the parameters.


-   Confirm that the security library is correctly installed and accessible. For more information, see [The SAP Security Library \(SAPSECULIB\)](https://help.sap.com/docs/SAP_NETWEAVER_700/12a37b156c5310149ffbe290df0708d6/b8821ff4dadd11d2a60a0000e835363f.html) on the SAP help site.
-   Verify that the SNC parameters are correctly set. For more information, see [Setting the SNC Parameters](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/2f64847a81a84bda878e32d5a4dae0a2/ce1dfd3d4aefd95ee10000000a114084.html) on the SAP help site.
-   Check the SNC PSE for validity and correct DN entries. For more information, see [Creating or Replacing a PSE](https://help.sap.com/doc/saphelp_nw73ehp1/7.31.19/en-US/59/6b653a0c52425fe10000000a114084/content.htm?no_cache=true) on the SAP help site.
-   Confirm that the SAP clients are properly configured to use SNC. For more information, see Configuring MID Server.

**Parent Topic:**[Use an SNC \(Secure Network Communication\) connection in Zero Copy Connector for ERP](../concept/erpc-use-an-snc-connection-in-erp-canvas.md)

