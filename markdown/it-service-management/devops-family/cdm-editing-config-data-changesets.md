---
title: Viewing and editing config data
description: You can update the config data of an application by creating or opening a changeset on the Config data tab, where you update the structure and CDIs of the config data.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use, DevOps Config, IT Service Management]
---

# Viewing and editing config data

You can update the config data of an application by creating or opening a changeset on the **Config data** tab, where you update the structure and CDIs of the config data.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## Tabs on the Application page

When you open an application, the header area for each tab displays administrative details for the application: Application name, name of the user that created the application, and timestamp of creation.

-   **Overview**: Basic settings of the application and a **Manage deployables** button that enables you to edit config data.
-   **Snapshots**: List of snapshots for each deployable in the application. Each entry includes validation and publication status. Policies that execute against a snapshot return validation result. Published snapshots are available for release to the CI/CD pipeline.
-   **Config data**: Read-only view of the config data in a tree structure. Select a node in the tree to view the config data for that node in the application service or infrastructure service. \(You can edit an open changeset or create a new or changeset. The tab then updates to show an Editor panel and a Preview panel where you can create, edit, and save the changeset. You cannot change an existing snapshot, but you can start with a snapshot changeset and save the changes in a new changeset.\)

    **Important:** Save your changes whenever you are confident of the changes and before you leave the **Config data** tab.

-   **Settings**: A list of policies that are mapped to the deployables. Select an item to open it.
-   **Activity**: List of changesets. On this tab, you can open a changeset to continue editing or publish a changeset as a new version of the application config data.

## Config data tab

After you open a changeset by selecting **Edit config data**, you can edit the config data on the Config Data tab. In the config data tree \(A in the screenshot\), select the node to edit. By default, the editing panel \(C\) displays the script view of the key-value pairs \(the config data items or CDIs\) in the selected node.

![Config data tab on the Changeset form of a CDM application.](../image/cdm-config-data-tab-nav2.png)

-   **A: Config data tree**

    The config data tree displays the structured config data. Select a node to edit the associated data.

-   **B: View selector**

    To switch from the Script view \(shown as panels C and D\) to an editable list of CDIs and their values, slide the selector to **List view**.

-   **C: Editor panel**

    The Editor panel displays the contents of the selected node. You can edit the config data directly in the Editor panel.

    **Important:** To ensure that you edit only the data that you intend to edit, the panel displays only data that is directly in the selected node. The Editor panel lists all included collection and component names but not their contents. This strategy reduces clutter and clarifies the structure of the deployable. To view the fully resolved config data, view the Preview panel \(D\).

-   **D: Preview panel**

    The Preview panel displays the persisted state of the data in structured form. If you make any changes in the Editor panel and save the changes, the data in the Preview panel is updated to include the changes.

    -   To resolve variables and view the fully resolved data in the preview panel: In the More actions menu \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\), select **Apply variables**.
    -   Encrypted data appears as \*\*\*\*\*\*\*\*. Users with the CDM Secrets \[sn\_cdm.cdm\_secrets\] role can view all encrypted values in the preview panel. In the More actions menu \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\), select **View encrypted data**.
    -   To see nodes and CDIs that are excluded from inheritance: In the More actions menu \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\), select **View excluded data**.
-   **E: Actions**
    -   **Refresh View**: Update data in the view.
    -   **Save Changes**: Save \(persist\) the current changes but do not commit the data. The Editor panel, List view, and Preview panel refreshes to reflect the resolved state of the changeset. The system updates the changeset but does not update the application. Changes appear on the **Activity** tab. You must commit a changeset to update the config data for the application. After saving, you can move on to other activities and return later to edit the changeset. The button appears only if you have made changes.
    -   **Delete Changeset**: Delete the record of the changeset.
    -   **Commit Changeset**:  The system generates a snapshot of each deployable that is affected by the changes.

        **Note:** Because changes in two changesets that are open at the same time can conflict, the system blocks such commits. See [Conflicts between changeset commits](cdm-changeset-conflicts.md).

-   **F: Header for the changeset**

    The header displays general read-only information about the changeset. You can view this information and additional information on the **Details** tab, as described in the next section.

-   **G: Name path of the selected node**

    The name path is the complete folder path of the selected node in the list. Select the copy name path to clipboard icon \(![Copy name path to clipboard icon.](../image/cdm-icon-copy-path.png)\) to copy the name path of the node.


## Changeset - Header and Details tab

<table id="table_zpb_vyg_rpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Changeset number

</td><td>

Unique sequential changeset number that the system auto-assigns.

</td></tr><tr><td>

Description

</td><td>

Description that helps other users understand the purpose, scope, and intent of the changeset.

</td></tr><tr><td>

Application

</td><td>

Application on which the changeset is based.

</td></tr><tr><td>

State

</td><td>

-   Committed: This draft of the changeset has been committed.
-   Open: The changeset is being updated and is not committed.
-   Blocked: Other commits conflict with this commit. The changeset cannot be committed. See [Conflicts between changeset commits](cdm-changeset-conflicts.md).
-   Commit in progress: A draft of the changeset that is currently being committed.

</td></tr><tr><td>

Created / Created by

</td><td>

User who created the changeset and the timestamp of creation.

</td></tr><tr><td>

Updated / Updated by

</td><td>

User who updated the changeset and the timestamp of the update.

</td></tr><tr><td>

Committed / Committed by

</td><td>

User who committed the changeset and the timestamp of the commit.

</td></tr></tbody>
</table>