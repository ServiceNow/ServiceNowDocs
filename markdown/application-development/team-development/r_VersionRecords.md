---
title: Version records
description: The Update Versions \[sys\_update\_version\] table contains records that represent the state of a customizable object at a particular time.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Versions, Using Team Development, Team Development, Planning your application, Building applications]
---

# Version records

The Update Versions `[sys_update_version]` table contains records that represent the state of a customizable object at a particular time.

A customizable record is any object that is tracked by Update Sets, such as business rules or script includes. A new version record is created automatically whenever a user changes a customizable record or changes the application file for the customizable record.

A record represents the version of a base system object as it was delivered in the most recent upgrade. Baseline versions are created only for objects that have been modified by a user, and they are updated each time the system is upgraded.

<table id="table_bqn_rf3_bq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique identifier for coalescing versions of the same customized record.

</td></tr><tr><td>

Record name

</td><td>

Name of the customized record.

</td></tr><tr><td>

Source

</td><td>

Indicator of how the version was added on the instance.-   System Upgrade: from a software upgrade \(the baseline version\).
-   Update Set: from an update set that was created or committed on the instance.
-   Pull History: from a pull in Team Development.

</td></tr><tr><td>

State

</td><td>

Indicator of whether the version is or has ever been loaded on the instance.-   Current: the version is currently loaded.
-   Previous: the version has previously been loaded on the instance. When a current version is replaced by a new version, it becomes a previous version.
-   History: the version was never loaded on the instance and was only inserted for historical purposes, such as when pulling versions from the parent in Team Development.

</td></tr><tr><td>

Application

</td><td>

The application for the customized record, if it is assigned to an application.

</td></tr><tr><td>

Payload

</td><td>

The data for this version of the customized record.

</td></tr><tr><td class="sub-head" colspan="2">

Additional fields on the list view

</td></tr><tr><td>

Reverted from

</td><td>

A reference to the older version record, if this version was created by [reverting to an older version](../task/t_RevertAChange.md).

</td></tr><tr><td class="sub-head" colspan="2">

Fields that can be added by configuring the form

</td></tr><tr><td>

Instance Name

</td><td>

The name of the remote instance where the version was originally created.

</td></tr><tr><td>

Instance ID

</td><td>

The URL of the remote instance where the version was originally created.

</td></tr><tr><td class="sub-head" colspan="2">

Related lists on the form view

</td></tr><tr><td>

Version List

</td><td>

All versions of the customized record that are available on the instance.

</td></tr></tbody>
</table>-   **[Merge tool](../concept/diff-merge-tool.md)**  
The Diff Merge tool enables administrative users to compare differences between two versions of a record.

**Parent Topic:**[Versions](../concept/c_Versions.md)

**Related topics**  


[Team Development](../concept/c_TeamDevelopment.md)

