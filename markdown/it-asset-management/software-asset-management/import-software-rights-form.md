---
title: Entitlement import error actions
description: Entitlement Import Error form action descriptions.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Entitlement import error actions

Entitlement Import Error form action descriptions.

## Entitlement Import Errors actions

<table id="table_jlx_prz_4hb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import

</td><td>

Option that saves the Entitlement Import Error record. After you save the record, you remain on the Entitlement Import Error form, so you can easily save the form between actionsUpon saving, all values are reevaluated and the form is updated.

 For example, if both the publisher part number and software model fields are missing, once a known publisher part number is added and the form is saved, the **Software model** field is filled in automatically.

**Note:** Because the form is reevaluated after each save, changes made to one entitlement may cause an error for another entitlement, such as a **Duplicate entry**.

 When all required fields are filled in and the form is saved, an entitlement record is created and the error status is changed to Fixed.

</td></tr><tr><td>

Create PPN

</td><td>

Part number for custom software. If you are importing entitlements using the Software Asset Management workspace application, on selecting **Create PPN**, you are taken to the Custom Part Numbers list view page. Select **New** to create a new publisher part number.

 If you are importing entitlements using the Software Asset Management classic application, on selecting **Create PPN**, the Create Discovery Map for Publisher Part Number dialog box appears. Select a product name in the **Product** field and select **Submit** to create a custom discovery map which is automatically associated with the publisher part number.

</td></tr><tr><td>

Create duplicate entitlement

</td><td>

Duplicate entitlement records cause an import error. Select **Create duplicate entitlement** to override the error and create an entitlement for the duplicate record. **Note:** This action only appears if there is an entitlement that already exists and a duplicate entitlement is being created.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

