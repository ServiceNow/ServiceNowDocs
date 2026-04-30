---
title: Migrate and sync existing data to the CSDM framework
description: You complete several tasks to ensure that your existing application data migrates successfully to the required tables in the CMDB.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Migrate and sync existing data to the CSDM framework

You complete several tasks to ensure that your existing application data migrates successfully to the required tables in the CMDB.

## Before you begin

Role required: admin

## About this task

**Keep the following points in mind:**

-   Some CSDM tables have been introduced recently so you might not be familiar with them. See the documentation for your product to learn about unfamiliar tables.
-   You can continue to use customized or non-conforming CMDB tables. If you do so, however, you might not get the full benefit of your products.
-   Be sure to use the migration tools that are described in [Assistance with the CSDM life-cycle sync process](../concept/csdm-migrate-tools.md).

**Manage the attributes that you are using.** Rationalize your custom attributes. Use the following guidelines to decide whether you really need to keep all customizations:

-   Preferred: The custom attribute doesn't have a related base-system attribute but you need to use it.
-   Keep: The custom attribute doesn't have a related base-system attribute but it's required for a unique use case.
-   Refactor: The custom attribute does have a base-system attribute or a capability that can be migrated.
-   Do Not Need: The customization is no longer needed. Delete the attributes that you don’t use or use only rarely. Consider deleting attributes if there’s a better way to address a use case.

**Consider related dependencies.** Moving configuration items \(CIs\) to a new table doesn't automatically move related dependencies. To identify related dependencies, use the scripts described in [Migrating into CSDM identifying table dependencies](https://community.servicenow.com/community?id=community_article&sys_id=a777f564db9dbfc4d58ea345ca961996) \(available on the [ServiceNow Community](https://community.servicenow.com/community)\).

**Important:** The script only identifies the dependencies — it doesn't move your data or their dependencies. You refactor data and dependencies as part of the migration.

After running the scripts and evaluating the data, you will have a better idea of the effort required to migrate your data. Decide whether you need all referenced reports, rules, and scripts. Then decide what you want to migrate and make a migration plan.

![Steps in the migration workflow.](../image/migration-path.png "Migration workflow")

## Procedure

1.  Back up your data.

    Export your data \(with all attributes\) to Excel and keep the file in a secure location. Have a contingency plan in case issues arise.

2.  Map the attributes.

    Identify the table where the data should go. Make sure that destination table has the required base-system attributes. Rationalize your custom attributes. Decide which customizations you will keep.

3.  Move CIs from existing classes to CMDB classes.

    **Note:** Don’t forget about non-conforming tables and their dependencies. You could have hundreds of reports, business rules, scripts, table references, and more that need the data in your non-conforming tables.

    Moving CIs to a new table does not automatically move reports, business rules, and so on. As described in the following steps, the fix script identifies dependencies that you need to refactor. You can [download the fix script](https://community.servicenow.com/community?id=community_article&sys_id=a777f564db9dbfc4d58ea345ca961996) from the ServiceNow Community.

4.  Refactor the attributes.

    Solidify the data model and get the data ready for migration.

    Make sure you have completed the attribute mapping-related tasks described in earlier steps. Follow the guidelines and refactor your data as needed.

5.  Migrate the data.

    **Note:** Make sure that you have a valid and recent backup. Make another backup if necessary. During migration, you lose all customized or base-system attributes that are not in the same table hierarchy.

    Keep these points in mind as you proceed:

    -   Migrate your CIs to the new class to move the CI and all its related objects, incidents, and changes to the new table.
    -   Start with a few CIs and increase the number when you feel comfortable.
6.  Remediate your table dependencies:

    1.  Modify reports to use the new table.

    2.  Migrate business rules and scripts as needed.

    3.  Update table references as needed.

7.  Reload data into the new attributes using the backup that you made earlier.

8.  Validate all data and dependencies.


## Result

You've successfully migrated your application to the CSDM framework, and your data is in the required CMDB locations.

-   **[Assistance with the CSDM life-cycle sync process](../concept/csdm-migrate-tools.md)**  
Several features help you to ensure accuracy and completeness for the process of syncing legacy data with life-cycle data in the CSDM framework.
-   **[Legacy status values that are auto-updated](../reference/csdm-lifecycle-status-auto-updated.md)**  
Several legacy statuses are automatically mapped to the **Life Cycle Stage** and **Life Cycle Stage Status** fields.

**Parent Topic:**[Configuring CSDM](../concept/configure-csdm.md)

