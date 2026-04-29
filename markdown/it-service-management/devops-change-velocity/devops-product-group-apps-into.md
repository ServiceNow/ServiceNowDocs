---
title: Group DevOps applications into a product
description: Products that use an application model in the CSDM support hierarchies of applications. You can customize hierarchies to simplify tracking of "rolled-up" data on DevOps Insights reports. This is used for the Product filter in insights.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Insights reports, DevOps Change Velocity, IT Service Management]
---

# Group DevOps applications into a product

Products that use an application model in the CSDM support hierarchies of applications. You can customize hierarchies to simplify tracking of "rolled-up" data on DevOps Insights reports. This is used for the Product filter in insights.

## Before you begin

Role required: application owner, sn\_devops.admin

## About this task

For example, you can include multiple DevOps microservice applications into a product, include multiple such products into a portfolio, and then include \("roll up"\) the portfolio in an organization. Another example structure might be **application &gt; team &gt; product &gt; portfolio or business unit**.

-   A DevOps application can belong to one or multiple products.
-   A product or multiple products can belong to one or multiple other products.
-   Multiple applications and products can belong to a product.

For every product, the system creates a corresponding entry in the application model and SDL component tables.

**Important:** To add an application to a product, the application must hold execution data. For a newly added application, therefore, you must wait until the data import job has run.

## Procedure

1.  Create applications as described in [Create an application - Workspace](app-create-workspace.md).

2.  Open the application models table: `<instanceName>/cmdb_application_product_model_list.do` and then follow this procedure to configure each application that will be included in a product.

    1.  In the Application models list, select the application model to open the record.

    2.  On the Application model form, in the **Model categories** field, select the appropriate category.

    3.  Save the record.

3.  Follow this procedure to create a product that will act as a parent.

    1.  In the Application models list, select **New**.

    2.  On the Application model form, in the **Name** field, enter the name of the product.

    3.  In the **Model categories** field, select **Bundle**.

    4.  Enter a short description.

    5.  Save the record.

4.  Open the Model category of component table \(`<instanceName>/cmdb_m2m_model_component_list.do`\) to specify the category of each application \(the application is the component in this case\).

5.  For each application, select **New**, specify the following settings, and then submit the record.

    |Field|Description|
    |-----|-----------|
    |Model category of component|The **Model categories** value that you specified for the application on the Application model form.|
    |Component|The application.|
    |Bundle|The product that will act as a parent of the application.|

    The application is now a member of the specified product.


## Result

The DevOps Insights tabs provides filters for the reports.

-   The scheduled "Data collection" job processes your changes. When the job finishes, you can view reports for the added products. If you are running the job manually, execute the "Update Repo Details and Work Item State Detail" job before executing the Data collection job.
-   The **Application** filter lists all applications.
-   The **Product** filter lists all applications plus all products.
-   To view the members of a product, view the list in the Model category of component table \(`<instanceName>/cmdb_m2m_model_component_list.do`\). Applications are listed in the **Component** column and products are listed in the **Bundle** column.

