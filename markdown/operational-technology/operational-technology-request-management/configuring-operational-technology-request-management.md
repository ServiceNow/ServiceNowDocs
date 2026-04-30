---
title: Configuring Operational Technology Request Management
description: Configure Operational Technology Request Management so that you can create the data foundation for the Operational Technology \(OT\) solution.
locale: en-US
release: zurich
product: Operational Technology Request Management
classification: operational-technology-request-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Operational Technology Request Management, Operational Technology]
---

# Configuring Operational Technology Request Management

Configure Operational Technology Request Management so that you can create the data foundation for the Operational Technology \(OT\) solution.

If you have the admin role, you can use Guided Setup to lead you through the setup of Operational Technology Request Management. Guided Setup is a tool that assists with application or capability configuration. It organizes the configuration activities into categories. These categories contain the information about the setup tasks, the steps to complete each task, and the links to the pages in your instance where you perform the configuration. The links to useful help content are also provided.

To access Guided Setup, navigate to **Industrial Workspace Admin** &gt; **Guided Setup**.

The following table lists the Guided Setup tasks and their purposes for Operational Technology Request Management.

**Note:** Operational Technology Request Management is included with the Industrial Workspace Common. No additional plugins are needed.

The following table shows the tasks that your users must complete for a successful setup and configuration.

<table id="table_vwx_mgb_1zb"><thead><tr><th>

Task

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

Load demo data.

</td><td>

To load the demo data for Operational Technology Request Management, you must load the demo data of the Industrial Workspace Common plugin. To load the demo data, complete the following steps.

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.
2.  In the search bar, search for the `Industrial Workspace Common` plugin.
3.  Once the results load, select the **Installed** tab and open the Industrial Workspace Common page.
4.  Under **Quick Actions**, select **Load demo data**.

</td></tr><tr><td>

Assign Operational Technology Request Management roles.

</td><td>

Assigns the roles to control the actions that are available for each user.

</td></tr><tr><td>

Create catalog items for your OT service catalog using the catalog builder.

</td><td>

Create catalog items for the OT Service Catalog using the catalog builder so other users can submit their OT requests and choose the catalog item that best fits their needs.

</td></tr><tr><td>

Add catalog item categories for the catalog items you create in the OT Service Catalog.

</td><td>

Select different categories for the catalog items you create in the OT Service Catalog to organize OT catalog items into logical groups.

</td></tr><tr><td>

Create a fulfillment flow for an OT request in Workflow Studio.

</td><td>

Create a fulfillment flow with catalog tasks in Workflow Studio for your catalog item as needed to fulfill an OT request.

</td></tr></tbody>
</table>-   **[Assign roles to your Operational Technology Request Management users](../task/assign-roles-oper-tech-request-management.md)**  
Assign roles to your users so that you can control their access to the features, capabilities, and data for Operational Technology Request Management.
-   **[Catalog item categories](catalog-item-categories-otrm.md)**  
You can select different categories for the catalog items you create in the Operational Technology \(OT\) Service Catalog. Categories help organize OT catalog items into logical groups. When requesters submit an OT request, they can choose the catalog item that best fits their needs based on its designated category.
-   **[Create a catalog item for your Operational Technology Service Catalog](../task/create-catalog-item.md)**  
Create a catalog item for the Operational Technology \(OT\) Service Catalog using the catalog builder so that other users can submit OT requests categorized by catalog item.
-   **[Create a fulfillment flow for an Operational Technology request](../task/create-a-fulfillment-flow-ot-request.md)**  
Create a fulfillment flow with catalog tasks in Workflow Studio for your catalog item as needed to fulfill an Operational Technology \(OT\) request.

**Parent Topic:**[Operational Technology Request Management](operational-technology-request-management-landing-page.md)

