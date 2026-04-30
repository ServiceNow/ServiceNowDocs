---
title: Create software models for SAP
description: Create software models to record SAP product information.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create software models for SAP

Create software models to record SAP product information.

## Before you begin

Role required: sam\_user

**Important:** You can create software models in both the Software Asset Management classic application and the Software Asset Workspace. The following steps provide details on creating software models in the Software Asset Management classic application. For details on creating software models in the Software Asset Workspace, see [Create software models in workspace](create-swmodels-workspace.md).

## About this task

Software models are automatically created for engines and license metrics that are pulled from your SAP systems. You can manually create additional software models for SAP products as needed.

The following steps describe information that is specific to SAP. For general instructions on creating software models, see [Create software models in Software Asset Management classic](record-terms-software-licenses.md).

## Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Software Models** and select **New**.

2.  On the form, fill in the fields.

    **Note:** Only the fields that are specific to SAP software models are shown below. For detailed descriptions of all software model fields, see [Software model fields](../reference/software-model-fields.md).

<table id="table_nr2_nd1_y4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_jbl_lqs_mfb"><td>

Named user type

</td><td>

SAP named user type. **Note:** This field appears only when **Named Users** is selected from the **Product** field.

</td></tr><tr id="row_vsz_pqs_mfb"><td>

Price List

</td><td>

Software group that corresponds to the named user type.**Note:** This field appears only when **Named Users** is selected from the **Product** field.

</td></tr><tr><td>

SAP license metric

</td><td>

License metric that is used to calculate license consumption for an engine. Examples of license metrics are number of employees or number of contracts.**Note:** This field appears only when an SAP engine is selected from the **Product** field.

</td></tr><tr><td>

Is relevant

</td><td>

Some SAP engines don't require additional licensing. Select the check box if the engine requires additional licensing. Software models with **Is relevant** set to false will always be considered compliant by reconciliation.**Note:** This field appears only when an SAP engine is selected from the **Product** field.

</td></tr><tr><td>

Threshold

</td><td>

Some SAP engines allow a certain amount of unlicensed usage before your licence position becomes not compliant. The threshold defines the allowed usage and is specific to each engine and license metric. If your engine usage exceeds your licensed amount but is less than the threshold value, the software model is still considered compliant by reconciliation.**Note:** This field appears only when an SAP engine is selected from the **Product** field.

</td></tr></tbody>
</table>3.  Select **Submit**.


## What to do next

[Create a software entitlement](create-entitlement-sap.md) to record your licenses for the software model.

**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](import-abap-program-sap.md)

[Establish an SAP connection](add-sap-connection.md)

[Create entitlements for SAP](create-entitlement-sap.md)

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

