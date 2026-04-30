---
title: Configure the ERP Data Hub credentials and connection
description: Connect ERP Data Hub to a system of record \(such as SAP\) directly or using a load balancer to enable access to the ERP \(Enterprise Resource Planning\) system. You must select an existing, configured connection when you set up an ERP system.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring ERP Data Hub, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Configure the ERP Data Hub credentials and connection

Connect ERP Data Hub to a system of record \(such as SAP\) directly or using a load balancer to enable access to the ERP \(Enterprise Resource Planning\) system. You must select an existing, configured connection when you set up an ERP system.

## Before you begin

You must first create the alias for ERP Data Hub. For more information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

Role required: admin

## About this task

ERP Data Hub and ERP-CM currently support ECC \(minimum SAP Netweaver 7.31\) and S/4HANA SAP systems.

**Note:** The credentials you specify for the ERP Data Hub connection must match the service user credentials in the system of record.

Alternatively, you can run Guided Setup. For more information, see [Run Guided Setup for ERP Data Hub](erp-canvas-guided-setup.md).

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select the alias that you created for the new connection.

3.  Create a connection and credential.

    |Option|Description|
    |------|-----------|
    |**Create an RFC connection and credential**|Select a **Configuration Template** \(for example, ERP Data Hub SAP\) and then select **Create New Connection &amp; Credential** from the Related Links.|
    |**Create an HTTP connection and credential \(for OData to connect an external client to SAP\)**|Select **New**.|

4.  On the form, fill in the fields.

    You must specify a connection and login credential to be used simultaneously. That is, the connection you configure uses the defined login credentials for the connection.

    For a description of the field values, see [ERP Data Hub connection and credentials field descriptions](../reference/erp-canvas-system-connection-form-details.md). If you're creating an HTTP connection, see [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for field and MID Server details.

5.  Set up the ERP Data Hub connection.

    1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Home**.

    2.  Open the ERP systems list by selecting the systems icon \(![ERP systems icon](../image/erp-systems-icon-sidebar.png)\) in the side panel.

    3.  In the **Connection** column, select the **\(empty\)** cell.

        **Important:** You must select the empty row instead of creating a new row.

    4.  In the search box that appears, select the search icon \(![Search icon](../../erp-customization-mining/image/search-icon-connection.png)\).

    5.  On the Connection &amp; Credential Aliases dialog, select **sn\_erp\_integration.ERP\_Integration**.

    6.  Select the selection icon \(![Selection icon](../../erp-customization-mining/image/selection-check-icon.png)\).


**Parent Topic:**[Configuring ERP Data Hub](../concept/erp-integration-configuration-overview.md)

