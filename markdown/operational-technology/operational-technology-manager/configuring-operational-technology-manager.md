---
title: Configuring the Operational Technology Manager
description: Configure the Operational Technology Manager application so that you can create the data foundation for the ServiceNow Operational Technology solution.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Operational Technology Manager, Operational Technology]
---

# Configuring the Operational Technology Manager

Configure the Operational Technology Manager application so that you can create the data foundation for the ServiceNow® Operational Technology solution.

<table id="table_dt5_rxj_4nb"><thead><tr><th>

Task

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

1. Install Operational Technology \(OT\) extension classes.

</td><td>

Extend the Configuration Management Database \(CMDB\) class hierarchy for use in Operational Technology processing.

</td></tr><tr><td>

2. Install Operational Technology Manager.

</td><td>

Install the Operational Technology Manager application.

</td></tr><tr><td>

3. Assign Operational Technology roles.

</td><td>

Assigns roles to control the actions that are available for each user.

</td></tr><tr><td>

4. Prepare a Microsoft Excel spreadsheet for Service Graph Connector import.

</td><td>

Create and populate a Microsoft Excel spreadsheet with your existing Operational Technology data for upload to the ServiceNow AI Platform.For more information, see [Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import](../task/preparing-your-pre-import-ot-worksheet-entry-review-tool-for-sgc-import.md).

</td></tr><tr><td>

5. Import your Excel spreadsheet with an import task.

</td><td>

Upload your Operational Technology data to the Configuration Management Database \(CMDB\).For more information, see [Using the Service Graph Connector for Microsoft Excel through import tasks](use-excel-sgc-through-import-tasks.md).

</td></tr><tr><td>

6. Run the IT Discovery for OT Networks function.

</td><td>

Discover Operational Technology \(OT\) devices in the designated Purdue levels in your Industrial Control System \(ICS\) networks.For more information about Discovery for Operational Technology, see [IT Discovery for Operational Technology \(OT\) Networks](discovery-for-operational-technology.md).

</td></tr><tr><td>

7. Install Service Graph Connectors that are provided by ServiceNow® partners.

</td><td>

Install ServiceNow, Inc. connectors that are provided by partners as they become available in the ServiceNow® Store.

</td></tr><tr><td>

8. Use the **All OT Devices** or **All OT Devices by IP Address** selections on the **Operational Technology \(OT\)** menu.

</td><td>

Edit or view detailed information for the OT devices in your enterprise, after you've imported your Excel spreadsheet, or have run the IT Discovery for OT Networks function.

</td></tr></tbody>
</table>-   **[Implementing the CSDM framework for Operational Technology](../../operational-technology-management/csdm-implementation/concept/ot-use-case-product-view.md)**  
Following the CSDM framework ensures that you meet your primary goal of consistent accuracy in reporting and analytics so that you can effectively manage your Operational Technology \(OT\) environment.
-   **[Operational Technology \(OT\) extension classes installation](../task/install-operation-technology-ot-extension-classes.md)**  
You must install the Operational Technology \(OT\) extension classes that are the foundation of the Operational Technology Manager.
-   **[Install Operational Technology Manager](../task/install-operational-technology-manager.md)**  
If you have the admin role, you can install the Operational Technology Manager application. The application includes demo data and installs that are related ServiceNow® Store applications and plugins, if they are not already installed.
-   **[Script includes installed with Operational Technology Manager](../task/script_includes_installed_with_operational_technology_manager.md)**  
The Operational Technology Manager plugin installs the following script includes.
-   **[Assign Operational Technology Manager roles](../task/assign-operational-technology-manager-roles.md)**  
Assign roles to your users so that you can control their access to the features, capabilities, and data in the Operational Technology Manager application.

**Parent Topic:**[Operational Technology Manager](operational-technology-manager.md)

