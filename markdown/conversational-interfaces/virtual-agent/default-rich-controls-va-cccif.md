---
title: Default input and output rich controls for a custom chat integration
description: Input and output rich controls must be mapped to your custom chat integration in the Custom Adapter Configurations \[sys\_cs\_custom\_adapter\_config\] table. If a rich control is missing an outbound transformer implementation, a response is not served to the end user and that user may get an unsatisfactory chat experience.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Default input and output rich controls for a custom chat integration

Input and output rich controls must be mapped to your custom chat integration in the Custom Adapter Configurations \[sys\_cs\_custom\_adapter\_config\] table. If a rich control is missing an outbound transformer implementation, a response is not served to the end user and that user may get an unsatisfactory chat experience.

The following default rich controls map to input and output rich controls. The **uiType** parameter refers to a topic control used to build conversations in Virtual Agent Designer.

<table id="table_rqm_lvn_qmb"><thead><tr><th>

Rich control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ActionRichControl

</td><td>

This component handles the different events and actions that occur in a conversation. Some actions may not apply to all channels. For example, StartSpinnerActionMsg is ignored in SMS.ServiceNow® Virtual Agent produces the following types of action messages through this framework. The custom chat interface only recognizes certain action message types.

 -   SeparatorActionMsg \|\|actionMsg instanceof
-   SystemActionMsg \|\|actionMsg instanceof
-   TopicFinishedActionMsg \|\|actionMsg instanceof
-   SwitchToVirtualAgentActionMsg \|\|actionMsg instanceof
-   SwitchConversationActionMsg \|\|actionMsg instanceof
-   ChatSubHeaderActionMsg \|\|actionMsg instanceof
-   StartSpinnerActionMsg \|\|actionMsg instanceof EndSpinnerActionMsg
-   SubscribetoSupportQueue \|\|actionMsg instanceof
-   SubscribeToChatPresence \|\|actionMsg instanceof
-   SwitchToLiveAgentActionMsg \|\|actionMsg instanceof

 ActionRichControl wraps these messages inside the **actionMsg** element. So, a single outbound transformer for ActionRichControl can handle all of these messages. There is no need for an inbound transformer for this component.

</td></tr><tr><td>

**agentInfo** parameter

</td><td>

If the rich control is sent from a live agent, then the **agentInfo** attribute is added to the rich control.Example:

```
{
     uiType: "someType",
     group: "someGroup"
     agentInfo: { sentFromAgent: true }  // please note that this object may contain more info in subsequent releases.
     ...
} 
```

</td></tr><tr><td>

DefaultPicker

</td><td>

Maps to [File Picker](va-file-picker.md), Topic Picker, and [Boolean](va-boolean-user-input.md) controls.Example:

```
{
    uiType: "Picker/TopicPicker/Boolean",
    group: "DefaultPicker",  
    nluTextEnabled: true/false,
    promptMsg: "", // optional (needed for TopicPicker)
    label: "The question for the list",   // always filled
    itemType: "Picture/List"  // needed to user key to expect picture attached
    options: [
        {
            label: "display label prompt",
            value: "the value required to satisfy the question",
            description: "a description of value_1 item"
	    attachment: "www.foo",
            enabled: true/false
        }, 
	...
    ]
}
```

 The optional **order** parameter lets you specify the order in which promoted topics should display. For example:

 ```
"options": [
    {
      label: "Check IT Ticket Status",
      value: "55720b465bf0201024f11fc40a81c72d",
      order: 100,
      enabled: true
    },
    {
      label: "Live Agent Support",
      value: "ce2ee85053130010cf8cddeeff7b12bf",
      order: 200,
      enabled: true
    },
    {
      label: "Open IT Ticket 2",
      value: "2a46cffbc7602010v088bbf603c260a7",
      order: 300,
      enabled: true
    }
]
```

</td></tr><tr><td>

DefaultText

</td><td>

Maps to [Input Text](va-text-input.md), [Output Text](va-text-response.md), and File Upload controls.Example:

```
{
    uiType: "InputText/OutputText/FileUpload/Picture",
    group: "DefaultText", 
    required: true/false,
    nluTextEnabled: true/false,
    itemType: "file/image/inputtext/outputtext",
    maskType: "SECURE/SENSITIVE/NONE"  // null except for InputText/OutputText
    label: "The Question?"        
}
```

</td></tr><tr><td>

DefaultDate

</td><td>

Maps to [Date and Time](va-date-time-input.md) controls.```
{
    uiType: "Date/DateTime/Time",
    group: "DefaultDate", 
    required: true/false,
    nluTextEnabled: true/false,   
    label: "The Question?"
     
}
```

</td></tr><tr><td>

DefaultOutputLink

</td><td>

Maps to [link response](va-link-output.md) controls.Example:

```
{
    uiType: "OutputLink",
    group: "DefaultOutputLink",
    label: "link label",
    header: "link header",
    type: "link",
    value: {
        action: "www.foo",
    }	
}
     
}
```

</td></tr><tr><td>

DefaultOutputImage

</td><td>

Maps to [image response](va-image-output.md) controls.Example:

```
{
    uiType: "OutputImage",
    group: "DefaultOutputImage",
    value: "www.foo"
}
```

</td></tr><tr><td>

DefaultOutputCard

</td><td>

Maps to [card response](va-card-output.md) controls.Example:

```
{
    uiType: "OutputCard",
    group: "DefaultOutputCard",
    templateName: "Card",
    data: "some json data string"
}
```

</td></tr><tr><td>

DefaultOutputHtml

</td><td>

Maps to [HTML response](va-html-output.md) controls.Example:

```
{
    uiType: "OutputHtml",
    group: "DefaultOutputHtml",
    style: "inline",
    height: 100,
    width: 100,
    value: "<div>html</div>"
}
```

</td></tr><tr><td>

DefaultOutputTable

</td><td>

Maps to [table response](table-bot-response.md) controls.Example:

```
{
    uiType: "OutputTable",
    group: "DefaultOutputTable",
    label: "Table Title",
    headers: ["Column 1", "Column 2"],
    navigationBtnLabel: "See next",
    data: [
        ["foo1", "foo2"],
        ["bar1", "bar2"]
    ]
}
```

</td></tr><tr><td>

DefaultGroupedPartsOutputControl

</td><td>

Maps to [multi-response](va-multi-flow-output.md) controls.Example:

```
{
    uiType: "GroupedPartsOutputControl",
    group: "DefaultGroupedPartsOutputControl"
    groupPartType: "Link",
    header: "header message",
    values: [
	{
	    action: "www.foo",
	    description: "description",
	    label: "link_1 label",
	    context: "ITSM"
	},
	...
    ]
}
```

</td></tr><tr><td>

DefaultMultiPartOutput

</td><td>

Maps to [multi-response](va-multi-flow-output.md) controls.Example:

```
{
    uiType: "MultiPartOutput",
    group: "DefaultMultiPartOutput"
    navigationBtnLabel: "Go next",
    content: {
        uiType: "OutputHtml",
        style: "inline",
        type: "html",
        height: 100,
        width: 100,
        value: "<div>html</div>"
     }
}
```

</td></tr><tr><td>

DefaultCustomControl

</td><td>

Maps to [custom controls](va-custom-control-util.md).Example:

```
{
    uiType: "CustomControl",
    group: "DefaultCustomControl",
    name: "The name of the Custom Control (sys_cs_custom_control.name)",
    required: true/false,
    uxComponentDefinitionSysId: "seismicComponentId" // or null if not
    isInput: true/false, // whether to wait for a response value or if just output
    serializedControlData: "User defined JSON from generateControlData function";    
}
```

</td></tr></tbody>
</table>