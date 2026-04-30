---
title: Configuring the Industrial Process Manager
description: Configure the Industrial Process Manager application so that you can create the Equipment Model data foundation that is required for the ServiceNow Operational Technology solution.
locale: en-US
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Industrial Process Manager, Operational Technology]
---

# Configuring the Industrial Process Manager

Configure the Industrial Process Manager application so that you can create the Equipment Model data foundation that is required for the ServiceNow® Operational Technology solution.

**Note:**

If you have the admin role, you can use the Industrial Guided Setup to lead you through the setup of the Industrial Process Manager application.

To access the Guided Setup, navigate to **Industrial Workspace Admin** &gt; **Guided Setup**.

<table id="table_dt5_rxj_4nb"><thead><tr><th>

Task

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

1. Install the Industrial Process Manager from the ServiceNow Store.

</td><td>

Installs the Industrial Process Manager application and supporting plugins.

</td></tr><tr><td>

2. Assign Industrial Process Manager roles.

</td><td>

Assigns roles to control the actions that are available for each user.

</td></tr><tr><td>

3. Populate a Microsoft Excel spreadsheet for Service Graph Connector import.

</td><td>

Creates and populates a Microsoft Excel spreadsheet with your existing ISA-95 Equipment Model data for upload to the ServiceNow AI Platform.

</td></tr><tr><td>

4. Import your Excel spreadsheet.

</td><td>

Uploads your existing ISA-95 Equipment Model data to the Configuration Management Database \(CMDB\).

</td></tr><tr><td>

5. Install Service Graph\[service-graph\] connectors that are provided by ServiceNow® partners, and import the equipment model data using the integrations.

</td><td>

Installs ServiceNow connectors that are provided by partners as they become available in the ServiceNow® Store, and imports equipment model data.

</td></tr><tr><td>

6. Grant equipment model site access to users with non-administrative roles.

</td><td>

Assigns or removes site access for users with assigned cmdb\_ot\_isa\_viewer or cmdb\_ot\_isa\_editor roles.

</td></tr><tr><td>

Optional: [Automate mapping of OT devices](../../operational-technology-management/task/automate-mappings-between-ot-assets-and-equipment-model-entity.md)

</td><td>

Automates mapping of OT devices to the production process. **Note:** Enabling the mapping feature requires the following plugins:

-   [Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/operational-technology-manager.md)
-   [Industrial Process Manager](industrial-process-manager-overview.md)

</td></tr></tbody>
</table>-   **[Install the Industrial Process Manager](../task/install-manufacturing-process-mgr.md)**  
If you have the required entitlement and the Administrator \[admin\] role, you can install the Industrial Process Manager application and the related plugins.
-   **[Industrial Workspace Admin application menu and Guided Setup](../task/manufacturing-app-menu-guided-setup.md)**  
After you install the application and related plugins, you can use the Industrial Workspace Admin application menu to access the related Operational Technology Manager, Industrial Process Manager, Operational Technology Incident Management, Operational Technology Vulnerability Response, Operational Technology Change Management, Operational Technology Knowledge Management, and Operational Technology Request Management functions.
-   **[Assign Industrial Process Manager user roles](../task/assign-manufacturing-process-manager-roles.md)**  
Assign roles to your users so that you can control their access to the features, capabilities, and data in the Industrial Process Manager application.
-   **[View and edit OT system properties](../task/view-and-edit-ot-system-properties.md)**  
View and edit all of the Operational Technology \(OT\) related system properties for different applications.
-   **[Defining equipment model templates](defining-equipment-model-templates.md)**  
Create templates that you can assign to the equipment model entities that you created in the ServiceNow AI Platform. You can use these templates to characterize an equipment model or structure the data that describes your physical industrial facility by grouping similar types of equipment model entities.
-   **[Importing equipment model data](importing-isa95-equipment-model-etl.md)**  
The scheduled import function enables you to import your existing equipment model data from a populated Microsoft Excel flat-file spreadsheet. You can use it to import your ISA-95 Equipment Model data to the Configuration Management Database \(CMDB\).
-   **[Assign or remove equipment model site access for non-administrators](../task/create-user-criteria-for-equipment-model-entity-site-users.md)**  
Assign or remove equipment model site access for non-administrators. You can create the user criteria to determine whether certain users can access the equipment model entities for specific sites.
-   **[Managing an equipment model entity schedule](managing-equipment-entity-schedules.md)**  
You can manage an equipment model entity schedule with the Industrial Process Manager application. By using a schedule, you can track several maintenance tasks for one equipment model entity.

**Parent Topic:**[Industrial Process Manager](industrial-process-manager-overview.md)

