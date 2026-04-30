---
title: Integration with Industry products
description: Provides an integration between the Industry products and Field Service Management application.
locale: en-US
release: xanadu
product: Field Service Integrations
classification: field-service-integrations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating Field Service Management with other applications, Configuring Field Service Management, Field Service Management]
---

# Integration with Industry products

Provides an integration between the Industry products and Field Service Management application.

Customers and consumers can view case-related work orders from all Industry products portals and application interfaces. Users can view account and contact information on work orders and work order tasks in the Field Service Management application.

When a user creates a work order from a customer service case, initiated from industry products, the forms include case-related information like the account and contact.

When a customer or consumer views a case from any of the Industry products, they can view the details of work orders and tasks related to the case.

## Industry products

The following ServiceNow® Industry Products extend the value of supporting data models, frameworks, and capabilities required to integrate with work orders in Field Service Management.

-   Financial Services Operations. For more information, see [Financial Services Operations integration with Field Service Management](https://www.servicenow.com/docs/access?context=integration-with-fsm&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US).
-   -   Technology Provider Service Management. For more information, see [Technology Provider Service Management integration with Field Service Management](https://www.servicenow.com/docs/access?context=technology-provider-service-mgt-overview&version=xanadu&pubname=xanadu-technology&ft:locale=en-US).

## Product use rights included with Industry products

If you have purchased a subscription for the Customer Service Management application and have the customer service agent \[sn\_customerservice\_agent\] or customer service agent manager \[sn\_customerservice\_manager\] role, you can create and view all work orders and appointments related to your case. If you’re an external user with the snc\_external role, you can create and view all work orders and appointments related to your account or a related account.

## Access to Field Service Management plugin

Industry products gain access to field service work orders and tasks using Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\). This plugin requires:

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

**Parent Topic:**[Integrating Field Service Management with other applications](integrate-fsm-other-applications.md)

