---
title: Dependent CIs management
description: A life cycle update for a CI affects its dependent CIs. For example, when the CI that a dependent CI depends on is deleted, the dependent CI becomes orphan with no further use. To maintain the integrity and health of the CMDB, the system applies cascade-cleanup processes to dependent CIs that are affected by a life cycle update.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Dependent CIs management

A life cycle update for a CI affects its dependent CIs. For example, when the CI that a dependent CI depends on is deleted, the dependent CI becomes orphan with no further use. To maintain the integrity and health of the CMDB, the system applies cascade-cleanup processes to dependent CIs that are affected by a life cycle update.

For information about independent and dependent CIs, see [CMDB classifications and class dependency](c_CMDBClassifications.md).

To ensure that dependent CIs are properly managed after deleting or archiving CIs, you must:

1.  Enable dependent CIs management as described on this page.
2.  Manually approve the [CMDB Data Manager](cmdb-data-management.md) tasks that dependent CIs management generates, or configure those tasks to not require a review or an approval.

**Note:** An Orphan dependent CI in the context of Data Manager is different from an orphan CI in the context of CMDB Health. An orphan dependent CI within the context of Data Manager belongs to a dependent class, and is missing the dependent relationship. The definition of an orphan CI in the context of CMDB Health is broader, and includes any CI that matches CMDB Health orphan rules. For more information about orphan CIs in CMDB Health, see [CMDB Health KPIs and metrics](../reference/r_CMDBHealthMetrics.md).

Examples of dependent CIs needing cascade-cleanup:

-   Tomcat application \(T1\) runs on a Linux Server \(L1\) and contains a WAR file \(W1\). When L1 is deleted, T1 and W1 become orphan dependent CIs.
-   Network Adapters become orphan dependent CIs when the hardware itself is deleted.
-   A Linux Server has retired and is set with end of life, the assumption is that if the server is no longer operational then applications which depend on it shouldn’t be operational either.

## Enable dependent CIs management

To enable dependent CIs management:

-   Configure your environment for CMDB Data Manager. For details about how to configure the environment for CMDB Data Manager and the CMDB Data Manager own prerequisites, see [Working with CMDB Data Manager](cmdb-data-management.md).
-   Ensure that the **cmdb.dependent.ci.cascade.op.enabled** system property is set to **true** \(true by default\). This property enables cascade operations and doesn't exist in the base system. Therefore, to view or modify the property value, you must first add it to the System Properties \[sys\_properties\] table.
-   To enable cascade-retirement processes, ensure that the system property **cmdb.dependent.ci.cascade.retire.enabled**, which is used to manage cascade-retirement of CIs, is set to true \(false by default\). The business rule **After BR: Track “Retired” CIs**, that checks for downstream CI dependencies, runs only if this property is set to true. This property doesn't exist in the base system and to view or modify it, you must first add it to the System Properties \[sys\_properties\] table.

Cascade-cleanup operations apply only from when you enable the dependent CIs management feature. To apply cascade-cleanup to orphan dependent CIs that already existed in the CMDB before enabling the feature, see [Cascade-cleanup existing orphan dependent CIs](manage-dependent-ci.md#section_cascade-cleanup-existing-dependentCIs).

## Use of CMDB Data Manager to perform cascade-cleanup operations

Dependent CIs management processes use the [CMDB Data Manager](cmdb-data-management.md) to process the life cycle updates for the dependent CIs in the CMDB Dependent CI Ledger \[cmdb\_dependent\_ci\_ledger\] table in the following ways:

1.  Requesting and getting approvals from users for the life cycle updates for the CIs.
2.  Performing the actual delete, archive, or retire CI updates after these operations are approved.

The system generates tasks for the 'Dependent CI - Deletion', 'Dependent CI - Archive', and 'Dependent CI - Retire' Data Manager policies, with the CIs that are ready to be deleted, archived, or retired as target CIs. These policies are set with the respective 'On Demand' policy types. Then, a Data Manager admin or user, according to the **Managed By Group** setting, must review and approve these tasks before the Data Manager applies the respective subflow to the dependent CIs.

To automatically approve those tasks, use the CMDB Data Manager to clear the **Needs Review** flag of the respective Data Manager policies. Those tasks will then run without requiring any user intervention.

## Cascade-retire dependent CIs

When a CI is set to retire, dependent CIs management data processes attempt to cascade-update all the CIs depending on that CI, also to retire.

1.  CI is updated to retire as the CI’s **Life Cycle Stage** attribute is set to **End of Life** according to CSDM standards.
2.  Business rule **After BR: Track “Retired” CIs** runs \(only if the system property **cmdb.dependent.ci.cascade.retire.enabled** is **true**\) to check if the CI belongs to a class which has any downstream dependencies.

    If yes: The CI is added to the CMDB CI End Of Life Ledger \[cmdb\_ci\_end\_of\_life\_ledger\] table.

3.  For each CI in the CMDB CI End Of Life Ledger \[cmdb\_ci\_end\_of\_life\_ledger\] table, the scheduled job **CMDB Cascade Retire Dependent CIs** checks the CI’s relationships in the CI Relationship \[cmdb\_rel\_ci\] table. If there is a dependent relationship with a dependent CI, then that dependent CI is added to the CMDB Dependent CI Ledger \[cmdb\_dependent\_ci\_ledger\] table with the **Retire** action.

    For more information about dependent relationship rules, see [CMDB dependent relationship rules](c_ServiceRulesMetadata.md).

4.  Scheduled Job **CMDB DependentCI Policy Processor** runs \(if the system property **cmdb.dependent.ci.cascade.retire.enabled** is true\) to process the CIs in the CMDB Dependent CI Ledger \[cmdb\_dependent\_ci\_ledger\] table. Those CIs are set as being ready to retire upon approval using the [CMDB Data Manager](manage-dependent-ci.md#section-cmdb-datamgr-apply-cascade-cleanup). A task is created in the CMDB Data Manager against the Dependent CI Retire policy to actually retire the CIs.

## Cascade-archive dependent CIs

Archiving a CI can leave its dependent CIs as orphans in the CMDB. To prevent the accumulation of stale data, the system applies cleanup processes that cascade-archive those orphan dependent CIs.

Orphan dependent CIs are not immediately archived. When a CI is archived, all the CI relationship records for that CI in the \[cmdb\_rel\_ci\] table, are also archived. The system then checks for any dependent CIs that were orphaned as a result of this archiving. Any CIs in the dependency chain that are identified as orphan dependent CI, are checked for any of the following conditions. CIs that meet any of these conditions are not orphan dependent CIs and therefore will not be archived:

-   The CI is an unhandled duplicate CI \(the CI is associated with an unresolved de-duplication task\).
-   The CI has multiple parent CIs.
-   The CI belongs to an excluded class. Excluded classes are stored in the CMDB Dependent CI Class Exclusion \[cmdb\_dependent\_ci\_class\_exclusion\] table. In the base system, that table is pre-populated with some classes such as **cmdb\_ci\_vm**, **cmdb\_ci\_vmware\_instance**, and other VMware-related classes. You can manage the set of classes that are exempt from management of orphan dependent CIs, by adding or removing records to that table.

Eventually, only those CIs that these conditions do not apply to are added to the CMDB Dependent CI Ledger \[cmdb\_dependent\_ci\_ledger\] table. Those CIs are set as being ready for archival using the [CMDB Data Manager](manage-dependent-ci.md#section-cmdb-datamgr-apply-cascade-cleanup), upon approval.

## Cascade-delete dependent CIs

Deleting a CI can leave its dependent CIs as orphans in the CMDB. To prevent the accumulation of stale data, the system applies cleanup processes that cascade-delete those orphan dependent CIs.

1.  CI is updated to be deleted as the CI’s Life Cycle Stage attribute is set to End of Life according to CSDM standards.
2.  All relationships in the cmdb\_rel\_ci table, associated with the deleted CI, are deleted.

3.  Business rule **After BR: CMDB Dependent CI Delete** runs \(only if the system property **cmdb.dependent.ci.cascade.op.enabled** is **true**\) to check each of the deleted relationships in the CI Relationship \[cmdb\_rel\_ci\] table, whether the other CI \(parent or child\) in the relationship is an orphan dependent CI.

    If yes: Those orphan dependent CIs are added to the CMDB Dependent CI Ledger \[cmdb\_dependent\_ci\_ledger\] table and set with Action = Delete.

4.  Scheduled Job **CMDB DependentCI Policy Processor** runs \(if the system property **cmdb.dependent.ci.cascade.retire.enabled** is true\) to process the CIs in the CMDB Dependent CI Ledger \[cmdb\_dependent\_ci\_ledger\] table. Those CIs are set as being ready to be deleted upon approval using the CMDB Data Manager. A task is created in the CMDB Data Manager against the Dependent CI Delete policy to actually delete the CIs.

Orphan dependent CIs aren't immediately deleted. Prior to deleting each of the CIs relationship in the CI Relationship \[cmdb\_rel\_ci\] table, the system checks if other CI in the relationship belongs to a dependent class. Any CIs in the dependency chain that are identified as dependent on the deleted CI, are checked for any of the following conditions. CIs that meet any of these conditions aren't orphan dependent CIs and therefore aren't marked for deletion:

-   The CI is an unhandled duplicate CI \(the CI is associated with an unresolved de-duplication task\).
-   The CI has multiple parent CIs.
-   The CI belongs to an excluded class. Excluded classes are stored in the CMDB Dependent CI Class Exclusion \[cmdb\_dependent\_ci\_class\_exclusion\] table. In the base system, that table is pre-populated with some classes such as **cmdb\_ci\_vm**, **cmdb\_ci\_vmware\_instance**, and other VMware-related classes. You can manage the set of classes that are exempt from management of orphan dependent CIs, by adding or removing records to that table.

Eventually, only those CIs that these conditions don't apply to are added to the CMDB Dependent CI Ledger \[cmdb\_dependent\_ci\_ledger\] table. Those CIs are set as being ready for deletion using the [CMDB Data Manager](manage-dependent-ci.md#section-cmdb-datamgr-apply-cascade-cleanup), upon approval.

## Extraneous relationships

For the delete and archive operations, the system also tracks CIs' extraneous relationships in the Dependent CI Relations Evaluation Config \[cmdb\_dependent\_ci\_extra\_rels\_config\] table. Extraneous relationships are those relationships that aren't in the CI’s chain of dependency and deleting or archiving them depends on the value of the **cmdb.dependent.ci.extra.rel.check** system property. This property is set to **true** by default, in which case extraneous relationships aren'tt deleted or archived. You can set the property to **false** to delete and archive extraneous relationships.

The **cmdb.dependent.ci.extra.rel.check** property doesn't exist in the base system and to view or modify the property value, you must first add it to the System Properties \[sys\_properties\] table.

## Cascade-cleanup existing orphan dependent CIs

When enabling the dependent CIs management feature, the cascade-cleanup operations apply only from when the feature is enabled. However, it might be necessary to apply a similar cascade-cleanup operation to orphan dependent CIs that already existed in the CMDB before the feature was enabled.

Activate the Cleanup Orphan CIs scheduled job to perform a one-time cascade-cleanup of orphan dependent CIs across the CMDB. The Cleanup Orphan CIs scheduled job checks throughout the entire CMDB to identify any orphan dependent CIs. These CIs are then processed in the same manner that CIs that are cascade-deleted are processed. CIs that are ready to be deleted are added to the CMDB Dependent CI Ledger \[cmdb\_dependent\_ci\_ledger\] table. The CMDB Data Manager is then leveraged as described in the [Use of CMDB Data Manager to perform cascade-cleanup operations](manage-dependent-ci.md#section-cmdb-datamgr-apply-cascade-cleanup) section.

The Cleanup Orphan CIs scheduled job is intended to run only once, after which the job deactivates itself. Depending on the size of the CMDB, it might take the Cleanup Orphan CIs scheduled job several days to complete.

## Configure automatic recovery settings

You can use the system property **cmdb.dependent.ci.stale.record.cleanup.duration** to control the automatic recovery mechanism for stuck CI records in the CMDB Dependent CI Ledger \[cmdb\_dependent\_ci\_ledger\] and CMDB CI End Of Life Ledger \[cmdb\_ci\_end\_of\_life\_ledger\] tables. This property defines how many days a CI record can remain in **PROCESSING** state before being automatically reset to **NEW** for reprocessing.

About the property:

-   Type: Integer
-   Default value:
    -   For the CMDB Dependent CI Ledger table processing: 2
    -   For the CMDB CI End Of Life Ledger table processing: 1
-   Other values: The general guideline for most environments is to set the property to 1-3 days. For high-volume environments where quick recovery is critical, set to a shorter duration such as 1 day, and for environments with long-running CI processing jobs, set to a longer duration such as 3-5 days.

    **Note:** If **cmdb.dependent.ci.stale.record.cleanup.duration** is set to zero or a negative value, the system uses the default value \(2 days\). Setting too low may reset legitimately long-running processes, and setting too high may delay recovery of genuinely stuck records.


When the CMDB Data Manager processes dependent CIs \(for retire, archive, or delete operations\), the state of records is set to **PROCESSING**. If processing fails due to system errors, crashes, or timeouts, these records can become stuck and processing never completes.

The cleanup job:

1.  Identifies records in **PROCESSING** state that haven't been updated in the number of days specified in the **cmdb.dependent.ci.stale.record.cleanup.duration** property.
2.  Sets the state of those records to **NEW**.
3.  Assigns those records to the current cluster node for reprocessing.

This property is used in the following two scenarios:

-   **Dependent CI Policy Processing**
    -   Location: CMDBDataManagementPolicyProcessor.java:561-571
    -   Default: 2 days
    -   Triggered by: Scheduled job for dependent CI management policies
    -   Purpose: Cleans stuck records in the cmdb\_dependent\_ci\_ledger table
-   **End-of-Life CI Ledger Processing**
    -   Location: CMDBCiEndOfLifeLedger
    -   Processor.java:57
    -   Default: 1 day
    -   Triggered by: Scheduled job for EOL CI processing
    -   Purpose: Cleans stuck records in the CI end-of-life ledger table

For monitoring purposes, check the system logs for cleanup activity. Log messages such as "Completed cleaning cis which are stuck in processing state, updated X CIs from PROCESSING to NEW state", indicate how many records were reset from **PROCESSING** to **NEW** state.

## Sample scenario: cascade-retire

1.  Enable dependent CIs management.
2.  In CMDB Data Manager, create and publish a Retire policy. For example, retire an independent Linux Server CI with relationships to the dependent CIs Network Adapter and File System.
3.  Wait for the scheduled job **CMDB Data Manager Retire Policy Processor** to run, or run it manually.
4.  In the Data Manager overview page, select the Open task card and approve the retirement task \(Approval=Approved\). Change the state of the task to 'Work in progress' if it doesn't change automatically. This will retire the Linux Server CI and add it to the cmdb\_ci\_end\_of\_life\_ledger table.
5.  Run the scheduled job **CMDB Cascade Retire Dependent CIs**.

    This scheduled job processes each CI in the cmdb\_ci\_end\_of\_life\_ledger table, and queries the relationships in the cmdb\_rel\_ci table for this CI. If a relationship exists with other dependent CI, then those dependent CI are added to the cmdb\_dependenct\_ci\_ledger table with the settings of state = 'Ready' and action = 'Retire'.

6.  Wait for the scheduled job **CMDB DependentCI Policy processor** to run, or run it manually. This scheduled job creates a task against the OOB Dependent CI Retire policy, targeting the CIs in the cmdb\_dependenct\_ci\_ledger table.
7.  In the Data Manager overview page, select the Open task card and approve the task described with “Dependent CI – Retire..”.

**Parent Topic:**[CMDB classifications and class dependency](c_CMDBClassifications.md)

**Related topics**  


[CMDB record types](../reference/r_CMDBRecordTypes.md)

[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)

[Create a CI class](../task/t_CreateCIType.md)

[Reclassify a CI](../task/t_ManuallyReclassifyCI.md)

[Delete CIs](../task/delete-class-records-ci-class-mgr.md)

[View and edit class definitions and metadata](../task/t_ViewTableDefinitions.md)

[Update the list of classes in the Principal Class filter](../task/update-principal-class-filter.md)

