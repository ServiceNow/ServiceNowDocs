---
title: Run Guided Setup for ERP Data Hub
description: Run the Guided Setup to configure ERP Data Hub.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring ERP Data Hub, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Run Guided Setup for ERP Data Hub

Run the Guided Setup to configure ERP Data Hub.

## Before you begin

You must first download and install ERP Data Hub from the ServiceNow Store. For more information, see [Install ERP Data Hub](install-erp-integration.md).

Role required: sn\_erp\_integration.erp\_admin

## About this task

For more information on using Guided Setup, see [Guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Guided Setup**.

2.  Set up the MID Server in the MID Server setup section.

    1.  Select **Create MID user** and create the user account on the ServiceNow instance that will connect to the MID Server.

        For example, you can create mid.user.

    2.  Select **Download and install MID** and follow the instructions to download the appropriate MID Server installer archive for the operating system.

    3.  Select **Configure MID server files** and follow the instructions to configure the required MID Server files, which are detailed in the Guided Setup.

        For more information, see [Install ERP Data Hub](install-erp-integration.md).

3.  Set up the connection and credentials.

    1.  Select **Create credential record for the ERP system** and follow the steps.

    2.  Select **Create a connection record for ERP Data Hub** and follow the steps.

    3.  Select **Configure connection and capabilities** and complete the steps.

    Alternatively, you can configure without Guided Setup. For more information, see [Configure the ERP Data Hub credentials and connection](set-up-erp-integration-connection.md).

4.  Create and validate the ERP system.

    1.  Select **Create system** and follow the steps.

    2.  Select **Validate system** and follow the steps.

    Alternatively, you can configure without Guided Setup. For more information, see [Create an ERP system in ERP Data Hub](create-an-erp-system.md).

5.  Configure remote tables and extraction sources.

    1.  Select **Configure remote tables** and follow the steps.

        Alternatively, you can configure without Guided Setup. For more information, see [View and edit ERP remote table details with ERP Data Hub](erpi-find-tables.md).

    2.  Select **Configure extraction sources** and follow the steps.

        Alternatively, you can configure without Guided Setup. For more information, see [Add a new ERP extraction table in ERP Data Hub](erp-canvas-add-new-extraction-table.md).


**Parent Topic:**[Configuring ERP Data Hub](../concept/erp-integration-configuration-overview.md)

