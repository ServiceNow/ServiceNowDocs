---
title: Upgrade Details form
description: From the Upgrade Details form, you can review an individual record affected by the upgrade and reconcile conflicts between the upgrade and customizations.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Resolve conflicts for an individual record, Upgrade Monitor module: Upgrade an individual instance, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Details form

From the Upgrade Details form, you can review an individual record affected by the upgrade and reconcile conflicts between the upgrade and customizations.

![Upgrade Details form](../image/upgrade-details-form-small.png "Upgrade Details form")

<table><thead><tr><th>

Screen element

</th><th>

Description

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

How you elected to resolve this conflict:-   **Not Reviewed**
-   **Reviewed** - reviewed but no action yet taken
-   **Reviewed and Merged** - made changes to the record to reconcile the customized and upgraded versions
-   **Reviewed and Retained** - left customizations in place without update from upgrade
-   **Reviewed and Reverted** - customizations discarded, record updated according to upgrade

For more information, see [Process the skipped records list](../task/upgrademon-process-skip-list.md).

</td></tr><tr><td>

Disposition

</td><td>

Action performed on this file during the selected upgrade:-   Inserted: The system inserted a new record.
-   Updated: The system updated this record.
-   Deleted: The system deleted this record.
-   Skipped: The system did not change this record in order to preserve customizations.
-   Reverted: This record was reverted to the base version.
-   Table not found: The system could not find the table that contains this record.
-   Unchanged: The system did not change this record because the baseline component has not changed since the last release.
-   Skipped Manual Merge: The system did not change this record because updating it requires manual intervention.
-   Skipped Apply Once: The system skipped this record because it had already applied an update from an xml file in the apply once folder.
-   Not Latest: The system applied a change, but this change was overwritten later during the same upgrade.

</td></tr><tr><td>

Type

</td><td>

The record type, for example Script include.

</td></tr><tr id="phd_1pz_dx"><td>

Target name

</td><td>

Name of the skipped record, if applicable.

</td></tr><tr id="l3d_1pz_dx"><td>

Update set

</td><td>

Unused.

</td></tr><tr id="cjd_1pz_dx"><td>

Plugin

</td><td>

The plugin containing this record.

</td></tr><tr id="qjd_1pz_dx"><td>

Table

</td><td>

The table containing this record.

</td></tr></tbody>
</table>**Parent Topic:**[Resolve conflicts for an individual record](../task/upgrademon-resolve_conflicts.md)

