---
title: Update an ERP Semantic Mining connection
description: Update the Connections and Credentials alias for ERP Semantic Mining to change the connection to the ERP \(Enterprise Resource Planning\) system. For example, you may want to change from a non-production system to a production system.
locale: en-US
release: zurich
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Update an ERP Semantic Mining connection

Update the Connections and Credentials alias for ERP Semantic Mining to change the connection to the ERP \(Enterprise Resource Planning\) system. For example, you may want to change from a non-production system to a production system.

## Before you begin

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

You should install Zero Copy Connector for ERP and add credentials there before you install and configure ERP Semantic Mining. For more information, see [Connect to a system of record from Zero Copy Connector for ERP](../../erp-integration/task/set-up-erp-integration-connection.md).

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_mining.erp\_admin

## About this task

**Warning:** Changing the system and credential alias deletes all existing data in the ERP Semantic Mining workspace and restarts the data integration process.

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Semantic Mining**.

2.  Select the connection status icon ![](../image/configuration-alias-icon.png) in the side panel.

3.  Select the **Change system** button.

4.  In the **Change system &amp; delete data** box, choose the system you configured in Zero Copy Connector for ERP from the **Select system to change to** field.

5.  Confirm your choice by selecting the **Yes, I am sure I want to change system and delete data** option.

6.  Select the **Change and delete data** button.

    ERP Semantic Mining begins to delete current data and restarts the data integration process.

7.  Refresh the Issues to review list and the Executed tasks list by selecting their respective refresh icons ![](../image/refresh-icon.png).


## What to do next

After the system is connected, you can check the connection status and investigate errors at any time on the Connection status page. For more information, see [Check and troubleshoot the data refresh status for ERP Semantic Mining](erpcm-check-data-connection.md).

**Parent Topic:**[Configuring ERP Semantic Mining](../concept/configuring-ecm.md)

