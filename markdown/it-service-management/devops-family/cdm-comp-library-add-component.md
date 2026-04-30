---
title: Add or update a shared component in a component library
description: Add or update a shared component in a component library.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Sharing components among applications — Component libraries, Use, DevOps Config, IT Service Management]
---

# Add or update a shared component in a component library

Add or update a shared component in a component library.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_editor or cdm\_admin

## About this task

You can also add a component to the library as a shared component from a request. For more information, see [Accept or reject a component request for inclusion in a component library](cdm-comp-library-request-approval.md).

## Procedure

1.  Navigate to **All** &gt; **DevOps Config** &gt; **DevOps Config Workspace**.

2.  Select the component libraries icon \(![Component libraries icon.](../image/icon-component-libraries.png)\) in the left navigation pane to open the **Component libraries** tab.

3.  Select a component library from the **Component libraries** list tab to which you want to add a shared component.

4.  Select **Edit** to create a changeset or select an open changeset to work.

5.  Add a shared component to the library.

    1.  On the **Config data** tab of the changeset record, select the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for the **components** node and select **Create shared component**.

    2.  In the Create shared component dialog box, enter a unique and meaningful name for the component.

    3.  Select **Create**.

        A component is created.

6.  Add config data items \(CDIs\) and values for the shared component.

    1.  With the shared component node selected, add one or more CDIs and values in the Editor pane.

    2.  Select **Save**.

7.  Add a file node to the component.

    For more information on adding files, see [Manage files in the config data model using file nodes](cdm-manage-file-config-data-file-node.md).

8.  Select the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for a component to rename or delete it.

    -   To rename the component, select **Rename** from the menu.
    -   To delete the component, select **Delete** from the menu.
    **Note:** These options are available only if the component is not being used in any application.

9.  Select **Commit** to commit all changes for the shared component.

    A new version of the shared components is created.

10. In the **Additional actions** field, select an option to either publish the latest version or do it later.

    -   **No additional actions**: Does not process anything for the latest version of the component.
    -   **Publish latest version**: Publishes the latest version of the component.

        **Note:** For a shared component, only one version can be published at a time. So, any existing published version is unpublished and the new version is published.


