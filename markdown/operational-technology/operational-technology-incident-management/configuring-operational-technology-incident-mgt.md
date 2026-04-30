---
title: Configuring Operational Technology Incident Management
description: Configure the Operational Technology Incident Management application so that you can create the data foundation for the ServiceNow Operational Technology solution.
locale: en-US
release: xanadu
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Operational Technology Incident Management, Operational Technology]
---

# Configuring Operational Technology Incident Management

Configure the Operational Technology Incident Management application so that you can create the data foundation for the ServiceNow® Operational Technology solution.

Operational Technology Incident Management v2 is dependent on Tokyo P5 or later.

**Note:**

If you have the admin role, you can use the Guided Setup to lead you through the setup of the Operational Technology Incident Management application. To access the Guided Setup, navigate to **Industrial Workspace Admin** &gt; **Guided Setup**.

<table id="table_dt5_rxj_4nb"><thead><tr><th>

Task

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

1. Install the Operational Technology Incident Management application from the ServiceNow Store.

</td><td>

Installs the Operational Technology Incident Management application and supporting plugins.

</td></tr><tr><td>

2. Assign Operational Technology Incident Management roles.

</td><td>

Assigns roles to control the actions that are available for each user.

</td></tr><tr><td>

3. Migrate OT Incidents.

</td><td>

Migrates OT incidents from the incident table to the OT incident table.**Note:** This step applies only when upgrading from Paris, San Diego, or Tokyo to Utah.

</td></tr><tr><td>

4. Configure categories and subcategories for OT incidents.

</td><td>

Configures categories and subcategories for OT incidents as needed.

</td></tr><tr><td>

5. Configure state models.

</td><td>

Configures state models for OT incident sites.

</td></tr><tr><td>

6. \(Optional\) Create an assignment rule.

</td><td>

Create an assignment rule to automatically assign an OT incident to the right group or user.

</td></tr></tbody>
</table>-   **[Install Operational Technology Incident Management](install-operational-technology-service-management.md)**  
You can install the Operational Technology Incident Management application \(sn\_ot\_inc\_mgmt\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Migrate incidents to the new incident table](../task/migrate-operational-technology-incidents.md)**  
Migrate Operational Technology incidents from the old incident table to the new incident table. Migrating incidents lets the Operational Technology Incident Management application know that the old table is no longer applicable.
-   **[Assign roles to your users](../task/assign-operational-technology-incident-management-roles.md#)**  
Assign roles to your users in the Operational Technology Incident Management application so that you can control their access to the features, capabilities, and data.
-   **[Create an assignment group](../task/create-ot-specific-assignment-groups.md)**  
Create an Operational Technology \(OT\) specific assignment group to assign to OT incident records.
-   **[Incident categories and subcategories](../reference/ot-incident-categories-subcategories.md)**  
By categorizing Operational Technology \(OT\) incidents, you can group and narrow the search for specific OT incidents.
-   **[Create an incident state model](../task/create-ot-incident-site-state-model.md)**  
Create an Operational Technology \(OT\) incident state model for your sites. By using an incident state model, you can manage the life cycle of the related incidents.
-   **[Define a priority lookup rule for incidents](../task/define-priority-lookup-rules.md)**  
Define the impact and urgency of an Operational Technology incident to calculate its priority. You can then use the priority calculation to prioritize your work and to drive service level agreements \(SLAs\) in your organization.
-   **[Set the system properties](../task/configure-ot-incident-management-properties.md)**  
Set the system properties for the Operational Technology Incident Management application so that you can enable the incident properties as needed.
-   **[Create an assignment rule](../task/create-assignment-rule.md)**  
Create an assignment rule to automatically assign an Operational Technology \(OT\) incident to a group or user according to one or more conditions in the assignment rule. You use assignment rules to run at the time that you open an OT incident.

**Parent Topic:**[Operational Technology Incident Management](operational-technology-incident-management-landing-page.md)

