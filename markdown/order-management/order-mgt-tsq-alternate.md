---
title: Alternate proposal for service orders
description: Learn how you can provide alternate proposals if a service qualification isn't met.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service qualification requests, Managing service orders, Order Management, Use, Sales Customer Relationship Management]
---

# Alternate proposal for service orders

Learn how you can provide alternate proposals if a service qualification isn't met.

Qualification requests can be created for a service specification using information from existing inventory. If the requested service with the specified characteristics or date is not available, an alternate proposal may be provided. The alternate proposal can be similar to the requested one or may be the same service but available on a different date.

When you receive an alternate qualification request and click **Qualify Order** in the top level order line item form, the Result field is updated to **Alternate** and a list of alternate proposals are listed in the Alternate proposals related list. A single service order can have multiple alternate proposals. This list can also be manually updated by the service order agent.

**Note:** When you initiate a new qualification request is initiated and receive an alternate proposal for a service order, any existing alternate proposal entries will be deleted before new entries are created.

Navigate to the **CSM/FSM Configurable Workspace**, click a service order with Fulfilment type as **Qualify** and select the **Alternate proposal\(s\)** tab.

![Infographic displaying the Alternate proposals tab view with its list and details. For the text description, refer to the steps that follow.](../image/order-mgt-tsq-process-alternate.png)

Select the Number link to view the alternate proposal. It contains the following information:

|Field name|Description|
|----------|-----------|
|Number|Number of the alternate proposal.|
|Domain order|The domain order for which the alternate proposal is created.|
|Specification|The alternate service specification that has been proposed.|
|Available date|The date on which the alternate proposal will be available.|
|Order characteristics|The specification characteristics \(in JSON format\) provided as part of the alternate proposal in the response from the inventory system.|

**Parent Topic:**[Service qualification requests](order-mgt-tsq-about.md)

