---
title: Integration with Industry products
description: Provides an integration between the Industry products and Field Service Management application. This integration allows customers and consumers to manage case-related work orders and tasks across Industry Products portals and application interfaces, enhancing visibility and operational efficiency.
locale: en-US
release: australia
product: Field Service Integrations
classification: field-service-integrations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating Field Service Management with other applications, Configure, Field Service Management]
---

# Integration with Industry products

Provides an integration between the Industry products and Field Service Management application. This integration allows customers and consumers to manage case-related work orders and tasks across Industry Products portals and application interfaces, enhancing visibility and operational efficiency.

Key Features of the Integration

1.  Unified case and work order view:
    -   Customers and consumers can view case-related work orders and tasks directly from all Industry Products portals and application interfaces.
    -   Work orders and tasks include account and contact information, providing comprehensive details related to customer service cases.
2.  Case-initiated work orders:
    -   When a work order is created from a customer service case initiated through Industry Products, the work order and task forms include case-related details, such as account and contact information.
    -   Customers can view related work orders and tasks from within their Industry Product portals.

## Supported Industry Products

This integration supports all Industry Products, each extending the value of data models, frameworks, and capabilities required for work order management in Field Service Management. For more information, see [Industry Products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industry-products/industry-products-landing.md).

## Access to work orders and work order tasks

Access to FSM work orders and tasks through Industry Products requires the Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\). For more information, see [Integration with Customer Service Management](customer-service-integration.md). This plugin requires:

-   Field Service Management
-   Customer Service Management
-   Customer Service Portal

## Enhanced security with roles

To ensure data security and control, the following roles can be used to manage access to work orders and tasks:

-   `wm_location_agent`: Restricts agents to viewing work orders and work order tasks relevant to their provider service organization.
-   `wm_location_assignment.manager`: Allows managers to oversee work orders and work order tasks within their specific provider service organization.

These roles are available when the Work Management and Service Organization plugins are installed. They help:

-   Restrict access to relevant work orders and tasks.
-   Secure data within the context of the provider service organization.

## Product use rights included with Industry products

-   If you have a subscription to the FSM application and the Customer Service Agent \(`sn_customerservice_agent`\) or Customer Service Agent Manager \(`sn_customerservice_manager`\) roles, you can create and view all work orders and appointments related to your cases.
-   External users with the `snc_external` role can create and view case-related work orders and appointments associated with their account or related accounts.

**Parent Topic:**[Integrating Field Service Management with other applications](integrate-fsm-other-applications.md)

