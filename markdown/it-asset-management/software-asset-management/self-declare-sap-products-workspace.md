---
title: Self-declare SAP engine license usage in the Software Asset Workspace
description: Use the Software Asset Workspace to self-declare the license usage for any SAP engines that cannot be measured by the automated SAP engine measurement process.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Self-declaring SAP engine license usage, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Self-declare SAP engine license usage in the Software Asset Workspace

Use the Software Asset Workspace to self-declare the license usage for any SAP engines that cannot be measured by the automated SAP engine measurement process.

## Before you begin

Role required: admin or sam\_user

## About this task

To determine if you must self-declare the license usage for a given engine, see [Engine &amp; Self-Declaration Product Measurement](https://support.sap.com/en/my-support/systems-installations/system-measurement/engine-self-declaration-product-measurement.html) in the SAP Support Portal. You must self-declare the license usage for any engine that is included in the list of Self-Declaration Products.

**Important:** You must have an SAP Support Portal account to access the SAP Support Portal.

## Procedure

1.  Create a software model for the SAP engine.

    Refer to [Create software models in workspace](create-swmodels-workspace.md) for detailed instructions.

    **Note:**

    On the Create New Software Model form, you must set the **Publisher** field to `SAP`. The form then reloads with only the software model fields that are applicable to SAP.

    In addition, you must set the **Product** field to the SAP engine that you want to self-declare the license usage for.

2.  Create entitlements for your software model.

    You can create entitlements using either of the following options:

    -   The **Create entitlement** button on the Software asset overview.

        Refer to [Create entitlements in workspace](create-entitlements-workspace.md) for detailed instructions on how to create entitlements using this option.

        **Note:** On the Create New Software Entitlement form, you must set the **Software model** field to the same software model that you created in [step 1](self-declare-sap-products-workspace.md#create-software-model).

    -   The **Software Entitlements** tab on the software model record.

        To create entitlements using this option, open the record for the software model that you created in [step 1](self-declare-sap-products-workspace.md#create-software-model). On the **Software Entitlements** tab of the software model record, select **New** and then fill in the fields on the corresponding Create New Software Entitlement form.

        Refer to [Software entitlement fields](../reference/software-entitlement-fields.md) for detailed descriptions of each field.

        **Note:** The **Software model** field populates automatically.

3.  Specify the license usage of the SAP engine.

    1.  Open the record for the software model that you created in [step 1](self-declare-sap-products-workspace.md#create-software-model).

    2.  On the **SAP Engine Usages** tab, select **New**.

    3.  On the Create new SAP Engine Usage form, fill in the fields.

<table id="table_x32_wfs_g5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that is used to identify and track your SAP engine license usage.

</td></tr><tr><td>

Software model

</td><td>

Software model that the SAP engine is associated with. This field populates automatically.

</td></tr><tr><td>

SAP client

</td><td>

SAP client that the SAP engine is installed or running on.

</td></tr><tr><td>

Usage

</td><td>

License usage of the SAP engine.

 This value is based on the license metric that is associated with the engine. For example, the license metric for the SAP E-Recruiting engine is **Employees**. If 200 employees are using an SAP E-Recruiting license, you must enter a license usage value of `200` in the **Usage** field. Refer to [Engine &amp; Self-Declaration Product Measurement](https://support.sap.com/en/my-support/systems-installations/system-measurement/engine-self-declaration-product-measurement.html) for more information on the license metrics that are associated with each SAP engine.

</td></tr></tbody>
</table>    4.  Select **Save**.


## Result

After you self-declare the license usage for the SAP engine, it is automatically included in the next SAP reconciliation that runs on your ServiceNow instance. Reconciliation runs weekly or on-demand.

**Parent Topic:**[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

