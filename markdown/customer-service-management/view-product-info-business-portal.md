---
title: View product information from Business Portal
description: View a list of products to track the products or services sold to your account and manage your services using service catalogs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/view-product-info-business-portal.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Use Business Portal, Customer communication, Use, Customer Service Management]
---

# View product information from Business Portal

View a list of products to track the products or services sold to your account and manage your services using service catalogs.

## Before you begin

Role required: sn\_customerservice.customer, sn\_customerservice.customer\_admin, sn\_customerservice.partner, or sn\_customerservice.partner\_admin

## About this task

You can view a list of products or services that have been sold to your account. You can also view any cases created on the product and all active contracts and entitlements for the product.

An entitlement is active if:

-   Its end date isn’t in the past or it has no end date.
-   The contract it’s linked to is also active.

A contract is active if:

-   Its state is set to active
-   It’s linked to a product with an active entitlement.

You can modify the **Active Entitlements** widget to define your own filters for active entitlements.

If product catalog items have been set up in your instance, you can use the **Service Catalogs** widget to view context-sensitive service catalogs based on the services you’re subscribed to. Extend your services using service catalogs and request additional items on the services that you have subscribed to.

## Procedure

1.  Navigate to the business portal.

2.  Select **My hub** &gt; **Manage sold products** in the header menu.

    The system displays a list of products or services sold to your account.

    You can only view sold products and all extensions of sold products that are not product inventories.

3.  Select a sold product to view the details associated to it.

    |Field|Description|
    |-----|-----------|
    |Number|Unique number of the sold product.|
    |Product|Reference to the product model from the CMDB table.|
    |Name|Name of the sold product.|
    |Account|Account associated with the sold product.|
    |Contact|Contact associated with the sold product.|
    |Product offering|Product offering that is associated to the sold product.|
    |Product specification|Product specification associated to the sold product.|
    |Product location|Location associated to the sold product.|
    |State|State of the sold product.|
    |Unit Net Price|Net price of a single unit of sold product.|
    |Quantity|Quantity of a product or service sold to a customer.|
    |Model categories|Reference to the model category table.|
    |Product model's short description|Brief description of the product model.|
    |Product model's description|Detailed description of the product model.|

4.  View the cases and characteristics associated to the sold product in the related list.

    |Related list|Description|
    |------------|-----------|
    |Cases|View all cases associated to the sold product.|
    |Characteristics|View the characteristics associated to a particular sold product like the characteristic value and the option.|
    |Child sold products|View the child sold products associated to the sold product.|
    |Product information|View the pricing related information of the sold product.|

5.  Perform one of the desired actions on the sold product.

    Install the Customer Life Cycle Management Self service plugin \(sn\_clm\_selfservice\) to perform the **Modify**, **Suspend**, **Resume**, and **Disconnect** actions. The flows can be performed only by the customer personas and only on the sold products where the **Contact** field is the same as the logged in user.

    -   Modify a sold product. To learn how to modify a sold product, see [Modify a sold product and hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/modify-a-sold-product.md)
    -   Suspend a sold product. To learn how to suspend a sold product, see [Supending sold products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/supending_sold_products.md).
    -   Resume a sold product. To learn how to resume a sold product, see [Resuming sold products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/resuming_sold_products.md).
    -   Disconnect a sold product. To learn how to disconnect a sold product, see [Disconnecting sold products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/disconnecting_sold_products.md)

**Related topics**  


[Activate Customer Life Cycle Management Self-Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/activate-customer-life-cycle-management-self-service.md)

[View Product Inventory information on Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/view-product-inventory-information-on-business-portal.md)

