---
title: Plugins activated for the Strategic Portfolio Management \(SPM\) integration
description: The Strategic Portfolio Management \(SPM\) integration is included with the Order Management application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Order Management integration with Strategic Portfolio Management, Integrate, Sales Customer Relationship Management]
---

# Plugins activated for the Strategic Portfolio Management \(SPM\) integration

The Strategic Portfolio Management \(SPM\) integration is included with the Order Management application.

The integration requires the following plugins, which are activated by users with the admin role:

|Plugin|Description|
|------|-----------|
|PPM Standard plugin \(com.snc.financial\_planning\_pmo\)|Activates the Project Portfolio Management Standard application, which installs Financial Management and the Project Portfolio Suite. The suite includes various applications for handling projects in your organization, such as Program Management, Project Management, and Demand Management. For more information on the Project Portfolio Suite, see [Project Portfolio Suite with Financials](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuiteWithFinancials&version=australia&pubname=australia-it-business-management&ft:locale=en-US).|
|Customer Project Management plugin\(com.snc.csm\_ppm\)|Activates the Customer Project Management integration with the PPM Standard application. This integration enables customer project managers to create and manage complex projects with multiple tasks. This integration also provides end users with visibility into those projects. For details on Customer Project Management, see [Integrating with Customer Project Management](https://www.servicenow.com/docs/access?context=csm-ppm-integration&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).|

## Access controls in the SPM integration

The SPM integration supports certain access controls for users with the following roles.

<table id="table_vkg_5vm_dyb"><thead><tr><th>

Role

</th><th>

Access controls in SPM integration

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

-   Order fulfillment agent \[sn\_ind\_tmt\_orm.order-fulfillment\_agent\]
-   Service order agent \[sn\_ind\_tmt\_orm.service\_order\_agent\]

</td><td>

Order fulfillment agents have read access to product orders, product order tasks, service orders, and resource orders. Service order agents have read access to service order requests, service orders, resource orders, and related fulfillment tasks. Agents have access to the following project information:

-   Read access to the Project form fields.
-   Read access to the Order Line Item to Project Relationship table.
-   Read access to the Order Line Item and Order Task related lists in PPM.
-   Read access to the Order task to Project Task related list in Order Management.

</td><td>

-   it\_project\_user
-   sn\_customerservice.projectmanager \(if using Customer Project Management\)

</td></tr><tr><td>

-   Order fulfillment manager \[sn\_ind\_tmt\_orm.order\_fulfillment\_manager\]
-   Service order manager \[sn\_ind\_tmt\_orm.service\_order\_manager\]

</td><td>

Order fulfillment managers receive orders, review order line items, verify that orders are ready for fulfillment, and then approves orders. Service order managers ensure that service orders are ready for fulfillment and then approve them. Managers can:

-   Post notes and comments on order lines and order tasks to communicate with the project manager.
-   View the relationship between a project and an order line item, project tasks, and order tasks. Managers have the following access to project information:
    -   Read access to the Order Line Item to Project Relationship table.
    -   Read access to the Order Line Item and Order Task related lists in PPM.
    -   Read access to the Order task to Project Task related list in Order Management.

</td><td>

sn\_ind\_tmt\_orm.order\_creator

</td></tr><tr><td>

IT project user \[it\_project\_user\]

</td><td>

-   Read access to the Project form fields.
-   Read access to the Order Line Item to Project Relationship table.
-   Read access to the Order Line Item and Order Task related lists in PPM.
-   Read access to the Order task to Project Task related list in Order Management.
-   Read access to the Project Template Creation table.

</td><td>

sn\_ind\_tmt\_orm.order\_viewer

</td></tr><tr><td>

IT project administrator \[it\_project\_admin\]

</td><td>

-   Configure access to all Project Management features.
-   Read and write access to the Project Template Creation table.
-   Read and write access to the Order Line Item related list in PPM.
-   Write access to the Order Task related list in PPM.
-   Read access to the Order Line Item to Project Relationship table.
-   Write access to the Order task to Project Task related list in Order Management.

</td><td>

-   it\_project\_user
-   sn\_ind\_tmt\_orm.order\_creator

</td></tr><tr><td>

Administrator \[admin\]

</td><td>

-   Creates the PPM project templates used to generate the projects for orders that require project oversight automatically.
-   Configures the mapping between order tasks and planned project tasks associated with project templates
-   Specifies the conditions and decision rules for determining project oversight and the project templates used to create those projects.
-   Controls automatic closure of project tasks

</td><td>

 

</td></tr></tbody>
</table>