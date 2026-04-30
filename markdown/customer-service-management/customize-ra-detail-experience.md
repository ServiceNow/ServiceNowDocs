---
title: Customize a guidance detail experience in the UI Builder
description: Customize how your detail experience looks in the contextual side panel or in a subtab of the Recommended Actions card using UI Builder. The detail experience can include things such as user inputs and drill down actions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating guidance and field recommendation in Recommended Actions, Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Customize a guidance detail experience in the UI Builder

Customize how your detail experience looks in the contextual side panel or in a subtab of the Recommended Actions card using UI Builder. The detail experience can include things such as user inputs and drill down actions.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author and ui\_builder\_admin, admin

## About this task

You begin by creating a UI page variant of a guidance detail experience. When you create a UI page variant from a page template, you start with a base structure that you can customize. By configuring the components and using the component properties, you can change how your detail experience looks in the contextual side panel or in a subtab.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Action Types** &gt; **Guidances**.

2.  Select a guidance from the Guidances list.

3.  Select **Create detail UI** to create a UI page variant of a guidance detail experience.

    This page includes an empty container with the properties listed in the following table.

    |Property|Description|
    |--------|-----------|
    |guidanceInputs|The inputs required to perform the guidance.|
    |guidanceOutputs|The outputs of the guidance.|
    |status|The status of the guidance.|
    |guidanceMessage|The message for the detail experience.|
    |guidanceActions|The guidance actions in the detail view.|
    |errorMessages|The error message to display when the recommendation fails to display.|

    The following example shows properties and their sample values for the detail experience.

    ```
    {
        "guidanceInputs": {},
        "guidanceOutputs": {
            "meta": []
        },
        "status": "waiting",
        "guidanceMessage": "",
        "guidanceActions": [
            {
                "label": "Attach",
                "action_sys_id": "1e8392aa436f0210f81d92621ab8f291",
                "variant": "primary",
                "isExecuted": false,
                "completionMessage": "Knowledge article successfully attached.",
                "action_behaviour": "contextual_side_panel",
                "primary": true
            }
        ],
        "errorMessage": "",
        "actionConfigurations": {},
        "guidanceId": "",
        "tableName": "sn_customerservice_case",
        "bare": true,
        "scrollable": "none"
    }
    
    ```

4.  Select **Edit detail in UI Builder**.

    The UI page variant opens in UI Builder, where you can add and configure components to customize the look and feel of the detail experience. For more information, see [Working with components in the UI Builder](https://www.servicenow.com/docs/access?context=work-components&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

5.  Bind the preview experience properties to your custom detail UI.

    Data bindings are located in the **Config** tab of the configuration panel in UI Builder. For more information, see [Data resources in UI Builder](https://www.servicenow.com/docs/access?context=data-resources&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

6.  Add and bind scripts to components in your custom detail UI to dispatch events by using an event handler to execute, skip, or mark complete a recommendation with a corresponding payload.

<table id="table_grp_flc_xvb"><thead><tr><th>

Events handled

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GUIDANCE\_ACTION\_CLICKED

</td><td>

The action that is selected. This event passes the action selected to the payload.```
api.emit( 
  ‘GUIDANCE_ACTION_CLICKED’,{ 
        model: {
               fields: [{'name': 'input',
               'value':  '100'}]
               },
        action: api.context.props.guidanceActions.find(action => action.label == "guidance action label"); 
    } 
);
```

**Note:** In the `guidanceActions[n]` property in the response, provide the index number of the action that you want to apply.

</td></tr><tr><td>

SKIP\_GUIDANCE

</td><td>

Skips the guidance.```
api.emit(
   ‘SKIP_GUIDANCE’
);

```

</td></tr><tr><td>

GUIDANCE\_MESSAGE\_PUBLISHED

</td><td>

Passes data to an upstream application.```
api.emit( 
  ‘SN_GUIDANCE_EXPERIENCE_CONNECTED#GUIDANCE_MESSAGE_PUBLISHED’,
    { 
     name:'decision-tree-payload'
     jsonPayload: jsonObject
    } 
);

```

</td></tr><tr><td>

GUIDANCE\_MARK\_COMPLETE

</td><td>

Marks a custom guidance as completed.```
api.emit(
  'GUIDANCE_MARK_COMPLETE'
);
```

</td></tr><tr><td>

GO\_BACK\_GUIDANCE

</td><td>

Goes back to the previous node in a decision tree.```
api.emit(
   ‘GO_BACK_GUIDANCE’
);

```

</td></tr><tr><td>

ACTION\_TRIGGERED\_PROPAGATION

</td><td>

Enables you to add UI specific behavior for guidance actions. This event propagates the payload details to the parent where this event can be handled.```
api.emit(
    ‘SN_NEXT_BEST_ACTION_LIST_CONNECTED #ACTION_TRIGGERED‘, {
   "actionSysId":api.context.props.guidanceId,
   "actionName": api.context.props.actionConfigurations[api.context.props.guidanceId][“actionName”]
   "actionType": "guidance",
   "eventName": "<eventName>",
   "payload": {}

```

</td></tr></tbody>
</table>    For more information, see [Define and bind client scripts to components](https://www.servicenow.com/docs/access?context=define-client-scripts&version=zurich&pubname=zurich-application-development&ft:locale=en-US).


