---
title: Create entitlements for SAP
description: Create software entitlements to record your license information for SAP products. You can create entitlements individually or import them from a spreadsheet.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create entitlements for SAP

Create software entitlements to record your license information for SAP products. You can create entitlements individually or import them from a spreadsheet.

## Before you begin

Role required: sam\_user or sam\_admin

**Note:** The sam\_admin role is required to import entitlements.

**Important:** You can create and import entitlements in both the Software Asset Management classic application and the Software Asset Workspace. The following steps provide details on creating entitlements in the Software Asset Management classic application. For details on creating entitlements in the Software Asset Workspace, see [Create entitlements in workspace](create-entitlements-workspace.md). For details on importing entitlements in the Software Asset Workspace, see [Import bulk entitlements in workspace](import-entitlements-workspace.md).

## About this task

The following steps describe information specific to SAP. For general instructions on creating software entitlements, see [Create entitlements in Software Asset Management classic](track-software-rights.md).

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **Software Entitlement** and select **New**.

2.  On the form, fill in the fields.

    **Note:** Only information specific to SAP software entitlements is shown in the following table. For a detailed description of all software entitlement fields, see [Software entitlement fields](../reference/software-entitlement-fields.md).

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

 For more information about license metrics, see [Software license metrics](../concept/c_SAMLicenseMetrics.md).

</td></tr></tbody>
</table>3.  Select **Save**.

4.  After the form reloads, select **Publish**.


**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](import-abap-program-sap.md)

[Establish an SAP connection](add-sap-connection.md)

[Create software models for SAP](add-software-model-sap.md)

[Create a custom SAP named user type](create-named-user.md)

[Map a role to a named user type](create-named-user-type-role-mapping.md)

[Create custom SAP price lists](create-sap-pricelist.md)

[Import custom SAP named user types](import-custom-sap-named-user-type.md)

[Import custom SAP price lists](import-custom-sap-price-list.md)

[SAP USMM-based optimization](../concept/usmm-optimization.md)

[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

