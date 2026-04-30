---
title: Creating or editing catalog item template
description: Pre-specify values or provide restrictions for attributes such as catalogs, categories, variable types, and portal settings, which are applicable during the catalog item creation or editing process. You can create a template for a catalog item or record producer.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Creating or editing catalog item template

Pre-specify values or provide restrictions for attributes such as catalogs, categories, variable types, and portal settings, which are applicable during the catalog item creation or editing process. You can create a template for a catalog item or record producer.

## Before you begin

Role required: admin or catalog\_admin

Create a catalog item template in catalog builder

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  Select the **Dashboard** tab and select **Create a catalog item template**.

3.  Select any of the following options.

    -   **Standard** for a catalog item.
    -   **Record Producer** for a record producer
4.  In the wizard, specify the information for each step.

<table id="table_l45_cs2_g4b"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template Details

</td><td>

-   Basic info: Contains the template name, short description, and an option to use the template scope for creating records. If you select the **Use template scope for creating records** check box, the record producers or catalog items created using this template would be created in the scope of the template.
-   Template Available for: Specifies the user criteria for users who can use the template. Users matching the criteria must have the catalog\_builder\_editor role.

**Note:** You can add up to a maximum of 50 user criteria.

</td></tr><tr><td>

Details

</td><td>

-   Basic info: Suggestions for the item name and short description.
-   Item details: Suggestions for the description of the item.


</td></tr><tr><td>

Destination

</td><td>

Destination table in which a record producer creates records.

 **Note:** This step is available for a record producer template.

</td></tr><tr><td>

Location

</td><td>

Catalogs, categories, and topics that the item can be associated with.

 Configure catalogs and categories to make the catalog item discoverable on the Service Portal. In the Topics card, select the taxonomy and its associated topics for a catalog item to make the catalog item discoverable on the Employee Center.

 **Note:** You can add up to a maximum of 50 catalogs or categories.

</td></tr><tr><td>

Questions

</td><td>

Question sets \(variable sets\) that should be included in the item.You can also restrict question types that can be used for items using the template by selecting the define owner permissions icon \(![define owner permissions icon](../image/define-owner-permission.png)\).

</td></tr><tr><td>

Settings

</td><td>

Settings to configure the catalog item behavior in portals, such as Employee Center and Service Portal.

 Determine whether to display the following buttons or options on the portals:

-   Add to cart
-   Save as draft
-   Quantity selector
-   Delivery time
-   Attachment
-   Make the attachment mandatory
For example, if you don't want to display the **Save as draft** button on the portal for the catalog item, select the **Hide 'Save as draft'** option.

</td></tr><tr><td>

Access

</td><td>

User criteria to specify users for whom the item is available or not available.

</td></tr><tr><td>

Fulfilment

</td><td>

Flow or workflow that you want to associate with the item using this template.

</td></tr><tr><td>

Overrides

</td><td>

Restrictions that apply while creating the catalog item. -   Can Edit: Only the attributes specified here can be edited.
-   Must specify: Editable attributes that should be answered. The following attributes must be made mandatory:
    -   Item name
    -   Record submission table
-   Restricted selections: For the attributes that enable selection of multiple values \(for example, catalogs, categories, Available For, Not Available For\), the user creating the item can only select or deselect the options from within the values specified in the template.


</td></tr><tr><td>

Review and submit

</td><td>

Review the template information and submit it.

</td></tr></tbody>
</table>    **Note:** For each step, you can review the information in the feedback panel to know more about that step.

5.  Select **Submit**.

6.  To edit the catalog item template, select the **Catalog item templates** tab, select the required template, and perform any of these actions.

    1.  To edit the item, make the necessary changes, and select **Save**.

        **Note:**

        -   The changes to the template don’t automatically apply to existing items.
        -   While editing an existing catalog item, the new values in the template aren’t automatically updated in the item but the new restrictions apply. For example, if a new category is added to the template, that category isn’t automatically added to the catalog item. However, the restrictions to the categories apply.
        -   When question sets are added to the template, they don’t have any impact on the existing catalog items using the template.
    2.  To duplicate the catalog item template, select **Duplicate**.

    **Note:** You can’t delete a catalog item template in the catalog builder, but it can be deleted in ServiceNow AI Platform. After a template is deleted, it’s disassociated from all catalog items using the template and the restrictions no longer apply to those items.


-   **[Create a catalog item using a template](create-item-cat-builder.md)**  
Make an item available in service catalog for catalog item requests.
-   **[Create a question for a catalog item in Catalog Builder](create-question-cat-builder.md)**  
Specify a question that the requester should answer before submitting the catalog item.
-   **[Edit a question in Catalog Builder](edit-question-cat-builder.md)**  
Edit an existing question if you want to improve it by adding dynamic form behavior.
-   **[Edit a catalog item in Catalog Builder](edit-cat-item-cat-builder.md)**  
Make changes to an existing catalog item if you have permissions to edit the item.
-   **[Transfer catalog items using update sets](transfer-catalog-items-using-update-sets.md)**  
Transfer catalog items published through Catalog Builder from one instance to another easily by using update sets automatically created for the catalog item. For example, you can transfer catalog items created by a business user from a non-production to production instance.
-   **[Localization Framework integration with Catalog Builder](../concept/c-CB-LF-translation.md)**  
The **Translation Status** tab in the Catalog items tab on the Catalog Builder dashboard enables you to view the translation status of catalog items, and translate catalog items on the fly using manual or machine translation methods.

**Parent Topic:**[Catalog Builder](../concept/catalog-builder.md)

