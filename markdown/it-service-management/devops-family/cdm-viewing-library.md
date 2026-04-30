---
title: Working on component libraries with a unified view
description: The unified view of component libraries in the DevOps Config Workspace provides a single location to view and manage component libraries and the components within them.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Sharing components among applications — Component libraries, Use, DevOps Config, IT Service Management]
---

# Working on component libraries with a unified view

The unified view of component libraries in the DevOps Config Workspace provides a single location to view and manage component libraries and the components within them.

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Using the unified view, you can:

-   Search for a component library or shared component.
-   Navigate quickly between different component libraries or shared components.
-   View a list of all applications that use shared components of a library.
-   Edit the config data of a library.
-   View and create changesets for the library and components.
-   View different versions of a shared component, and publish or unpublish them.

## Users

The following users can view and manage the component libraries and shared components in the DevOps Config Workspace.

-   CDM admin can view and manage the libraries and shared components.
-   CDM editor can view and manage the shared components within the libraries.
-   CDM viewers can view the libraries and shared components.

## Accessing the component libraries

To open the Component libraries, navigate to **All** &gt; **DevOps Config** &gt; **DevOps Config Workspace** and select the component libraries icon \(![Component libraries icon.](../image/icon-component-libraries.png)\).

## Component libraries list

On the Component libraries list, you can review all component libraries and shared components within them. The list pane has the following sections to enable you to access and manage the libraries and components quickly.

-   **View**: Filter libraries by the categories: All libraries and Editable libraries. Editable libraries are the libraries that you create or that others create but grant you permission to view and edit through the associated authoring groups.
-   **Search**: Search library or component by their names.
-   **Create new library**: Create a library using this option.
-   **Listing**: Select a library node or shared component node to view it in the form pane.

The following is an example of a unified view for Component libraries.

![Unified view in DevOps Config Workspace to manage component libraries and shared components.](../image/cdm-comp-library-unified-view.png "Unified view in DevConfig Workspace to manage component libraries")

## Component library form

On the Component library form pane, you can review and manage your libraries and components within them. Select a library node in the left pane to view and edit the associated data.

-   **Header**: The header section shows the status and other metadata of the component library. You can take the following actions:
    -   Mark a library as available or unavailable for use by using the **Available** toggle switch.
    -   Save the changes to the library.
    -   Edit to create or open a changeset for updating shared components.
-   **Tabs**: The following tabs are available:
    -   **Details**: View and update a library's details such as name, description, and authoring groups. The tab also includes a list of all applications that are using one or more components of the library.
    -   **Components**: View all the components available in the library.
    -   **Config data**: Review the config data in each component of the library. You can switch between Editor and List view using the **List view** toggle switch.
    -   **Activity**: View a list of all changesets created for updating the library, its components, and config data.

The following is an example of a component library form in the DevOps Config Workspace.

![Component library form.](../image/cdm-comp-library-form.png "Component library form")

## Shared component form

On the Shared component form pane, you can review and manage components within your libraries. Select a component node in the left pane to view and edit the associated data.

-   **Header**: The header section shows the status and other metadata of the component library. You can take the following actions:
    -   Save the changes to the component.
    -   Edit to create or open a changeset for updating the component.
    -   Refresh the form data.
-   **Tabs**: The following tabs are available:
    -   **Details**: View the component's details and update its description as required. The tab also includes a list of all applications that are using the components.
    -   **Versions**: View all the published and unpublished versions of the component. You can also publish a component's version or unpublish a version.

The following is an example of a shared component form in the DevOps Config Workspace.

![Shared component form.](../image/cdm-component-form.png "Component library form")

