---
title: Ordering a service
description: As a provider, use Order Capture to create a service order in the ServiceNow AI Platform for your consumers or internal personnel.OM revamp project - This topic is redundant and obsolete and has been removed from the SOM bundle on Oct 6, 2025.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/order-capture-create-service-order.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Services, service changes, or disconnects, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Ordering a service

As a provider, use Order Capture to create a service order in the ServiceNow AI Platform for your consumers or internal personnel.

## Before you begin

Complete the following configuration tasks before you use Order Capture:

1.  Assign the order fulfillment and provider roles to your users.
2.  Define and publish your customer-facing service specifications.
3.  Configure order fulfillment.

Role required: sn\_ind\_tmt\_orm.service\_order\_agent, sn\_ind\_tmt\_orm.service\_order\_manager

## About this task

Here's how a service order is created:

1.  In the Create Order form, you select the **Service** order type, and then select a customer account and contact.
2.  In the Select Service form, you select one or more service specifications and destination locations for the service order.
3.  In the Configure Service form, you configure each service order line item, apply those service configurations to one or more locations, and then configure the ordered service configurations by location.
4.  In the Review Order form, you review and submit the service order.
5.  A service manager can now review and approve it for fulfillment. To learn more, see [Creating, reviewing, approving, and fulfilling service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-fulfilling-service-orders.md).

When you directly enter a service order, it creates a service order record in the ServiceNow AI Platform to manage the service order fulfillment. A service order has one or more associated order line items, which describe the services being performed.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Access Order Capture from the **Configurable Workspace Lists** tab.

3.  Depending on whether you're creating an order for an existing customer account, or first creating a customer account before you create the order, you can select one of the following actions.

<table id="choicetable_hfw_sqp_wrb"><thead><tr><th align="left" id="d31365e147">

 

</th><th align="left" id="d31365e149">

Description

</th></tr></thead><tbody><tr><td id="d31365e155">

**Create an order for an existing customer account**

</td><td>

1.  From the **Configurable Workspace Lists** tab \[Omitted image "list-outline-24.svg"\] Alt text:, select **Customer Orders** or **Service Orders**.
2.  Select **All** or select **Open**.
3.  To create order, select **New**.


</td></tr><tr><td id="d31365e199">

**Create a customer account before creating the order**

</td><td>

**Note:** Most of the customer accounts in Order Management for Telecommunications, Media, and Technology are existing accounts that have been imported into the ServiceNow AI Platform from external order management systems via APIs. To learn how to create new customer accounts, see [Configure accounts and contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-csm-accounts-contacts.md) in Customer Service Management \(CSM\).

</td></tr></tbody>
</table>4.  When the Choose an order type dialog appears, select **Order a new service** and select **Create**.


