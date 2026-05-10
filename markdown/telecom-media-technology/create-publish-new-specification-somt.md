---
title: Create and publish a specification version
description: Create and publish a version of an existing specification in a Published state so that you can offer an improved version of it to your customers in your product catalog.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-15"
reading_time_minutes: 4
breadcrumb: [Creating and publishing specification versions, Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Create and publish a specification version

Create and publish a version of an existing specification in a Published state so that you can offer an improved version of it to your customers in your product catalog.

## Before you begin

Before you can create a version of a specification, an initial base version of the specification must exist and already be published. The information that you supply for a new version is the same as what you entered for an initial base version, but with some important differences. To learn more, see [Create and publish product specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-create-product-specification.md).

Role required: sn\_prd\_pm.product-catalog\_manager

## About this task

You create versions of service and resource specifications in the same manner as you do a resource specification.

## Procedure

1.  Navigate to **All** &gt; **Product Catalog Management** &gt; **Product Specifications**.

2.  In the Product Specifications list, select the product specification that you want to create a version for.

3.  On the form, select **Create New Version** and then fill in the fields.

    The manner in which you create a version of a specification is similar to how you created its initial version, with the differences that are explained in the following table.

<table id="table_pyl_fvq_4nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new product specification. If the name of the item for the new version differs from the previous version, you can enter a new name.

</td></tr><tr><td>

Version

</td><td>

Version number that is assigned to a specification:

-   When you create the initial version, 1 appears in this field, and can't be changed.
-   When you create subsequent versions of the specification, the next incremental number appears in this field after you select **Create New Version**. For example, 4 appears in this field if 3 was the previous version number.


</td></tr><tr><td>

Display Name

</td><td>

Displayed name that appears for the specification in the ServiceNow AI Platform when this version of the specification is in effect.

-   When you create the initial, or base version of the specification \(for example, version 1\), you must enter free-form text, which is usually the name of the specification, into the field.
-   When you create versions of the specification, a system-assigned concatenation of the specification name and its current version number appears, but can be overwritten.


</td></tr><tr><td>

Initial Version

</td><td>

Name of the base version of the specification that appears but can't be changed.

</td></tr><tr><td>

Previous Version

</td><td>

Name of the previous version of the specification. For example:

-   When you create the initial version of the specification \(for example, version 1\), this field is empty.
-   When you create a version \(version 2\) with a slightly different name, the name of the specification at its initial creation appears here.
-   When you create a subsequent version \(version 3\), the name of the specification as it was at version 2 appears here.
You can't change this field.

</td></tr></tbody>
</table>    **Note:** For information about the remaining field descriptions, see [Field descriptions for product catalog forms in Order Management for Telecommunications, Media, and Technology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/field-descriptions-for-product-catalog-fields.md).

4.  To reflect the engineering changes that were made to the physical product, update the specification relationships, decomposition rules, quantity mappings, and attribute propagation rules as follows:

    1.  To update the characteristics and characteristic options that are associated with your specification, use the Specification Characteristics related list. To learn more, see [Create specification relationships, quantity mapping, and decomposition rules for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-specification-rels.md).
    2.  To update the specification relationships and accompanying decomposition rules, use the Specification Relationships related list. To learn more, see [Create specification relationships, quantity mapping, and decomposition rules for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-specification-rels.md).
    3.  To update attribute mappings, use the Attribute Mappings related list. To learn more, see [Defining mappings for attribute value propagation to domain orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-define-propagate-domain-order-attributes.md).
    4.  To create a product offering from the specification, navigate to the Product Offerings related
5.  When you finish creating the specification version, do one of the following actions.

<table id="choicetable_product_offering"><thead><tr><th align="left" id="d38375e267">

Action

</th><th align="left" id="d38375e270">

Description

</th></tr></thead><tbody><tr><td id="d38375e276">

**Publish**

</td><td>

Publish the draft specification so that you can use it in a product catalog as follows: -   When you publish it, its state changes from Draft to Published.
-   After you publish a specification, you can't change or delete it, unless you create a version for it.


</td></tr><tr><td id="d38375e294">

**Update**

</td><td>

Update the specification with the new data that you added, but do not publish it for use in a product catalog.

</td></tr><tr><td id="d38375e303">

**Copy**

</td><td>

Copy the data in this specification so that you can create a specification from it. When you use the Copy function, it creates a base version specification, and sets the values in these fields:

-   **Version**: 1 \(base version\)
-   **Initial Version**:
-   **Previous Version**: blank


</td></tr></tbody>
</table>    **Note:** To learn more about the validations that are performed when you publish a new specification version, and how to resolve any reported errors, see the section about validations in [Create and publish a specification version](create-publish-new-specification-somt.md).


**Related topics**  


[Technical product catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-product-data-model.md)

[Create and publish product specifications](create-product-specifications.md)

[Create and publish service specifications](create-service-specification.md)

