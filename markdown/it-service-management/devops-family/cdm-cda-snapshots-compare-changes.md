---
title: Compare two snapshots of a deployable
description: Use the Config Data Analyzer tool to find changes between two snapshots of a deployable of an application.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, DevOps Config, IT Service Management]
---

# Compare two snapshots of a deployable

Use the Config Data Analyzer tool to find changes between two snapshots of a deployable of an application.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

There must be more than one snapshot available in a deployable to compare and the target snapshot must not be the first snapshot in the deployable.

Role required: cdm\_viewer, cdm\_editor, or cdm\_admin

## About this task

To compare snapshots from different deployables or applications, see [Compare snapshots from the same or different applications](cdm-cda-snapshots-compare.md).

## Procedure

1.  While viewing an application, select the **Snapshots** tab.

2.  Open a snapshot of a deployable.

3.  In the Snapshot record page, select the **Config data changes** tab.

    The current snapshot is auto-populated in the **Target snapshot** field.

    ![Compare config data tab for comparing application snapshots.](../image/cdm-snapshot-compare-change.png)

4.  Select another snapshot in the **Reference snapshot** field.

    The **Reference snapshot** field lists all snapshots that are older than the target snapshot. The **Reference snapshot** field is inactive when older snapshots are not available. Even if newer snapshots created after the target snapshots exist in the deployable, they are not listed.

5.  If you've the cdm\_secrets role, you can select **View encrypted data** to view encrypted values in clear text in the comparison results.

    **Note:** The check box is inactive for users who don’t have the cdm\_secrets role. When the values in the target and reference differ, the comparison results indicate that the values differ, but the data itself still appears as \*\*\*\*\*\*\*\*.

6.  Select **Compare**.

    The Config data changes section displays the comparison results. It shows the changes between the selected reference and target snapshots.

    The following image displays the Config data changes section that contains the comparison result that you can use to analyze the data.

    ![The Configuration data changes section, which includes a navigation panel and a changes panel, displays the comparison result.](../image/cdm-snapshot-compare-change-result.png)

    -   **A: Navigation panel**

        The navigation panel displays the node structure of the deployable.

        -   Nodes that include changed CDIs \(either directly or in descendent nodes\) are annotated with **Edited**.
        -   Nodes that include newly added CDIs \(either directly or in descendent nodes\) are annotated with **Added**.
        You can search for a node name in the **Search** field. Select a node to view its contents in the Changes panel.

    -   **B: Changes panel**

        The panel displays a list of changes to individual CDIs for the node that is selected in the navigation panel.

        -   By default, the root node is selected and the data panel includes all CDIs for both snapshots. Select a node in the navigation panel to display data for only that node and its descendents.
        -   Node paths are displayed in gray. Use the expansion icon \(![expansion icon](../image/cdm-icon-expand.png)\) to view CDIs in a folder.
        -   When **Changes only** is selected, the number of CDIs that have changes appears after the node path.
        -   When **Script view** is selected, the list view toggles to editor view.
<table id="table_znm_bcc_yvb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Indicator to show what was the change type.-   Added: A CDI appears only in the target snapshot.
-   Deleted: A CDI appears only in the reference snapshot.
-   Edited: For the specified CDI, the values in the target and reference snapshots differ.


</td></tr><tr><td>

Name

</td><td>

Name of the CDI.

</td></tr><tr><td>

Reference snapshot

</td><td>

Value of the CDI in the reference snapshot.

</td></tr><tr><td>

Target snapshot

</td><td>

Value of the CDI in the target snapshot.

</td></tr></tbody>
</table>    If a file node is selected in the tree, the comparison result displays the changes in the file between the selected reference and target snapshots.

<table id="table_b2t_r3q_byb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Indicator to show what was the change type.-   Added: The file node is available only in the target snapshot.
-   Deleted: The file node is available only in the reference snapshot.
-   Edited: The file node data differs in the target and reference changesets.


</td></tr><tr><td>

File metadata

</td><td>

Metadata of the file attached to the file node.-   File name: Name of the attached file in the file node.
-   Content type: Content type of the file.
-   Content: Content of the attached file. Preview is not available on the list, but you can download the file to preview it.
-   File URL: Folder path where the file exists.


</td></tr><tr><td>

Reference snapshot

</td><td>

Details of the file present in the reference changeset.

</td></tr><tr><td>

Target snapshot

</td><td>

Details of the file present in the target changeset.

</td></tr></tbody>
</table>
