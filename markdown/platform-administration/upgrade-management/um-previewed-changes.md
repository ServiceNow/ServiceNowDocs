---
title: Preview predicted changes
description: Use the previewed changes table to view the list of total records that are predicted to change when the upgrade occurs.
locale: en-US
release: australia
product: Upgrade Management
classification: upgrade-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Upgrade Preview tool in Upgrade Console, Upgrade Console tools, Use, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Preview predicted changes

Use the previewed changes table to view the list of total records that are predicted to change when the upgrade occurs.

## Preview skipped list prediction

The **Total record changes** also includes records that are predicted to be skipped due to various reasons. The most common reason is due to customization. The reason an upgrade skips customizations is to avoid overwriting your customizations. Upgrade Preview attempts to predict which records will be skipped when the actual upgrade occurs. It predicts skips due to customizations, and some of the other more complex scenarios as well. It is possible to use Upgrade Preview to address these predicted customization skips before the upgrade occurs, which can prevent that skip from happening.

Click **View preview details** link on the **Previewing version** card. The Upgrade Preview form appears along with the following related lists details.

<table id="table_ycy_np2_clb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File name

</td><td>

Record that has been flagged for reconciliation.

</td></tr><tr><td>

Predicted Disposition

</td><td>

Action predicted to be performed on this file during the selected upgrade:-   Predicted Insert: The system is predicted to insert a new record.
-   Predicted Update: The system is predicted to update this record.
-   Reverted: This record was reverted to the base version, and won’t be skipped on the next upgrade.
-   Predicted Skip: The system won't change this record in order to preserve customizations.
-   Predicted Skip \(Manual Merge\): The system won't change this record because updating it requires manual intervention.
-   Predicted Skip \(Apply Once\): The system is predicted to skip this record because it had already applied an update from an xml file in the apply once folder.

</td></tr><tr><td>

Priority

</td><td>

Priority that has been assigned to resolve the conflict. Values range from one to five, with one representing the highest priority.**Note:** ServiceNow prioritizes the skipped records based on the importance of the file types. The prioritization is done as follows:

-   Priority 1 \(highest priority\): UI pages, UI macros, and more
-   Priority 2: Business Rules, Security ACLs, and more
-   Priority 3: Reports and more
-   Priority 4: Form Sections, Choice Sets, and more
-   Priority 5 \(lowest priority\): other

</td></tr><tr><td>

Resolution

</td><td>

Ways to resolve a conflict.-   **Not reviewed**: Conflicted files that have not been reviewed yet
-   **Reviewed**: Reviewed but no action has been taken yet
-   **Review not needed**: Review of the skipped files are not required
-   **Reviewed and Retained**: Left customizations in place without update from upgrade
-   **Reviewed and Reverted**: Customizations discarded, record updated according to the upgrade version

</td></tr><tr><td>

Plugin

</td><td>

Plugin containing the record

</td></tr><tr><td>

Related record

</td><td>

Record that the changelist entry applies to

</td></tr></tbody>
</table>**Parent Topic:**[Upgrade Preview tool in Upgrade Console](../concept/um-upgrade-preview-tool.md)

