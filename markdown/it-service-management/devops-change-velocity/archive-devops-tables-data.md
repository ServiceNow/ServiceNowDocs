---
title: Data archiving rules for DevOps tables
description: Base system table archiving rules ensure that DevOps data stored in the Configuration Management Database \(CMDB\) are systematically archived and purged.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Data archiving rules for DevOps tables

Base system table archiving rules ensure that DevOps data stored in the Configuration Management Database \(CMDB\) are systematically archived and purged.

## Archiving rules for DevOps data in CMDB tables

Data archiving involves managing table size growth and archiving old data. It moves data that is no longer needed every day from primary tables to a set of archive tables. For more information, see [Data archiving](https://www.servicenow.com/docs/access?context=c_ArchiveData&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). Base-system archive rules are configured to auto-archive DevOps tables that are older than a specified period. An archive table is created for any table that has an archive rule associated with it. You can also choose to restore data from archive tables.

**Note:** While you can restore any record from the archive tables. Once archived data is restored, the same data is no longer auto-archived. For more information, see [Managing archived data](https://www.servicenow.com/docs/access?context=managing-archived-data&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

-   Navigate to **System Archiving** &gt; **Archive Rules** and select the individual archive rule whose data you restored.
-   Enable the **Auto rearchive** check box, to resume auto-archiving for that archive rule.

## Modify base system value for archive rules

You can configure the auto archive duration for all the archive rules that are applicable to DevOps tables from the **Auto archive \(in months\)** DevOps system property. By default, this property's value is set to 9 \(months\). Navigate to **DevOps** &gt; **Administration** &gt; **Properties** &gt; **Auto archive \(in months\)**, to modify the value. For more information on configuring data archiving, see [Create an archive rule](https://www.servicenow.com/docs/access?context=t_CreateAnArchiveRule&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

The following list indicates the tables that are auto-archived.

|Table|Table Name|Archived table name|
|-----|----------|-------------------|
|Artifact Staged Request|sn\_devops\_artifact\_staging|ar\_sn\_devops\_artifact\_staging|
|Artifact Version|sn\_devops\_artifact\_version|ar\_sn\_devops\_artifact\_version|
|Branch|sn\_devops\_branch|ar\_sn\_devops\_branch|
|Build Test Result|sn\_devops\_build\_test\_result|ar\_sn\_devops\_build\_test\_result|
|Build Test Summary|sn\_devops\_build\_test\_summary|ar\_sn\_devops\_build\_test\_summary|
|Callback|sn\_devops\_callback|ar\_sn\_devops\_callback|
|Commit|sn\_devops\_commit|ar\_sn\_devops\_commit|
|Commit Details|sn\_devops\_commit\_details|ar\_sn\_devops\_commit\_details|
|Deployed Artifact to TaskExecution|sn\_devops\_m2m\_artifact\_execution|ar\_sn\_devops\_m2m\_artifact\_execution|
|Artifact Version to Commit|sn\_devops\_m2m\_artifact\_version\_commit|ar\_sn\_devops\_m2m\_artifact\_version\_commit|
|Branch To Commit|sn\_devops\_m2m\_branch\_commit|ar\_sn\_devops\_m2m\_branch\_commit|
|Run Commit|sn\_devops\_m2m\_commit\_execution|ar\_sn\_devops\_m2m\_commit\_execution|
|Commit To Work Item|sn\_devops\_m2m\_commit\_work\_item|ar\_sn\_devops\_m2m\_commit\_work\_item|
|Pipeline Execution|sn\_devops\_pipeline\_execution|ar\_sn\_devops\_pipeline\_execution|
|Software Quality Scan Summary|sn\_devops\_software\_quality\_scan\_summary|ar\_sn\_devops\_software\_quality\_scan\_summary|
|Software Quality Scan Summary Relations|sn\_devops\_software\_quality\_scan\_summary\_relations|ar\_sn\_devops\_software\_quality\_scan\_summary\_relations|
|Step Execution|sn\_devops\_step\_execution|ar\_sn\_devops\_step\_execution|
|Tag|sn\_devops\_tag|ar\_sn\_devops\_tag|
|Task Execution|sn\_devops\_task\_execution|ar\_sn\_devops\_task\_execution|
|Task Summary|sn\_devops\_test\_summary|ar\_sn\_devops\_test\_summary|
|Test Summary Relations|sn\_devops\_test\_summary\_relations|ar\_sn\_devops\_test\_summary\_relations|
|Work Item|sn\_devops\_work\_item|ar\_sn\_devops\_work\_item|

The data archiving rules feature considers and honors parent rules before individual archive rules are run. If you have an associated parent archive rule, the child rules are run only when the parent rules are run. Similarly, when you modify individual rules, you must first disable or disassociate the parent archive rule, make the configuration changes, and re-enable the parent archive rule. Changes to the **Auto archive \(in months\)** DevOps property overrides any configuration changes made to the duration of child archive rules. For example, you could update the archive rule condition for any of the **Active** DevOps archive rules to a custom value, say three months instead of the default 9 months. However, if you modify the **Auto archive \(in months\)** DevOps property, all modifications made to the conditions of individual archive rules are overwritten by the value in the **Auto archive \(in months\)** system property.

**Note:** The override function is binding for all scenarios except:

-   When an archive rule does not belong to the DevOps scope.
-   When an archive rule belongs to the DevOps scope but is inactive.

## Base system destroy rules for DevOps data

Base-system destroy rules are also enabled and activated on all the archived DevOps tables. By default, data is deleted from an archived table after 36 months or 1095 days have passed from the time the data is stored in the archive table. For more information, see [Create a destroy rule](https://www.servicenow.com/docs/access?context=t_CreateAnArchiveRule&version=yokohama&pubname=yokohama-platform-administration&section=t_CreateADestructionRule&ft:locale=en-US).

**Parent Topic:**[Managing DevOps Change Velocity](using-devops-change-velocity.md)

