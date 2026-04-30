---
title: Customize a guidance preview experience in the UI Builder
description: Customize a preview of a Recommended Actions card that displays in the contextual side panel using UI Builder. The preview experience includes a hint, an icon, a message, and an action button.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Creating guidance and field recommendation in Recommended Actions, Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Customize a guidance preview experience in the UI Builder

Customize a preview of a Recommended Actions card that displays in the contextual side panel using UI Builder. The preview experience includes a hint, an icon, a message, and an action button.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author and ui\_builder\_admin, admin

## About this task

You begin by creating a UI page variant of a guidance preview experience. When you create a UI page variant from a page template, you start with a base structure that you can customize. By using the component properties, you can change how your recommendation card preview looks.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Action Types** &gt; **Guidances**.

2.  Select a guidance from the Guidances list.

3.  Select **Create preview UI** to create a UI page variant of a guidance preview experience.

    This page includes an empty `customExpProps` container with the properties listed in the following table during run-time. The Recommended Actions framework passes the `customExpProps` object as a property to the custom experience.

    |Property|Description|
    |--------|-----------|
    |sysId|ID of the recommendation.|
    |name|Title of the preview experience.|
    |description|Message for the preview experience.|
    |recommendationHint|Text that tells the agent why a recommendation is being suggested.|
    |callToActions|Settings for the guidance action.|
    |actionTypeLabel|Label for the recommended action type.|
    |icon|Icon for the recommendation card.|
    |actionStateLabel|External name of the action state.|
    |actionStateValue|Internal name of the action state.|
    |previewFields|The fields to display in the guidance preview experience.|
    |errorMessage|Error message to display when the recommendation fails to display.|
    |ariaHidden|On the Recommended Actions grouped list, the sn-carousel component will pass this property to each card to determine if the content is hidden within the carousel. If the card is hidden, we should use this value to set aria-hidden or disable any actionable component to true and avoid accessibility issues.|
    |useCase|Search/RA tab where the guidance is getting rendered.|
    |actionInputs|Guidance Inputs.|
    |actionTypeSysId|Sys Id of the recommendation type.|
    |actionId|Sys Id of the recommendation.|
    |table|Recommended Actions Context table.|
    |tableSysId|Recommended Actions Context table record sys\_id.|
    |renderer|Component responsible to render the detailed experience|
    |secondaryCallToAction|Secondary actions to be shown on card.|
    |isGenius|Is genius result card, used in Search tab genius result.|
    |contextSysId|Recommended Actions context sysId.|
    |actionConfigurations|Recommended Actions actionConfigurations property value. The Value field is left empty by default.|
    |isFullSearchView|If search displayed in full search view of side panel view, the value is true.|
    |contextInputs|Recommended Actions contextInput property value. To get the predefined syntax, navigate to All &gt; Recommended Actions &gt; Context &gt; Context Inputs and copy the JSON format of the context inputs.|

    The following example shows properties and sample values for the preview experience.

    ```
    "customExpProps": {
            "sysId": "e8421a2a436f0210f81d92621ab8f2da",
            "name": "Attach and share article",
            "description": null,
            "recommendationHint": "Knowledge",
            "callToActions": [
                {
                    "label": "",
                    "name": "",
                    "id": "1e8392aa436f0210f81d92621ab8f291",
                    "actionBehavior": "contextual_side_panel",
                    "primary": "true",
                    "order": "100",
                    "completionMessage": "Knowledge article successfully attached."
                }
            ],
            "recommendationAction": "",
            "actionTypeLabel": "Guidance",
            "icon": "magnifying-glass-sparkle-outline",
            "actionStateLabel": "New",
            "actionStateValue": "new",
            "previewFields": null,
            "attributes": "",
            "errorMessage": "",
            "ariaHidden": false,
            "useCase": "search",
            "actionInputs": {},
            "actionTypeSysId": "",
            "actionId": "",
            "table": "sn_customerservice_case",
            "tableSysId": "",
            "renderer": "sn-guidance-experience-connected",
            "secondaryCallToAction": {},
            "isGenius": false,
            "contextSysId": "",
            "actionConfigurations": {},
            "isFullSearchView": false
        }
    
    ```

4.  Select **Edit preview in UI Builder**.

    The UI page variant opens in UI Builder, where you can add and configure components to customize the look and feel of the preview experience. For more information, see [Working with components in the UI Builder](https://www.servicenow.com/docs/access?context=work-components&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

5.  Bind the preview experience properties to your preview UI.

    Data bindings are in the **Config** tab of the configuration panel in UI Builder. For more information, see [Data resources in UI Builder](https://www.servicenow.com/docs/access?context=data-resources&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

6.  Add and bind scripts to components in your preview UI to dispatch events by using an event handler to execute or skip a recommendation with a corresponding payload.

    The following table shows the list of events that are emitted with respect to the actions perform by an agent:

<table id="table_grp_flc_xvb"><thead><tr><th>

Events handled

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ON\_SINGLE\_CLICK\_ACTION\_INITIATE

</td><td>

Initiates and completes the action when an agent selects the action button. This event passes the following parameters in the payload:```
api.emit( 
    ‘ON_SINGLE_CLICK_ACTION_INITIATE‘, { 
        sysId: api.context.props.customExpProps.sysId, 
        
        name: api.context.props.customExpProps.name, 
        
        actionStateValue: api.context.props.customExpProps.actionStateValue, 
        actionMetadata: api.context.props.customExpProps.callToActions[0] ,
        table: api.context.props.customExpProps.table,
        tableSysId: api.context.props.customExpProps.tableSysId,
        contextSysId: api.context.props.customExpProps.contextSysId,
        actionType: api.context.props.customExpProps.actionTypeSysId,
        actionInputs: api.context.props.customExpProps.actionInputs,
        formFieldInputs: { <actionInputs key>: <actionInputs value> },
        actionId: api.context.props.customExpProps.actionId,
        name: api.context.props.customExpProps.name,
        actionMetadata: api.context.props.customExpProps.callToActions[0],
        actionStateValue: api.context.props.customExpProps.actionStateValue,
    }
)

```

The `formFieldInputs` contains the `actionInputs` which must be updated when the event is emitted.

</td></tr><tr><td>

ON\_DRILL\_DOWN\_ACTION\_INITIATE

</td><td>

Expands the action and displays more actions or information after an agent selects the primary action button. This event passes the following parameters in the payload:```
api.emit( 
          ‘ON_DRILL_DOWN_ACTION_INITIATE ‘, { 
          table: api.context.props.customExpProps.table,
          tableSysId: api.context.props.customExpProps.tableSysId,
          actionType: <sys_id for "Guidance" action type/ e38f55b9b72120107d472397ee11a9be>,
          actionInputs: api.context.props.customExpProps.actionInputs,
          formFieldInputs: {"<actionInputs Key>":"<new value which needs to be set>"},
          actionId: api.context.props.customExpProps.actionId,
          sysId: api.context.props.customExpProps.sysId,
          name: api.context.props.customExpProps.name,
          actionStateValue: api.context.props.customExpProps.actionStateValue,
          actionMetadata: api.context.props.customExpProps.callToActions[0],
          renderer: api.context.props.customExpProps.renderer,
          contextSysId: api.context.props.customExpProps.contextSysId,
          sysId: api.context.props.customExpProps.sysId, 
          name: api.context.props.customExpProps.name }

)

```

</td></tr><tr><td>

DISMISS\_ACTION\_CLICK

</td><td>

Cancels the action.```
api.emit( 
    ‘DISMISS_ACTION_CLICK‘, { 
         sysId: api.context.props.customExpProps.sysId
    }
)
```

</td></tr><tr><td>

ACTION\_TRIGGERED\_PROPAGATION

</td><td>

Enables user to add UI specific behavior for guidance actions. This event propagates the payload details to the parent where this event can be handled.```
api.emit(
    ‘SN_NEXT_BEST_ACTION_LIST_CONNECTED#ACTION_TRIGGERED_PROPAGATION' ‘, {
   "actionSysId": api.context.props.customExpProps.actionId
   "actionName": api.context.props.customExpProps.actionConfigurations[api.context.props.customExpProps.actionId ][“actionName”]
   "actionType": "guidance",
   "eventName": "<eventName>",
   "payload": {
   }
}

```

</td></tr></tbody>
</table>    For more information, see [Define and bind client scripts to components](https://www.servicenow.com/docs/access?context=define-client-scripts&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).


