---
title: Set the domain-specific property to publish your software products
description: Use the domain separation application property of Software Asset Management to set the publish software products property for specific domains.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage phase-wise Software Asset Management implementation, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Set the domain-specific property to publish your software products

Use the domain separation application property of Software Asset Management to set the publish software products property for specific domains.

## Before you begin

To set up domain separation application properties for Software Asset Management, you must activate the Domain Support - Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\) plugin on your ServiceNow instance.

Role required: sam\_admin or admin

## About this task

The **com.snc.samp.manage.published.product** application property enables you to specify the domains for which you want to enable publishing the software products in a phase-wise implementation of Software Asset Management.

## Procedure

1.  Navigate to **All** &gt; **Software Asset Management** &gt; **Administration** &gt; **Application Properties**.

2.  From the list of available application properties, select **com.snc.samp.manage.published.products**.

3.  Create or update an application property value.

    -   To create an application property value, select **New**.
    -   To update an existing application property value, select that application property value from the list of available values.
4.  On the form, fill in the fields.

<table id="table_tdn_xtf_vzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Value

</td><td>

Value of the application property. You can specify one of the following:-   **true** to enable the property.
-   **false** to disable the property.


</td></tr><tr><td>

Domain

</td><td>

Domain that you want the application property value to apply to.

</td></tr></tbody>
</table>5.  Save the application property values.

    -   To update an existing application property value, select **Update.**
    -   To save a new application property value, select **Submit**.

## What to do next

Publish the software products that you want to manage as part of phase-wise implementation of Software Asset Management. For more information, see [Publish a specific set of your software products](add-published-products.md).

**Parent Topic:**[Manage phase-wise Software Asset Management implementation](../concept/manage-phasewise-imp-of-sam.md)

**Related topics**  


[Publish a specific set of your software products](add-published-products.md)

[Remove published software products](remove-published-products.md)

