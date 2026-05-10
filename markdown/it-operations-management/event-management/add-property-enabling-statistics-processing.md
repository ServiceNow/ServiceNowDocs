---
title: Enable processing of event process statistics
description: Enable the system property that switches on statistics processing for events to let the platform collect and analyze metrics such as event volume, processing flow, and handling time. This helps you monitor system performance, identify bottlenecks, and optimize event handling for faster and more efficient operations.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View event processing statistics, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Enable processing of event process statistics

Enable the system property that switches on statistics processing for events to let the platform collect and analyze metrics such as event volume, processing flow, and handling time. This helps you monitor system performance, identify bottlenecks, and optimize event handling for faster and more efficient operations.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Select **New** and fill in the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the property you are creating.|
    |Description|Narrative that describes the property and its function.|
    |Choices|Comma-separated values for a choice list. If you need a different choice list label and value, use an equal sign \(=\) to separate the label from the value. For example, Blue=0000FF, Red=FF0000,Green=00FF00 displays Blue, Red, and Green in the list, and saves the corresponding hex value in the property value field.|
    |Type|Data type, that is selected from a list \(for example, integer, string, or true\|false\).|
    |Value|Desired value for the property. When retrieving properties using the **gs.getProperty\(\)** method, treat the results as strings. For example, a true\|false property returns 'true' or 'false' \(strings\), not the Boolean equivalent.|
    |Read roles|Roles that have read access to this property.|
    |Write roles|Roles that have write access to this property.|

3.  Select **Submit**.


**Related topics**  


[Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md)

