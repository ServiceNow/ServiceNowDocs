---
title: Source type structure adjustment
description: Health Log Analytics enables you to reclassify auto-classified properties and change auto-mapped labels. These adjustments help Health Log Analytics machine learning to better understand your priorities.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, source type structure, change labels, classification, classifying, reclassify, source type]
breadcrumb: [Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Source type structure adjustment

Health Log Analytics enables you to reclassify auto-classified properties and change auto-mapped labels. These adjustments help Health Log Analytics machine learning to better understand your priorities.

Health Log Analytics automatically separates the transport header from the inner log message and sends the inner log message to the source type structure. It extracts properties from incoming log messages and auto-maps labels to source type fields.

Modifying the source type structure and classification is your chance to make sure that the Health Log Analytics AI engine extracts all the properties properly and classifies them appropriately. Because a single data input can contain more than one source type, the system structures log data by source type and not by data input.

For example, consider the following log:

```
{
  "TenantId": "abc-01-02-03-04-05050708091011121314",
  "@timestamp": "2020-08-28T08:29:23.967Z",
  "Computer": "john Doe_computer",
  "EventType_s": "LogMessage",
  "Job_s": "johnDoe_cell",
  "IP_s": "1.00.00.00",
  "message": "This is the extracted message. This part of the message includes superfluous content and values",
  "MessageType_s": "OUT",
  "Timestamp_d": 1598603359017850000,
  "Type": "my_LogMessage_is",
  "_ResourceId": ""
}
```

The sample code contains `"key":"value"` pairs. The key is the property name, and the value is the property value.

The key "message" has the following value: `"This is the extracted message. This part of the message includes superfluous content and values"`. If you wanted your logs to contain only the meaningful part of that message, you would add JavaScript code instructing the system to extract only that part.

```
//Added JavaScript to extract only the first sentence in the message! if (output['message'] != null){ output['message'] = output['message'].slice(0, output['message'].indexOf("\.")); } (edited) 
```

You could use the same logic to reclassify a value. For example, if the key "Computer" is insignificant, you could set its value to "Invalid".

For more information about the source type structure, see the [Source Type Structure – Labels &amp; Classifications \[KB0863562\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0863562) article in the Now Support Knowledge Base.

**Note:** You can reactivate the learning mode for a source type structure if you'd like to use the AI Engine's learning functionality again after the initial learning period has become outdated. On the **Source Type Structure** form, select **Relearn** to reset parsing, extraction, classification, and labeling for the source type structure and start the learning process anew.

-   **[Refine the source type structure](../task/hla-source-type-structure-refine.md)**  
Fine-tune how Health Log Analytics reads your inner log messages and detects anomalies by customizing the extracted properties in the source type structure.

**Parent Topic:**[Set up data inputs for Health Log Analytics manually](../task/hla-data-input-setup-manual.md)

