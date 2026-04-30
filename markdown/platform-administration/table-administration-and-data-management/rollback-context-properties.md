---
title: Rollback context properties
description: Change the default expiration period for different types of rollback context records.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Roll back and delete recovery, Tables and data, Configure core features, Administer]
---

# Rollback context properties

Change the default expiration period for different types of rollback context records.

Because rollback contexts contain a significant amount of data, they're deleted after 10 days by default. The Clean Expired Rollback Contexts scheduled job runs daily to delete expired records in the Rollback Context \[sys\_rollback\_context\] table. If you need to retain a rollback context for more than 10 days, you can do so by adding a system property.

To add a system property, navigate to the System Properties \[sys\_properties\] table and add a property for the type of rollback context record that you want to preserve. You can determine which property to add for a given rollback context by matching the property name to the Type column on the Rollback Context \[sys\_rollback\_context\] table.

<table id="table_okp_mc3_l1c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

The number of days to retain the rollback context for an app install

 `glide.rollback.expiration_days_app_install`

</td><td>

By default, you have 15 days to roll back an application installed from the ServiceNow® Store before the rollback context expires. You can extend the expiration period by updating this property.-   Type: integer
-   Default value: 15

</td></tr><tr><td>

The number of days to retain the rollback context for a batch app install

 `glide.rollback.expiration_days_batch_app_install`

</td><td>

By default, you have 10 days to roll back apps installed using the Batch Installation feature before the rollback context expires. You can change the expiration period by adding this property and setting a new value.-   Type: integer
-   Default value: 10

</td></tr><tr><td>

The number of days to retain the rollback context for demo data

 `glide.rollback.expiration_clean_demo_data`

</td><td>

By default, you have 10 days to roll back before the rollback context expires. You can change the expiration period by adding this property and setting a new value.-   Type: integer
-   Default value: 10

</td></tr><tr><td>

The number of days to retain the rollback context for recorded delete operations

 `glide.rollback.expiration_days_delete`

</td><td>

By default, you have 10 days after a delete operation completes to roll back before the rollback context expires. You can change the expiration period by adding this property and setting a new value.-   Type: integer
-   Default value: 10

</td></tr><tr><td>

The number of days to retain the rollback context created for validating Workflow Studio flow execution before and after an upgrade

 `glide.rollback.expiration_days_flow`

</td><td>

By default, you have 10 days to roll back before the rollback context expires. You can change the expiration period by adding this property and setting a new value.-   Type: integer
-   Default value: 10

</td></tr><tr><td>

The number of days to retain the rollback context for IRE changes recorded from CMDB Integration Studio.

 `glide.rollback.expiration_days_inst_preview`

</td><td>

By default, you have 10 days after IRE changes are recorded from CMDB Integration Studio to roll back before the rollback context expires. You can change the expiration period by adding this property and setting a new value.-   Type: integer
-   Default value: 10

</td></tr><tr><td>

The number of days to retain rollback contexts in which the Type is set to Other.

 `glide.rollback.expiration_days_other`

</td><td>

By default, you have 10 days to roll back before the rollback context expires. You can change the expiration period by adding this property and setting a new value.-   Type: integer
-   Default value: 10

</td></tr><tr><td>

The number of days to retain the rollback context for a plugin activation

 `glide.rollback.expiration_days_plugin`

</td><td>

By default, you have 15 days to roll back plugins activated in Application Manager before the rollback context expires. You can extend the expiration period by updating this property.-   Type: integer
-   Default value: 15

</td></tr><tr><td>

The number of days to retain the rollback context for an anonymization job.

 `glide.rollback.expiration_days_redact`

</td><td>

By default, you have 10 days after data is redacted by a Data anonymization job to roll back before the rollback context expires. You can change the expiration period by adding this property and setting a new value.-   Type: integer
-   Default value: 10

</td></tr><tr><td>

The number of days to retain the rollback context for a background script execution

 `glide.rollback.expiration_days_scripts_bg`

</td><td>

By default, you have 10 days to roll back script execution before the rollback context expires. The rollback context tracks all INSERT, DELETE, and UPDATE statements executed by the script and recovers the data by undoing the SQL statements. You can extend the expiration period by updating this property.-   Type: integer
-   Default value: 10

</td></tr><tr><td>

The number of days to retain the rollback context for changes recorded during test executions

 `glide.rollback.expiration_days_test_execution`

</td><td>

By default, you have 10 days after test execution to roll back before the rollback context expires. You can change the expiration period by adding this property and setting a new value.-   Type: integer
-   Default value: 10

</td></tr><tr><td>

The number of days to retain the rollback context for an upgrade

 `glide.rollback.expiration_days_upgrade`

</td><td>

By default, you have 10 days after the latest upgrade to roll back the upgrade before the rollback context expires. You can change the expiration period by adding this property and setting a new value.-   Type: integer
-   Default value: 10

</td></tr></tbody>
</table>**Parent Topic:**[Roll back and delete recovery](../concept/rollback-delete-recovery.md)

