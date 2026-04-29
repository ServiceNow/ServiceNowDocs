---
title: Review skipped records using related lists
description: Use different related lists to resolve, track and review the skipped records in an upgrade.The following table gives the description of each field in all the related lists within the upgrade history module.
locale: en-US
release: australia
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reviewing upgrade history, Upgrade History tool in Upgrade Console, Upgrade Console tools, Use, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Review skipped records using related lists

Use different related lists to resolve, track and review the skipped records in an upgrade.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to Upgrade History using one of the following ways.

    |Option|Navigation|
    |------|----------|
    |Using left navigation|Navigate to **All** &gt; **Admin Center** &gt; **Upgrade Management** &gt; **Upgrade History**.|
    |Using Admin tab option|Navigate to **Admin** &gt; **Upgrade Management** &gt; **Upgrade History**.|

    A list of upgrades is displayed.

2.  Select an upgrade from the list.

    System Upgrades form is displayed.

3.  Select any of the following related lists to review the skipped records.

    -   **Skipped Changes to Review related list**

        Resolve the skipped update records by tracking and reviewing them in the Skipped Changes to Review related list. To prevent your customizations from being overwritten during system upgrades, the upgrade process skips \(does not apply the update to\) objects that have been customized. See [Resolve a skipped update and set a resolution status](um-resolve-skipped-update.md) for more information.

    -   **Skipped Changes Reviewed related list**

        View the list of the reviewed skipped records in the Skipped Changes Reviewed related list. When you select a skipped record to review and set a **Resolution Status** to a value other than Not Reviewed, the update record moves from Skipped Changes to Review related list to the Skipped Changes Reviewed related list.

    -   **Copies to Review related list**

        Copies to Review lists all the records that need to be reviewed.

    -   **Copies Reviewed related list**

        Copies Reviewed lists all the records that have been reviewed.

    -   **Customization Unchanged related list**

        Customizations Unchanged lists all records that were skipped \(due to a customization\), but there have been no changes from the last upgrade. See [Revert a customization](um-revert-customization.md) for more information.

    -   **Changes Applied related list**

        Changes Applied lists all changes that were applied in this upgrade.

    -   **Claim Outcomes to Review related list**

        During system upgrades, the Claim Status tab displays outcomes to review and resolve.

    -   **Upgrade Details related list**

        Upgrade Details lists all Upgrade Details records for this upgrade.

    **Note:** The Copies to Review and Copies Reviewed related lists are Platform specific related lists.


**Parent Topic:**[Reviewing upgrade history](../concept/um-review-history.md)

## Upgrade history related lists details

The following table gives the description of each field in all the related lists within the upgrade history module.

<table id="table_b5b_p14_dlb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

File name

</td><td>

File name has different description for different related lists-   Skipped Changes to Review related list: Name of skipped Upgrade Detail record
-   Skipped Changes Reviewed related list: Name of the reviewed Upgrade Detail record
-   Copies to Review related list: Name of the record that needs to be reviewed
-   Copies Reviewed related list: Name of the record that has been reviewed
-   Customization Unchanged related list: Name of unchanged sys\_upgrade\_history\_log record. Select it if you want to access Upgrade Details and add comment text, or set a resolution status for it
-   Changes Applied related list: Current upgrade file name
-   Claim Outcomes to Review related list: Name of skipped Upgrade Detail record
-   Upgrade Details related list: Current upgrade file name

</td></tr><tr><td>

Disposition

</td><td>

Action performed on this file during the selected upgrade:-   Inserted: The system inserted a new record.
-   Updated: The system updated this record.
-   Deleted: The system deleted this record.
-   Skipped: The system did not change this record in order to preserve customizations.
-   Skipped Error: The system didn't have the upgrade on this file but skipped due to reasons like the record already exist in the system in a different scope or a system property exists.

**Note:** This is editable only by a maint.

-   Reverted: This record was reverted to the base version.
-   Table not found: The system could not find the table that contains this record.
-   Unchanged: The system did not change this record because the baseline component has not changed since the last release.
-   Skipped Manual Merge: The system did not change this record because updating it requires manual intervention.
-   Skipped Apply Once: The system skipped this record because it had already applied an update from an xml file in the apply once folder.
-   Not Latest: The system applied a change, but this change was overwritten later during the same upgrade.

</td></tr><tr><td>

Priority

</td><td>

Relative importance of the conflict that caused the skip.**Note:** ServiceNow prioritizes the skipped records based on the importance of the file types. The prioritization is done as follows:

-   Priority 1 \(highest priority\): UI pages, UI macros, and more
-   Priority 2: Business Rules, Security ACLs, and more
-   Priority 3: Reports and more
-   Priority 4: Form Sections, Choice Sets, and more
-   Priority 5 \(lowest priority\): other

</td></tr><tr><td>

Reason

</td><td>

States the reason why a particular record has been moved to the Skipped Error disposition.

</td></tr><tr><td>

Resolution

</td><td>

-   Reviewed
-   Retained
-   Reverted

</td></tr><tr><td>

Comment

</td><td>

During the process of resolving a skipped update, you have the option to add a **Comment** to any record. For example, the comment might explain the action that you took to future reviewers.

</td></tr><tr><td>

Target name

</td><td>

Name of the record corresponding to the current file.

</td></tr><tr><td>

Plugin

</td><td>

Plugin that contains the record.

</td></tr><tr><td>

Type

</td><td>

Current file type \(such as Business Rule or UI Policy\).

</td></tr><tr><td>

Table

</td><td>

Table that contains the record.

</td></tr></tbody>
</table>