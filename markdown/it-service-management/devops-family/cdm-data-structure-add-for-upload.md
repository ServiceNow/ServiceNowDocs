---
title: Add the nodes that will contain config data to a new CDM application
description: Add the data structure to a new application that will accept the uploaded config data into appropriate nodes.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Uploading your config data, Configure, DevOps Config, IT Service Management]
---

# Add the nodes that will contain config data to a new CDM application

Add the data structure to a new application that will accept the uploaded config data into appropriate nodes.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: CDM Admin \[sn\_cdm.cdm\_admin\]

## About this task

When the system creates a new application, the application has only the highest level of structure: **components**, **collections**, and **deployables** folders. In this procedure, you add the component, collection, and deployable nodes that will accept the uploaded config data. When you upload existing config data into the application, the system maps the data as `[name:value]` pairs \(config data items — CDIs\) in the appropriate node in the data structure of the CDM application. For more information, see [CDM data model](../reference/cdm-data-model.md).

**Note:**

Starting with Configuration Data Management version 4.2, you can define a node using any UTF-8 character, including the forward slash \(`/`\).

## Procedure

1.  Create the components that will be included in the collections.

    For more information, see [Define or update a component](cdm-component-define.md) and [Define or update a collection in an application](cdm-collection-define.md).

2.  Add a collection to one or multiple deployables:

    1.  For the collection node in the tree, select the menu icon \(![Menu icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) and select **Include in deployables**.

    2.  Select all deployables in which to include the collection and then select **Include**.

        **Note:** Only deployables that do not already include the collection or any of its descendants appear in the list. If the collection has the same name as an existing node, then the collection is transformed into an override or overlay.

        The collection is included in each selected deployable.

    When you add a collection to a deployable, the **Editor** panel displays the included collection names but not their contents \(overrides or overlays do appear\). This strategy reduces clutter and clarifies the structure. To view the fully-resolved content of the data, view the **Preview** panel.

3.  Create the components that will be included in the collections.

4.  Add CDIs to the deployable that will override or overlay settings in components or collections.

    **Note:** Uploaded data items are sorted alphabetically within the structural folders to enable you to locate particular items quickly.

    The system places the following limits on the count of config data items \(CDIs\):

    -   An application can contain a maximum total of 100,000 CDIs.
    -   Any single deployable can contain a maximum of 10,000 CDIs.
    See [CDM system properties](../reference/cdm-system-properties.md) for information on configuring the **sn\_cdm.max\_allowed\_cdi\_per\_application** and **sn\_cdm.max\_allowed\_cdi\_per\_deployable** property settings.

    For more information, see [Define or update a component](cdm-component-define.md), [Define or update a collection in an application](cdm-collection-define.md), or [Create or update a variable CDI](cdm-variables-crud.md).

5.  Select **Save** to save the changes in the changeset and ready the changes in the changeset to be committed.

    The Editor panel, List view, and Preview panel refreshes to reflect the resolved state of the changeset. The system updates the changeset but does not update the application. Changes appear on the **Activity** tab. You must commit a changeset to update the config data for the application. After saving, you can move on to other activities and return later to edit the changeset.

6.  Select **Commit**.

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

The application does not yet contain config data, so the next step is to import your existing configuration data into the appropriate nodes in the application. See [Uploading your config data](../concept/cdm-upload-process.md).

**Related topics**  


[CDM data model](../reference/cdm-data-model.md)

[Parsing of XML files in CDM](../concept/cdm-parsing-xml-file.md)

[Parsing of CSV files in CDM](../concept/cdm-parsing-csv-file.md)

[Viewing and editing config data](../concept/cdm-editing-config-data-changesets.md)

[Define or update a component](cdm-component-define.md)

[Define or update a collection in an application](cdm-collection-define.md)

[Create or update a variable CDI](cdm-variables-crud.md)

[How encrypted data is handled](../concept/cdm-secrets-managing.md)

