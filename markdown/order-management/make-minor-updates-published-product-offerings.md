---
title: Make minor updates to published product offerings
description: Make minor changes to certain  fields  in  a published product offering  and  its  related  entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/make-minor-updates-published-product-offerings.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Minor changes to published offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Make minor updates to published product offerings

Make minor changes to certain  fields  in  a published product offering  and  its  related  entities.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to  **Offerings** &gt; **Product Offerings**. 

4.  Select the product offering to be  changed  and choose the  appropriate tab  \(related list\).

    You can change any of the product offering fields listed in the following table.

<table id="table_zdy_fsg_4hc"><thead><tr><th>

Product offering entity

</th><th>

Fields that can be updated

</th></tr></thead><tbody><tr><td>

Product offering

</td><td>

-   Name
-   Display name
-   Description
-   Sellable
-   Allow multiple configurations:  Change the setting from unselected to selected \(true\). 


</td></tr><tr><td>

Product Offering Characteristics

</td><td>

-   Customer input required
-   Order
-   Mandatory


</td></tr><tr><td>

New Characteristic Option

</td><td>

Add Characteristic option

</td></tr><tr><td>

Product Offering Relationship

</td><td>

-   Display name
-   Order


</td></tr><tr><td>

Product Offering Relationship Groups

</td><td>

-   Name
-   Description
-   Order


</td></tr><tr><td>

Product Offering Relationship Characteristics

</td><td>

Order

</td></tr><tr><td>

Relationship  Characteristic Option 

</td><td>

Add Characteristic option

</td></tr></tbody>
</table>5.  Add a child product offering.

    **Note:** If a specification is associated with more than one product offerings, then it can't be added to the product offering as a child product offering relationship. You must create a new version of the parent product offering.

    1.  Navigate to the **Product Offering Relationships** tab.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        For a description of the form fields, see [Create product offering relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-offering-relationships.md).

    4.  Select **Save**.

    The optional child offering is added without incrementing the parent product offering version. The child becomes available for eligible transactions on or after the relationship’s effective date.

6.  Add a characteristic to the product offering.

    1.  Navigate to the **Product Offering Characteristics** tab.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        For a description of the form fields, see [Add characteristic and characteristic options to a product offering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/add-characteristics-to-product-offering.md).

        The **Mandatory** option is disabled.

    4.  Select **Save**.


