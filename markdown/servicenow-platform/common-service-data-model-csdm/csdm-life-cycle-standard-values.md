---
title: Enabling life-cycle sync from legacy-to-asset
description: You can align life-cycle values for each product instance on the asset, CI, and IBI tables. A one-time process moves legacy status values for asset and CI across the platform to standard CSDM life-cycle value pairs \(life cycle stage and life cycle stage status\). Business rules then run regularly to ensure identical IBI, asset, and CI life-cycle data for each product instance.Use the Life Cycle Mapping module to specify how existing legacy status values should be converted to CSDM life-cycle value pairs \(life cycle stage and life cycle stage status\). You map both asset and CI legacy status values to life-cycle value pairs.Activate life-cycle sync to migrate your legacy asset and CI status settings to the CSDM standard life-cycle value pairs. After the one-time migration process, business rules maintain sync among IBI, asset, and CI life-cycle values.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Enabling life-cycle sync from legacy-to-asset

You can align life-cycle values for each product instance on the asset, CI, and IBI tables. A one-time process moves legacy status values for asset and CI across the platform to standard CSDM life-cycle value pairs \(*life cycle stage* and *life cycle stage status*\). Business rules then run regularly to ensure identical IBI, asset, and CI life-cycle data for each product instance.

This topic provides an overview of the entire align-and-sync process.

-   Detailed instructions for running the align-and-sync process appears in [Migrate legacy asset and CI settings to CSDM life-cycle values](csdm-life-cycle-standard-values.md#).
-   A detailed reference to all sync options appears in [How life-cycle values for Asset, CI, and IBI are synced](../../csdm-implementation/reference/cmdb-asset-CI-IBI-sync-options.md).

**Tip:** Terms used in this document are defined in [CSDM life-cycle terms](../reference/csdm-life-cyle-terms.md).

## Why enable CSDM life-cycle sync between CI and asset entities

When the one-time data sync operation finishes, CSDM life-cycle values for each product instance as represented in the asset and CI tables will be identical. Business rules then sync life-cycle value pairs among the asset, CI, and IBI tables. The business rules then run on regular schedules to ensure that life-cycle values for the asset, CI, and IBI tables remain aligned.

See [How life-cycle values for Asset, CI, and IBI are synced](../../csdm-implementation/reference/cmdb-asset-CI-IBI-sync-options.md).

The following products, for example, benefit from the standardized values:

-   To handle alerts appropriately, the Event Management and Operational Intelligence features need to know whether a CI is in the maintenance life cycle stage status.
-   To report cost data effectively, the Cloud Cost Management feature needs to know the CSDM life-cycle values of a CI.
-   To generate consistent tasks and workflows, the Audit Management and Compliance features need to use standard CSDM life-cycle values.

## How the mapping between legacy status values and CSDM CSDM life-cycle values is specified

A life-cycle value pair is the combination life cycle stage and life cycle stage status values for a CI, asset, or IBI over the life cycle of a product instance. The base system includes the life-cycle mapping \[life\_cycle\_mapping\] table that holds mapping rules. The default rules specify how to align common legacy status values to a CSDM life-cycle value pair. You can update and add rules as needed. \(The table is described more fully in [Life cycle mapping table](../reference/csdm-life-cyle-terms.md#section_csdm-lifecycle-mapping-table).\)

![Mapping rule that specifies the mapping between a legacy status value and the equivalent CSDM life-cycle value pair.](../../csdm-implementation/image/csdm-lifecycle-mapping-form-annota.png)

**Note:** If you are activating the CSDM \(csdm.lifecycle.migration.activated\) plugin for the first time, and you have custom states and substates for assets or CIs, then you will create and configure mapping between the custom legacy values and the CSDM life-cycle values.

## Alignment/sync process

To start the align and sync process, you select **Enable life cycle sync** on the Life cycle mapping table list page. That action sets the **csdm.lifecycle.sync.between.ci.and.asset.activated** system property to `true` and starts the following activities:

## Phase 1: Run the discrepancy check and correct all mappings

-   **The system runs the discrepancy check**

    The discrepancy check script checks all mapping rules:

    -   Verify CSDM life-cycle mapping rules for asset tables.
    -   Verify CSDM life-cycle mapping rules for CMDB CI tables.
    -   Verify legacy asset-to-CI mapping rules that appear in the alm\_hardware\_state\_mapping and alm\_asset\_ci\_state\_mapping tables.

        **Note:** For each CI that is not associated with an asset \(non-asset CI\), use CSDM mapping tables to derive the life-cycle value pair for the CI from the legacy status.

    ![Discrepancy report that lists mapping errors.](../../csdm-implementation/image/csdm-lcss-discrepancy.png)

    The script generates a discrepancy report. The report displays the list of missing or inactive mappings that you need to repair before you can perform bulk alignment of life-cycle values.

    -   Legacy status values that aren't yet mapped to life-cycle value pairs.
    -   Legacy status values that aren't included in a mapping rule or that are included in an inactive rule.
    -   Custom legacy status values. For each custom value, the system adds a record to the life\_cycle\_mapping table. Those mapping records, however, are inactive because some required field values are not yet set. You will edit and activate those records so all custom legacy status values will be aligned.
    -   After the one-time alignment, legacy status values between CI and asset will be auto-synced. The report therefore identifies hardware statuses or install statuses that are not present or that are included in an inactive mapping rule between asset and CI.
-   **Manual process: If there are mapping errors, add or update mappings**

    Add missing mapping rules and ensure that current rules are correct and active. The buttons open mapping tables where you can update mapping rules. Instructions for updating individual rules appear in [Map legacy status values to CSDM life-cycle values](csdm-life-cycle-standard-values.md#).

-   **Run the discrepancy check again**

    Run the discrepancy check and fix errors until all errors are fixed.


## Phase 2: Automated bulk alignment: Align all legacy CMDB CI and asset data to CSDM life-cycle value pairs

When all mapping errors are fixed, a scheduled job in the batch process performs one-time-only bulk alignment to *life cycle stage* and *life cycle stage status* life-cycle value pairs.

During bulk alignment, the process uses the mapping rules to derive the CSDM life-cycle value pair from legacy status values for both asset and CMDB CI records. During the process, the **Activate** button is disabled and you are blocked from updating mapping rules.

**Note:** IBI records do not change. Active sync between legacy and life-cycle values for IBI records is already in place.

![Overall flow of the one-time bulk alignment of legacy status data to CSDM life-cycle value pairs.](../../csdm-implementation/image/csdm-legacy-to-lcss-migration.png)

-   **Step 1: For all assets that do not have life-cycle value pairs, generate the values**

    Use the CSDM life-cycle mapping rules for asset tables to derive the life-cycle value pairs from the legacy status values.

-   **Step 2: One-time sync: For each CI whose CSDM life-cycle values do not match the asset values, update the CI with the asset values**

    This one-time sync will not be repeated because in one of the following phases, bi-directional sync is implemented between CI life-cycle value pairs and asset life-cycle value pairs.

-   **Step 3: One-time sync: If a CI is not associated with an asset, use CSDM mapping tables to derive the CI's life-cycle values from the legacy status.**

    This one-time sync will not be repeated because bi-directional sync continues between CI legacy values and asset legacy values. Future CI values will derive from the new bi-directional sync between asset and CI life-cycle value pairs.


## Phase 3: Automated update to sync operations

![Updates to sync operations.](../../csdm-implementation/image/csdm-lcss-new-sync.png)

-   **New: Activate sync of life-cycle data between asset and CMDB CI**

    CSDM life-cycle value pairs are bi-directionally synced between asset and CI.

-   **New: Deactivate Bi-directional sync between CMDB CI legacy values and CSDM life-cycle values**

    As a result, changes to CI legacy values will not update CSDM life-cycle value pairs \(the values will diverge over time\). Instead, CSDM life-cycle value pairs are updated by the bi-directionally sync with asset life-cycle value pairs. A report on the CSDM dashboard lists CIs whose life-cycle values diverge from legacy values.

-   **No change: Sync between asset legacy values and CI legacy values**

    The existing bi-directional sync between asset legacy values and CI legacy values continues.

-   **\(No change if sync is currently active\): Activate sync between asset legacy and asset life-cycle values.**

    Bi-directional sync between asset legacy values and life-cycle value pairs continues.


## Phase 4: Ongoing automated sync operations

![Ongoing sync of all CSDM life-cycle values.](../../csdm-implementation/image/csdm-lcss-ongoing-sync.png)

Immediately after sync operations are completed, business rules run to align life-cycle value pairs in the asset, CI, and IBI tables for each product instance. Business rules then run on a regular schedule to incorporate changes to legacy status values as updates to life-cycle value pairs and to maintain alignment among Asset, CI, and IBI.

## Activate life-cycle alignment and sync

Instructions [Migrate legacy asset and CI settings to CSDM life-cycle values](csdm-life-cycle-standard-values.md#)

**Parent Topic:**[Implementing the CSDM framework in stages](../../csdm-implementation/concept/csdm-implementation-stages.md)

## Map legacy status values to CSDM life-cycle values

Use the Life Cycle Mapping module to specify how existing legacy status values should be converted to CSDM life-cycle value pairs \(**life cycle stage** and **life cycle stage status**\). You map both asset and CI legacy status values to life-cycle value pairs.

### Before you begin

Role required: itil\_admin or asset\_admin

### About this task

Several legacy statuses are automatically mapped to the **Life Cycle Stage** and **Life Cycle Stage Status** fields. For more information, see [Legacy status values that are auto-updated](../../csdm-implementation/reference/csdm-lifecycle-status-auto-updated.md).

Because the base system includes a large number of default mappings, you might not have to create many custom mappings. To view the list of default mappings, navigate to **All** &gt; **CSDM** &gt; **Life Cycle Mapping**.

**Tip:** Terms used in this document are defined in [CSDM life-cycle terms](../reference/csdm-life-cyle-terms.md).

In the following example, your existing data uses a status attribute named **Install Status** for hardware CIs. You configure the Life cycle mapping form to map the existing **Pending Install** value of the **Install Status** attribute to the **Deploy/Test** life-cycle value pair in the CMDB.

![Map existing legacy values to CSDM life-cycle values.](../../csdm-implementation/image/csdm-lifecycle-mapping-form.png)

### Procedure

1.  Navigate to **All** &gt; **CSDM** &gt; **Life Cycle Mapping**.

2.  On the Life cycle mappings list view, select **New** and then fill in the Life cycle mapping form as described in [Life cycle mapping form](../reference/csdm-life-cycle-mapping-form.md).

3.  Select **Submit**.

4.  Repeat the process and, when you have mapped all legacy status values, migrate them to the CMDB.

    For instructions, see [Migrate legacy asset and CI settings to CSDM life-cycle values](csdm-life-cycle-standard-values.md#).


## Migrate legacy asset and CI settings to CSDM life-cycle values

Activate life-cycle sync to migrate your legacy asset and CI status settings to the CSDM standard life-cycle value pairs. After the one-time migration process, business rules maintain sync among IBI, asset, and CI life-cycle values.

### Before you begin

**Tip:** Terms used in this document are defined in [CSDM life-cycle terms](../reference/csdm-life-cyle-terms.md).

Before you enable life-cycle sync, navigate to **CSDM** &gt; **Life Cycle Mapping**. Review the prepopulated mappings in the **Life Cycle Mappings** list view:

-   Adjust and add any mappings as needed for your environment.
-   Review mappings for any custom status values. Those mappings are incomplete and you must provide the desired standard life cycle control to map to.
-   Ensure that all mappings are configured with a life cycle control.
-   Ensure that all mappings are activated.

Activation can proceed only if the following conditions apply:

-   All mapping records are set to active and are configured with a life cycle control
-   All mapping records for custom legacy values are fully configured.

Role required: itil\_admin or asset\_admin

### Procedure

1.  Navigate to **CSDM** &gt; **Life Cycle Mapping**.

2.  On the **Life Cycle Mappings** list view, select **Enable life cycle sync** on the Life cycle mapping table list page.

    That action sets the **csdm.lifecycle.sync.between.ci.and.asset.activated** system property to `true` and runs a script that validates mappings. The script generates a discrepancy report. The report displays the list of missing or inactive mappings that you need to repair before you can perform bulk alignment of life-cycle values.

3.  Select an item on the report to access the mappings that need attention, correct the mappings, and then select **Refresh** to run the report again.


### Result

One-time sync is done. All cmdb\_ci and asset records should have *life cycle stage* and *life cycle stage status* values, either coming directly from what the asset had \(if you have an asset/CI combo\), or from the life cycle mapping table directly for non-asset CIs.

Business rules now perform ongoing alignment of life-cycle data as described in [Enabling life-cycle sync from legacy-to-asset](csdm-life-cycle-standard-values.md#).

### What to do next

After the data has migrated successfully, you can start managing data following the CSDM model:

1.  [Activate the CSDM Activation \(com.snc.cmdb.csdm.activation\) plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
2.  Use the [CMDB Data Manager](cmdb-data-management.md) to centrally govern the life cycle of CIs in bulk and in a standard and consistent way.

