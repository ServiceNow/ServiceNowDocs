---
title: Configure a new ERP Customization Mining connection
description: Specify the Connections and Credentials alias for ERP Customization Mining \(ERP-CM\) to connect to the ERP \(Enterprise Resource Planning\) system.
locale: en-US
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Customization Mining, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Configure a new ERP Customization Mining connection

Specify the Connections and Credentials alias for ERP Customization Mining \(ERP-CM\) to connect to the ERP \(Enterprise Resource Planning\) system.

## Before you begin

You should install ERP Data Hub and add credentials there before you install and configure ERP-CM. For more information, see [Configure the ERP Data Hub credentials and connection](../../erp-integration/task/set-up-erp-integration-connection.md).

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_mining.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Customization Mining**.

2.  Select the connection status icon \(![Credential alias page link](../image/credential-alias-icon.png)\) in the side panel.

3.  Select the **Select connection** button.

    If you have already configured a system connection and want to use a different connection and credential, see [Update an ERP-CM connection](update-ecm-connection.md).

4.  In the Connections and Credentials alias box, choose the credentials you configured in ERP Data Hub from the **Select connection &amp; credential alias** field.

5.  Select **Connect**.

    ERP-CM begins extracting data from the connection.

6.  Refresh the Issues to review list and the Executed tasks list by selecting their respective refresh icons \(![Refresh the Executed tasks list](../image/refresh-icon.png)\).

    ![Refresh the issues list or active connection tasks](../image/ecm-connection-status-page.png)


## What to do next

After the system is connected, you can check the connection status and investigate errors at any time on the Connection status page. For more information, see [Check and troubleshoot the data refresh status for ERP Customization Mining](erpcm-check-data-connection.md).

**Parent Topic:**[Configuring ERP Customization Mining](../concept/configuring-ecm.md)

