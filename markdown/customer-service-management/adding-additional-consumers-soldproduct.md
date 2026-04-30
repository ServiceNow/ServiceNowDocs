---
title: Add additional consumers for the sold product
description: Add additional consumers for your business-to-consumer \(B2C\) or business-to-business-to-consumer \(B2B2C\) sold products by defining the type and responsibility of additional consumers. After you add this information, additional consumers can have the same access to the consumer associated with the sold product and the related entities.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Adding related parties to a sold product, Using customer access management, Customer management, Use, Customer Service Management]
---

# Add additional consumers for the sold product

Add additional consumers for your business-to-consumer \(B2C\) or business-to-business-to-consumer \(B2B2C\) sold products by defining the type and responsibility of additional consumers. After you add this information, additional consumers can have the same access to the consumer associated with the sold product and the related entities.

## Before you begin

Role required: admin and sn\_customerservice\_manager

## About this task

The responsibility assigned to the additional consumer that is associated with a sold product gets access to the sold product and the related entities, which include installed products, install base items, and cases associated with sold products.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Sold Products**.

2.  Select the desired record where you want to add additional consumers.

3.  From the Additional Consumers related list, select **New**.

    Starting with the Utah release, the Additional Consumers related list has been deprecated for new customers. For upgrade customers, the Additional Consumers related list continue to be supported along with the Sold Product Related Parties related list.

4.  On the form, fill in the fields.

<table id="table_esz_qdw_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sold Product

</td><td>

Products and components sold to a consumer.

</td></tr><tr><td>

Type

</td><td>

Related party type.**Note:** By selecting the related party type, the default responsibility mentioned in the type is added in the related party responsibility.

</td></tr><tr><td>

Consumer

</td><td>

Contact responsible for the sold product.

</td></tr><tr><td>

Responsibility

</td><td>

Access level to sold product and related information.Additional consumer with Authorized Representative responsibility requires the sn\_install\_base.sold\_product\_authorized\_consumer role to get access to associated sold product and related entities. For details, see [Roles installed with customer access management](../reference/r_rolesinstalledwithcustaccessmgmt.md).

 **Note:** If the **Responsibility** field is empty, consumers can’t access the sold product and associated case.

</td></tr><tr><td>

Order

</td><td>

Specifies the sequence in which records are displayed, organized according to business preferences.

</td></tr></tbody>
</table>5.  Select **Submit**.

    Additional consumers are added to the consumer sold product.


## Result

Once additional consumers are added to the sold product with a proper functional role having Authorized Representative responsibility, they can perform the following actions.

-   View the list of sold products and associated install base items.
-   Create cases by selecting sold products or install bases.
-   View the list of cases related to the sold products or affected install bases.
-   View the list of installed products.
-   Access cases associated with the sold product.
-   Manage service catalog requests from the sold product.

**Note:**

-   While creating a case for a sold product, you can only see authorized consumers on the consumer sold product.
-   If you choose someone as a consumer, you can only associate the sold products they have full access to on the case.

