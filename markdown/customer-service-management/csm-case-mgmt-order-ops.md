---
title: Order Operations Case Management
description: The Order Operations Case Management application enables customer service agents to create cases for multiple customer orders or for specific products within an order.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Order Operations Case Management

The Order Operations Case Management application enables customer service agents to create cases for multiple customer orders or for specific products within an order.

![Order case page with customer and account information, SLA, and case details. Center panel displays the Order Case Line list. Page also includes the configurable side panel.](../image/csm-order-ops-order-case-page.png "Order case page with Order Case Line list")

The Order Operations Case Management application includes the Orders case type. This case type provides the ability to reference multiple orders or order lines as case line items on an order case record. By using case line items, agents can track multiple issues for the same order case and resolve the issues in each case line item independently before resolving and closing the order case.

Use order cases to handle issues such as change order requests, including changes in ordered quantities or expedited shipping requests, or other order-related issues. With this application, agents can:

-   Create new order cases and add the requested orders or order lines to the case as case line items.
-   Add or remove orders or order lines from existing order cases.
-   Edit existing case line items or create new case line items for order cases.
-   Review the changes that have been requested on case line items.
-   Create tasks for case line items and assign them to other agents or team members.
-   Manage and track the requests and the actions taken to fulfill orders.
-   Resolve the individual case line items before resolving the case.

## Benefits of using order cases

Businesses can encounter order issues for many reasons such as inventory discrepancies, payment processing problems, or shipping and delivery errors. Order issues can also result from customer input mistakes or changes in customer needs, such as faster shipping or quantity changes. The following table provides some examples of these issues and the resulting order cases.

|Reason|Request/Issue|Order case example|
|------|-------------|------------------|
|Change in quantity|A customer wants to increase or decrease the quantity of an item in their order.|An order case is created to document the request and confirm stock availability.​|
|Change in delivery date|A customer requests to change the delivery date for their order.|An order case is created to coordinate with logistics and confirm the new delivery schedule.​|
|Change in address|A customer needs to update the shipping address after placing the order.​|An order case is created to ensure the change is processed before shipping.​|
|Price discrepancy|A customer notices that the price charged differs from the agreed price.|An order case is created to investigate and correct the billing.​|
|Incorrect item ordered|A customer received the wrong product.|An order case is created to initiate the return process and ensure the correct item is sent.​|
|Cancellation of order lines|A customer wants to cancel specific items in their order. ​|An order case is created to confirm which items can be canceled and update the order accordingly.|

## Overview of creating an order case

The following table provides an overview of the process for creating an order case. For detailed steps, see [Create an order case](../task/csm-order-ops-create-order-case.md).

<table id="table_hpc_lhk_fdc"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Creating an order case

</td><td>

An agent can create an order case in the following ways:-   Selecting **Create case** from a customer order.
-   Selecting **Create case** from the Order Line Items list on a customer order \(after selecting one or more order lines\).
-   Selecting **Create case** from an interaction record.
-   Selecting **New** from the Order Cases list view.

</td></tr><tr><td>

Selecting a service

</td><td>

After initiating an order case, the agent selects an order-related service from the case type selector modal.This modal displays the services that are available for order cases, such as Sales Order Change Request or Sales Order Dispute.

</td></tr><tr><td>

Filling in details on the Create New Order Case intake form

</td><td>

Selecting **Create case** from the case type selector modal displays the intake form where the agent can enter the following order case details:-   **Account**: the account for the order.
-   **Scope of request**: the agent can create a case for order lines from a single order or for multiple complete orders.
-   **Order number**: the order number associated with the order case.
-   **Short description**: a brief description of the order case.

Depending on where the agent creates the order case from, some of these fields are auto filled.

</td></tr><tr><td>

Viewing the order case record

</td><td>

Selecting **Save** on the intake form creates the Order case record in Draft state.From this record, agents can:

-   Add orders or order lines to the order case.
-   Delete orders or order lines from the order case.
-   Create new order case line items.
-   Edit the details of order case line items.
-   Assign order case line items to themselves.
-   Create tasks for order case line items.

</td></tr><tr><td>

Submitting the order case record

</td><td>

Selecting **Submit** on the Order case record moves the order case and the order case line items to the New state. Once in the New state, agents can begin working to resolve the order case. This includes [creating tasks for order case line items](../task/csm-order-ops-order-case-create-task.md), assigning them to other agents or team members, and monitoring case progress.

</td></tr></tbody>
</table>## Order Operations Case Management plugin

Order Operations Case Management \(com.sn\_order\_case\) is a case management application for handling support requests on orders or order lines. This application enables customers to process order-related services such as inflight order changes, order inquiries, and order dispute requests. It provides an order case type that includes order line items that need changes, workflows, and agent and customer experiences.

The Order Operations Case Management application includes list views for CSM Configurable Workspace and Core UI.

-   In CSM Configurable Workspace, expand the **Order Cases** list category in the Lists tab.
-   In Core UI, navigate to **All** &gt; **Customer Order Management** &gt; **Order Cases**.

The Order Operations Case Management application also includes tables, roles, service definitions and other components. For more information, see [Components installed with Order Operations Case Management](csm-case-mgmt-order-ops-install-comp.md).

The Order Operations Case Management application is available from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Related topics**  


[Case lines and workflows](csm-case-mgmt-case-lines.md)

