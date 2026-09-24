---
title: Create a log source configuration
description: Regulate and set filters on the logs to be forwarded by creating a log source configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/les-create-source-configuration.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Administer, Log Export Service \(LES\), Platform Security]
---

# Create a log source configuration

Regulate and set filters on the logs to be forwarded by creating a log source configuration.

## Before you begin

Role required: admin or sn\_logstoanalytics.admin

## Procedure

1.  Navigate to **All** &gt; **Log Export Service** &gt; **Sources**.

    A list of source configurations shows up.

2.  Select **New** to create a new source configuration.

    You can also select an existing source configuration if you want to modify it.

    The Source form shows up.

3.  On the form, fill up the fields.

<table id="table_ph5_fns_xjb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Type

</td><td>

Types of log sources-   Node Log
-   Table
See [Log sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-log-sources-export.md) for more information.

</td></tr><tr><td>

Log Level

</td><td>

A set of standard logging levels that can be used to control logging output. Following convention, each level will forward logs of equal or greater severity.**Note:** This field is visible only when one of the following conditions is met.

-   When you select Node Log as the Source Type
-   When you select Table as the Source Type and the table is syslog


</td></tr><tr><td>

Table

</td><td>

Selection of table for exporting table type logs. For more information on supported tables, see [Log sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-log-sources-export.md).**Note:** This field is visible only when you select Table as the Source Type.

</td></tr><tr><td>

Filter Type

</td><td>

Conditions to forward logs selectively.**Note:** This field is visible only if you select syslog, sys\_audit, sys\_audit\_delete, or sys\_audit\_relation as the table.

</td></tr><tr><td>

Topic

</td><td>

Select an existing topic, or create a topic through the lookup icon. For more information on creating a topic, refer [Create source type and multi topics in the LES source table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-multi-topics-v2.md)

</td></tr><tr><td>

Accepts

</td><td>

Specifies the format in which the logs are forwarded to Hermes. They can either be sent as JSON or as plain text.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the Source log is active.

</td></tr></tbody>
</table>4.  Complete the flow that matches the table you selected.

    -   **Standard source**

        Select **Submit** to save the source configuration. The source details appear in the Sources list, where you can review its source type, table, topic, and active status.

        **Note:**

        -   Applies when you select Source type as Node Log and any table other than the syslog and sys\_audit tables.
        -   The configuration is complete. Skip the remaining steps.
    -   **syslog table**

        When you select **Source type** as Table and syslog in the **Table** field:

        **Note:** You can create multiple source topics for this selection.

        1.  Select the **Log level**.
        2.  Select **Submit**. The **Source topics** related list appears, and the log export filters become available.
        3.  Select **New** to create a new source topic.
        4.  In the **Filter** field, select a value from the dropdown list.
            -   **All**: No additional field appears.
            -   **Application Family**, **Package**, or **Scope**: A corresponding lookup field appears. Select the lookup icon to select a value.
        5.  In the **Topic** field, select an existing topic, or create a topic through the lookup icon. For more information on creating a topic, refer [Create source type and multi topics in the LES source table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-multi-topics-v2.md).
        6.  Select **Submit**, and then review the source topics that you created.
    -   **sys\_audit table with the Log table filter**

        When you select the **Table** as sys\_audit and **Filter type** as Log table:

        **Note:** You can create multiple source topics for this selection.

        1.  The **Source topics** related list appears, and the log export filters become available.
        2.  Select **New** to create a new source topic.
        3.  Select the required table in the **Log table** field using the lookup icon.
        4.  In the **Topic** field, select an existing topic, or create a topic through the lookup icon. For more information on creating a topic, refer [Create source type and multi topics in the LES source table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-multi-topics-v2.md).
        5.  Select **Submit**, and then review the source topics that you created.

-   **[Create source type and multi topics in the LES source table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-multi-topics-v2.md)**  
Consume logs for each source type by creating multiple topics per source type. You can now leverage the option of customized selection of specific topics for different log sources during the debugging process, without impacting the other log tables.

**Parent Topic:**[Administering Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-administer.md)

