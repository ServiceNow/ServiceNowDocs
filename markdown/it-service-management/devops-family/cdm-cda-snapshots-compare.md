---
title: Compare snapshots from the same or different applications
description: Use the Config Data Analyzer tool to find similarities and differences between two snapshots from the same or different applications.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using DevOps Config, DevOps Config, IT Service Management]
---

# Compare snapshots from the same or different applications

Use the Config Data Analyzer tool to find similarities and differences between two snapshots from the same or different applications.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_viewer, cdm\_editor, or cdm\_admin

## About this task

You can compare and contrast snapshots from any deployable of the same or different applications.

To see the changes between two snapshots from the same deployables, see [Compare two snapshots of a deployable](cdm-cda-snapshots-compare-changes.md).

## Procedure

1.  While viewing an application, select **Compare config data**.

    The **Compare config data** tab opens. The current application is the target application, and its name is pre-populated in the **Target application**.

    ![Compare config data tab for comparing application snapshots.](../image/cdm-snapshot-compare.png)

2.  Select the **Snapshot** option in the **Compare type** field.

3.  Select an application and then their snapshots to compare.

    |Option|Description|
    |------|-----------|
    |Reference application|Application to compare with the target application. The field lists the latest committed data for all applications including the target application.|
    |Reference snapshot|Snapshot of the reference application to compare.|
    |Target snapshot|Snapshot of the target application against which the reference snapshot is compared.|

4.  If you've the cdm\_secrets role, you can select **View encrypted data** to view encrypted values in clear text in the comparison results.

    **Note:** The check box is inactive for users who don’t have the cdm\_secrets role. When the values in the target and reference differ, the comparison results indicate that the values differ, but the data itself still appears as \*\*\*\*\*\*\*\*.

5.  Select **Compare**.

    The Config data differences section displays the comparison results. It shows the differences between the selected reference and target snapshots.

    **Important:** If you commit changes to a reference application while the **Compare config data** tab is open: When you return to the **Compare config data** tab and select **Compare**, the system uses the most recent committed changeset, performs the comparison again, and then displays the new results in the results section.

    The letters in the following illustration identify the tools that you can use to analyze the data.

    ![Tools in the Config data differences section.](../image/cdm-snapshot-compare-result.png)

    -   **A: Navigation panel**

        The navigation panel displays the node structure of the applications.

        -   Nodes that include changed CDIs \(either directly or in descendent nodes\) are annotated with **Different**.
        -   Nodes that include newly added CDIs \(either directly or in descendent nodes\) are annotated with the identity of the application changeset that includes the new data, either **Reference** or **Target**.
        You can search for a node name in the **Search** field. Select a node to view its contents in the Differences panel.

    -   **B: Differences panel**

        The **CDIs and variables** tab displays changes to individual CDIs for the node that is selected in the navigation panel.

        -   By default, the root node is selected and the data panel includes all CDIs for both changesets. Select a node in the navigation panel to display data for only that node and its descendents.
        -   When **Diff only** is selected, the number of CDIs that differ appears after the node path.
        -   Node paths are displayed in gray. Use the expansion icon \(![expansion icon](../image/cdm-icon-expand.png)\) to view CDIs in a folder.
<table id="table_znm_bcc_yvb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Differences

</td><td>

Indicator to show where the differences are.-   Target: The CDI appears only in the target changeset.
-   Reference: The CDI appears only in the reference changeset.
-   Different: For the specified CDI, the values in the target and reference changesets differ.


</td></tr><tr><td>

Description

</td><td>

Statement of how the changesets differ. For example, the text might indicate that a CDI appears only in the reference changeset or that the values for a variable differ between the changesets. See [Types of differences between CDM applications](../reference/cdm-cda-diff-types.md) for the full list of difference types and their causes.

</td></tr><tr><td>

Name

</td><td>

Name of the CDI.

</td></tr><tr><td>

Reference \(R\)

</td><td>

Value of the CDI in the reference changeset.

</td></tr><tr><td>

Target \(T\)

</td><td>

Value of the CDI in the target changeset.

</td></tr><tr><td>

Source level \(R/T\)

</td><td>

The node level in the code at which the CDI is defined. -   Direct: The CDI is defined in the selected node.
-   Include: The value of the CDI is obtained from a node that is included in the selected node.
-   Override: The value of the CDI in an included node is overridden by a value that is specified in the including node.
Values appear in the following formats:

-   `<reference level / target level>` when a value appears in both target and reference.
-   `<reference level>` when a value appears in only the reference changeset.
-   `<target level>` when a value appears in only the target changeset.
For example, when a CDI is defined in the reference changeset with the value `true` and the CDI doesn’t appear in the target changeset, then the last three columns in the **CDIs and variables** tab will have the following values:

-   **Reference \(R\)**: `true`
-   **Target \(T\)**: \[Empty\]
-   **Source level \(R/T\)**: `Direct`


</td></tr></tbody>
</table>    If a file node is selected in the tree, the **File information** tab displays its metadata.

<table id="table_avm_33q_byb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Differences

</td><td>

Indicator to show where the differences are.-   Target: The file node is available only in the target changeset.
-   Reference: The file node is available only in the reference changeset.
-   Different: The file node data differs in the target and reference changesets.


</td></tr><tr><td>

File metadata

</td><td>

Metadata of the file attached to the file node.-   File name: Name of the attached file in the file node.
-   Content type: Content type of the file.
-   Content: Content of the attached file. Preview is not available on the list, but you can download the file to preview it.
-   File URL: Folder path where the file exists.


</td></tr><tr><td>

Reference \(R\)

</td><td>

Details of the file present in the reference changeset.

</td></tr><tr><td>

Target \(T\)

</td><td>

Details of the file present in the target changeset.

</td></tr></tbody>
</table>
