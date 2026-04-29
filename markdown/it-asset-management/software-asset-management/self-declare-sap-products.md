---
title: Self-declare SAP engine license usage in the Software Asset Management classic application
description: Use the Software Asset Management classic application to self-declare the license usage for any SAP engines that cannot be measured by the automated SAP engine measurement process.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Self-declaring SAP engine license usage, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Self-declare SAP engine license usage in the Software Asset Management classic application

Use the Software Asset Management classic application to self-declare the license usage for any SAP engines that cannot be measured by the automated SAP engine measurement process.

## Before you begin

Role required: sam\_user

## About this task

To determine if you must self-declare the license usage for a given engine, see [Engine &amp; Self-Declaration Product Measurement](https://support.sap.com/en/my-support/systems-installations/system-measurement/engine-self-declaration-product-measurement.html) in the SAP Support Portal. You must self-declare the license usage for any engine that is included in the list of Self-Declaration Products.

**Important:** You must have an SAP Support Portal account to access the SAP Support Portal.

## Procedure

1.  Create a software model for the SAP engine.

    Refer to [Create software models for SAP](add-software-model-sap.md) for detailed instructions.

    **Note:**

    On the Software Model form, you must set the **Publisher** field to `SAP`. The form then reloads with only the software model fields that are applicable to SAP.

    In addition, you must set the **Product** field to the SAP engine that you want to self-declare the license usage for.

2.  Create entitlements for your software model.

    Refer to [Create entitlements for SAP](create-entitlement-sap.md) for detailed instructions.

    **Note:** On the Software Entitlement form, you must set the **Software model** field to the same software model that you created in [step 1](self-declare-sap-products.md#create-software-model).

3.  Create a client access record to specify the license usage of the SAP engine.

    1.  On the page header of your ServiceNow instance, select **All**.

    2.  In the menu navigation filter, enter `samp_sw_client_access_list.do`.

        The Client Access \[samp\_sw\_client\_access\] table opens.

    3.  Select **New**.

    4.  In the **Name** field of the Client Access form, enter a name for the client access record.

    5.  Select the Lookup using list icon \(![Lookup using list icon.](../image/search-icon.png)\) next in the **Software model** field to locate and select the software model for the SAP engine.

        **Note:** Select the same software model that you created in [step 1](self-declare-sap-products.md#create-software-model).

    6.  Enter an engine license usage value in the **Usage** field.

        This license usage value is based on the license metric that is associated with the engine. For example, the license metric for the SAP E-Recruiting engine is **Employees**. If 200 employees are using an SAP E-Recruiting license, you must enter a license usage value of `200` in the **Usage** field.

        Refer to [Engine &amp; Self-Declaration Product Measurement](https://support.sap.com/en/my-support/systems-installations/system-measurement/engine-self-declaration-product-measurement.html) for more information on the license metrics that are associated with each SAP engine.

    7.  Select **Submit**.


## Result

After you self-declare the license usage for the SAP engine, it is automatically included in the next SAP reconciliation that runs on your ServiceNow instance. Reconciliation runs weekly or on-demand.

**Parent Topic:**[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

