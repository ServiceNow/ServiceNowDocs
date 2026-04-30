---
title: Open a changeset to update config data
description: Update config data in an existing changeset or in a new changeset. You can save your changes for later updates or save and commit the changes. Committing the changes generates a snapshot for each deployable that is affected by the changes.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Changesets and version control in CDM, Use, DevOps Config, IT Service Management]
---

# Open a changeset to update config data

Update config data in an existing changeset or in a new changeset. You can save your changes for later updates or save and commit the changes. Committing the changes generates a snapshot for each deployable that is affected by the changes.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_editor or cdm\_admin

## About this task

-   When you commit the changes that you have made to an application \(commit the changeset\), the system generates a snapshot of each deployable that has been updated. A snapshot is an exact record of the config data for a deployable. Snapshots are read-only — you cannot modify a snapshot. You can, however, start a new changeset that is based on a particular snapshot.
-   Sometimes, another user has committed changes to a data set \(thus creating a new snapshot\) while you are working on a changeset of the same data. In this case, the data that you are working on is stale \(the data is in the state it was in before the other user committed changes\). This can result in data conflicts. Learn more about how you use changesets and how CDM manages version control at [Changesets and version control in CDM](../concept/cdm-changesets-version-control.md).

## Procedure

1.  Use one of the following methods to open a changeset for editing:

    -   On the **Activity** tab for an application, select a changeset number.
    -   On the **Overview** or **Config data** tab for an application, select **Edit Config Data**.
    **Important:** Save your changes whenever you are confident of the changes and before you leave the **Config data** tab.

    The changeset opens on the **Config data** tab.

2.  In the config data tree, select the item to edit in either the script view or the list view.

    By default, the Editor panel displays the script view of the key:value pairs \(the config data items — CDIs\) in the selected node. See [Viewing and editing config data](../concept/cdm-editing-config-data-changesets.md) for details on operations in the **Config data** tab.

3.  Add components, collections or deployables, see the instructions in [Define or update a component](cdm-component-define.md), [Define or update a collection in an application](cdm-collection-define.md), and [Create and update a deployable](cdm-deployable-define.md).

4.  Select **Save** to save the changes in the changeset and ready the changes in the changeset to be committed.

    The Editor panel, List view, and Preview panel refreshes to reflect the resolved state of the changeset. The system updates the changeset but does not update the application. Changes appear on the **Activity** tab. You must commit a changeset to update the config data for the application. After saving, you can move on to other activities and return later to edit the changeset.

5.  Select **Commit**.

    The Commit changeset dialog box opens and lists each deployable that is affected by the changes.

    **Note:** After you commit a changeset, the changeset cannot be modified.

    The system generates a snapshot of each deployable that is affected by the changes. The dialog box offers the following **Additional actions**:

    -   If no deployables are affected by the changes, select **No additional actions**. The system will update the application to persist the changes.
    -   -   Select **Validate snapshots** to perform the following operations on all generated snapshots:
    -   The system executes all policies that are statically or dynamicallymapped to the associated deployable.
    -   If the snapshot passes all policies, then the Validation status value is set to **Passed** and no entries are listed on the **Validation Results** tab. If validation was invoked with the **Publish Valid** publish option, then valid snapshots are auto-published.
    -   If any policy encounters issues, then the Validation status value is set to **Failed**. The **Validation Results** tab displays all failures or warnings returned by policies.
    -   If any policy failed to run to completion, then the Validation status value is set to **Execution error** and the **Validation Results** tab indicates that validation failed due to error.
-   Select **Validate and publish snapshots** to perform validation as described in the **Validate snapshots** action. Only snapshots that pass validation are published. Only published snapshots can be exported.
        Select **Commit**. 

        -   The system updates the application to persist the changes to config data.
        -   The changeset state changes to **Committed**.
        -   The changeset cannot be modified.
        -   If snapshots were created, the confirmation message includes a link to the snapshots.
        -   If an error occurs during the commit process, the changeset state is set to Commit failed.

**Related topics**  


[Changesets and version control in CDM](../concept/cdm-changesets-version-control.md)

[Define or update a component](cdm-component-define.md)

[Define or update a collection in an application](cdm-collection-define.md)

[Publish or unpublish a snapshot](cdm-snapshot-publish.md)

[Validate a snapshot manually](cdm-snapshot-validate-manually.md)

[View the results of snapshot validation](cdm-validation-results-view.md)

[View snapshots](cdm-snapshots-view-list.md)

