---
title: Create and update a deployable
description: Create a deployable while working in a changeset. You can add multiple components and collections to a deployable.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configure, DevOps Config, IT Service Management]
---

# Create and update a deployable

Create a deployable while working in a changeset. You can add multiple components and collections to a deployable.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_editor or cdm\_admin

## About this task

**Important:** Save your changes whenever you are confident of the changes and before you leave the **Config data** tab.

**Note:** Uploaded data items are sorted alphabetically within the structural folders to enable you to locate particular items quickly.

The system places the following limits on the count of config data items \(CDIs\):

-   An application can contain a maximum total of 100,000 CDIs.
-   Any single deployable can contain a maximum of 10,000 CDIs.

See [CDM system properties](../reference/cdm-system-properties.md) for information on configuring the **sn\_cdm.max\_allowed\_cdi\_per\_application** and **sn\_cdm.max\_allowed\_cdi\_per\_deployable** property settings.

## Procedure

1.  On the **Settings** tab for an application, select **Deployables** in the tree view and then select **New**.

2.  Fill in the fields on the Enter details page of the wizard and then select **Next**.

<table id="table_dnk_smg_44b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and meaningful name for the deployable.

</td></tr><tr><td>

Description

</td><td>

Description that helps other users understand the purpose, scope, and intent of the deployable.

</td></tr><tr><td>

Environment

</td><td>

The kind of application or infrastructure environment that the deployable implements.-   Development
-   Production
-   Test


</td></tr><tr><td>

Restrict export

</td><td>

Option to ensure that only snapshots that pass validation can be exported.

</td></tr></tbody>
</table>    The wizard moves to the Link to CMDB page of the wizard.

3.  On the Link to CMDB page and perform either of the following actions:

    -   Link the deployable to a CI in the CMDB: Select the cmdb\_ci and then select **Next**.
    -   Create a CI to link to: Select **New**, define the CI, and then select **Next**.
    The wizard moves to the Review page.

4.  On the Review page, verify the settings for the new deployable.

    Select **Back** to change settings. Select **Create** to create the deployable.

    The system generates the deployable and displays it in the list on the **Settings** tab for the application.

    ![Deployables for various environments](../image/cdm-deployables-list-for-app.png)

5.  Follow this procedure to add a collection to one or multiple deployables:

    1.  For the collection node in the tree, select the menu icon \(![Menu icon.](../../site-reliability-ops/image/icon-actions-menu.png)and select **Include in deployables**.

    2.  Select all deployables in which to include the collection and then select **Include**.

        **Note:** Only deployables that do not already include the collection appear in the list.

        The collection is included in each selected deployable.

    When you add a collection to a deployable, the Editor panel lists included collection names but not contents. The Preview panel displays the full state of the data.

6.  Add CDI settings to the deployable that will override or overlay settings in components or collections.

    For more information, see [Define or update a component](cdm-component-define.md), [Define or update a collection in an application](cdm-collection-define.md), or [Create or update a variable CDI](cdm-variables-crud.md).

7.  Select **Save** to save the changes in the changeset and ready the changes in the changeset to be committed.

    The Editor panel, List view, and Preview panel refreshes to reflect the resolved state of the changeset. The system updates the changeset but does not update the application. Changes appear on the **Activity** tab. You must commit a changeset to update the config data for the application. After saving, you can move on to other activities and return later to edit the changeset.

8.  Select **Commit**.

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

## What to do next

[Map policies to the deployable](cdm-deployable-map-policy-to.md)

**Related topics**  


[CDM data model](../reference/cdm-data-model.md)

[Viewing and editing config data](../concept/cdm-editing-config-data-changesets.md)

[Define or update a component](cdm-component-define.md)

[Define or update a collection in an application](cdm-collection-define.md)

[Create or update a variable CDI](cdm-variables-crud.md)

[How encrypted data is handled](../concept/cdm-secrets-managing.md)

