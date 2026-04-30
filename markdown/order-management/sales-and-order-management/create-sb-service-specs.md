---
title: Create a service specification for a remote catalog item
description: Create a service specification on a Service Exchange provider instance. When you publish the service specification, a remote record producer creates the remote catalog item for the service specification.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configuring Service Exchange Order Management for Providers, Order Management for providers with Service Exchange, Extending Order Management with ServiceNow applications and integrations, Sales Customer Relationship Management]
---

# Create a service specification for a remote catalog item

Create a service specification on a Service Exchange provider instance. When you publish the service specification, a remote record producer creates the remote catalog item for the service specification.

## Before you begin

Define the characteristics, characteristic options, and specification categories before you create a service specification.

Role required: sn\_prd\_pm.product\_catalog\_admin or sn\_prd\_pm.product\_catalog\_manager

## About this task

When you create a service specification for a service request, use the **Distribution channel** field to set the channel to Service Exchange. When the service specification is published, a remote record producer is created for the specification.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Specifications** &gt; **Service specifications** and select **New**.

    On the Details tab, fill in the form.

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
-   When you create versions of the specification, a system-assigned concatenation of the specification name and its current version number appears, but can be overwritten. For example, SD-WAN Edge Device v2 appears in this field when:
    -   SD-WAN Edge Device is the name of the specification.
    -   Version 2 is the current version of the specification.


</td></tr><tr><td>

Category

</td><td>

Specification category that the service specification belongs to.-   If the selected category that belongs to 5G services doesn't have any matching slice templates, the system checks for existing templates.
-   If the selected category has multiple templates mapped to it, the systems chooses the latest published template to the specification.


</td></tr><tr><td>

Type

</td><td>

Type of service specification: -   **Customer Facing**

Customers can create a ticket or a case for the service. When you select this type, the **Distribution channel** field is displayed to specify how the service is provided.

**Note:** If you're using Service Exchange Order Management for Providers, only Customer Facing Service specifications are eligible for remote catalog creation. Service Exchange must be specified as the distribution channel so that remote record producers can be created.

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

Templates that you've defined if you're using 5G services.**Note:** When you change a template, it deletes all the specification characteristics that are marked as true and are associated with the old template and re-associates the specification characteristics as per the new template that you've selected.

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

Option to set and lock in a distribution channel. For example, you can specify web as a channel. You can specify multiple channels. **Note:** If you're using the Service Exchange Order Management for Providers application and have a customer facing specification, enter Service Exchange as the distribution channel so that remote record producers can be created for remote catalog creation.

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
</table>3.  Select **Save** and then **Publish**.

    A remote record producer creates the remote catalog item for the specification.


## What to do next

[Associate consumer criteria to a remote record producer](associate-criteria-remote-catalog.md) for this remote catalog item.

