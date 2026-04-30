---
title: Configure the estimated spend offering cost source
description: Define the source used to calculate the estimated cost for service offerings. You can use the default local model or access the preconfigured Financial Management service offering cost models.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Financial Management for Service Owner Workspace, Using Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Configure the estimated spend offering cost source

Define the source used to calculate the estimated cost for service offerings. You can use the default local model or access the preconfigured Financial Management service offering cost models.

## Before you begin

Role required: admin

## About this task

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](../concept/SPM2-premium.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Use Service Owner Workspace](../image/SOWUseBanner2.png "Navigate")

</td></tr></tbody>
</table>The Service Portfolio Management Estimated Spend plugin \(com.snc.spm.spend\) is automatically activated with Service Owner Workspace.

Activate the Financial Management for SPM plugin \(com.snc.financial\_management\_for\_spm\) to enable the associated cost model.

Service Portfolio Management Estimated Spend provides the **sn\_spm\_spend.offering\_cost\_source** system property. With this property, you can define the source used to calculate the estimated cost for service offerings. Values include:

-   **Local Model**
-   **Financial Management**
-   **None**

The default value is **Local Model**.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter to open the System Properties \[sys\_properties\] table.

2.  Find the **sn\_spm\_spend.offering\_cost\_source** system property and set it to the desired value.

    **Note:** Users can choose not to use the local cost model or the Financial Management model, by selecting **None** as the desired value.

<table id="table_ivh_l3f_f3b"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Local Model**

</td><td>

With this default source, the offering Estimated Spend cost is calculated based on the following fields on the Service Offering form:-   **Cost model**: Choices include, **Fixed** and **Per unit**.
-   **Estimated spend**: The estimated cost of the offering for the associated time period.
 When the **Cost model** value is **Fixed**, additional fields appear on the Service Offering form, including: **Offering cost**, **Time period**, and **Cost Unit**.

 When the **Cost model**is **Per Unit**, additional fields appear on the Service Offering form, including: **Offering cost**, **Time period**, **Units per period**, and **Cost Unit**.

</td></tr><tr><td>

**Financial Management**

</td><td>

With this source, the offering **Estimated Spend** cost is calculated based on the following Service Offering form fields, as calculated by the Financial Management application:-   **FM period**: Fiscal calendar period.
-   **FM cost**: The actual currency amount.


</td></tr><tr><td>

**None**

</td><td>

With this value, or any incorrect values, the system ignores both the local and Financial Management cost models and does not display associated Service Offering form fields.

</td></tr></tbody>
</table>3.  Click **Update** to save any changes.


