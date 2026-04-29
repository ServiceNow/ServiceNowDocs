---
title: Discovery models fields
description: Discovery Models form and related list field descriptions.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Discovery models fields

Discovery Models form and related list field descriptions.

## Discovery Models form

<table id="table_cql_sx5_hp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_xv5_pcp_sfb"><td>

Display name

</td><td>

Name of the discovery model as it appears in record lists. This value is generated automatically using the discovered publisher, discovered product, and discovered version.

</td></tr><tr><td>

Normalization status

</td><td>

[Status](normalization-status.md) of the normalization process:-   Normalized
-   Partially Normalized
-   Publisher Normalized
-   Match Not Found
-   Manually Normalized
-   New

 **Note:** If a normalization suggestion record exists, a caution icon is shown next to the **Normalization status** field.

The caution icon opens the [Normalization Suggestion](../task/view-norm-suggestions-sam.md) record for the discovery model.

</td></tr><tr id="row_z1l_pcp_sfb"><td>

Publisher

</td><td>

Normalized publisher of the software.

</td></tr><tr id="row_anb_pcp_sfb"><td>

Product

</td><td>

Normalized product name of the software.

</td></tr><tr id="row_phr_4cp_sfb"><td>

Version

</td><td>

Normalized version of the software product.

</td></tr><tr id="row_oth_4cp_sfb"><td>

Discovered publisher

</td><td>

Discovered publisher of the software.

</td></tr><tr id="row_vjz_ncp_sfb"><td>

Discovered product

</td><td>

Discovered name of the software.

</td></tr><tr id="row_zvr_ncp_sfb"><td>

Discovered version

</td><td>

Discovered version of the software.

</td></tr><tr><td class="sub-head" colspan="2">

Additional Information

</td></tr><tr id="row_vkw_mcp_sfb"><td>

Product type

</td><td>

-   Child: Subcomponent of main software \(not licensable\).
-   Driver: Software product that controls a device.
-   Licensable: Software product that is licensable.
-   Not Licensable: Software product that is not licensable.
-   Patch: Software product designed to update, fix, or improve an existing computer program.
-   Unknown: Not discovered.

For unknown product types, the product type can be changed to another value.

When the product type is changed, the normalization status of the discovery model is updated to Manually Normalized.


 The reconciliation process only considers software discovery models that are licensable.

</td></tr><tr id="row_pqm_mcp_sfb"><td>

Platform

</td><td>

Platforms include:-   Windows
-   macOS
-   UNIX

</td></tr><tr id="row_r2c_mcp_sfb"><td>

Language

</td><td>

Languages include:-   Dutch
-   English
-   French
-   German
-   Italian
-   Spanish

 If discovered, more languages are generated.

</td></tr><tr id="row_zbp_lcp_sfb"><td>

Edition

</td><td>

Normalized edition of the software.

</td></tr><tr id="row_hzc_lcp_sfb"><td>

Full version

</td><td>

Normalized full version of the software.

</td></tr><tr><td>

Exclude from content service

</td><td>

Option that excludes the software discovery model details from being transferred to the [Software Asset Management Content Service](../concept/c_SAMContentService.md).The value is set on the [custom product](../task/t_AddACustomProduct.md) form.

 **Note:** This field is only shown for custom products when you have opted in to the Software Asset Management Content Service.

</td></tr></tbody>
</table>## Additional Information section

<table id="table_qfv_kk2_1kb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product type

</td><td>

-   Child: Subcomponent of main software \(not licensable\).
-   Driver: Software product that controls a device.
-   Licensable: Software product that is licensable.
-   Not Licensable: Software product that is not licensable.
-   Patch: Software product designed to update, fix, or improve an existing computer program.
-   Unknown: Not discovered.

For unknown product types, the product type can be changed to another value.

When the product type is changed, the normalization status of the discovery model is updated to Manually Normalized.


 The reconciliation process only considers software discovery models that are licensable.

</td></tr><tr><td>

Platform

</td><td>

Platforms include:-   Windows
-   macOS
-   UNIX

</td></tr><tr><td>

Language

</td><td>

Languages include:-   Dutch
-   English
-   French
-   German
-   Italian
-   Spanish

 If discovered, more languages are generated.

</td></tr><tr><td>

Edition

</td><td>

Normalized edition of the software.

</td></tr><tr><td>

Full version

</td><td>

Normalized full version of the software.

</td></tr><tr><td>

Exclude from content service

</td><td>

Option that excludes the software discovery model details from being transferred to the [Software Asset Management Content Service](../concept/c_SAMContentService.md).The value is set on the [custom product](../task/t_AddACustomProduct.md) form.

 **Note:** This field is only shown for custom products when you have opted in to the Software Asset Management Content Service.

</td></tr></tbody>
</table>## Software Installation related list

|Field|Description|
|-----|-----------|
|Display name|Name of the software install as it appears in the record lists.|
|Publisher|Name of the publisher of the software.|
|Version|Version of the software.|
|Installed on|Name of the hardware the software is installed on.|

**Parent Topic:**[Software Asset Management references](references.md)

