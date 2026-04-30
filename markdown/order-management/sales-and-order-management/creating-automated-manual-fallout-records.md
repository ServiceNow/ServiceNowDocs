---
title: Creating automated and manual fallout records
description: With Fallout Management, a provider can create manual or automated fallout records for specific order tasks so that your orders can continue processing through to completion.Create a fallout record manually for an order task that has a condition or issue that prevents it from being completed.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Managing order fallout, Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Creating automated and manual fallout records

With Fallout Management, a provider can create manual or automated fallout records for specific order tasks so that your orders can continue processing through to completion.

## Creating automated fallout records

To enable creation of automated fallout records, you configure an order fulfillment workflow in the Workflow Studio.

-   To do so, use the **Create fallout** action when defining processing scenarios and conditions.
-   You can define workflows for the parent records that the order tasks originate from. Generally, order tasks originate from the customer or service orders and order line items.

To learn more, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

You might encounter the following scenarios when you are attempting to fulfill customer and service orders.

Scenarios of fallout failures with downstream systems

This fallout scenario could be a situation where failures are expected to be temporary and resolved over time. Ideally, order processing should not be affected, and work should resume after the network and system resources come back online. A typical scenario is as follows:

-   The order task sends a request to an external or provisioning system.
-   The response from the external system comes back as `Timeout` or `Unable to reach`.

You can requeue the task to be sent to the downstream system for processing, up to a pre-defined number of times. If the error persists after the predefined number of times, you should change the status of the order task to Failed, and then create an incident. You can define a workflow that automatically creates a fallout record whenever you send or retrieve order data to or from an external system that is not available.

Scenarios that involve data problems

If data problems originate with an order that you captured from an external order system, you should revise the order there. You then submit the revised order to the Order Management for Telecommunications, Media, and Technology application. If data problems originate with the tasks that are executed earlier in the process, you can do the following actions:

-   Create an exception from the order task.
-   Enable the revision of the existing order.
-   Create an order task.

Inventory availability issues

You can define a workflow that automatically creates fallout records whenever inventory availability issues prevent the fulfillment of order line items.

External system issues

Even when the right data structure is submitted in an external system, errors can happen due to the business logic that is implemented in the external system.

**Parent Topic:**[Managing order fallout](fallout-management-overview.md)

## Create a manual fallout record

Create a fallout record manually for an order task that has a condition or issue that prevents it from being completed.

### Before you begin

Role required: sn\_fallout\_mgmt.fallout\_manager

### About this task

You can create manual records as needed basis so that you can raise awareness of an issue or condition that is preventing order fulfillment. By creating a record manually, you can also assign it to a person for resolution.

### Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  From the Configurable Workspace Lists icon \(![Lists icon](../image/Lists.png), click **Customer Orders**

    1.  Click **Customer Orders** or **Service Orders**.
    2.  Click **All** for all customer orders, or click **Open** for open, unfulfilled customer orders only.
3.  Select and open an existing customer or service order.

4.  To view the line item details, click **Order Line Items \(n\)** where \(n\) represents the number of the total number of line items for the order.

5.  In the Order Line Items form, select the order line item that you want to review.

6.  Click **Order Tasks \(n\)** where \(n\) is the number of order tasks that are associated with the selected order line item.

7.  In the Order Tasks form, select the order tasks that you want to review.

8.  When you finish updating the order task, or encounter issues preventing its closure, click the options icon \(![Options icon](../image/more-options.png)\) next to the **Save** button and then click **Create Fallout**\).

9.  On the form, fill in the fields.

    For information about field descriptions, see the Create Fallout form fields section in Field descriptions for Fallout Management.

10. Click **Save**.


### Result

When you create a manual fallout record, or an automated one is generated, the following occurs in the related order task:

-   Its **State** field changes to On Hold, with a comment on which logged-in user caused it to change.
-   In the Activity section, a work order note indicates that the order task state has changed from its former state, usually In Progress, to On Hold. A work order note with the message `A fallout record FOnnnn has been created` also appears.

**Related topics**  


[Fallout Management data model](order-mgt-fallout-management.md)

[order-mgt-roles]

[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

[Flows](https://www.servicenow.com/docs/access?context=flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

[Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

