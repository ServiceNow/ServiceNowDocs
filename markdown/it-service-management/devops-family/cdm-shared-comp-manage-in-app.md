---
title: Manage shared components in a CDM application
description: Add a shared component to an application, view shared components that are available to add, or remove a shared component from an application.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Sharing components among applications — Component libraries, Using DevOps Config, DevOps Config, IT Service Management]
---

# Manage shared components in a CDM application

Add a shared component to an application, view shared components that are available to add, or remove a shared component from an application.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Roles required: CDM Editor \[sn\_cdm.cdm\_editor\]

## About this task

-   While working in an application changeset, you can add, update, or remove a shared component.
-   While working in an application changeset, you cannot modify a shared component in the same way as you can modify a direct component. A collection in an application can, however, override any value in a shared component. Also, you cannot rename a shared component in an application. If such a change is needed, a new shared component with the required name must be created, and then added again in the application.

All of these changes are withing the application changeset.

## Procedure

1.  While working on the **Config data** tab for an application changeset, select the shared components icon \(![Shared components icon.](../image/icon-shared-components-panel.png)\).

    -   Each card on a Shared components tab displays the name, parent component library, and version for a shared component.
    -   Components are grouped by library and are sorted alphabetically.
    -   Use the **Libraries** selector to display only components in the selected library.
    -   Use the **Search** text box to filter the list of components or libraries.
    ![Viewing available shared components](../image/cdm-shared-components-panel.png)

    -   **Available:** List of shared components that the application can include in its config data.

        For a shared component to be available for use in applications, the component must be in the **Published** state and the library that holds the component must be in the **Available** state.

    -   **In use:** List of shared components that are currently used in the application.
    -   **Updates:** A card appears when a newer published version of a component is available. Select the **refresh** icon \(![refresh icon](../../site-reliability-ops/image/icon-refresh.png)\) to ensure that you’re viewing all current updates.
2.  Add a shared component to application data: On the **Available** tab, select **Add**.

    -   The component is added to the **components** folder in the application.
    -   The shared component icon \(![shared component icon](../image/icon-shared-component.png)\) indicates that the component comes from a component library.
    -   The component is selected and the **Editor** and **Preview** panels display the code of the shared component.
3.  View the config data in a shared component: On any card, select the additional actions menu \(![Additional actions menu icon](../../site-reliability-ops/image/icon-actions-menu.png)\) and then select **View config data**.

    A pop-up displays the latest published version of the shared component code. Variables are not resolved and encrypted data is not decrypted in the pop-up view.

4.  Remove a shared component: Use either of the following methods to remove a shared component from the application data.

    -   On the **In use** tab, select the **X** in the component card and then confirm the action in the pop-up.
    -   On the **Config data** tab for an application, select the **Actions** menu \(![Actions menu icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for the component and then select **Remove**. Confirm the action in the pop-up.
    **Note:** Removal is not deletion. Removal takes the component's config data out of the application, but the component remains unchanged in the component library. When you remove a component from an application, the component card reappears on the **Available** tab.

5.  Update a shared component.

    Select the **refresh** icon \(![refresh icon](../../site-reliability-ops/image/icon-refresh.png)\) to ensure that you’re viewing all current updates. The system indicates that a newer published version of a component is available in the following ways:

    -   Highlighted text "Update" appears next to the component in the **components** folder.
    -   The **Updates** tab displays a card for the component.
    -   The pop-up for committing a changeset includes a notification: "One or more of the shared components have updates available".
    Follow this procedure to review the updated config data and then update a component:

    1.  On the **Updates** tab, select **Update** for the component.

    2.  Review the information on the Update a shared component pop-up and then select **Update**.

        -   The **Details** tab displays name and version information.
        -   The **Latest config data** tab displays the latest version of the shared component code. In the view, variables are not resolved and encrypted data is not decrypted.
6.  Commit the application changeset to generate a snapshot containing all these changes.

    The system generates a snapshot of each deployable that is affected by the changes.


**Related topics**  


[Sharing components among applications — Component libraries](../concept/cdm-component-libraries.md)

