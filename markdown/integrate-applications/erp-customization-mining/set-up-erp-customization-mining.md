---
title: Configure a new ERP Semantic Mining connection
description: Specify the Connections and Credentials alias for ERP Semantic Mining to connect to the ERP \(Enterprise Resource Planning\) system.
locale: en-US
release: zurich
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Configure a new ERP Semantic Mining connection

Specify the Connections and Credentials alias for ERP Semantic Mining to connect to the ERP \(Enterprise Resource Planning\) system.

## Before you begin

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

You should install Zero Copy Connector for ERP and add credentials there before you install and configure ERP Semantic Mining. For more information, see [Connect to a system of record from Zero Copy Connector for ERP](../../erp-integration/task/set-up-erp-integration-connection.md).

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_mining.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Semantic Mining**.

2.  Select the configuration icon ![](../image/configuration-alias-icon.png) in the side panel.

3.  Select the **Select connection** button.

    If you have already configured a system connection and want to use a different connection and credential, see [Update an ERP Semantic Mining connection](update-ecm-connection.md).

4.  In the Connections and Credentials alias box, choose the credentials you configured in Zero Copy Connector for ERP from the **Select connection &amp; credential alias** field.

5.  Select **Connect**.

    ERP Semantic Mining begins extracting data from the connection.

6.  Refresh the Issues to review list and the Executed tasks list by selecting their respective refresh icons ![](../image/refresh-icon.png).


## What to do next

After the system is connected, you can check the connection status and investigate errors at any time on the Connection status page. For more information, see [Check and troubleshoot the data refresh status for ERP Semantic Mining](erpcm-check-data-connection.md).

**Parent Topic:**[Configuring ERP Semantic Mining](../concept/configuring-ecm.md)

