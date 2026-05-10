---
title: Populate the Type field in relationship tables using the fix script
description: Leverage the fix script to add and manage the Type field in relationship tables. This script simplifies data mapping and enhances record consistency across the base system.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Create related party configurations, Configuring customer access management, User management, Set up your environment, Configure, Customer Service Management]
---

# Populate the Type field in relationship tables using the fix script

Leverage the fix script to add and manage the **Type** field in relationship tables. This script simplifies data mapping and enhances record consistency across the base system.

## Before you begin

Role required: admin

## About this task

Starting with the Yokohama release, a new optional **Type** field is added to the account team member \[sn\_customerservice\_team\_member\] table, which previously included the fields **Account**, **User**, and **Responsibility**. This fix script applies to all relationship tables in the base system.

The **Type** field references the related party configuration \[sn\_customerservice\_related\_party\_configuration\]​ table, a metadata table that enables administrators to define a **Type Configuration** for each responsibility. This field enables administrators to assign meaningful business names to responsibilities, reducing duplication. By internally referencing the same responsibility, the **Type** field simplifies data management and improves record consistency.

You can use the following procedure to populate the **Type** field using the fix script.

## Procedure

1.  Identify distinct Responsibility values in the relationship table that you want to update.

2.  Create corresponding Type Configuration records in the related party configuration \[sn\_customerservice\_related\_party\_configuration\]​ table.

3.  Run the following fix script to populate the **Type** field.

    ```
    fixRelatedPartyTypeField(String tableName, String appliesTo, String entityType, String typeField, String responsibilityField)
    /**
    	 * Fixes the related party type field in the specified table.
    	 *
    	 * @param tableName  The name of the table to update.
    	 * @param appliesTo  The value for the applies_to field.
    	 * @param entityType The value for the entity_type field.
    	 * @param typeField  The name of the type field to update. If null, defaults to FIELD_TYPE.
    	 * @param responsibilityField The name of the responsibility field to update. If null, defaults to FIELD_RESPONSIBILITY.
    	 */
    ```


## Result

The fix script:

-   Automatically populates the **Type** field for matching records in the selected relationship table.
-   Maps existing responsibilities to their corresponding Type Configuration records.
-   Processes updates in batches for optimized performance.
-   Logs updates for reference.

**Note:** For large record volumes, run the fix script during system downtime to avoid performance impacts.

You can manually populate the **Type** field by navigating to the related party configuration \[sn\_customerservice\_related\_party\_configuration\]​ table and creating Type Configuration records for each distinct responsibility.

## Example

Suppose that you want that to populate the **Type** field in the account team member \[sn\_customerservice\_team\_member\] table, where the table uses the following responsibilities:

-   Account Manager 1
-   Account Manager 2
-   Account Manager 3

1.  Navigate to the related party configuration \[sn\_customerservice\_related\_party\_configuration\]​ table.
2.  Create three Type Configuration records, one for each responsibility.
3.  Run the fix script that automatically:
    -   Maps each responsibility to its corresponding **Type**.
    -   Populates the **Type** field for all records in the account team member \[sn\_customerservice\_team\_member\] table.

