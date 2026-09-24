---
title: Service catalog workflows
description: Two service catalog workflows are provided in the base system. Use the Graphical Workflow Editor to modify the default workflows or to create additional service catalog workflows. Service catalog workflows support domain separation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/request-management/c\_ServiceCatalogWorkflowDefinition.html
release: brazil
product: Request Management
classification: request-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Service Catalog request fulfillment, Configure, Request Management, IT Service Management]
---

# Service catalog workflows

Two service catalog workflows are provided in the base system. Use the Graphical Workflow Editor to modify the default workflows or to create additional service catalog workflows. Service catalog workflows support domain separation.

## Default service catalog workflows

-   **Service Catalog Request**: a simple workflow that fulfills a simple order.
-   **Service Catalog Item Request**: a more complex workflow that fulfills a more complex order.

\[Omitted image "image.SCWorkflow1"\] Alt text: Service Catalog Request workflow

\[Omitted image "image.SCWorkflow2"\] Alt text: Service Catalog Item Request workflow

## Defining service catalog workflows

Creating a workflow involves the following processes:

-   Create a workflow to process the catalog item.
-   Define the workflow activities to process the catalog item.
-   Publish the catalog item workflow.
-    to call the catalog item workflow

**Note:** If your catalog workflow requires catalog tasks to access catalog variables, create the catalog tasks from a parent workflow. A catalog workflow cannot access catalog variables from catalog tasks created by a subflow.

## Deleting catalog workflow records

Workflow stage fields for service catalog workflows display when a user deletes a record required by the workflow. If a user deletes a catalog item and that catalog item has active request workflows running, the workflow stage field displays **Catalog item removed**. Similarly, deleting the associated workflow context causes the stage field to display **Workflow context removed**.

## Associating items with the domain-specific workflow

When using service catalog workflows with domain separation, ensure your catalog items use the domain-specific workflow. If you create a domain-specific version of a workflow, existing catalog items continue to use the original workflow. To configure the catalog item to use the domain-specific workflow, select the new workflow in the **Workflow** field on the catalog item record.

-   **[Create a catalog workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/t_CreateANewServiceCatalogWorkflow.md)**  
Create service catalog workflows when the default workflows are not appropriate for a fulfillment process.
-   **[Add an activity to a catalog workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/t_AddActiviToServiceCataWorkflow.md)**  
You can add activities to a workflow to perform tasks such as running a script, sending notifications, or requesting approvals. Activities can succeed or fail, which can result in actions performed by other activities.
-   **[Publish a catalog workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/t_PublishAServiceCatalogWorkflow.md)**  
Publish the catalog workflow to make it available for use in the system.

**Parent Topic:**[Service Catalog request fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/request-fulfillment.md)

