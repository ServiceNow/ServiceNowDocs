---
title: Configuring Recommended Actions guidances
description: After creating guidances with the Recommended Actions application, you can configure the Recommended Actions component in UI Builder to determine how those guidances are displayed in CSM Configurable Workspace.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-12-03"
reading_time_minutes: 5
breadcrumb: [Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Configuring Recommended Actions guidances

After creating guidances with the Recommended Actions application, you can configure the Recommended Actions component in UI Builder to determine how those guidances are displayed in CSM Configurable Workspace.

## Guidance overview

A guidance is a suggested action that an agent can take as they work to resolve tasks, such as customer service cases. Guidances are created with the Recommended Actions application. For more information, see [Create a guidance in Recommended Actions](../task/ra-csm-guidances-create.md).

After creating a guidance, you can configure a preview experience \(card view\) and a detail view \(full article view\). These experiences determine how a guidance is displayed in the Recommended Actions tab of the contextual side panel in CSM Configurable Workspace. For more information, see the following topics:

-   [Configure a guidance preview experience](../task/ra-csm-guidance-configure-preview.md)
-   [Customize a guidance preview experience in UI Builder](../task/customize-ra-preview-experience.md)
-   [Customize a guidance detail view in U Builder](../task/customize-ra-detail-experience.md)

## Recommended Actions component configuration

Recommended Actions is a component that you can add to a record page in [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US). This component displays a list of recommended actions to an agent, based on the context of the current record.

You can use the Recommended Actions component properties to configure additional guidance settings. For more information about configuring the Recommended Actions component, including the properties and events, in the [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/now-experience/rome/components) documentation.

## Recommended action specific configuration property

The Recommended Actions component includes the **Recommended action specific configuration** property, which stores additional Recommended Actions properties. You can use this property to define the UI behaviors of different actions on a record page such as:

-   Selecting the guidances or decision trees to show or hide in the Recommended Actions tab.
-   Selecting the order of the actions to determine the primary action \(displayed as a button on the guidance card\) and secondary actions \(displayed on the overflow menu\).
-   Selecting which type of experience to uptake on a record page: modal or modeless dialog. For more information, see [Modal and modeless dialog experiences](ra-csm-guidances-attach-share-article.md#section_kwb_pbf_ddc).

The **Recommended action specific configuration** property is available in the Configure tab of the Recommended Actions component. Point to the property and select **Edit** to display the property details in a modal. This property includes expandable sections for each guidance, which are identified by the sys ID of the guidance or decision tree record. Within these sections are settings for each action associated with the guidance or decision tree.

![The recommended action specific configuration property includes sections for each guidance and settings that are specific to the actions in each guidance.](../image/ra-csm-specific-config-property.png "Recommended action specific configuration property")

The property displays the following fields for each guidance.

|Field|Description|
|-----|-----------|
|actionSysId|The sys id of the guidance or decision tree.|
|actionType|The type of action, either guidance or decision tree.|
|actionName|The name of the action, either guidance or decision tree. For example, attachAndShareArticle.|
|configurations|The JSON object includes action specific properties.|

For each of the actions associated with a guidance or decision tree, such as **Attach and add link in comment**, the property includes some or all of the following fields.

<table id="table_hcc_zqm_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isSupported

</td><td>

-   True: Recommended Actions emits an event when an agent selects the action.
-   False: Recommended Actions opens a modal for the respective actions.

</td></tr><tr><td>

isSupported

</td><td>

-   True: The button for this action is visible on the guidance card.
-   False: The button for this action is hidden on the guidance card.

</td></tr><tr><td>

orderInPreview

</td><td>

The order in which the action appears in the preview experience \(card view\) in the contextual side panel.Each card contains a primary action, which appears as a button on the card. The guidance action with the lowest **orderInPreview** value is the primary action.

Guidance actions with higher **orderInPreview** values are available as secondary actions and appear in the More actions menu in the upper right corner of the card.

These values also determine the order in which actions appear in the More actions menu. Actions with lower values appear in the menu above actions with higher values.

</td></tr><tr><td>

orderInDetail

</td><td>

The order in which the action appears in the detail experience \(full article view\) in the contextual side panel.The full article view includes a primary action, which appears at the bottom of the side panel. The guidance action with the lowest **orderInDetail** value is the primary action.

Guidance actions with higher **orderInDetail** values are available as secondary actions and appear in the More actions menu next to the primary action.

These values also determine the order in which actions appear in the More actions menu. Actions with lower values appear in the menu above actions with higher values.

</td></tr><tr><td>

visibleInPreview

</td><td>

Determines the visibility of the action in the preview guidance experience \(card view\).-   True: The action is shown.
-   False: The action is not shown.

</td></tr><tr><td>

visibleInDetail

</td><td>

Determines the visibility in of the action in the detail guidance experience \(full article view\). -   True: The action is shown.
-   False: The action is not shown.

</td></tr></tbody>
</table>The **Recommended action specific configuration** property includes a default set of values that provide the user with the modal experience and the following actions:

-   Attach and add link in comment
-   Add link in work note

## Trigger attach and share article guidance action event

Selecting an action triggers certain events, which are read by the record page. Events are available in the Events tab of the Recommended Actions component.

The **Trigger attach and share article guidance action** event launches the modal experience or modeless dialog experience for attaching and sharing a knowledge article in email, work notes, or comments.

Payload:

-   articleSysId: The ID of the knowledge article.
-   articleTitle: The title of the knowledge article.

