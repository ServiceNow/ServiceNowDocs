---
title: Analyze CMDB settings for Data Foundations
description: Monitor and optimize Configuration Management Database \(CMDB\) settings that support configuration item \(CI\) data quality, Common Service Data Model \(CSDM\) alignment, and Data Foundations outcomes.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-08-07"
reading_time_minutes: 2
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyze CMDB settings for Data Foundations

Monitor and optimize Configuration Management Database \(CMDB\) settings that support configuration item \(CI\) data quality, Common Service Data Model \(CSDM\) alignment, and Data Foundations outcomes.

Use the **Settings** tab in the CMDB success advisor for Data Foundations to review configuration indicators and identify opportunities to improve CMDB alignment with Data Foundations guidelines.

The CMDB success advisor for Data Foundations evaluates your current configuration across key areas such as:

-   CMDB Data Manager ownership policies for principal classes
-   Reconciliation rules ensuring the right integration source owns each attribute
-   CI class manager configuration for principal class designation

Settings are categorized as `Ideal` or `Requires attention`, enabling you to prioritize actions and maintain a healthy CMDB for Data Foundations.

For a quick reference to validate CMDB settings for Data Foundations, see [Settings checklist for Data Foundations in CMDB success advisor](cmdb-sa-df-settings-checklist.md).

## Access settings

Navigate to the CMDB success advisor landing page, and on the Data Foundations card, select **View insights**. Select the **Settings** tab to access settings-related details. For more information, see [Access CMDB success advisor](../task/cmdb-sa-access.md).

**Note:** The CMDB success advisor for Data Foundations dashboard is available only after the setup process is complete. For more information, see [Set up CMDB success advisor for Data Foundations](cmdb-sa-df-config-settings.md).

## Required roles

You need the sn\_cmdb\_admin role to access the CMDB success advisor for Data Foundations.

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

-   Make sure Data Manager ownership policies are configured for all principal classes
-   Verify reconciliation rules prevent lower-quality sources from overwriting high-quality CI data
-   Identify CI classes with no Data Manager policy coverage and remediate gaps
-   Align CMDB settings with CSDM to support service mapping and dependency tracking

</td></tr></tbody>
</table>## Settings features

The **Settings** tab in the CMDB success advisor for Data Foundations provides visibility into key configuration areas that promote accurate and complete CI data for your principal classes. These settings include business rules for CI creation, reconciliation rules that govern attribute ownership across integration sources, and Data Manager policies that support automated life cycle management and data integrity. To maintain CMDB data quality for Data Foundations, regularly review and validate these settings. For more information, see [CMDB and Data Foundations settings assessed in the CMDB success advisor](../reference/cmdb-sa-df-settings.md).

