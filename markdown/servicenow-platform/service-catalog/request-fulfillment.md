---
title: Service Catalog request fulfillment
description: When a user orders a catalog item, a request is created that follows a fulfillment process. A fulfillment process defines the steps to request approval, assign fulfillment tasks, and fulfill requests. Workflow Studio flows, workflows, or execution plans are used to define fulfillment processes.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog request fulfillment

When a user orders a catalog item, a request is created that follows a fulfillment process. A fulfillment process defines the steps to request approval, assign fulfillment tasks, and fulfill requests. Workflow Studio flows, workflows, or execution plans are used to define fulfillment processes.

Preparing to fulfill catalog item requests involves the following activities.

-   Set up fulfillment groups to assign to tasks.
-   Define the fulfillment processes using Workflow Studio flows, workflows, or execution plans.
-   Assign the fulfillment process to catalog items.

## Using Workflow Studio flows

The Workflow Studio application enables process owners to automate work, such as approvals, tasks, and notifications, without having to code. Build multi-step flows from reusable components. For more information, see [Exploring Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-workflow-studio&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Using workflows

Workflows provide greater flexibility than execution plans, which are linear. Workflows allow for different paths to the end of the process. For example, an approver can reject a request, ending the process. If the request is approved, the process continues through fulfillment to the end of the process.

Use the Workflow Editor to define fulfillment workflows. The Workflow Editor offers the following features.

-   Edit workflows graphically.
-   Modify activities and conditions.
-   Define transitions between workflow activities.
-   Summarize workflow progress through stages.
-   Validate workflows to identify potential problems.
-   Publish workflows for other users.

-   **[Service catalog workflows](c_ServiceCatalogWorkflowDefinition.md)**  
Two service catalog workflows are provided in the base system. Use the Graphical Workflow Editor to modify the default workflows or to create additional service catalog workflows. Service catalog workflows support domain separation.
-   **[Execution Plans](c_ExecutionPlans.md)**  
An execution plan describes how a catalog item is procured, configured, and installed.
-   **[Service Catalog checkout models](c_EnableATwoStepCheckout.md#)**  
The service catalog defaults to one-step checkout model, but also allows two-step checkout. Administrators and users with the catalog\_admin role can enable and configure the two-step checkout model and control how the delivery address is populated.
-   **[Create a catalog request from another flow](../task/create-request-from-other-flow.md)**  
You can create a catalog request to join the Service Catalog flow from a different flow. For example, from an incident flow, you can create a request, and associate the request with the incident. It helps you in tracking the requests associated with an incident and vice versa.
-   **[Configure a parent mapping for a request](../task/configure-mapping-for-request.md)**  
You can configure a mapping that specifies the association between the parent record and the request record.
-   **[State closure in the request fulfillment execution plan](../reference/state-closure-request.md)**  
The state closure in the request fulfillment process of a catalog item depends on the status of the associated catalog tasks, request items, and the request. It is applicable only for execution flows.
-   **[View request notifications](../task/view-request-notification.md)**  
View request notifications that are sent during specific events in a catalog request life cycle. These notifications are sent to various recipients including the Employee Center and ITIL users.

**Parent Topic:**[Configuring Service Catalog](configuring-service-catalog.md)

