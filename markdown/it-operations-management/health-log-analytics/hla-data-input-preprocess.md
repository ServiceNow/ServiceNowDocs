---
title: Edit raw log data before processing in Health Log Analytics
description: You can modify raw log data and drop or break up log messages before they are treated in the MID Server, and therefore before Health Log Analytics maps and structures them. For example, you could prevent sensitive data from reaching Health Log Analytics by replacing user names and passwords with an asterisk \(\*\).
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [ServiceNow, Health Log Analytics, HLA, change raw log data, edit raw log messages, user names, passwords, disable raw log samples]
breadcrumb: [Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Edit raw log data before processing in Health Log Analytics

You can modify raw log data and drop or break up log messages before they are treated in the MID Server, and therefore before Health Log Analytics maps and structures them. For example, you could prevent sensitive data from reaching Health Log Analytics by replacing user names and passwords with an asterisk \(\*\).

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input Preprocessor**.

2.  Open a record.

    **Note:** The first time the preprocessing form is displayed, Health Log Analytics fetches log samples automatically. In subsequent sessions, fetch fresh samples manually by selecting **Refresh Samples**.

3.  Prevent showing log samples that are taken from your organization’s raw logs by selecting **Disable raw log samples**.

    Select this option if you don't want to expose your logs to Health Log Analytics.

4.  View how the current JavaScript function affects the log lines.

    1.  Add a sample message in the **Test manual sample** field.

    2.  Select **Go**.

    3.  Note how the JavaScript function affects the log lines.

5.  In the **Raw input samples** field, choose a log sample that will show the effect of your new JavaScript function on log lines when you test it.

6.  Define a JavaScript function that modifies your raw log data before Health Log Analytics maps and structures it.

    **Note:**

    \(ACC data inputs only\) When the Agent Client Collector switches to a different MID Server to provide failover protection, it must switch to a different ACC data input. Therefore, all ACC data inputs must have the same JavaScript function. Health Log Analytics provides the latest published JavaScript function to all existing and future ACC data inputs, replacing the previous script. This feature is supported in the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). For information about failover protection in Agent Client Collector Log Analytics \(ACC-L\), see [Agent Client Collector Log Analytics](../../agent-client-collector/concept/acc-log-analytics.md).

    1.  In the JavaScript console, either change the provided default JavaScript function, modify an existing custom JavaScript function, or define a new one.

        **Note:** In addition to the default JavaScript function for data preprocessing, Health Log Analytics provides a JavaScript function template named Scrubbing. This JavaScript function removes personally identifiable information such as email addresses, social security numbers, and passwords, from the raw log data. The template can act as a starting point for your custom script code. This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

        **Note:** \(ACC data inputs only\) Make sure that your JavaScript function can be used to handle data streamed by all ACC data inputs.

        JavaScript functions for preprocessing raw log data use the following objects:

        -   Signature: function process\(sample, metadata\)

<table id="table_krp_n31_24b"><thead><tr><th>

Object

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sample

</td><td>

The current log sample.

</td></tr><tr><td>

metadata

</td><td>

Object that contains the event stream. To access the event stream, call the metadata.eventStream function. Because event stream is an object, you can access each of its properties by calling the metadata.eventStream.origin or metadata.eventStream.LocalPort functions.

 The list of available event stream properties is available in the **Event Stream: access via metadata** tab.

</td></tr></tbody>
</table>        -   Return type and structure

            **Note:** The JavaScript function returns a map of two entries. Do not change this return structure.

            |Object|Description|
            |------|-----------|
            |modifiedInput|The current log message after the JavaScript function has modified the original message. If null, the original log message is used.|
            |splitEvents|Array of log messages after the JavaScript function has divided the original message.|

        -   To discard a log message, call `return drop()`.
    2.  Test the JavaScript function by selecting **Test** and viewing the outcome on your log sample in related lists.

        |Tab|Description|
        |---|-----------|
        |Outcome|The result of running the JavaScript function on your log sample.|
        |Event Stream: access via metadata|The key-value pairs that present the event stream metadata.|
        |Failures|The log samples on which the JavaScript function failed to run successfully.|

        **Note:** If your new JavaScript function is not behaving as expected, you can revert to the last published one by selecting the **Revert JS Function** related link.

    3.  Make any necessary adjustments and then test the JavaScript function again.

7.  Select the **Save template** option to save the JavaScript function.

    You can either save the JavaScript function as a new template or overwrite the currently selected template.

    -   To save the JavaScript function as a new template, enter a new name in the **Template name** field.
    -   To overwrite the template currently selected in the **JS function templates** field, leave the **Template name** field empty.
8.  Select **Publish** to save the JavaScript function to the database.


## Result

When the JavaScript function is published, Health Log Analytics uses it to pre-process your raw log data before mapping and structuring it.

The new script is automatically added to the list of JS function templates from which you can choose. This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

\(ACC data inputs only\) Health Log Analytics provides the published JavaScript function to all existing and future ACC data inputs. The new JavaScript function replaces the previous script.

## What to do next

Proceed to the **Data Input Mapping** page by selecting the **Go to Mapping** related link. [Map raw data](hla-data-input-mapping.md) that streams into your instance to determine how Health Log Analytics processes it.

