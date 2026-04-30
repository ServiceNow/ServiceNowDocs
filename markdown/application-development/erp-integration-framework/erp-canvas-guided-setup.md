---
title: Run Guided Setup for Zero Copy Connector for ERP
description: Run the Guided Setup to configure Zero Copy Connector for ERP.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Zero Copy Connector for ERP, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Run Guided Setup for Zero Copy Connector for ERP

Run the Guided Setup to configure Zero Copy Connector for ERP.

## Before you begin

You must first download and install Zero Copy Connector for ERP from the ServiceNow Store. For more information, see [Install Zero Copy Connector for ERP](install-erp-integration.md).

Role required: sn\_erp\_integration.erp\_admin

## About this task

For more information on using Guided Setup, see [Guided Setup](https://www.servicenow.com/docs/access?context=guided-setup&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Guided Setup**.

2.  Set up the MID Server in the MID Server setup section.

    1.  Select **Create MID user** and create the user account on the ServiceNow instance that will connect to the MID Server.

        For example, you can create mid.user.

    2.  Select **Download and install MID** and follow the instructions to download the appropriate MID Server installer archive for the operating system.

    3.  Select **Configure MID server files** and follow the instructions to configure the required MID Server files, which are detailed in the Guided Setup.

        For more information, see [Install Zero Copy Connector for ERP](install-erp-integration.md).

3.  Set up the connection and credentials.

    1.  Select **Create credential record for the ERP system** and follow the steps.

    2.  Select **Create a connection record for Zero Copy Connector for ERP** and follow the steps.

    3.  Select **Configure connection and capabilities** and complete the steps.

    Alternatively, you can configure without Guided Setup. For more information, see [Configure the Zero Copy Connector for ERP credentials and connection](set-up-erp-integration-connection.md).

4.  Create and validate the ERP system.

    1.  Select **Create system** and follow the steps.

    2.  Select **Validate system** and follow the steps.

    Alternatively, you can configure without Guided Setup. For more information, see [Create an ERP system in Zero Copy Connector for ERP](create-an-erp-system.md).

5.  Configure remote tables and extraction sources.

    1.  Select **Configure remote tables** and follow the steps.

        Alternatively, you can configure without Guided Setup. For more information, see [View and edit ERP remote table details with Zero Copy Connector for ERP](erpi-find-tables.md).

    2.  Select **Configure extraction sources** and follow the steps.

        Alternatively, you can configure without Guided Setup. For more information, see [Add a new ERP extraction table in Zero Copy Connector for ERP](erp-canvas-add-new-extraction-table.md).


**Parent Topic:**[Configuring Zero Copy Connector for ERP](../concept/erp-integration-configuration-overview.md)

