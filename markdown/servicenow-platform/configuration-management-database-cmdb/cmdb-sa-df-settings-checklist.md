---
title: Settings checklist for Data Foundations in CMDB success advisor
description: Use this checklist to review Configuration Management Database \(CMDB\) and Data Foundations settings in CMDB success advisor that directly affect Data Foundations data quality, configuration item \(CI\) to asset synchronization, and life cycle alignment.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-08-08"
reading_time_minutes: 1
breadcrumb: [Analyze CMDB settings, Use Data Foundations advisor, CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Settings checklist for Data Foundations in CMDB success advisor

Use this checklist to review Configuration Management Database \(CMDB\) and Data Foundations settings in CMDB success advisor that directly affect Data Foundations data quality, configuration item \(CI\) to asset synchronization, and life cycle alignment.

## CMDB and Data Foundations settings checklist

Confirm that each setting is configured to support accurate and complete CI data for your principal classes in the CMDB.

|Select|Check item \(field\)|Description|Action|
|------|--------------------|-----------|------|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|CI creation from assets using IRE|Enables the automatic creation of a CI from an asset record using the CMDB Identification and Reconciliation Engine \(IRE\) for CI classes identified by serial number and without dependent relationships.|Verify that the rule is active for all applicable principal classes.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Review reconciliation rules|Evaluates whether reconciliation rules correctly assign attribute ownership to the authoritative integration source for each principal CI class, preventing lower-quality sources from overwriting high-quality data.|Update reconciliation rules to ensure the most authoritative source owns each CI attribute.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Review CMDB Data Manager policies|Assesses the configuration of Data Manager policies, including archive, attestation, certification, delete, and retire, for your principal classes.|Enable and configure appropriate policies for all principal classes.|

## Final validation

Once all settings checks are complete:

-   The business rule for CI creation from assets using IRE is `Active` for applicable principal classes.
-   Reconciliation rules are configured to protect high-quality CI attribute data from being overwritten by lower-quality sources.
-   Data Manager policies are configured for all principal classes.
-   No `Requires attention` status is displayed for any setting in the **Settings** tab.

