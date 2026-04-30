---
title: Add timestamp formats
description: Define any timestamp format that does not appear in the list of defined formats. Health Log Analytics must be able to read timestamps of any format contained in your log files.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, Timestamp Formats, manually define, custom timestamp format]
breadcrumb: [Additional data input setup tasks, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Add timestamp formats

Define any timestamp format that does not appear in the list of defined formats. Health Log Analytics must be able to read timestamps of any format contained in your log files.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Timestamp Formats**.

2.  To determine whether your timestamp format matches a predefined format in the system, do the following:

    1.  Select **Find format**.

    2.  Enter a sample of your timestamp.

    3.  Select **Find format**.

    If the sample matches an existing format, the system provides its ID.

3.  If your timestamp sample doesn't match an existing format, then manually define your custom format and add it to the available timestamp formats.

    1.  On the Timestamp Formats page, select **New**.

    2.  On the form, fill in the fields.

<table id="table_jdl_nmt_2pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

ID of the timestamp format. This value is selected automatically.

</td></tr><tr><td>

Format

</td><td>

Valid timestamp format. For example, dd-MMM-yyyy, HH:mm.**Note:** Health Log Analytics uses the [Java 8 API](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) for timestamp syntax.

</td></tr><tr><td>

Sample

</td><td>

Example of the timestamp format. For example, 03-May-2018, 10:20.

</td></tr><tr><td>

Description

</td><td>

Description of the timestamp format.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The system validates the timestamp format and adds it to the list of available timestamps.

**Parent Topic:**[Additional data input setup tasks](../concept/hla-data-input-setup-extra.md)

