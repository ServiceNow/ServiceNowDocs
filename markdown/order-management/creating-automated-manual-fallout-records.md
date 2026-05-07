---
title: Creating automated fallout records
description: With Fallout Management, a provider can create automated fallout records for specific order tasks so that your orders can continue processing through to completion.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing order fallout, Order Management, Use, Sales Customer Relationship Management]
---

# Creating automated fallout records

With Fallout Management, a provider can create automated fallout records for specific order tasks so that your orders can continue processing through to completion.

To enable creation of automated fallout records, you configure an order fulfillment workflow in the Workflow Studio.

-   To do so, use the **Create fallout** action when defining processing scenarios and conditions.
-   You can define workflows for the parent records that the order tasks originate from. Generally, order tasks originate from the customer or service orders and order line items.

To learn more, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US).

You might encounter the following scenarios when you are attempting to fulfill customer and service orders.

## Scenarios of fallout failures with downstream systems

This fallout scenario could be a situation where failures are expected to be temporary and resolved over time. Ideally, order processing should not be affected, and work should resume after the network and system resources come back online. A typical scenario is as follows:

-   The order task sends a request to an external or provisioning system.
-   The response from the external system comes back as `Timeout` or `Unable to reach`.

You can requeue the task to be sent to the downstream system for processing, up to a predefined number of times. If the error persists after the predefined number of times, you should change the status of the order task to Failed, and then create an incident. You can define a workflow that automatically creates a fallout record whenever you send or retrieve order data to or from an external system that is not available.

## Scenarios that involve data problems

If data problems originate with an order that you captured from an external order system, you should revise the order there. You then submit the revised order to the Order Management for Telecommunications, Media, and Technology application. If data problems originate with the tasks that are executed earlier in the process, you can do the following actions:

-   Create an exception from the order task.
-   Enable the revision of the existing order.
-   Create an order task.

## Inventory availability issues

You can define a workflow that automatically creates fallout records whenever inventory availability issues prevent the fulfillment of order line items.

## External system issues

Even when the right data structure is submitted in an external system, errors can happen due to the business logic that is implemented in the external system.

**Parent Topic:**[Managing order fallout](fallout-management-overview.md)

