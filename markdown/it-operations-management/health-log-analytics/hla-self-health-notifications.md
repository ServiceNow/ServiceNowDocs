---
title: Health Log Analytics self-health checks, notifications, and proposed actions
description: Health Log Analytics provides self-health checks, notifications, and proposed problem-solving steps.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Health Log Analytics self-health checks, notifications, and proposed actions

Health Log Analytics provides self-health checks, notifications, and proposed problem-solving steps.

|Self-health check|Notification|Proposed action|
|-----------------|------------|---------------|
|Maximum AI engine queue size exceeded|The AI engine is running at overcapacity \(size=%s, threshold=%s, duration=%s\). As a result, the accuracy of anomaly detection might deteriorate.|Contact ServiceNow support.|
|High rate of unclassified errors in %s %s|"%s %s has a high rate of unclassified errors and is failing frequently.|Contact ServiceNow support.|
|Errors invoking glide API|Errors invoking '%s' for %s.|Contact ServiceNow support.|
|Log size limitation was exceeded|Log messages from %s: %s are being dropped because the log size limitation was exceeded.|If the difference is minor, increase the log size limitation by adjusting the property **mid.data\_inputs.max\_length\_bytes\_per\_stream** on the MID Server Properties form. If the logs are too long or multi-line, you can also modify the log size at the source of the logs.|
|Excessive data volume for data input %s.|The data volume for data input %s is too high. Log messages are being discarded.|Contact ServiceNow support.|
|Log messages are being dropped due to failed auto-structuring|Log messages are being dropped because auto-structuring of Source Type %s failed.|In the Source Type, find out what could be causing auto-structuring to fail. Inspect the error logs to determine which component or parsing action is failing.|
|Excessive number of script errors per second in %s:%s|The rate of script errors in %s:%s is too high.|Review the JavaScript Parsing Error in the source given in the message: Data Input Mapping Screen or Source Type Structure Screen.|
|Log messages that exceed the permitted number of properties are being discarded|The source type %s contains multiple log messages with too many properties. Such log messages are discarded. Review the Source Type Structure record.|On the relevant Source Type Structure record, review the properties that are being extracted. Check for script loops or conditions that might cause too many properties to be created. Avoid using a dynamic property name. For more information, see [Refine the source type structure in Health Log Analytics](../task/hla-source-type-structure-refine.md).|
|Too many clusters are being generated. The accuracy of anomaly detection might deteriorate.|Too many clusters are being generated for Source Type %s. As a result, the accuracy of anomaly detection might deteriorate.|Inspect the created patterns and verify that the Message label is being assigned correctly. On the Source Type Structure form, review the Message property.|
|Sources are being created at a very high rate|Sources are being created at a very high rate. Data input %s was stopped automatically.|On the Data Input Mapping form, inspect the Mapping script and fix any JavaScript errors that might cause too many sources to be created.|
|Source Types are being created at a very high rate|Source Types are being created at a very high rate. Data input %s was stopped automatically.|On the Data Input Mapping form, inspect the Mapping script and fix any JavaScript errors that might cause too many Source Types to be created.|
|Metrics are being created at a very high rate|Source Type %s is generating too many metrics. The properties %s were automatically classified as invalid.|On the Source Type Structure form, observe the metrics being generated. Make sure that the Metric label is assigned only to the required properties. A dynamic property name or inaccurate JavaScript function can cause too many properties to be generated.|
|Processing duration of REST calls in the AI Engine is too high|Processing of REST calls in the AI Engine is taking too long.|Contact ServiceNow support.|
|The number of log messages being discarded is too high|Too many log messages are being discarded from source %s.|Review the log retention settings. Verify that the log lines timestamp is correct and does not represent a future or past time outside the retention period.|
|Auto-structuring is slowing down the AI engine|Auto-structuring is slowing down the AI engine.|Contact ServiceNow support.|
|Log messages are being dropped due to a timestamp parsing failure|Log messages from %s %s are being dropped due to a timestamp parsing failure. Search for 'Failed parsing timestamp from log message' in the logs for the relevant Service instance and Component and fix the issue.|On the Data Input Mapping form, locate the extracted timestamp. If it is missing, navigate from the form to the relevant Source Type Structure and open the Timestamp Parsing Error tab. The tab displays the issue that led to the parsing error. Fix the issue.|
|No memory consumption drop|Memory consumption hasn’t dropped in the last few minutes.|Contact ServiceNow support.|
|Pings the Elasticsearch clusters' health endpoints to determine the health of the connection|Elasticsearch connectivity issues.|Contact ServiceNow support.|
|Uses the Metric base client connection check to determine the health of the connection|Metric base connectivity issues.|Contact ServiceNow support.|
|Uses the Glide client connection check to determine the health of the connection|Glide connectivity problems.|Contact ServiceNow support.|
|The data input is in Failed state|The data input %s failed to stream logs.|On the Data Input form, check the connection to the MID Server and review the error message.|

**Parent Topic:**[Health Log Analytics reference](../concept/hla-reference.md)

