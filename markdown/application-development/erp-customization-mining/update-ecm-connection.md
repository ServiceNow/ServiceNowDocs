---
title: Update an ERP-CM connection
description: Update the Connections and Credentials alias for ERP Customization Mining \(ERP-CM\) to change the connection to the ERP \(Enterprise Resource Planning\) system. For example, you may want to change from a non-production system to a production system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/erp-customization-mining/update-ecm-connection.html
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Customization Mining, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Update an ERP-CM connection

Update the Connections and Credentials alias for ERP Customization Mining \(ERP-CM\) to change the connection to the ERP \(Enterprise Resource Planning\) system. For example, you may want to change from a non-production system to a production system.

## Before you begin

You should install ERP Data Hub and add credentials there before you install and configure ERP-CM. For more information, see [Configure the ERP Data Hub credentials and connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/set-up-erp-integration-connection.md).

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_mining.erp\_admin

## About this task

**Warning:** Changing the system and credential alias deletes all existing data in the ERP-CM workspace and restarts the data integration process.

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Customization Mining**.

2.  Select the connection status icon \(\[Omitted image "credential-alias-icon.png"\] Alt text: Credential alias page link\) in the side panel.

3.  Select the **Change system** button.

4.  In the **Change system &amp; delete data** box, choose the system you configured in ERP Data Hub from the **Select system to change to** field.

5.  Confirm your choice by selecting the **Yes, I am sure I want to change system and delete data** option.

6.  Select the **Change and delete data** button.

    ERP-CM begins to delete current data and restarts the data integration process.

7.  Refresh the Issues to review list and the Executed tasks list by selecting their respective refresh icons \(\[Omitted image "refresh-icon.png"\] Alt text: Refresh the Executed tasks list\).

    \[Omitted image "ecm-connection-status-page.png"\] Alt text: Refresh the issues list or active connection tasks


## What to do next

After the system is connected, you can check the connection status and investigate errors at any time on the Connection status page. For more information, see [Check and troubleshoot the data refresh status for ERP Customization Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-customization-mining/erpcm-check-data-connection.md).

**Parent Topic:**[Configuring ERP Customization Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-customization-mining/configuring-ecm.md)

