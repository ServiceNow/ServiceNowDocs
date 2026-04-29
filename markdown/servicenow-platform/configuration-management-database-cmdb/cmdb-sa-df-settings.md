---
title: CMDB and Data Foundations settings assessed in the CMDB success advisor
description: The Configuration Management Database \(CMDB\) and Data Foundations settings review provides a configuration-level assessment of the CMDB configuration item \(CI\) classes for your principal classes to support data quality, life cycle management, and integration accuracy.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Analyze CMDB settings, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB and Data Foundations settings assessed in the CMDB success advisor

The Configuration Management Database \(CMDB\) and Data Foundations settings review provides a configuration-level assessment of the CMDB configuration item \(CI\) classes for your principal classes to support data quality, life cycle management, and integration accuracy.

## Settings overview

Each setting is checked for alignment with suggested business rules, reconciliation guidelines, and Data Manager policy coverage.

<table id="table_obb_mh2_dgc"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI creation from assets using IRE

</td><td>

Enables the automatic creation of a CI from an asset record using the CMDB Identification and Reconciliation Engine \(IRE\) for CI classes identified by serial number and without dependent relationships. Requires the relevant business rule to be active for CI creation to occur during asset insertion.

</td></tr><tr><td>

Review reconciliation rules

</td><td>

Evaluates whether reconciliation rules correctly assign attribute ownership to the authoritative integration source for each principal CI class. Helps prevent lower-quality integration sources from overwriting high-quality CI attribute data, maintaining accuracy and consistency across the CMDB.

</td></tr><tr><td>

Review CMDB Data Manager policies

</td><td>

Assesses the configuration of CMDB Data Manager policies, including archive, attestation, certification, delete, and retire, for your principal classes. Each policy type manages a specific life cycle action:-   **Archive**

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


[Administer CMDB Data Manager](../../configuration-management/concept/administer-data-manager.md)

