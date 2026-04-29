---
title: Integrating with Field Service Management
description: The Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\) provides an integration between the Customer Service Management and Field Service Management applications.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate with FSM, Configure order fulfillment, Order management, Configure, Sales and Order Management]
---

# Integrating with Field Service Management

The Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\) provides an integration between the Customer Service Management and Field Service Management applications.

Users can view account and contact information on work orders and work order tasks in the Field Service Management application. Customers and consumers can view case-related work orders from the Customer Service and Consumer Service Portals.

When an agent creates a work order from a customer service case, the work order and task forms include case-related information. This information includes the account and contact details.

When a user views a case from either the Customer or Consumer Service Portals, they can view the details of any work orders and tasks related to the case.

## Product use rights included with this application

If you have purchased a subscription for the Field Service Management \(FSM\) application, Customer Service Management you can create and view all FSM work orders and appointments. External CSM users can create and view FSM work orders and appointments of their own or related accounts.

## Changes to the Field Service Management application

In the Field Service Management application, this integration adds the following fields to the Work Order form. These fields are visible in the Case view. To display these fields, right-click the Work Order form header and select **View** &gt; **Case**.

-   Account
-   Consumer
-   Contact
-   Asset
-   Partner
-   Partner Contact

Updating the **Account** field on the Work order form also updates the **Company** field. Updating the **Contact** field on the Work Order form updates the **Caller** field.

## Changes to the Customer Service Management application

In the Customer Service Management application, this integration adds the **Work Orders** link to the Customer Service Portal and Consumer Service Portal headers. Select this link to view a list of work orders, including the work order number, priority, state, and short description. The work orders displayed in this list on the Customer Service Portal depend on the customer role: customer, customer admin, partner, or partner admin.

Select a work order in this list to display the work order details.

## Known Limitations

There is no synchronization between the Work Order form and the associated Case form. If information changes on the Case form, it does not get updated on the Work Order form.

**Parent Topic:**[Integrate with Field Service Management](../task/activate-fsm-csm-integration.md)

