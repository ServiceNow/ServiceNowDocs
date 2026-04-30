---
title: Analyze CMDB settings for HAM
description: Monitor and optimize Configuration Management Database \(CMDB\) settings that support configuration item \(CI\) to hardware asset synchronization, life cycle alignment, and Hardware Asset Management \(HAM\) data quality.Identify and evaluate settings including Hardware Asset Management \(HAM\) business rules, configuration item \(CI\) to asset field mappings, hardware model categories, and CMDB Data Manager policies that support synchronization and automation between hardware assets and CIs.The Configuration Management Database \(CMDB\) and Hardware Asset Management \(HAM\) settings review provides a configuration-level assessment of the CMDB configuration item \(CI\) classes and HAM assets for maintaining data accuracy.Use this checklist to review Configuration Management Database \(CMDB\) and Hardware Asset Management \(HAM\) settings in CMDB success advisor that directly affect HAM data quality, configuration item \(CI\) to asset synchronization, and life cycle alignment.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-08-07"
reading_time_minutes: 8
breadcrumb: [Use HAM advisor, CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyze CMDB settings for HAM

Monitor and optimize Configuration Management Database \(CMDB\) settings that support configuration item \(CI\) to hardware asset synchronization, life cycle alignment, and Hardware Asset Management \(HAM\) data quality.

Use the **Settings** tab in the CMDB success advisor for HAM to review configuration indicators and identify opportunities to improve CMDB alignment with HAM guidelines.

The CMDB success advisor for HAM evaluates your current configuration across key areas such as:

-   Automatic asset and CI creation
-   Field and model category mappings
-   CI state and substate usage
-   CMDB Data Manager policy coverage

Settings are categorized as `Ideal` or `Requires attention`, enabling you to prioritize actions and maintain a healthy CMDB for HAM.

For a quick reference to validate CMDB settings for HAM, see [Settings checklist for HAM in CMDB success advisor](cmdb-sa-ham-analyze-settings.md#).

## Access settings

Navigate to the CMDB success advisor landing page and for the HAM card, select **View insights**. Select the **Settings** tab to access settings-related details. For more information, see [Access CMDB success advisor](../task/cmdb-sa-access.md).

**Note:** The CMDB success advisor for HAM dashboard is available only after the setup process is complete. For more information, see [Set up CMDB success advisor for HAM](cmdb-sa-ham-config-settings.md).

## Required roles

You need the sn\_cmdb\_admin role to access the CMDB success advisor for HAM.

To manage business rules, change the application scope from CMDB success advisor to Global in the [application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Use cases

For examples of how different people in your organization would use this feature, see these use cases.

<table id="table_lnc_zz1_2gc"><thead><tr><th>

User

</th><th>

Feature use

</th></tr></thead><tbody><tr><td>

CMDB administrator

</td><td>

-   Improve the accuracy of asset reconciliation by aligning CI and asset record creation.
-   Promote consistent asset life cycle management through status field alignment across asset and CI records.
-   Automate policy-based workflows for asset retirement, deletion, certification, or archival using policy-driven rules.
-   Standardize hardware model categories to improve normalization processes and reporting accuracy.

</td></tr></tbody>
</table>## Settings features

The **Settings** tab in the CMDB success advisor for HAM provides visibility into key configuration areas that promote accurate synchronization between hardware assets and CIs. These settings include business rules, field mappings, model categories, and Data Manager policies that support automated life cycle management and data integrity. To maintain CMDB data accuracy and HAM integration, regularly review and validate these settings. For more information, see [CMDB and HAM settings assessed in the CMDB success advisor](cmdb-sa-ham-analyze-settings.md#).

## Evaluate CMDB settings for HAM

Identify and evaluate settings including Hardware Asset Management \(HAM\) business rules, configuration item \(CI\) to asset field mappings, hardware model categories, and CMDB Data Manager policies that support synchronization and automation between hardware assets and CIs.

### Before you begin

Role required: sn\_cmdb\_admin

### Procedure

1.  Navigate to the CMDB success advisor landing page.

2.  On the HAM card, select **View insights**.

3.  Select the **Settings** tab.

4.  Select a status tile to view settings by category.

    |Tile|Description|
    |----|-----------|
    |**All**|Total number of evaluated settings.|
    |**Ideal**|Settings that follow general guidelines.|
    |**Requires attention**|Settings that are inactive, incorrectly configured, or missing.|

5.  Evaluate each setting that requires attention and use the available actions to open the related configuration pages and make updates.

<table id="choicetable_acr_fw5_ggc"><thead><tr><th align="left" id="d567959e505">

Action

</th><th align="left" id="d567959e508">

Description

</th></tr></thead><tbody><tr><td id="d567959e514">

**Manage rule**

</td><td>

Opens the configuration page for the related business rule that automates tasks between assets and CIs.

</td></tr><tr><td id="d567959e523">

**Manage model categories**

</td><td>

Opens the Model categories list page where you can select a model category to review and update mappings between asset model categories and CI classes.

</td></tr><tr><td id="d567959e532">

**Manage mappings**

</td><td>

Opens the Asset CI Field Mappings list page where you can select a CI and review and change how asset fields connect to CI fields to keep data accurate.

</td></tr><tr><td id="d567959e541">

**Manage policies**

</td><td>

Opens the Data Manager overview page where you can create or update policies for different CI classes to automate asset management.

</td></tr><tr><td id="d567959e551">

**Create policy**

</td><td>

Opens the New policy form to create a policy for a CI class. The **Create policy** action is available in the policy summary dialog box displayed after selecting the policy coverage count in the **Classes with active policies** column within the Review Data Manager policies section.

</td></tr></tbody>
</table>    **Tip:** Select **Learn more** next to a setting to open a related help topic in a new browser tab or window with additional details about that setting.

6.  To view any updated configuration status on the **Settings** tab, select the refresh icon ![](../../api-insights/image/refresh-list.png).


**Related topics**  


[Administer Data Manager in CMDB Workspace](../../configuration-management/concept/administer-data-manager.md)

[Asset and CI management](https://www.servicenow.com/docs/access?context=c_ManagingAssets&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)

[Model categories](https://www.servicenow.com/docs/access?context=c_ModelCategories&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)

## CMDB and HAM settings assessed in the CMDB success advisor

The Configuration Management Database \(CMDB\) and Hardware Asset Management \(HAM\) settings review provides a configuration-level assessment of the CMDB configuration item \(CI\) classes and HAM assets for maintaining data accuracy.

### Settings overview

Each setting is checked for alignment with suggested business rules and mapping guidelines.

<table id="table_obb_mh2_dgc"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create asset on CI insertion

</td><td>

Enables the automatic creation of an asset record when a CI is inserted into the CMDB. Requires the Create Asset on Insert business rule to be active for asset creation to occur during CI insertion.

</td></tr><tr><td>

Update asset fields on CI change

</td><td>

Enables automatic updates to asset records when a related CI is modified. Requires the Update Asset Fields on Change business rule to be active to synchronize CI changes with asset data.

</td></tr><tr><td>

Create CI on asset insertion

</td><td>

Enables the automatic creation of a configuration item when an asset record is added. Requires the Create CI on Insert business rule to be active to reflect asset data in the CMDB.

</td></tr><tr><td>

Update CI on asset update

</td><td>

Enables automatic updates to configuration item records when associated asset data is changed. Requires the Update CI Fields on Change business rule to be active to maintain data consistency.

</td></tr><tr><td>

Review custom model categories

</td><td>

Validates that custom model categories are properly mapped to predefined model categories. Verifies accurate classification, consistent reporting, and standardized data alignment.

</td></tr><tr><td>

Review asset CI field mappings

</td><td>

Evaluates whether asset fields are correctly mapped to configuration item fields using standard mappings. Helps prevent data discrepancies caused by custom or incorrect mappings.

</td></tr><tr><td>

Review asset CI install status mappings

</td><td>

Checks that CI install status values are accurately mapped to the state and substate fields of the corresponding asset record. Verifies precise life cycle tracking and status reporting.

</td></tr><tr><td>

Review asset CI hardware status mappings

</td><td>

Verifies that CI hardware status values align with the state and substate fields of the corresponding asset record. Supports consistent representation of physical asset conditions.

</td></tr><tr><td>

Review Data Manager policies

</td><td>

Assesses the configuration of CMDB Data Manager policies, including archive, attestation, certification, delete, and retire, for the selected hardware CI classes. Each policy type manages a specific life cycle action:-   **Archive**

Archives inactive CIs without deleting them.

-   **Attestation**

Validates CI data or runs automated checks.

-   **Certification**

Verifies CI data for accuracy and readiness.

-   **Delete**

Removes CIs based on defined criteria such as inactivity.

-   **Retire**

Marks CIs as retired when no longer in use.


</td></tr></tbody>
</table>**Related topics**  


[Administer Data Manager in CMDB Workspace](../../configuration-management/concept/administer-data-manager.md)

## Settings checklist for HAM in CMDB success advisor

Use this checklist to review Configuration Management Database \(CMDB\) and Hardware Asset Management \(HAM\) settings in CMDB success advisor that directly affect HAM data quality, configuration item \(CI\) to asset synchronization, and life cycle alignment.

### CMDB and HAM settings checklist

Confirm that each setting is configured to support accurate and consistent hardware asset records in the CMDB.

|Select|Check item \(field\)|Description|Action|
|------|--------------------|-----------|------|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Create asset on CI insertion|Enables the automatic creation of an asset record when a CI is inserted into the CMDB.|Verify that rule is active and set to create asset records on CI insertion.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Update asset fields on CI change|Enables automatic updates to asset records when a related CI is modified.|Verify that rule is active and correctly updates asset fields on CI change.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Create CI on asset insertion|Enables the automatic creation of a configuration item when an asset record is added.|Verify that rule is active and set to create CI records on asset insertion.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Update CI on asset update|Enables automatic updates to configuration item records when associated asset data is changed.|Verify that rule is active and correctly updates CI fields on asset changes.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Review custom model categories|Validates that custom model categories are properly mapped to predefined model categories|Map custom categories to predefined ones.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Review asset CI field mappings|Evaluates whether asset fields are correctly mapped to configuration item fields using standard mappings.|Try using predefined mappings.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Review asset CI install status mappings|Checks that CI install status values are accurately mapped to the state and substate fields of the corresponding asset record.|Try using predefined mappings.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Review asset CI hardware status mappings|Verifies that CI hardware status values align with the state and substate fields of the corresponding asset record.|Try using predefined mappings.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Review CMDB Data Manager policies|Assesses the configuration of Data Manager policies, including archive, attestation, certification, delete, and retire, for the selected hardware CI classes.|Enable and configure appropriate policies for the required CI classes.|

### Final validation

Once all settings checks are complete:

-   All business rules for automatic asset and CI creation or updates are `Active`.
-   Custom model categories are correctly mapped to predefined categories.
-   Data Manager policies are configured for all required CI classes.
-   No `Requires attention` status is displayed for any setting in the **Settings** tab.

