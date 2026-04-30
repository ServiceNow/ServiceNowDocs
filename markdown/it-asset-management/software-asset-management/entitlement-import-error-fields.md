---
title: Entitlement import error fields
description: Entitlement Import Error form and related list field descriptions.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Entitlement import error fields

Entitlement Import Error form and related list field descriptions.

## Entitlement Import Error form

<table id="table_ifb_whm_43b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Error status

</td><td>

Status of the entitlement. An error record can have either of the two statuses:-   Manually fixed: when all the errors in the error record are corrected and the entitlement is successfully created.
-   Needs review:the error record is created and you need to review and correct the errors.

</td></tr><tr><td>

Reason

</td><td>

Reason the imported entitlement couldn't be added to the Entitlement list.

</td></tr><tr><td>

Asset tag

</td><td>

Serial number and the bar code used for tracking the asset.

</td></tr><tr><td>

Publisher part number

</td><td>

Publisher part number from the Software Product Definitions lookup list of predefined software that may have already been purchased. When you select a publisher part number, you may encounter a message: `Many underlying software models are being created. These might be part of suite components, downgrade rights or next version. Please validate on completion`. The message appears only if there are greater than or equal to 50 suite components for the software model and if any of the following conditions are met:

-   A software model does not exist for any suite component
-   A software model does not exist for any downgrade right
-   A software model does not exist for the next version

 **Note:** If a software model exists for the publisher part number, the **Software model** field is automatically populated. Otherwise, the software model is automatically created for you directly from this form. If there are multiple software models created with the same discovery map conditions, the software model must be selected manually.

</td></tr><tr><td>

Software model

</td><td>

The software model to match the entitlement. **Note:** A warning message is shown if the publisher part number is not associated with the publisher and product for the software model. You can either change the software model, or save the entitlement as is.

</td></tr><tr><td>

License type

</td><td>

License type. Whether the rights grant full access to the software or if they are being upgraded from a previous version of the software.When the type is **Upgrade**, the Upgraded Entitlements related list is shown. The upgrade license type is used to specify the entitlements you are upgrading.

 This field becomes read-only after the form has been submitted.

 **Note:** For SaaS entitlements, keep the default value **\(Full\)**.

</td></tr><tr><td>

Metric group

</td><td>

This field is automatically populated based on the **Software Model** field. Each metric group has a set of license metrics that are specific to the software publisher.

</td></tr><tr><td>

License metric

</td><td>

License metric for the license group that the software license is counted against when reconciliation is run. The options for license metric change based on the **Metric group** field. The default value for SaaS entitlements is **User Subscription**.For more information, see [Software license metrics](../concept/c_SAMLicenseMetrics.md).

 **Note:** Use the Envelopes license metric only for Docusign entitlements.

</td></tr><tr><td>

Rights per license pack

</td><td>

Rights associated with each pack that is purchased for Microsoft Per Core or Microsoft Per Core with CAL licenses.

</td></tr><tr><td>

Number of packs

</td><td>

Number of packs for Microsoft Per Core or Microsoft Per Core with CAL licenses.

</td></tr><tr id="row_xnb_hss_mfb"><td>

Purchased right

</td><td>

Number of rights that you are purchasing.**Note:** If you've specified a Microsoft Per Core or Microsoft Per Core with CAL license type, this field is automatically populated. This value is based on the values entered in the **Rights per license pack** field multiplied by the value in the **Number of packs** field.

</td></tr><tr><td>

Agreement type

</td><td>

Based on the agreement type that you select, downgrade rights are automatically generated.

**Note:** If the agreement type is **Enterprise License Agreement** or **Unlimited Level Agreement**, the **Status** is Compliant even if there are unlicensed installations.

-   **Generic**: Downgrade rights are not automatically populated. If you change the agreement type on an existing software entitlement from **Generic** to any other type \(for example **CLP**\), the downgrade rights are automatically populated.
-   Any agreement type other than Generic: Downgrade rights are automatically populated. If you change the agreement type on an existing software entitlement from an agreement type other than **Generic** \(for example, **ELTA**\) to **Generic**, the downgrade rights that were already populated are not deleted or deactivated.

</td></tr><tr><td>

Purchased rights

</td><td>

Number of rights that you are purchasing.

</td></tr><tr><td>

Oracle options

</td><td>

Oracle options related to the entitlement.

</td></tr><tr><td>

Contract number

</td><td>

Contract number for the entitlement.

</td></tr></tbody>
</table>## Reference software related list

|Field|Description|
|-----|-----------|
|Publisher|Name of the software publisher.|
|Product|Name of the product.|
|Version|Version of the software product.|
|Edition|Edition of the software product.|
|Language|Language of the software product to use when searching for the normalized discovery model, which is populated once it has been normalized or added manually.|
|Platform|Platform of the software product to use when searching for the normalized discovery model.|

## General related list

|Field|Description|
|-----|-----------|
|Owned by|User or department with financial ownership of the asset. The asset owner can be different than the manager.|
|PO number|Purchase order number.|
|Company|Company that this asset belongs to.|
|Location|Where the license is used. For example, a specific site, country, or region.|
|Department|Department of the person **Assigned to** this software license.|

## Financial related list

<table id="table_ssn_cjm_43b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vendor

</td><td>

Company that the asset was purchased from.

</td></tr><tr><td>

Unit cost

</td><td>

Unit cost of the software. **Note:** Required for total cost and savings calculations on the [Software Asset Management dashboard.](../concept/c_SAMDashboard.md)

</td></tr><tr><td>

GL account

</td><td>

General ledger account number associated with the asset.

</td></tr><tr><td>

Cost center

</td><td>

Cost center financially responsible for the asset.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

