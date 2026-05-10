---
title: Creating and publishing specification versions
description: As a product catalog manager, you can create and publish the specification versions that list the improved products and services that you can offer to your customers in a technical product catalog.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-14"
reading_time_minutes: 5
breadcrumb: [Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Creating and publishing specification versions

As a product catalog manager, you can create and publish the specification versions that list the improved products and services that you can offer to your customers in a technical product catalog.

Your product catalogs define the products, services, and resources available to your customers so they can decide what to purchase from you. Your catalog items will continue to evolve over time to accommodate the changes that are related to how your items are sold, configured, and delivered to your customers. Typically, these changes are related to engineering improvements that make the products, services, and resources more marketable and appealing to your customers. The changes usually are to the fit, form and function, characteristics, and characteristic options, and specification relationships of your catalog items. For example, a home internet product may evolve over multiple revisions to support changes that are related to pricing and increased internet speeds.

By creating new specification and product offering versions for your products, you enable your agents to work with the latest versions of your product and service offerings when they sell more expensive, complementary, upgraded, or related products to your customers.

## Creating specification versions for use in product offerings

As a product catalog manager, you do the following actions when you create a version of a specification for use in a product offering:

1.  Create and assign a version number in each of the product, service, or resource specifications or product offering records that are affected by the changes.
2.  Create the required specification relationships, decomposition rules, and attribute mappings for each specification in the new version. As a product catalog manager, you update the following information to reflect the engineering changes that were made to the associated specifications:

    -   Characteristics
    -   Characteristic options
    -   Specification relationships
    -   Decomposition rules
    -   Quantity mappings
    -   Attribute propagation rules
    **Note:** To learn more, see [Create and publish a specification version](../task/create-publish-new-specification-somt.md).

3.  Create a product offering, and then publish it when you update your product catalog. To learn more, see [Create and publish a product offering version](../task/create-publish-product-offering-version-somt.md).
4.  Retire or archive old or unused specifications, and product offerings. To learn more, see [Retiring or archiving versioned specifications and product offerings](retiring-archiving-specifications-somt.md).

## Updates and validations that are performed when you create and publish a specification version

When you create a version for a currently published specification, the system copies the following data into, or populates, the new specification record as follows:

1.  Copies the following fields with these basic specification details:
    -   **Category**
    -   **Type**
    -   **Start** and **End** date
    -   **Description**
    -   **External ID**
    -   **Product code** and **Product line**
    -   **Cost to Company**
    -   **Composite**
    -   **Installation Required**
    -   **Location-specific**
2.  Blanks out the **External Version** field.

    **Note:** The **External ID** and **External Version** fields don't appear on the specification forms by default but can be added by changing the form layouts.

3.  Populates the following fields with the detailed information that you enter for the new specification version:
    -   **Version**. The next incremental number appears.
    -   **Display Name**. The display name is the system-assigned concatenation of the specification name and its current version number. You can overwrite this field.
    -   **Initial Version**. The name of the base version of the specification appears but can't be changed.
    -   **Previous Version**. The name of the specification is as it was in the previous version.
4.  Copies the associated characteristic and characteristic options. To learn more, see [Create the characteristics and characteristic options for your product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-characteristics.md).
5.  Copies the associated specification relationships, attribute mapping, decomposition rules, and quantity mappings when you use extension point scripts. When copied, the source specifications in the associated specification relationship and decomposition rule records are automatically updated to the current versions of the source specifications.

    **Note:** To learn more about these rules, see [Create specification relationships, quantity mapping, and decomposition rules for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-specification-rels.md).

6.  Copies the associated quantity mappings and attribute propagation rules. The source specifications in the quantity mappings and attribute propagation rules are also updated to the current versions. To learn more about these rules, see [Defining mappings for attribute value propagation to domain orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-define-propagate-domain-order-attributes.md).

When you publish the updated specification version, the ServiceNow AI Platform® performs validations on your edits. These validations ensure that all rules are valid with the characteristic and characteristic options that are available for the new specification version. An error might occur if you inadvertently remove or change the characteristics or characteristic options that are referenced by the other rules that are associated with the new specification version. If an error occurs, a message similar to this example appears.

## Copied rules validation errors

You can publish a new specification version only after you resolve all errors. This table contains some possible validation errors that you may see and the actions you can take to resolve the issue.

<table id="table_snw_zpt_2tb"><thead><tr><th>

Error

</th><th>

Resolution actions

</th></tr></thead><tbody><tr><td>

Invalid specification version in the specification relationship.

</td><td>

Update the source specification version to the current version: 1.  Select **Specification Characteristics**.
2.  Update the **Source Specification** field in the Specification Relationships form.

</td></tr><tr><td>

Invalid specification versions in the decomposition rule.

</td><td>

Update the source specification version to the current version: 1.  Select **Specification Relationships**.
2.  Update the **Source Specification** field in the Specification Relationships form.

</td></tr><tr><td>

Invalid characteristic in the decomposition rule.

</td><td>

Update or remove the invalid characteristic in the Decomposition Rules form:1.  Select **Specification Characteristics**.
2.  Update or remove any invalid characteristics.

</td></tr><tr><td>

Invalid characteristic options in the decomposition rule.

</td><td>

Update or remove the invalid characteristic options in the Decomposition Rules form:1.  Select **Specification Characteristics**.
2.  Update or remove any invalid characteristic options.

</td></tr><tr><td>

Invalid characteristic options in the quantity rule.

</td><td>

Update or remove the invalid characteristic options in the Attribute Mappings form:1.  Select **Attribute Mappings**.
2.  Update or remove any invalid characteristic options.

</td></tr><tr><td>

Invalid specification version in the attribute propagation rule.

</td><td>

Update the **Source Specification** field in the Attribute Propagation form to the current version.

</td></tr><tr><td>

Invalid characteristic in the attribute mapping rule.

</td><td>

Update or remove the invalid characteristics in the Attribute Mappings form:1.  Select **Attribute Mappings**.
2.  Update or remove any invalid characteristics.

</td></tr></tbody>
</table>