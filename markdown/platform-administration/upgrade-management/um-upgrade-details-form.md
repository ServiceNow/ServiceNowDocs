---
title: Upgrade details form
description: From the Upgrade Details form, you can review an individual record affected by the upgrade and reconcile conflicts between the upgrade and customizations.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Resolve conflicts for an individual record, Upgrade Monitor tool in Upgrade Console, Upgrade Console tools, Using Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade details form

From the Upgrade Details form, you can review an individual record affected by the upgrade and reconcile conflicts between the upgrade and customizations.

![Image showing the Upgrade Details form](../../upgrade-center/image/uc-upgrade-details-form.png)

<table id="table_znb_ggg_rlb"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

File name

</td><td>

The record the system has flagged as needing to be reconciled.

</td></tr><tr><td>

Priority

</td><td>

The priority the system has assigned to resolving this conflict. Values range from one to five, with one representing the highest priority.

</td></tr><tr><td>

Comment

</td><td>

Comments to document your decisions about reconciling this record.

</td></tr><tr><td>

Resolution

</td><td>

How you elected to resolve this conflict:-   **Not reviewed**: Not yet reviewed
-   **Reviewed**: Reviewed but no action yet taken
-   **Reviewed and Merged**: Made changes to the record to reconcile the customized and upgraded versions
-   **Reviewed and Retained**: Left customizations in place without update from upgrade
-   **Reviewed and Reverted**: Customizations discarded, record updated according to upgrade

For more information, see [Process the skipped records list](../task/um-process-skipped-records.md).

</td></tr><tr><td>

Disposition

</td><td>

Action performed on this file during the selected upgrade:-   Inserted: The system inserted a new record
-   Updated: The system updated the record
-   Deleted: The system deleted the record
-   Skipped: The system did not change this record in order to preserve customizations
-   Reverted: This record was reverted to the base version
-   Table not found: The system could not find the table that contains this record
-   Unchanged: The system did not change this record because the baseline component has not changed since the last release
-   Skipped Manual Merge: The system did not change this record because updating it requires manual intervention
-   Skipped Apply Once: The system skipped this record because it had already applied an update from an xml file in the apply once folder
-   Not Latest: The system applied a change, but this change was overwritten later during the same upgrade.

</td></tr><tr><td>

Type

</td><td>

Type of the record, for example, Script include.

</td></tr><tr><td>

Target name

</td><td>

Name of the skipped record, if applicable.

</td></tr><tr><td>

Update set

</td><td>

Unused.

</td></tr><tr><td>

Plugin

</td><td>

The plugin containing this record.

</td></tr><tr><td>

Table

</td><td>

The table containing this record.

</td></tr></tbody>
</table>**Parent Topic:**[Resolve conflicts for an individual record](../task/um-resolve-conflict.md)

