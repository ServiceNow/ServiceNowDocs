---
title: Map raw log data
description: Mapping raw log data that streams into your instance determines how the data is handled. Health Log Analytics automatically structures logs, creates metrics for anomaly detection, and presents alerts based on how your data is tagged.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
keywords: [ServiceNow, Health Log Analytics, HLA, logs, mapping, auto-map, data input, source type, JavaScript]
breadcrumb: [Log data auto-mapping and mapping, Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Map raw log data

Mapping raw log data that streams into your instance determines how the data is handled. Health Log Analytics automatically structures logs, creates metrics for anomaly detection, and presents alerts based on how your data is tagged.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

By default, Health Log Analytics tries to [auto-map](../concept/hla-data-input-automapping.md) every incoming log line to the correct tag. If properties aren't discovered automatically, map the data input sources manually by defining a JavaScript function.

In the JavaScript function, you are required to map only the service instance \(here called application service\). Mapping the component and the source type is optional: Health Log Analytics tries to extract their values from the log data automatically. If the attempt fails, it assigns the default values. If you map the component but not the source type or vice versa, the system tries to extract the missing value from the log data. If it fails, it assigns the component value to the source type or vice versa, depending on which one you have mapped. This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

**Note:**

\(ACC data inputs only\) When the Agent Client Collector switches to a different MID Server to provide failover protection, it must switch to a different ACC data input. Therefore, all ACC data inputs must have the same JavaScript function. Health Log Analytics provides the latest published JavaScript function to all existing and future ACC data inputs, replacing the previous script. This feature is supported in the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). For information about failover protection in Agent Client Collector Log Analytics \(ACC-L\), see [Agent Client Collector Log Analytics](../../agent-client-collector/concept/acc-log-analytics.md).

**Note:** You can manipulate raw log data before Health Log Analytics maps and structures it. For more information, see [Edit raw log data before processing](hla-data-input-preprocess.md).

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Mapping** &gt; **Data Input Mapping**.

2.  Open a record.

    **Note:** The first time the Data Input Mapping form is displayed, Health Log Analytics fetches log samples automatically. In subsequent sessions, fetch fresh samples by selecting **Refresh Samples**.

    **Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the Data Input Mapping page. When this happens, contact ServiceNow support.

3.  To forward the complete raw log message, disable automatic header properties detection for this data input by selecting **Disable header detection**.

    For more information, see [Header properties detection](../concept/hla-header-detection.md).

4.  Activate Test mode by setting the **Test mode** value to ON.

    In Test mode, Health Log Analytics doesn't create the source types, sources, or any other objects it creates in the standard flow to avoid blowing up Elasticsearch storage with sample data. For more information, see [Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md).

5.  View how the current JavaScript function affects log lines.

    1.  Add a sample message in the **Test manual sample** field.

    2.  Select **Go**.

    3.  Note how the JavaScript function affects the log lines.

6.  In the **Raw input sample** field, choose a log sample that will show the effect of your new JavaScript function on log lines when you test it.

7.  Define a JavaScript function that maps your data input sources to the correct service instance \(here called application service\), component, and source type.

    **Note:** \(ACC data inputs only\) Make sure that your JavaScript function can be used to handle data streamed by all ACC data inputs.

    1.  In the JavaScript console, either change the provided default JavaScript function, modify an existing custom JavaScript function, or define a new one.

        **Note:** In addition to the default JavaScript function, Health Log Analytics provides JS function templates for data mapping for Linux OS logs streamed with syslog and Windows event logs streamed with Filebeat or with Winlogbeat event logs streamed with Winlogbeat. The templates can act as a starting point for your custom script code. This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

<table id="table_uwr_pvg_3pb"><thead><tr><th>

Template

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Linux OS logs streamed with Syslog

</td><td>

Script used for mapping Linux logs. Maps logs of the various daemons to the correct source types, components, and service instances \(here called application services\).**Note:** Logs must have a syslog wrapper for this JavaScript function to work properly.

</td></tr><tr><td>

Windows Eventlog streamed with Filebeat

</td><td>

Script used for mapping Windows Event Logs streamed with Filebeat. Maps and groups the various Windows services to source types, components, and service instances \(here called application services\).

</td></tr><tr><td>

Windows - Winlogbeat logs streamed with Winlogbeat

</td><td>

Script used for mapping Windows Event Logs streamed with Winlogbeat. Maps the various Windows services to the correct source types, components, and service instances \(here called application services\).

</td></tr></tbody>
</table>        The JavaScript function for mapping raw log data uses the following objects:

        -   Signature: function map\(sample, metadata\)

<table id="table_k1s_br1_24b"><thead><tr><th>

Object

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sample

</td><td>

The current log sample after preprocessing.

</td></tr><tr><td>

metadata

</td><td>

Object that contains: -   Event Stream: Access via: &lt;metadata value&gt;. For example: metadata.eventStream.origin
-   Transform header 1: Access via: &lt;metadata value&gt;. For example: metadata.headers.i1.type
-   Transform header 2: Access via: &lt;metadata value&gt;. For example: metadata.headers.i2.type
-   type Transform header 3: Access via: &lt;metadata value&gt;. For example: metadata.headers.i3.type
-   Fallback Assignment: Access via: &lt;metadata value&gt;. For example: metadata.fallBacks.host


</td></tr></tbody>
</table>            **Note:** You can create and associate multiple services per source type.

        -   Return type and structure

            **Note:** The JavaScript function returns a map of two entries. Do not change this return structure.

<table id="table_z3g_fs1_24b"><thead><tr><th>

Object

</th><th>

Description

</th></tr></thead><tbody><tr><td>

applicationService

</td><td>

The existing application service \(that is, the service instance\) to which this sample will be assigned. **Note:** The service instance must be bound to anomaly alerts related to the log.

</td></tr><tr><td>

component

</td><td>

The component to which this sample will be assigned.

</td></tr><tr><td>

sourceType

</td><td>

The source type to which this sample will be assigned.

</td></tr></tbody>
</table>        -   To discard a log message, call `return drop()`.
    2.  Test the JavaScript function by selecting **Test**.

        Testing the JavaScript function enables you to view the outcome of the script on the log sample. For a description of the displayed fields, see [JavaScript function test outcome fields](../reference/hla-mapping-script-outcome-ref.md).

        **Note:** If your new JavaScript function is not behaving as expected, you can revert to the last published one by selecting the **Revert JS Function** related link.

    3.  Make any necessary adjustments and then test the JavaScript function again.

    4.  Compare the outcome of multiple tests.

        Comparing the test results of several versions of the JavaScript function can help you refine the script until it achieves the desired outcome.

8.  When you have finalized the JavaScript function, select **Save template** to save it.

    You can either save the JavaScript function as a new template or overwrite the currently selected template.

    -   To save the JavaScript function as a new template, enter a new name in the **Template name** field.
    -   To overwrite the template currently selected in the **JS function templates** field, leave the **Template name** field empty.
9.  Select **Publish** to save the JavaScript function to the database.


## Result

When the JavaScript function is published, Health Log Analytics uses it to map data input sources.

The new script is automatically added to the list of JS function templates from which you can choose. This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

\(ACC data inputs only\) Health Log Analytics provides the published JavaScript function to all existing and future ACC data inputs. The new JavaScript function replaces the previous script.

## What to do next

-   \(Optional\) [Edit your raw log data](hla-data-input-preprocess.md) before Health Log Analytics maps and structures it. If you want to perform this task immediately, click the **Go to Preprocessor** related link to proceed to the **Data Input Preprocessor** page.
-   \(Optional\) Fine-tune how the system reads your log data by [refining the Source Type structure](hla-source-type-structure-refine.md). This step enables you to reclassify auto-classified properties and change auto-mapped labels.

-   **[JavaScript function test outcome fields](../reference/hla-mapping-script-outcome-ref.md)**  
Description of the JavaScript function test outcome fields.

**Parent Topic:**[Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)

**Related topics**  


[Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)

[View the relationships between source types and log sources](hla-view-sources-vs-sourcetypes.md)

