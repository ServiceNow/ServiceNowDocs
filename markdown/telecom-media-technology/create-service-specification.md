---
title: Create and publish service specifications
description: Create and publish a base version of a service specification. A service specification defines all the service options that apply to a customer-facing product you sell, and designates how to fulfill these options.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 5
breadcrumb: [Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Create and publish service specifications

Create and publish a base version of a service specification. A service specification defines all the service options that apply to a customer-facing product you sell, and designates how to fulfill these options.

## Before you begin

-   Create the characteristics and characteristic options for your product offerings
-   [Create and associate specification categories with model categories](https://www.servicenow.com/docs/access?context=create-associate-specification-categories&version=australia&pubname=australia-order-management&ft:locale=en-US)

Role required: sn\_prd\_pm.product\_catalog\_manager

Role required: admin

## About this task

You create a service specification to define a service and the technical information for that service, which includes:

-   All the specification characteristic options that are available for a service, and how they should be fulfilled.
-   Various categories of information, including the cost, terms and conditions, and service-related materials. These resources include the service-related visuals and implementation guides. Service specifications can be customer-facing or resource-facing.
-   Its relationship to other product, service, and resource specifications.

## Procedure

1.  Navigate to **Specifications** &gt; **Service Specifications**.

2.  Select **New**.

3.  On the Details tab, fill in the fields.

<table id="table_p3t_cxq_4nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated ID for the service specification.

</td></tr><tr><td>

Name

</td><td>

Name of the service specification.

</td></tr><tr><td>

Version

</td><td>

Version number that is assigned to a specification: -   When you create the initial version, 1 appears in this field, and can't be changed.
-   When you create subsequent versions of the specification, the next incremental number appears in this field after you select **Create New Version**. For example, 4 appears in this field if 3 was the previous version number.


</td></tr><tr><td>

Display name

</td><td>

Display name that appears for the specification when this version of the specification is in effect. -   When you create the initial, or base version of the specification \(for example, version 1\), you must enter free-form text, which is usually the name of the specification, into the field.
-   When you create versions of the specification, a system-assigned concatenation of the specification name and its current version number appears, but can be overwritten.


</td></tr><tr><td>

Category

</td><td>

Specification category that the service specification belongs to.-   If the selected category that belongs to 5G services doesn't have any matching slice templates, the system checks for existing templates.
-   If the selected category has multiple templates mapped to it, the systems chooses the latest published template to the specification.


</td></tr><tr><td>

Type

</td><td>

Type of service specification: -   **Customer Facing**

Customers can create a ticket or a case for the service. When you select this type, the **Distribution channel** field is displayed to specify how the service is provided, for example web.

-   **Resource Facing**

Services are required for a resource to function properly.

-   **Not Applicable**

Service specification is not customer facing or resource facing.

</td></tr><tr><td>

Sub type

</td><td>

Sub-type of the specification. Choose **Slice** to define 5G network service specifications.**Note:**

-   When you select Slice as the sub type, the templates are automatically selected based on the mapping of templates with the specification categories of service specifications in the decision table.
-   If you select None as the sub type, you can manually specify a template.


</td></tr><tr><td>

Start date

</td><td>

Date that the specification is valid from. Use this field when you create a version to indicate when it takes effect. It’s informational only and isn't used for actual processing.

</td></tr><tr><td>

End date

</td><td>

Date up until which the specification is valid. Use this field when you create a version to indicate when it’s no longer in effect. It is informational only and isn't used for actual processing.

</td></tr><tr><td>

Template

</td><td>

Templates that you have defined if you're using 5G services.**Note:** When you change a template, it deletes all the specification characteristics that are marked as true and are associated with the old template and re-associates the specification characteristics according to the new template that you have selected.

</td></tr><tr><td>

Description

</td><td>

Description for the service specification.

</td></tr><tr><td>

State

</td><td>

State of the service specification. -   **Draft**

Unpublished draft service specification that is assigned when you first create the specification record.

-   **Published**

Published service specification that is assigned when you formally publish it for use in a product offering.

-   **Retired**

Service specification that is retired and can no longer be used to create another specification version.

-   **Archived**

Service specification is no longer used in the ordering or fulfillment process.

</td></tr><tr><td>

Distribution channel

</td><td>

Option to set and lock in a distribution channel. For example, you can specify web as a channel. You can specify multiple channels. **Note:** If you're using the Service Exchange Order Management for Providers application, enter Service Exchange as distribution channel.

</td></tr><tr><td>

External code

</td><td>

Service code of the specification.

</td></tr><tr><td>

Line

</td><td>

Service line of the specification.

</td></tr><tr><td>

Cost to company

</td><td>

Cost to the company for this service specification. This field is for profit-calculation purposes only.

</td></tr><tr><td>

Composite

</td><td>

Option indicating that the service specification is a parent specification composed of multiple child specifications.

</td></tr><tr><td>

Installation required

</td><td>

Option indicating that someone must install the service on site.

</td></tr><tr><td>

Location specific

</td><td>

Option indicating that this service specification requires the location details for fulfillment and installation.

</td></tr><tr><td>

Transient

</td><td>

Option that indicates the product for this service specification is for one-time use. **Note:** If you select this option, the sold product and or product inventory record for the transient product is set to an Inactive state when the order is completed. Move, Add, Change, Delete \(MACD\) actions can’t be performed on the sold product or product inventory records of transient products.

</td></tr><tr><td>

Initial version

</td><td>

Name of the base version of the specification that appears but can't be changed.

</td></tr><tr><td>

Previous version

</td><td>

Name of the previous version of the specification. For example:-   When you create the initial version of the specification \(for example, version 1\), this field is empty.
-   When you create a version \(version 2\) with a slightly different name, the name of the specification at its initial creation appears here.
-   When you create a subsequent version \(version 3\), the name of the specification as it was at version 2 appears here.
You can't change this field.

</td></tr></tbody>
</table>4.  Select **Save**.

    The service specification is created. The following tabs open for defining related information:

<table id="table_rgl_ffp_dfc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog Hierarchy

</td><td>

[View the complete hierarchy of a product offering and any associated specifications](https://www.servicenow.com/docs/access?context=som-catalog-hierarchy&version=australia&pubname=australia-order-management&ft:locale=en-US).Use the **Show specification** toggle to view the hierarchy of specifications.

</td></tr><tr><td>

Specification Characteristics

</td><td>

[Associate the characteristics and characteristic options with your specification](https://www.servicenow.com/docs/access?context=create-specification-characteristic&version=australia&pubname=australia-order-management&ft:locale=en-US).

</td></tr><tr><td>

Specification Relationships

</td><td>

[Create specification relationships, quantity mapping, and decomposition rules for Sales CRM for Telecommunications](create-specification-relationships-somt.md).

</td></tr><tr><td>

Versions

</td><td>

[Create another version of the specification](https://www.servicenow.com/docs/access?context=creating-publishing-new-versions-specifications&version=australia&pubname=australia-order-management&ft:locale=en-US).

</td></tr></tbody>
</table>5.  When you are finished creating the specification version, do one of the following actions.

<table id="choicetable_zw3_3sc_dtb"><thead><tr><th align="left" id="d21589e586">

Action

</th><th align="left" id="d21589e589">

Description

</th></tr></thead><tbody><tr><td id="d21589e595">

**Publish**

</td><td>

Publish the draft specification so that you can use it in a product offering. -   When you publish it, its state changes from Draft to Published.
-   After you publish a specification, you can't change or delete it, unless you create a version for it.


</td></tr><tr><td id="d21589e613">

**Update**

</td><td>

Update the specification with the new data that you added, but do not publish it for use in a product offering.

</td></tr><tr><td id="d21589e622">

**Copy**

</td><td>

Copy the data in this specification so that you can create a specification from it.

</td></tr></tbody>
</table>
