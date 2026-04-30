---
title: Create a chemical record for a new chemical
description: The chemical manager can create a chemical record for the new chemical request that has been approved.
locale: en-US
release: yokohama
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-11-27"
reading_time_minutes: 3
breadcrumb: [Chemical management, Use, Health and Safety Environmental Management, Health and Safety, Employee Service Management]
---

# Create a chemical record for a new chemical

The chemical manager can create a chemical record for the new chemical request that has been approved.

## Before you begin

Role required: sn\_hs\_chm.manager

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  In the primary navigation, select **Environmental Management** ![environmental management icon](../image/icon-hs-envt-mgmt.png) icon.

3.  In the **Chemical Requests** list, select the **Approved** tab and select a chemical request record.

4.  In the **Details** related list of the chemical request, select the **Create chemical** button.

5.  In the **Create chemical** form under the **Automatically** tab, the fields **Chemical name**, **Manufacturer**, and **Language** are automatically filled.

    -   The fields are populated automatically because of the integration with the 3E database. If this configuration isn’t done, the **Create chemical** form must be filled manually.
    -   To create chemical manually, use the **Manually** tab, enter the **Chemical name** and then select **Submit**. On the **Create chemical** form, fill in the fields. For more information, see [Chemical form](../reference/hs-chemical-form.md).
6.  In the **Country** field, select the name of the country.

    Enter the **Part number** that aligns with the 3E service providers if its available.

7.  Select **Submit**.


## Result

When the **Create chemical** form is,

-   Submitted through the **Automatically** tab in the form, the chemical record is filled automatically and its related lists are pre populated with information from the 3E database.
-   Submitted through the **Manually** tab in the form, the chemical record is created with the fields to be filled manually.

The **Chemical hazard identification**, **Chemical ingredients**, **Chemical ingredients**, **Chemical items**, **Risk assessments**, **Documents**, and **Service provider requests** tabs appear for this chemical record.

The new chemical record is added to the **Chemicals** list in the **Environmental Management** list view.

## What to do next

To complete the chemical record manually,

-   In the **Details** tab, fill in the form. For more information, see [Chemical form](../reference/hs-chemical-form.md).
-   In the **Chemical hazard identification** tab, select **New**. In the **Chemical hazard identification** form, select the hazard category, hazard statements, and precautionary statements.
-   In the **Chemical ingredients** tab, select **New** to add the name of the substance, its concentration, and function. For more information, see [Chemical ingredient form](../reference/hs-chemical-ingredient-form.md). If the substance does not exists in the chemical ingredient form, select **Create substance** to create a record under the **Substance** list in the **Environmental Management** list view.
-   In the **Chemical items** tab, update information about the chemical such as the responsible group, contact person, storage conditions. For more information, see [Chemical item form](../reference/hs-chemical-item-form.md).
-   In the **Risk assessments** tab, add existing risk assessments or select **New** to create risk assessment. For more information, see [Risk assessment form](../../hs-risk-management/reference/hs-risk-assessment-form.md).
-   In the **Documents** tab, select **Add** to add existing Health and Safety documents or select **New** to create a Health and Safety document. For more information, see [Add a new Health and Safety related document](../../ohs-incident-management/task/add-hs-related-document.md). The chemical safety data sheet can also be requested from this tab. For more information, see [Request a safety data sheet \(SDS\)](hs-request-safety-data-sheet-sds.md).
-   In the actions tab, select **New** to add any actions for the safety meeting. For more information, see [Health and Safety action form](../../ohs-incident-management/reference/hs-action-form.md)
-   The **Service provider requests** tab displays the requests submitted to the 3E service provider.

**Note:** The sync option can be used on any related list in a chemical record to obtain information from the 3 E database. For more info, see [Sync chemical information with the 3E database](hs-sync-chemical-data-with-3E.md).

**Parent Topic:**[Chemical management](../concept/hs-using-chemical-management.md)

