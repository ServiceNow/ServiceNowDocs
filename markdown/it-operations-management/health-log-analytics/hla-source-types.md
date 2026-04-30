---
title: Configure source type capabilities
description: Health Log Analytics extracts source types automatically in the mapping process. You can add timestamp formats and specify, delete, or exclude keywords for individual source types.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, extract, source type, log message, mapping, AI engine]
breadcrumb: [Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure source type capabilities

Health Log Analytics extracts source types automatically in the mapping process. You can add timestamp formats and specify, delete, or exclude keywords for individual source types.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Source Types**.

    The Source Types table lists all source types that were extracted automatically during raw data mapping.

<table id="table_hdc_xbx_l4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Auto extraction enabled

</td><td>

Auto-extraction for this source type is either enabled or disabled. This value is set on the Source Type Structure form. Default: true.

</td></tr><tr><td>

Learning mode

</td><td>

Learning mode for the source type is either ongoing or completed. The AI engine must learn the format of log messages in each new log stream. In Learning mode, it learns the format of messages for this source type and extracts properties based on that knowledge.

</td></tr><tr><td>

Stack trace detection enabled

</td><td>

Detection of active stack frames for this source type is either enabled or disabled. Typically, a stack trace enables tracking an error to the log in which it originated.

</td></tr></tbody>
</table>2.  Open a record.

3.  Add a timestamp format for this source type.

    1.  On the **Source Type Timestamps** tab, select **New**.
    2.  In the **Timestamp format** field, select a format from the list of available timestamp formats.
    3.  Select **Submit**.
4.  Specify a keyword for this source type.

    1.  On the **Lexical Keywords** tab, select **New**.

        **Note:** The **Lexical Keywords** tab contains both global and specified keywords. Selecting **New** creates a specified keyword for this source type.

    2.  On the form, fill in the fields.

<table id="table_jdt_jmt_m4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name for the keyword.

</td></tr><tr><td>

Regular expression

</td><td>

The regular expression \("regex"\) that defines matches.

</td></tr><tr><td>

Exact match

</td><td>

Boolean value. If selected, Health Log Analytics matches the exact regex. For example, 'NullPointerException' in a message would not match the regex 'exception'.Default: True

</td></tr><tr><td>

Case-sensitive

</td><td>

Boolean value. If selected, Health Log Analytics looks for a case-sensitive match of the regex. Default: False

</td></tr></tbody>
</table>    3.  Select **Submit**.
5.  Delete a keyword specified for this source type.

    1.  Select the row of the specified keyword that you want to delete.
    2.  From the **Actions on selected rows** list at the bottom of the page, select **Exclude keyword**.
    3.  Select **Continue** to delete the keyword.
6.  Exclude a global keyword for this source type

    When you exclude a keyword, Health Log Analytics no longer looks for it in the log data of this source type.

    1.  Select the row of the global keyword that you want to exclude.
    2.  From the **Actions on selected rows** list at the bottom of the page, select **Exclude keyword**.
    **Note:** You can delete global keywords from the [Lexical Keywords page](hla-lexical-keywords-admin.md).

7.  Select **Update**.


**Parent Topic:**[Set up data inputs for Health Log Analytics manually](hla-data-input-setup-manual.md)

