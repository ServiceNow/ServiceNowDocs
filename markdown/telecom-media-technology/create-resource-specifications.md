---
title: Create and publish resource specifications
description: Create and publish a base version of a resource specification to define all the resource options for a customer-facing product that you sell and to designate how to fulfill these options.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 4
breadcrumb: [Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Create and publish resource specifications

Create and publish a base version of a resource specification to define all the resource options for a customer-facing product that you sell and to designate how to fulfill these options.

## Before you begin

Create characteristics, characteristic options, and specification categories. To learn more about characteristics, characteristic options, and specification categories, see:

-   Create product characteristics and characteristic options
-   Create and associate specification categories with model categories

Role required: sn\_prd\_pm.product\_catalog\_manager

## About this task

You create a resource specification to define the technical information for a resource, which includes the following:

-   All the specification characteristic options that are available for a resource, and how they should be fulfilled.
-   Various categories of information, such as the manufacture, model, and brand-related information about a resource, including the resource visuals and activation guides. Resource specifications are not customer-facing.
-   Its relationship to other product, service, and resource specifications. You can enable the product and service delivery by using the required resource.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Specifications** &gt; **Resource specifications**.

3.  Select **New**.

4.  On the Details tab, fill in the fields.

<table id="table_jqn_vm4_dfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated ID for the resource specification.

</td></tr><tr><td>

Name

</td><td>

Name of the resource specification.

</td></tr><tr><td>

Version

</td><td>

Version number that is assigned to a specification:-   When you create the initial version, 1 appears in this field, and can't be changed.
-   When you create subsequent versions of the specification, the next incremental number appears in this field after you select Create New Version. For example, 4 appears in this field if 3 was the previous version number.


</td></tr><tr><td>

Display name

</td><td>

Name that appears for the specification in the ServiceNow AI Platform when this version of the specification is in effect.-   When you create the initial, or base version of the specification \(for example, version 1\), you must enter free-form text, which is usually the name of the specification, into the field.
-   When you create versions of the specification, a system-assigned concatenation of the specification name and its current version number appears but can be overwritten.


</td></tr><tr><td>

Category

</td><td>

Specification category that the resource specification belongs to.

</td></tr><tr><td>

Type

</td><td>

Type of resource specification. Select a type: -   Physical:Physical item, such as a router or a handset.
-   Logical: Logical item, such as an IP address.


</td></tr><tr><td>

Start date

</td><td>

Date that the specification is valid from. You can use this field when you create a version to indicate when it takes effect. However, it is informational only and isn’t used for actual processing.

</td></tr><tr><td>

End date

</td><td>

Date through which the specification is valid. You can use this field when you create a version to indicate when it is no longer in effect. However, it is informational only and isn’t used for actual processing.

</td></tr><tr><td>

Owner

</td><td>

Name of the person who is responsible for maintaining this specification. Select the search icon to choose the person.

</td></tr><tr><td>

Description

</td><td>

Description for this resource specification.

</td></tr><tr><td>

State

</td><td>

State of the resource specification.-   Draft: Unpublished draft resource specification that is assigned when you first create the specification record.
-   Published: Published resource specification that is assigned when you formally publish it for use in a product offering.
-   Retired: Resource specification that is retired and can no longer be used to create another specification version.
-   Archived: Resource specification that is no longer used in the ordering or fulfillment process.


</td></tr><tr><td>

External code

</td><td>

Product code of the specification.

</td></tr><tr><td>

Line

</td><td>

Product line of the specification.

</td></tr><tr><td>

Cost to company

</td><td>

Cost to the company for this resource specification. This field is for profit-calculation purposes only.

</td></tr><tr><td>

Composite

</td><td>

Option indicating that the resource specification is a parent that contains multiple child specifications.

</td></tr><tr><td>

Installation required

</td><td>

Option indicating that someone must install the product on site.

</td></tr><tr><td>

Location specific

</td><td>

Option indicating that this resource specification requires the location details for fulfillment and installation.

</td></tr><tr><td>

Transient

</td><td>

Option that indicates the product for this resource specification is for one-time use.**Note:** If you select this option, the sold product or product inventory record for the transient product is set to an Inactive state when the order is completed. Move, Add, Change, Disconnect \(MACD\) actions can’t be performed on the sold product or product inventory records of a transient product.

</td></tr><tr><td>

Initial version

</td><td>

Name of the base version of the specification that appears but can't be changed.

</td></tr><tr><td>

Previous version

</td><td>

Name of the previous version of the specification. For example:-   When you create the initial version of the specification \(for example, version 1\), this field is empty.
-   When you create a version \(version 2\) with a slightly different name, the name of the specification at its initial creation appears here.
-   When you create a subsequent version \(version 3\), the name of the specification as it was at version 2 appears here
You can't change this field.

</td></tr></tbody>
</table>5.  Select **Save**.

    The resource specification is created. The following tabs open for defining and viewing related information for the specification:

<table id="table_rgl_ffp_dfc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog Hierarchy

</td><td>

View the complete hierarchy of a product offering and any associated specifications.Use the **Show specification** toggle to view the hierarchy of specifications.

</td></tr><tr><td>

Specification Characteristics

</td><td>

Associate the characteristics and characteristic options with your specification.

</td></tr><tr><td>

Specification Relationships

</td><td>

[Create specification relationships, quantity mapping, and decomposition rules for Sales CRM for Telecommunications](create-specification-relationships-somt.md)

</td></tr><tr><td>

Versions

</td><td>

Create another version of the specification

</td></tr></tbody>
</table>6.  When you are finished creating the specification version, do one of the following actions.

<table id="choicetable_zw3_3sc_dtb"><thead><tr><th align="left" id="d26173e514">

Action

</th><th align="left" id="d26173e517">

Description

</th></tr></thead><tbody><tr><td id="d26173e523">

**Publish**

</td><td>

Publish the draft specification so that you can use it in a product offering. -   When you publish it, its state changes from Draft to Published.
-   After you publish a specification, you can't change or delete it, unless you create a version for it.


</td></tr><tr><td id="d26173e541">

**Update**

</td><td>

Update the specification with the new data that you added, but do not publish it for use in a product offering.

</td></tr><tr><td id="d26173e550">

**Copy**

</td><td>

Copy the data in this specification so that you can create a specification from it.

</td></tr></tbody>
</table>
