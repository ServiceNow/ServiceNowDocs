---
title: Run Guided Setup for ERP Canvas
description: Run the Guided Setup to configure ERP Canvas.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erp-canvas-guided-setup.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring ERP Canvas, ERP Canvas, Building low-code applications, Developing your application, Building applications]
---

# Run Guided Setup for ERP Canvas

Run the Guided Setup to configure ERP Canvas.

## Before you begin

You must first download and install ERP Canvas from the ServiceNow Store. For more information, see [Install ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/install-erp-integration.md).

Role required: sn\_erp\_integration.erp\_admin

## About this task

For more information on using Guided Setup, see [Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/guided-setup.md).

## Procedure

1.  Navigate to **All** &gt; **ERP Canvas** &gt; **ERP Canvas Guided Setup**.

2.  Set up the MID Server in the MID Server setup section.

    1.  Select **Create MID user** and create the user account on the ServiceNow instance that will connect to the MID Server.

        For example, you can create mid.user.

    2.  Select **Download and install MID** and follow the instructions to download the appropriate MID Server installer archive for the operating system.

    3.  Select **Configure MID server files** and follow the instructions to configure the required MID Server files, which are detailed in the Guided Setup.

        For more information, see [Install ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/install-erp-integration.md).

3.  Set up the connection and credentials.

    1.  Select **Create credential record for the ERP system** and follow the steps.

    2.  Select **Create a connection record for ERP Canvas** and follow the steps.

    3.  Select **Configure connection and capabilities** and complete the steps.

    Alternatively, you can configure without Guided Setup. For more information, see [Configure the ERP Canvas credentials and connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/set-up-erp-integration-connection.md).

4.  Create and validate the ERP system.

    1.  Select **Create system** and follow the steps.

    2.  Select **Validate system** and follow the steps.

    Alternatively, you can configure without Guided Setup. For more information, see [Create an ERP system in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/create-an-erp-system.md).

5.  Configure remote tables and extraction sources.

    1.  Select **Configure remote tables** and follow the steps.

        Alternatively, you can configure without Guided Setup. For more information, see [View and edit ERP remote table details with ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erpi-find-tables.md).

    2.  Select **Configure extraction sources** and follow the steps.

        Alternatively, you can configure without Guided Setup. For more information, see [Add a new ERP extraction table in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-add-new-extraction-table.md).


**Parent Topic:**[Configuring ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-integration-configuration-overview.md)

