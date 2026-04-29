---
title: Multi-response output controls
description: Implement controls that involve multiple steps to get user input.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Supported features for custom chat integrations, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Multi-response output controls

Implement controls that involve multiple steps to get user input.

Use the following API to configure context data for multi-output controls.

## Common use cases

1.  To achieve pagination of pickers: page\_no, pagination\_length updated in inbound based on next/previous button is read in outbound.
2.  Step by step response of date picker like first year, then month, and then date selection.

The following APIs are only available in inbound and outbound transformers.

```
sn_cs.VASystemObject.setProviderUserContext( key, contextData, providerAppId, providerUserId);
sn_cs.VASystemObject.getProviderUserContext(key, providerAppId, providerUserId);
sn_cs.VASystemObject.removeProviderUserContext(key, providerAppId, providerUserId);
sn_cs.VASystemObject.removeAllProviderUserContext(providerAppId, providerUserId)
```

The outbound transformer of the picker control can store current page details in user contextData.

```
 var paginationData = {
          "page_index": 1,
          "pagination_length": 2
    }
};
sn_cs.VASystemObject.setProviderUserContext("picker_pagination", paginationData, providerAppId, providerUserId, );
```

The inbound transformer of picker control can get current page details from user contextData.

```
var paginationData = sn_cs.VASystemObject.getProviderUserContext("picker_pagination", providerAppId, providerUserId);
```

## Example code for picker control outbound transformer

```
(function execute(inputs, outputs) {
    var control = inputs.rich_control;
    var payload = inputs.payload;
    var appId = payload.appId;
    var userId = payload.userId;

    var paginationData = sn_cs.VASystemObject.getProviderUserContext('picker_control', appId, userId);
    paginationData = JSON.parse(paginationData);
    //First time when the outbound picker is called when selecting the topic.
    if (paginationData == null) {
        paginationData = {
            'page_index': 1,
            'pagination_length': 5
        };
        sn_cs.VASystemObject.setProviderUserContext('picker_control', paginationData, appId, userId);
    }

    var page_index = paginationData['page_index'];
    var pagination_length = paginationData['pagination_length'];
    var start = (page_index - 1) * pagination_length;
    var end = page_index * pagination_length;

    if (control['options']) {
        var options = control['options'];
        var optionsLength = options.length;
        if (end > optionsLength)
            end = optionsLength;
        var picker = control["label"] + ":";
        if (start > 0)
            picker += "\n" + "*" + ": " + "prev";
        for (var x = start; x < end; x++) {
            gs.log("here " + x + " : " + options[x]);
            picker += "\n" + (x + 1) + ": " + options[x].label;
        }
        if (end < optionsLength)
            picker += "\n" + "#" + ": " + "next";
    }
    outputs.text_message = picker;
})(inputs, outputs);
Example Picker Control Inbound Tranformer
(function execute(inputs, outputs) {

    var request_context = inputs.request_context;
    var rich_control = inputs.rich_control;
    var appId = request_context.appId;
    var userId = request_context.userId;

    var selectedValue = request_context["typed_value"];
    var result = {};
    result["value"] = "";
    result["search_text"] = selectedValue;

    var options = rich_control['options'];

    var paginationData = sn_cs.VASystemObject.getProviderUserContext('picker_control', appId, userId);
    paginationData = JSON.parse(paginationData);

    switch (selectedValue) {
        case 'prev': {
            --paginationData["page_index"];
            result["send_prev_control"] = true;
        }
        break;
    case 'next': {
        ++paginationData["page_index"];
        result["send_prev_control"] = true;
    }
    break;
    default: {
        var selectedIndex = Number(selectedValue) - 1;
        if (paginationData["page_index"] != undefined && paginationData["pagination_length"] != undefined) {
            var highestOptionInPage = paginationData["page_index"] * paginationData["pagination_length"];
            if (selectedIndex >= 0 && selectedIndex < highestOptionInPage) {
                var selectedOption = options[selectedIndex];
                result["value"] = selectedOption.value;
                result["search_text"] = "";
            }
        } else {
            var selectedOption = options[selectedIndex];
            result["value"] = selectedOption.value;
            result["search_text"] = "";
        }
    }
    }
    sn_cs.VASystemObject.setProviderUserContext('picker_control', paginationData, appId, userId);
    outputs.result = result;
})(inputs, outputs);
```

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

