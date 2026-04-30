---
title: Integration with Customer Service Management
description: Provides an integration between the Customer Service Management and Field Service Management applications.
locale: en-US
release: yokohama
product: Field Service Integrations
classification: field-service-integrations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating Field Service Management with other applications, Configuring Field Service Management, Field Service Management]
---

# Integration with Customer Service Management

Provides an integration between the Customer Service Management and Field Service Management applications.

Users can view account and contact information on work orders and work order tasks in the Field Service Management application. Customers and consumers can view case-related work orders from the Customer Service and Consumer Service Portals.

When an agent creates a work order from a customer service case, the work order and task forms include case-related information such as the account and contact.

When a customer or a consumer views a case from either the Customer or Consumer Service Portals, they can view the details of any work orders and tasks related to the case.

## Product use rights included with this application

If you have purchased a subscription for the Customer Service Management application and have the customer service agent \[sn\_customerservice\_agent\] or the customer service agent manager \[sn\_customerservice\_manager\] role, you can create and view all work orders and appointments related to your case. If you are an external user with the snc\_external role, you can create and view all case-related work orders and appointments related either to your account or a related account.

## Customer Service with Field Service Management plugin

The Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\) integrates the Field Service Management and Customer Service Management applications. This plugin requires:

-   Field Service Management
-   Customer Service Management
-   Customer Service Portal

## Changes to the Field Service Management application

In the Field Service Management application, this integration adds the following fields to the Work Order form. These fields are visible in the Case view. To display these fields, right-click the Work Order form header and select **View** &gt; **Case**.

-   Account
-   Consumer
-   Contact
-   Asset
-   Partner
-   Partner Contact

Updating the **Account** field on the Work Order form also updates the **Company** field.

Updating the **Contact** field on the Work Order form updates the **Caller** field.

## Changes to the Customer Service Management application

In the Customer Service Management application, this integration adds the **Work Orders** link to the Customer Service Portal and Consumer Service Portal headers. Click this link to view a list of work orders, including the work order number, priority, state, and short description. The work orders displayed in this list on the Customer Service Portal depend on the customer role: customer, customer admin, partner, or partner admin.

Click a work order in this list to display the work order details.

## Known limitations

There is no synchronization between the Work Order form and the associated Case form. If information changes on the Case form, it does not get updated on the Work Order form.

-   **[Map case fields with work order table](../task/map-case-fields-to-work-order-table.md)**  
Define the fields you want to map between the case and the target work order table fields that you have already configured. This configuration automatically copies the values of mapped fields from the case to the work order when creating a work order from the case.

**Parent Topic:**[Integrating Field Service Management with other applications](integrate-fsm-other-applications.md)

