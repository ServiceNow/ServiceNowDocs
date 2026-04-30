---
title: Order Management integration with Strategic Portfolio Management
description: The Order Management application provides an integration with the ServiceNow Strategic Portfolio Management \(SPM\) application enables project oversight of complex order fulfillment tasks. Use this integration to handle order line items and planned order tasks as projects in SPM.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Extending Order Management with ServiceNow applications and integrations, Sales Customer Relationship Management]
---

# Order Management integration with Strategic Portfolio Management

The Order Management application provides an integration with the ServiceNow® Strategic Portfolio Management \(SPM\) application enables project oversight of complex order fulfillment tasks. Use this integration to handle order line items and planned order tasks as projects in SPM.

## Features

-   Automates the creation of SPM projects based on project oversight rules, enabling project managers to track order fulfillment activities within a project in SPM.
-   Synchronizes order fulfillment tasks in Order Management to an associated project in SPM, providing project managers with real-time task activity updates via state change information, notes, and comments.
-   Enable fulfillment agents, managers, and project managers to view related lists that show the relationship between an order line item and project, domain order and project task, and order task and project task.
-   Supports tracking and synchronization of one or more order tasks.
-   Supports staggered/in-flight orders for new tasks created as part of staggered decomposition or in-flight changes. Uses predefined planned order tasks that enable synchronization between order fulfillment and project tasks.
-   Closes project tasks automatically when child tasks and associated order tasks or domain orders are completed or canceled.

## Benefits

-   Gives project managers end-to-end project oversight of complicated orders, such as long-running orders that require delivery to a specific customer account with multiple locations.
-   Manages risks by identifying issues that affect project dependencies and timely order fulfillment.
-   Eliminates manual tracking of order status between SPM and Order Management applications. Reduces inefficient communication between project managers, fulfillment agents and managers, and other project stakeholders.

## How the SPM integration works

The Order Management integration with Strategic Portfolio Management uses the Project Portfolio Management \(PPM\) standard application in SPM to track fulfillment tasks as projects in your organization. This integration also works with the Customer Project Management application if you want to track customer order fulfillment tasks as customer projects automatically.

-   **Configuration**

    Admins set up the SPM integration by configuring these items:

    -   Project templates: Create the PPM project templates that are used to generate the SPM projects automatically for orders requiring project oversight. Project templates also define the planned tasks for order delivery.
    -   Order Management project oversight conditions and rules: Set the conditions and decision rules that determine the orders that qualify for project oversight and the project templates used to create those projects. You use different Project Management Oversight decision tables to specify the conditions and rules for order lines, domain orders, and order tasks and the appropriate project template to be used.
    -   Field mapping in CSM table maps: Associate Order Management fields to SPM project fields by configuring the field mapping in the CSM table maps.
    -   Property for automatic closure of project tasks: Control the automatic closure of project tasks when associated child tasks are completed by using the **sn\_ind\_tmt\_orm.project.task.auto.closure** system property.
-   **SPM integration flow**

    After an order line is created and approved, Order Management performs the following processing steps.

    -   Project oversight determination: Qualifies the order line for project oversight.

        -   Checks that the order line is valid and that the PPM Standard application is installed.
        -   Reviews the project oversight conditions and decision rules for order lines.
        -   If the order line matches the conditions, automatically creates the project and project tasks using the specified project template.
        **Note:** If multiple order lines are eligible for oversight, the system creates multiple projects.

    -   One-time synchronization: Synchronizes the order line with the project, establishing the relationship between the order line and the project.
    -   Project task oversight determination: After Order Management decomposes the order line item into domain orders and order tasks, it does the following:
        -   Checks the project oversight conditions for domain orders. If a domain order meets the project oversight conditions, creates the associated project and planned tasks using the project template task specified.
        -   Checks the project oversight conditions for order tasks. If order tasks meet the project oversight conditions, creates the associated project and planned tasks using the project template task specified.
        -   Links domain orders and order tasks back to the parent project, synchronizing attributes from the domain orders and order tasks to the project tasks.
    -   Order task state changes: As order task states change in Order Management, synchronizes the state and status with corresponding project tasks in SPM so that project managers and other project stakeholders can view the changes in real time.
    -   Updates to project notes and comments: Automatically updates project notes and project task notes when fulfillment managers or agents post work notes and comments in order line items, domain orders, and order tasks.
    -   Project task closure: Automatically closes project tasks for order tasks, including child tasks, that have been completed in Order Management.

## Plugins for the SPM integration

The SPM integration is included with the Order Management application. The integration requires the following plugins, which are activated by users with the admin role:

-   PPM Standard plugin \(com.snc.financial\_planning\_pmo\): Activates the Project Portfolio Management Standard application, which installs Financial Management and the Project Portfolio Suite. The suite includes various applications for handling projects in your organization, such as Program Management, Project Management, and Demand Management. For more information on the Project Portfolio Suite, see [Project Portfolio Suite with Financials](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuiteWithFinancials&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).
-   Customer Project Management plugin \(com.snc.csm\_ppm\): Activates the Customer Project Management integration with the PPM Standard application. This integration enables customer project managers to create and manage complex projects with multiple tasks. This integration also provides end users with visibility into those projects. For details on Customer Project Management, see [Integrating with Customer Project Management](https://www.servicenow.com/docs/access?context=csm-ppm-integration&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

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
</table>## Next step

As an admin, review the setup tasks in [Configuring the Strategic Portfolio Management integration](configuring-spm-integration.md).

