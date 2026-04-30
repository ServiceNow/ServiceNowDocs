---
title: Minor changes to published product offerings and specifications
description: As a product catalog admin, you can make minor changes to certain fields in published versions of a product offering or specification, without creating another version. Minor changes include updates such as modifying the product offering display name, description, or product image.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-16"
reading_time_minutes: 2
breadcrumb: [Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Minor changes to published product offerings and specifications

As a product catalog admin, you can make minor changes to certain fields in published versions of a product offering or specification, without creating another version. Minor changes include updates such as modifying the product offering display name, description, or product image.

**Note:** If you want to change fields other than the fields listed in the following sections, those changes are considered major updates. You must generate a new version of the product offering or specification.

## How minor  changes are processed 

The following sections describe the minor changes that  you can  make to published versions of product offerings  and specifications.  When you save your changes, the entities  are  immediately  updated.

If  you’re  using the  CPQ Configurator, minor changes are handled  as  follows: 

-   Minor changes to simple products are synchronized automatically.
-   Minor  changes  to  configurable products  require synchronization.  In the  CSM Configurable Workspace, the  **Save**  and  **Update Configuration ** buttons  are displayed  when you make  minor  changes to  a  product offering.  Selecting   **Update  Configuration ** synchronizes  the configurable  product  offering  with  its  corresponding blueprint.
-   If any blueprints  have a  reference  to a  simple or configurable product  with  minor  changes, you must  synchronize  those blueprints. 

## Make minor updates to published product offerings

Make minor changes to certain  fields  in  a published product offering  and  its  related  entities.

1.  In the CSM Configurable Workspace, select the List view. 
2.  Navigate to  **Offerings** &gt; **Product Offerings**. 
3.  Select the product offering to be  changed  and choose the  appropriate tab  \(related list\).

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
</table>4.  Repeat step 3 for each product offering entity that has minor changes. 
5.  When you finish the changes, select  **Save**.

    The changes to the published offering are updated immediately.


## Make minor changes to published specifications

Make minor changes to certain fields in a published specification and its related entities.

1.  In the CSM Configurable Workspace, select the List view. 
2.  Navigate to  **Specifications**. 
3.  Select the specification to be changed \(Product, Service, or Resource\) and choose the appropriate tab \(related list\) for the entity to be changed.

    You can change any of the minor fields listed in the following table.

<table id="table_zfd_dt4_4hc"><thead><tr><th>

Entity

</th><th>

Fields that can be updated

</th></tr></thead><tbody><tr><td>

-   Product Specification
-   Service Specification
-   Resource Specification


</td><td>

-   Name
-   Display name
-   Description
-   Line
-   External code


</td></tr><tr><td>

Specification Characteristics

</td><td>

Order

</td></tr><tr><td>

New Specification Characteristic

</td><td>

Add characteristic options

</td></tr><tr><td>

Specification Relationships

</td><td>

Order

</td></tr></tbody>
</table>4.  Repeat step 3 for each specification entity that has minor changes. 
5.  When you finish the changes, select **Save**.

    The changes to the published specification are updated immediately.


