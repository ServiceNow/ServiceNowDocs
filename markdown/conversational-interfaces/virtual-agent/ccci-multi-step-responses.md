---
title: Multi-step responses
description: An example of multi-step response is a set of images in a carousel or a date control.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Supported Virtual Agent and Agent Chat features for custom chat integrations, Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Multi-step responses

An example of multi-step response is a set of images in a carousel or a date control.

Multipart Control richControl has the following attributes, which can be used to transform control.

-   content: Rich Control which must be presented in current step.
-   navigationBtnLabel: Label for "next" or "more" button for user to click to move to next step.

Example:

```
{
        uiType: "MultiPartOutput",
        group: "DefaultMultiPartOutput",
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

## Outbound transformation script

```
(function execute(inputs, outputs) {

    try{
      var richControl = inputs.rich_control;
      var payload = inputs.payload;
  
      var content = richControl.content;
      var navigationBtnLabel = richControl.navigationBtnLabel;
      var uiType = content.uiType;
      var partResult = null;
  
      switch (uiType) {
        case "OutputText":
          partResult = sn_fd.FlowAPI.executeActionQuick('example_default_text_outbound_transformer', {
              rich_control : content,
              payload : payload
            });
          break;
        case "OutputLink":
          partResult = sn_fd.FlowAPI.executeActionQuick('example_default_output_link_outbound_transformer', {
              rich_control : content,
              payload : payload
            });
          break;
        case "OutputImage":
          partResult = sn_fd.FlowAPI.executeActionQuick('example_default_image_outbound_transformer', {
              rich_control : content,
              payload : payload
            });
          break;
        case "OutputHtml":
          partResult = sn_fd.FlowAPI.executeActionQuick('example_default_html_outbound_transformer', {
              rich_control : content,
              payload : payload
            });
          break;
        default:
          break;
      }
      partResult =  partResult + addButtonMore(navigationBtnLabel)
      outputs.result = JSON.stringify(outActivity);
    }
    catch(e){
      gs.error("Error in default multipart outbound transformer : " + e.message);
      throw e; 
    }
  
  })(inputs, outputs);
```

## Inbound transformation script

```
  (function execute(inputs, outputs) {
    try {
      var requestContext = inputs.request_context;
      var typedValue = requestContext.typed_value;
      outputs.result = typedValue;
    } catch(e) {
       gs.error("Error in default multipart inbound transformer : " + e.message);
       throw e; 
    }
  })(inputs, outputs);
```

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

