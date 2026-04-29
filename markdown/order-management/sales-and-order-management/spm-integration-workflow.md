---
title: Strategic Portfolio Management integration workflow
description: The workflow shows how the Strategic Portfolio Management integration works.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Order Management integration with Strategic Portfolio Management, Integrate, Sales and Order Management]
---

# Strategic Portfolio Management integration workflow

The workflow shows how the Strategic Portfolio Management integration works.

## How the SPM integration works

The Order Management integration with Strategic Portfolio Management uses the Project Portfolio Management \(PPM\) standard application in SPM to track fulfillment tasks as projects in your organization. This integration also works with the Customer Project Management application if you want to track customer order fulfillment tasks as customer projects automatically.

-   **Configuration**

    Admins set up the SPM integration by configuring these items:

    -   Project templates: Create the PPM project and site project templates that are used to generate the SPM projects automatically for orders requiring project oversight. Project templates also define the planned tasks for order delivery.
    -   Order Management project oversight conditions and rules: Set the conditions and decision rules that determine the orders that qualify for project oversight and the project templates used to create those projects. You use different Project Management Oversight decision tables to specify the conditions and rules for order lines, site locations, domain orders, and order tasks and the appropriate project template to be used.
    -   Field mapping in CSM table maps: Associate Order Management fields to SPM project fields by configuring the field mapping in the CSM table maps.
    -   Property for automatic closure of project tasks: Control the automatic closure of project tasks when associated child tasks are completed by using the **sn\_ind\_tmt\_orm.project.task.auto.closure** system property.
    -   Property for program and site project reuse: Use the system property **sn\_ind\_tmt\_orm.reuse\_existing\_program\_and\_project\_enabled** to reuse the program and site project for the following conditions:

        -   If the program is created for the same account.
        -   If the site project is already created for the same location.
        Set the property to true to reuse the program and site project.

        If the property is set to false, a new program and site project will be created for the new order.

-   **SPM integration flow**

    After an order line is created and approved, Order Management performs the following processing steps.

    -   Project oversight determination: Qualifies the order line for project oversight.

        -   Checks that the order line is valid and that the PPM Standard application is installed.
        -   Reviews the project oversight conditions and decision rules for order lines.
        -   If the order line matches the conditions, automatically creates the project and project tasks using the specified project template.
        **Note:** If multiple order lines are eligible for oversight, the system creates multiple projects.

    -   One-time synchronization: Synchronizes the order line with the project, establishing the relationship between the order line and the project.
    -   Site project oversight determination: Qualifies the site location for site project oversight.

        -   Checks that at least one order line project should be created.
        -   Reviews the site project oversight conditions and decision rules for site location.
        -   If the offering and site location matches the conditions, automatically creates the site project and site project tasks using the specified site project template.
        -   Site projects are created on **pm\_project table**.
        -   Establishing the relationship between the site project and site location in the relationship table.
        To configure site project oversight for product offering, see [Configure project oversight for Product offering](../task/configure-site-project-product-offering.md).

    -   Project task oversight determination: After Order Management decomposes the order line item into domain orders and order tasks, it does the following:
        -   Checks the project oversight conditions for domain orders. If a domain order meets the project oversight conditions, create the associated project and planned tasks using the project template task specified.
        -   Checks the project oversight conditions for order tasks. If order tasks meet the project oversight conditions, create the associated project and planned tasks using the project template task specified.
        -   Links domain orders and order tasks back to the parent project, synchronizing attributes from the domain orders and order tasks to the project tasks.
    -   Order task state changes: As order task states change in Order Management, synchronizes the state and status with corresponding project tasks in SPM so that project managers and other project stakeholders can view the changes in real time.
    -   Updates to project notes and comments: Use the task relationship table **task\_rel\_task** to synchronize between the order task and project task. Automatically updates project notes and project task notes when fulfillment managers or agents post work notes and comments in order line items, domain orders, and order tasks.
    -   Synchronization: Use the **csm\_table\_map** table to synchronize the work note fields between order task, domain order, and project task. It is possible to configure synchronization for fields such as name, work notes, description, and others as required.
    -   Project task closure: Automatically closes project tasks for order tasks, including child tasks, that have been completed in Order Management.

