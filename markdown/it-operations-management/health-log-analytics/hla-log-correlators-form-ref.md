---
title: Log correlators form fields
description: This section describes the fields on the Log correlators form.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Log correlators form fields

This section describes the fields on the Log correlators form.

<table id="table_rcp_spb_zmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of log correlator. Choices are as follows.-   **Free text correlator**: The log correlator analyzes text in the log message.
-   **Log-key correlator**: The log correlator analyzes log metadata. For example, the name of a service instance in your infrastructure. Log property correlators are specific to the business context of your environment.

For more information, see [Identifying related alerts in log data by using log correlators](../concept/hla-op-correlator-what-is-a.md).

</td></tr><tr><td>

Free text term or Identifier

</td><td>

Text that the log correlator isolates when parsing log lines. The label for this field is **Free text term** for free text log correlators and **Identifier** for log property correlators.

**Note:** The value of this field can be the text for either type of log correlator. As a result, the label for this column in the resulting list of log correlators is **Correlation indicator**.

</td></tr><tr><td>

Active

</td><td>

Option to apply the log correlator. When you select this field, the system applies the log correlator to the log stream.

</td></tr><tr><td>

Range of analysis

</td><td>

Set of sources whose log data are analyzed by this log correlator. Choices are as follows:-   **All sources**: The log correlator is applied to log lines from all sources in the data stream.
-   **Only new sources**: The log correlator is applied to log lines from all sources created after this log correlator is activated.
-   **Specified source**: The log correlator is applied only to the log lines from the source that you specify on this form.

</td></tr><tr><td>

Excluded sources

</td><td>

Sources that are excluded from the log correlator. The system does not analyze log lines from sources that are listed in this field.**Note:** This field applies only when the **Range of analysis** field is set **All sources** or **Only new sources**.

For information about excluding a source from a log correlator, see [Exclude a source from a log correlator](../../health-log-analytics-admin/task/hla-correlators-exclude-source.md).

</td></tr><tr><td>

Source

</td><td>

Source of the log correlator. The log correlator analyzes the data of this log source.This field appears only when you are adding the log correlator from the Log Sources form. The field is automatically set to the log source that you are working on.

</td></tr></tbody>
</table>**Parent Topic:**[Health Log Analytics reference](../../health-log-analytics-admin/concept/hla-reference.md)

