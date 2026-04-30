---
title: Limit access to product model data on the Customer Service Portal
description: Use a system property to limit customer access to data in the Product Models table.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Limit access to product model data on the Customer Service Portal

Use a system property to limit customer access to data in the Product Models table.

From the Customer Service Portal, product model data can be accessed by external users with the sn\_esm\_user role. System administrators can use the **csm\_cmdb\_model.customer\_visible\_flag** system property and the **Customer Visible** field on the Product Models table \(cmdb\_model\) and child tables to limit this access.

The **csm\_cmdb\_model.customer\_visible\_flag** system property enables the **Customer Visible** field for the tables listed below. By default, this property is set to false. When set to true, the system uses the setting in the **Customer Visible** field to determine access to product model data on the Customer Service Portal.

-   Product Models table \(cmdb\_model\)
-   Software Models table \(cmdb\_software\_product\_model\)
-   Application Models table \(cmdb\_application\_product\_model\)
-   Consumable Models table \(cmdb\_consumable\_product\_model\)
-   Facility Models table \(cmdb\_facility\_product\_model\)
-   Hardware Models table \(cmdb\_hardware\_product\_model\)

The Model Categories table \(cmdb\_model\_category\) doesn't have a **Customer Visible** field. Access to model categories data is restricted by using the **Customer Visible** field on the Product Model table. Only the categories for the products which are visible in the Product Model table would be visible in the Model Categories table.

For upgrades from Jakarta to Madrid, the **Customer Visible** field is added to each record in the Product Models table and set to false.

To limit access:

1.  Set the **csm\_cmdb\_model.customer\_visible\_flag** system property to true.
2.  Customize the Product Models table \(cmdb\_model\) and add the **Customer Visible** column.
3.  Set the value of the **Customer Visible** field to true for the product models that should be visible to external customers.

If the products are linked to a customer account, the external users can see these products using the product models.

