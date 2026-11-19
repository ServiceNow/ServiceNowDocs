---
title: Source type structure adjustment in Health Log Analytics
description: Health Log Analytics enables you to reclassify auto-classified properties and change auto-mapped labels. These adjustments help Health Log Analytics machine learning to better understand your priorities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/health-log-analytics/hla-source-type-structure-adjustment.html
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [ServiceNow, Health Log Analytics, HLA, source type structure, change labels, classification, classifying, reclassify, source type]
breadcrumb: [Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Source type structure adjustment in Health Log Analytics

Health Log Analytics enables you to reclassify auto-classified properties and change auto-mapped labels. These adjustments help Health Log Analytics machine learning to better understand your priorities.

## What HLA does automatically

HLA automatically separates the transport header from the inner log message and sends only the inner log message to the source type structure. The system extracts properties from incoming log messages and auto-maps labels to source type fields.

-   Classification determines how the HLA engine analyzes and processes each field. Available classifications are: METER, GAUGE, ARC\_ONLY, HISTOGRAM, INVALID.
-   Labels tell HLA what role a field plays in the log structure. Available labels are: MESSAGE, HOST, TIMESTAMP, SEVERITY, EVENT-ID.

Reviewing and, if necessary, modifying automatically mapped labels and auto-classified properties in the source type structure verifies the HLA engine interprets log fields correctly.

**Note:** Because a single data input can contain multiple source types, HLA structures log data by source type rather than by data input.

## AI-assisted log parsing with ServiceNow Otto

AI-assisted log parsing using ServiceNow Otto provides recommendations for optimal classifications and labels for parsed log properties based on your log patterns. This approach reduces manual effort and improves accuracy without requiring custom JavaScript functions.

To enable this capability, activate the integration with AI-powered capabilities by selecting the **Activate with AI** option. This option enables AI-powered automatic parsing and mapping of log data. When the integration is activated, ServiceNow Otto collects and analyzes log data and displays suggested classifications and labels for your source type properties. An AI icon indicates that AI is active. Verify that ServiceNow Otto correctly classified and labeled your log properties. You can override the suggestions by selecting a different classification or label from each list, if needed.

While ServiceNow Otto generates a parser automatically for a source type, a notification banner on the **Source Type Structure** page shows the current status of the generation process.

## Example

The following example shows how to modify values of extracted properties in the source type structure with JavaScript.

Consider the following log:

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

The sample code contains `"key":"value"` pairs: The key is the property name. The value is the property value.

The key "message" in the sample has the following value: `"This is the extracted message. This part of the message includes superfluous content and values"`.

If you wanted your logs to contain only the meaningful part of that message, you would add JavaScript code instructing the system to extract only that part:

```
//Added JavaScript to extract only the first sentence in the message! if (output['message'] != null){ output['message'] = output['message'].slice(0, output['message'].indexOf("\.")); } (edited) 
```

You could use the same logic to reclassify a value. For example, if the key "Computer" is insignificant, you could set its value to "Invalid."

For more information about the source type structure, see the [Source Type Structure – Labels &amp; Classifications \[KB0863562\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0863562) article in the Now Support Knowledge Base.

**Note:** You can reactivate the learning mode for a source type structure to use the HLA engine's learning functionality again after the initial learning period becomes outdated. On the **Source Type Structure** form, select **Relearn** to reset parsing, extraction, classification, and labeling for the source type structure and restart the learning process.

-   **[Refine the source type structure in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-source-type-structure-refine.md)**  
Fine-tune how Health Log Analytics reads your inner log messages and detects anomalies by customizing the extracted properties in the source type structure.

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-implement.md)

**Related topics**  


[Refine the source type structure in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-source-type-structure-refine.md)

