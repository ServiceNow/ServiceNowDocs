---
title: Log data auto-mapping and mapping
description: By default, the Health Log Analytics AI engine tries to auto-map every incoming log line to the correct tags. You can change automatic mapping results manually by defining a JavaScript function.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
keywords: [ServiceNow, Health Log Analytics, HLA, logs, tagging, mapping, auto-map, data input, source type, binding log data, CMDB]
breadcrumb: [Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Log data auto-mapping and mapping

By default, the Health Log Analytics AI engine tries to auto-map every incoming log line to the correct tags. You can change automatic mapping results manually by defining a JavaScript function.

## Auto-mapping incoming log lines

Health Log Analytics auto-mapping assigns log samples and metadata to three tags: service instance, component, and source type. The service instance assignment is based on the service instance specified in the data input setup. The remaining tags are assigned automatically.

For example, in the following example log line, Health Log Analytics uses the "source" field to find the component and source type.

```
{"beat":{"version":"6.8","name":"abc3.prd.acme.com","hostname":"abc3.prd.acme.com"},"@timestamp":"2020-08-27T10:12:24.792Z","prospector":{"type":"log"},"message":"**** User null is requesting the following page http://www.acme.com PROPS:{"subcategory1":"home pages","httpStatus":"200","loginLevel":"Anonymous","userAgent":"Mozilla5.0", ("pageUrl":\"http://www.acme.com","host":"abc3.prd.acme.com","@version":"1","source":"/opt/oracle/weblogic/abc/online_store3/logs/online_store3.out","offset":3951550786} 
```

In the example, Health Log Analytics extracts the string "online\_store". It analyzes the following fields if they exist in the log line: source, path, channel, namespace\_name, name, pod\_name, source\_name, and aws\_lambda\_name. When data is sent over Syslog, it also analyzes the syslog tag.

-   **Stop extraction of unneeded data**

    If an extracted string is not descriptive enough or contains redundant text or information, you can stop extracting such expendable data. For more information, see [Stop extraction of unneeded log data](../task/hla-log-data-exclude.md).

-   **Ensuring extraction of specific data**

    You can make sure that Health Log Analytics extracts specific desired terms. For more information, see [Ensure extraction of specific log data](../task/hla-log-data-extract.md).


## Mapping data input sources

You can change automatic mapping results manually by defining a JavaScript function. [Data input mapping](../task/hla-data-input-mapping.md) enables you to organize your log data by service instance and by availability zone. A single service instance can include multiple components, and a component can receive logs from many different source types. An service instance-component pair, however, is unique. Source types are based on a specific log structure and format. Service instances and components are defined more broadly and are therefore used mainly for logical mapping.

Activating **Test mode** avoids blowing up Elasticsearch storage with sample data that is used only for perfecting the log data mapping. When the data input is in Test mode, Health Log Analytics doesn’t create the source types, sources, or any other objects it creates in the standard flow. It saves the streamed data in dedicated temporary Elasticsearch indices that appear as components in the Log viewer. When you publish the script and exit Test mode, these temporary indices are deleted to minimize storage space consumption.

When you're defining a JavaScript function, select **Test** to view the outcome of the script as it is currently specified. This functionality enables you to preview the created source types and sources. You can then refine the script until it achieves the desired outcome. For example, it can be useful to compare the test outcome of several versions of the JavaScript function.

**Note:** By default, the test processes 100 log data samples. You can customize this number in the system properties. For more information, see [Configure global Health Log Analytics system properties](../task/hla-system-properties-configure.md).

During the data input setup, the system might create an excessive total number of data input sources. For example, this can be due to a faulty mapping script. You can configure limits for the number of sources created per data input in the [system properties](../task/hla-system-properties-configure.md):

|System property|Description|Default|
|---------------|-----------|-------|
|**log\_source.sources\_warning\_limit**|The warning limit for the number of sources created per data input.|500|
|**log\_source.sources\_critical\_limit**|The critical limit for the number of sources created per data input.|600|

The number of log sources that a specific data input has created displays in the **Sources count** field for that data input. When the total number of sources created during the data input setup reaches the warning limit, the system sends a warning notification by email. It also displays a message on the **Data Input mapping**, **Log sources**, and **Data input** pages. The notification and the message include the total number of sources created so far and the three data inputs that contributed the most sources to this total. If no action is taken, the system continues to create sources until the total number reaches the critical limit. When this happens, the data input setup and streaming from all data inputs stops automatically. You can't start data inputs again manually until the issue has been resolved. You can resolve this state by following the instructions in the [How to handle too many sources in data inputs \[KB0963067\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0963067) article in the Now Support Knowledge Base.

## Binding log data

Binding log data to Configuration Items \(CIs\) in the Configuration Management Database \(CMDB\) enables you to search the CMDB for endpoints that match a log. When you configure a data input, you bind log entries to a service instance that is bound to a CI in the CMDB. Binding log entries, service instances, and CIs enables the Health Log Analytics AI engine to correlate them for use in root cause analysis \(RCA\). For more information, see [Configure data inputs \(Rsyslog, Filebeat, or Winlogbeat\)](../task/hla-data-input-rsyslog-beats.md) or [Configure data inputs \(Elasticsearch\)](../task/hla-data-input-elastic.md).

-   **[Map raw log data](../task/hla-data-input-mapping.md)**  
Mapping raw log data that streams into your instance determines how the data is handled. Health Log Analytics automatically structures logs, creates metrics for anomaly detection, and presents alerts based on how your data is tagged.
-   **[View the relationships between source types and log sources](../task/hla-view-sources-vs-sourcetypes.md)**  
Explore the many-to-many relationships between source types and log sources in Health Log Analytics to help you optimize your data input mapping.
-   **[Header properties detection](hla-header-detection.md)**  
In Health Log Analytics, automatic header properties detection separates the transport header from the inner log message and forwards only the inner log message to the source type structure. The inner message contains the actual log data without including shipping information.
-   **[Stop extraction of unneeded log data](../task/hla-log-data-exclude.md)**  
If an extracted string of data is not descriptive enough or contains redundant text or information, you can set Health Log Analytics to stop extracting such data from your logs.
-   **[Ensure extraction of specific log data](../task/hla-log-data-extract.md)**  
Set Health Log Analytics to extract specified terms from fields and map them to specific components.

**Parent Topic:**[Set up data inputs for Health Log Analytics manually](../task/hla-data-input-setup-manual.md)

**Related topics**  


[Map raw log data](../task/hla-data-input-mapping.md)

[View the relationships between source types and log sources](../task/hla-view-sources-vs-sourcetypes.md)

