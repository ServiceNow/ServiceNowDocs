---
title: Limit access to product model data on the Customer Service Portal
description: Use a system property to limit customer access to data in the Product Models table.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer and Consumer Service Portals, Set up self-service, Configure, Customer Service Management]
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

The Model Categories table \(cmdb\_model\_category\) does not have a **Customer Visible** field. Access to model categories data is restricted by using the **Customer Visible** field on the Product Model table. Only the categories for the products which are visible in the Product Model table will be visible in the Model Categories table.

For upgrades from Jakarta to madrid, the **Customer Visible** field is added to each record in the Product Models table and set to false.

To limit access:

1.  Set the **csm\_cmdb\_model.customer\_visible\_flag** system property to true.
2.  Customize the Product Models table \(cmdb\_model\) and add the **Customer Visible** column.
3.  Set the value of the **Customer Visible** field to true for the product models that should be visible to external customers.

External users can see these product using these product models if the products are linked to the customer account.

