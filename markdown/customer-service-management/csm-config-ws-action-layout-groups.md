---
title: Create action layout group
description: The Create action on the Front-line case page displays a list of available actions that agents can select.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Front-line case page, Record pages, Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Create action layout group

The **Create** action on the Front-line case page displays a list of available actions that agents can select.

## Actions and action groups

Workspace record pages include individual actions that users can take when working with forms, such as **Save** or **Discuss**. Action groups combine multiple actions in the same button, such as **Create**, which displays a drop-down list with the available actions.

Customers can configure these action groups and arrange the order of the actions in the list using customizable form action layout groups.

Action groups are stored in the UX Form Actions Layout Group table \[sys\_ux\_form\_action\_layout\_group\]. The actions included in a group are displayed in the **Form actions in group** related list on the UX Form Actions Layout Group form and are stored in the Sys Ux M2m Action Layout Group Actions table \[sys\_ux\_m2m\_action\_layout\_group\_action\].

For more information about form action layout groups, see [Declarative actions](https://www.servicenow.com/docs/access?context=declarative-actions-landing&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) in the [Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) documentation.

## Create action layout group

The Front-line case page includes the **Create** action in the workspace action bar. Selecting **Create** displays a drop-down list with the available actions. These actions can include:

-   Create Escalation
-   Create Knowledge Gap
-   Create Problem
-   Create Incident
-   Create Normal Change
-   Create Work Order
-   Create Request
-   Create Standard Change

**Note:** Some actions that are available in the **Create** action group have been moved from the More actions menu. If you have customized the Create action for the Front-line case page, you need to manually upgrade to use the actions in the Create action layout group.

## Selecting an action

Depending on the action that an agent selects from the **Create** drop-down list, the system either opens a record in a sub-tab or in a [modeless dialog](csm-front-line-case-page-modeless-dialogs.md). The following actions open a record in a modeless dialog:

-   Create Escalation
-   Create Knowledge Gap
-   Create Problem
-   Create Incident
-   Create Normal Change
-   Create Work Order

From the modeless dialog, users can perform the following actions:

-   Minimize the record to the [workspace dock](csm-config-ws-bottom-utility-bar.md).
-   Open the record in a sub tab.
-   Save and stay.
-   Close the dialog.

