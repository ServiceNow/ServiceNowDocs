---
title: Create a Service Catalog client script
description: You can create client scripts to customize the catalog.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Service Catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a Service Catalog client script

You can create client scripts to customize the catalog.

## Before you begin

Role required: admin

## About this task

Use catalog client scripts to control the behavior of the catalog items when presented to your users. Catalog client scripts can be applied to a catalog item or a variable set. These scripts run on the browser instead of the server, allowing you to better control the information that the user submits.

The priority order for g\_form APIs is:

1.  Mandatory \(highest\)
2.  ReadOnly/Display

If a variable is set to mandatory and doesn’t have a value, readonly or hide doesn't work on that variable. If a variable is hidden or readonly, and then set to mandatory, the variable field becomes visible or editable.

This priority order is also applicable for variable sets and containers. If a variable set or container has a mandatory variable without any value, then the container or variable set can’t be hidden.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Catalog Client Scripts**.

    A list of current custom catalog client scripts appears.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_bw1_3g1_dq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the catalog client script.

</td></tr><tr><td>

Applies to

</td><td>

Item type this client script applies to:-   **A Catalog Item**: enables the Catalog item field.
-   **A Variable Set**: enables the Variable set field.


</td></tr><tr><td>

Active

</td><td>

Check box to enable the client script. Clear the check box to disable the script.

</td></tr><tr><td>

UI Type

</td><td>

Whether to apply this field to desktop, Classic Mobile, or both.

</td></tr><tr><td>

Script

</td><td>

Enter the client script to run on the service catalog item.

</td></tr><tr><td>

Type

</td><td>

Select when the script runs, such as **onLoad** or **onSubmit**.

</td></tr><tr><td>

Catalog item or Variable set

</td><td>

Select a catalog item or variable set from the list. The field name and options available depend on the selection in the **Applies to** field.

</td></tr><tr><td>

Applies on a Catalog Item view

</td><td>

Check box to apply the catalog client script to catalog items displayed within the order screen on the service catalog. Available in the requester view.

</td></tr><tr><td>

Applies on Requested Items

</td><td>

Check box to apply the catalog client script on a Requested Item form, after the item is requested. Available in the fulfiller view. See [VEditor](../concept/service-catalog-variable-editor.md#cat-VEditor).

</td></tr><tr><td>

Applies on Catalog Tasks

</td><td>

Check box to apply the catalog client script when a Catalog Task form for the item is being displayed. Available in the fulfiller view. See [VEditor](../concept/service-catalog-variable-editor.md#cat-VEditor).

</td></tr><tr><td>

Applies on the Target Record

</td><td>

Check box to support the catalog client script on a record created for task-extended tables via record producers. See [Default variable editor](../concept/service-catalog-variable-editor.md#cat-default-variable-editor).

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Service Catalog items](../concept/c_IntroductionToCatalogItems.md)

