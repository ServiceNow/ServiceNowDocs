---
title: Refine the source type structure in Health Log Analytics
description: Fine-tune how Health Log Analytics reads your inner log messages and detects anomalies by customizing the extracted properties in the source type structure.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [ServiceNow, Health Log Analytics, HLA, source type structure, adjust, inner log messages, anomalies, customize, properties, JavaScript]
breadcrumb: [Source type structure adjustment, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Refine the source type structure in Health Log Analytics

Fine-tune how Health Log Analytics reads your inner log messages and detects anomalies by customizing the extracted properties in the source type structure.

## Before you begin

For an overview, see [Source type structure adjustment in Health Log Analytics](../concept/hla-source-type-structure-adjustment.md).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Inputs** &gt; **Source Type Structure**.

2.  Open a record.

    **Note:**

    -   Health Log Analytics automatically separates the transport header from the inner log message when **Auto extraction** is selected \(default\).
    -   Health Log Analytics fetches log samples automatically the first time the **Source Type Structure** form displays. In subsequent sessions, fetch the latest samples by selecting **Refresh Samples**.
3.  Get AI-powered classification and labeling suggestions.

    AI can classify parsed log properties and suggest appropriate labels.

    1.  Select **Suggest classifications \(AI\)** from the **Source Type Structure** page.

        On the **Key/Value Mapping** tab, AI-suggested classifications and labels appear in the **AI-suggested classification** and **AI-suggested label** columns.

    2.  Review the suggestions.
    3.  In the **Classification** and **Labels to assign** columns, select your preferred classifications and labels from the lists.
4.  View how the current JavaScript function affects the log lines.

    1.  Add a sample message in the **Test manual sample** field.

    2.  Select **Go**.

    3.  In the **Key/Value Mapping** tab, note how the JavaScript function affects the log lines.

5.  In the **Raw input sample** field, choose a log message.

    When you test your JavaScript function, Health Log Analytics uses this sample message to show the joint effect of automatic extraction and the JavaScript function on the log lines.

    The following fields are read only:

<table id="table_i4l_z4z_fnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Duration \(ms\)

</td><td>

The processing time of all samples, in milliseconds.

</td></tr><tr><td>

Dropped

</td><td>

The total number of logs dropped in all the samples.

</td></tr><tr><td>

Errors

</td><td>

The total number of errors that occurred in all the samples.

</td></tr><tr><td>

Timestamp extraction failures

</td><td>

The number of timestamp extraction failures that occurred in all the samples.

</td></tr><tr><td>

Severity extraction failures

</td><td>

The total number of severity extraction failures that occurred in all the samples.

</td></tr><tr><td>

Message extraction failures

</td><td>

The total number of message extraction failures that occurred in all the samples.

</td></tr><tr><td>

Lengthy properties

</td><td>

The total number of lengthy properties in all the samples. Lengthy properties are properties with more than 256 characters.

**Note:** Because Health Log Analytics doesn't extract such properties, they aren’t indexed as keywords in Elasticsearch.

</td></tr></tbody>
</table>6.  Define a JavaScript function that customizes automatically extracted properties or adds properties to the source type structure.

    1.  In the JavaScript console, either change the provided default JavaScript function, modify an existing custom JavaScript function, or define a new one.

        **Note:** In addition to the default JavaScript function, Health Log Analytics provides several JS function templates for refining the source type structure. The templates can act as a starting point for your custom script code. This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

<table id="table_uwr_pvg_3pb"><thead><tr><th>

JS function templates

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Extract Key\_Values Using Regex

</td><td>

Script used for parsing logs into a series of key:value pairs by using regular expressions to identify specific regex patterns. Depending on the log data being sent to the source type, it parses either the inner message or the full log line. You can view how the data appears in the samples that are loaded into the source type structure.

 This process is iterative. It ’s repeated until all key:value pairs are found.

</td></tr><tr><td>

Extract Key\_Values Using split-regex

</td><td>

Script used for parsing logs into a series of key:value pairs by using regular expressions to identify specific regex patterns. This process captures the values in a LIST form first, then uses the Java split function to create the key:value pairs.

 Depending on how the data appears in the raw input, this function might be more efficient than `Extract Key_Values Using Regex`. The raw input is either the inner message that header detection passes on, or the full raw log. If header detection is turned off or doesn't work on that particular log, the full raw log is used.

</td></tr><tr><td>

JSON Parse - flatten

</td><td>

Script used for extracting JSON information that is part of another text string from the raw input. For example, the information could be a JSON request written as part of a longer inner message.Inner JSON sections are difficult to split. In such cases, this script can be used to "flatten" or parse out the key:value pairs.

</td></tr><tr><td>

Extract a new field from raw input

</td><td>

Script that extracts a new field from the raw input, using a regular expression with capture groups to identify the new field's pattern.

</td></tr><tr><td>

Parse XML format

</td><td>

Script used for extracting key:value pairs from the XML by using a regular expression to identify the XML format.This process is iterative. It's repeated until all key:value pairs are found.

</td></tr><tr><td>

Set numerical severity level as textual values

</td><td>

Script used for converting numerical severity values to their corresponding textual severity values.**Note:** To enable the system to identify the severity level of a log correctly, severity must be given in text format. No numerical severity values should remain.

</td></tr><tr><td>

Trim function

</td><td>

Script used for removing the double quotes that surround the string from VALUE. You can adapt this function to remove any other characters that surround the output VALUE of a key:value pair.

</td></tr></tbody>
</table>        The JavaScript function for refining the source type structure uses the following objects:

        |Object|Description|
        |------|-----------|
        |sample|The inner message extracted from the sample message.|
        |output|Object that contains the key-value pair map.|

    2.  Test the JavaScript function by selecting **Test**.

    3.  View the outcome of the JavaScript function in the related lists and modify if needed.

        -   The **Key/Value Mapping** tab shows the effect of your JavaScript function combined with the system's automatic extraction on your raw input sample.

            Modify keys where appropriate.

            -   The **Classification** field enables you to reset the classification of a property. The available types are:

<table id="table_y5w_hky_vnb"><thead><tr><th>

Type

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Meter

</td><td>

A property with this classification detects anomalies in the number of times the property appears in each log message. It presents changes in the quantity of this value as part of Automatic Root Cause analysis. **Note:** Properties classified as Meter consume resources.

</td><td>

Status codes, response codes, actions, or patterns

</td></tr><tr><td>

Gauge

</td><td>

A property with this classification detects anomalies in a numerical value that is reported continuously.**Note:** Properties with a classification of Gauge consume resources.

</td><td>

CPU, memory, or response time

</td></tr><tr><td>

Timeless Gauge

</td><td>

A property with this classification detects anomalies in a numerical value that is not reported continuously. The system notifies about an anomaly in this value regardless when the anomaly occurred.**Note:** This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

 

</td></tr><tr><td>

Automatic Root Cause \(ARC Only\)

</td><td>

A property with this classification reports the property as part of the Automatic Root Cause analysis of another anomaly and not as an anomaly by itself.

</td><td>

User name, IP addresses, application components, or datacenter

</td></tr><tr><td>

Invalid

</td><td>

A property with this classification isn’t calculated or shown in the Automatic Root Cause analysis. **Note:** Properties classified as Invalid save resources.

</td><td>

 

</td></tr></tbody>
</table>            -   The **Labels to assign** field enables you to set a property on a label.

<table id="table_z5w_hky_vnb"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Timestamp

</td><td>

The property that holds the timestamp of the event. **Note:** If automatic [header properties detection](../concept/hla-header-detection.md) is enabled and the source type lacks a timestamp, the system extracts the timestamp from the transport header. If header detection is turned off or doesn't work for the relevant log lines in the data input, all log lines must have proper timestamps.

</td></tr><tr><td>

Severity

</td><td>

The property that represents the severity level of the log.

</td></tr><tr><td>

Message

</td><td>

The log message. The system uses this property to identify textual patterns in the data.

</td></tr><tr><td>

Host

</td><td>

The property that represents the host from which the event was sent. **Note:** If automatic [header properties detection](../concept/hla-header-detection.md) is enabled and the source type lacks a host, the system extracts the host from the transport header. If header detection is turned off or doesn't work for the relevant log lines in the data input, all log lines must have a host.

</td></tr><tr><td>

External ID

</td><td>

The property that serves as a unique identifier for this event type. For example, Event ID in Windows event log.

</td></tr></tbody>
</table>            -   The **Rename key** field enables you to rename the key.
        -   The **Outcome Key-Value** tab shows how your JavaScript function processed the data.
        -   The **Data Input Mappings** tab shows the data input mappings for the current source type.

            The **Last event time** column on this tab shows the last date and time that the AI engine processed a log for the data input mapping. The system refreshes this information every five minutes. Knowing when the last log was processed for this data input mapping makes it easier to verify that log data is streaming.

        -   The remaining tabs show errors, message extraction failures, severity extraction failures, timestamp extraction failures, and lengthy properties.
        **Note:** If your new JavaScript function isn’t behaving as expected, you can revert to the last published one by selecting the **Revert JS Function** related link.

    4.  Make any necessary adjustments and then test the JavaScript function again.

7.  Select the **Save template** option to save the JavaScript function.

    You can either save the JavaScript function as a new template or overwrite the currently selected template.

    -   To save the JavaScript function as a new template, enter a new name in the **Template name** field.
    -   To overwrite the template currently selected in the **JS function templates** field, leave the **Template name** field empty.
8.  Select **Publish** to save the JavaScript function to the database.


## Result

When the JavaScript function is published, Health Log Analytics uses it to fine-tune how it reads your inner log messages and detects anomalies.

The new script is automatically added to the list of JS function templates from which you can choose. This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## What to do next

Continue with the [remaining data input setup tasks](../concept/hla-data-input-setup-extra.md): Verify that all your log sources are present and active, and add timestamp formats if necessary.

**Parent Topic:**[Source type structure adjustment in Health Log Analytics](../concept/hla-source-type-structure-adjustment.md)

**Related topics**  


[Source type structure adjustment in Health Log Analytics](../concept/hla-source-type-structure-adjustment.md)

