---
title: Create entitlements for SAP
description: Create software entitlements to record your license information for SAP products. You can create entitlements individually or import them from a spreadsheet.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/create-entitlement-sap.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create entitlements for SAP

Create software entitlements to record your license information for SAP products. You can create entitlements individually or import them from a spreadsheet.

## Before you begin

Role required: sam\_user or sam\_admin

**Note:** The sam\_admin role is required to import entitlements.

**Important:** You can create and import entitlements in both the Software Asset Management classic application and the Software Asset Workspace. The following steps provide details on creating entitlements in the Software Asset Management classic application. For details on creating entitlements in the Software Asset Workspace, see [Create entitlements in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-entitlements-workspace.md). For details on importing entitlements in the Software Asset Workspace, see [Import bulk entitlements in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/import-entitlements-workspace.md).

## About this task

The following steps describe information specific to SAP. For general instructions on creating software entitlements, see [Create entitlements in Software Asset Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/track-software-rights.md).

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **Software Entitlement** and select **New**.

2.  On the form, fill in the fields.

    **Note:** Only information specific to SAP software entitlements is shown in the following table. For a detailed description of all software entitlement fields, see [Software entitlement fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-entitlement-fields.md).

<table id="table_zql_nkm_11b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Metric group

</td><td>

SAP

</td></tr><tr><td>

License metric

</td><td>

Select any of the following values:

 -   **Named User**: To license the number of named users that can be assigned a given Named User Type. The Named User Type is defined by the software model linked to the entitlement.
-   **Engine Measurement**: To license the amount of usage for an SAP engine.
-   **Digital Access**: To license the indirect usage of SAP applications through a third-party application or a non-SAP intermediary software based on the count of documents created by the third-party application
-   **Full Usage Equivalent**: To license the number of users that are authorized to access specified solution capabilities of SAP S/4HANA Cloud Public Edition. Full Usage Equivalent \(FUE\) can be allocated to different user types with a specific weighing factor.
 When you select **Full Usage Equivalent** in the **License metric** field, the license type is automatically set to **Subscription**.

 The type of usage is defined by the **SAP license metric** field on the software model.

 For more information about license metrics, see [Software license metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/c_SAMLicenseMetrics.md).

</td></tr><tr><td colspan="2">

The following fields appear when you select **Engine measurement** in the **License metric** field.

</td></tr><tr><td>

Rights per license pack

</td><td>

Number of rights associated with each pack that is purchased for SAP Engine product.

</td></tr><tr><td>

Number of packs

</td><td>

Number of packs for SAP Engine measurement licenses.

</td></tr></tbody>
</table>3.  Select **Save**.

4.  After the form reloads, select **Publish**.


**Parent Topic:**[Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack]()

[Set up SAP integration to establish a connection with SAP]()

[Establish an SAP connection using basic authentication]()

[Establish an SAP connection using OAuth 2.0]()

[Create software models for SAP]()

[Create a custom SAP named user type]()

[Map a role to a named user type]()

[Create custom SAP price lists]()

[Import custom SAP named user types]()

[Import custom SAP price lists]()

[SAP USMM-based optimization]()

[User transaction activity for named user types]()

[Self-declaring SAP engine license usage]()

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic]()

[Publisher overview for SAP in the Software Asset Workspace]()

