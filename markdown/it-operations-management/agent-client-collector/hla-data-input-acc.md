---
title: Configure ACC data inputs manually
description: Agent Client Collector setup automatically creates an ACC data input for streaming log messages to your ServiceNow instance. You can set up additional ACC data inputs manually as needed.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up additional ACC data inputs, Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# Configure ACC data inputs manually

Agent Client Collector setup automatically creates an ACC data input for streaming log messages to your ServiceNow instance. You can set up additional ACC data inputs manually as needed.

## Before you begin

-   The Agent Client Collector Log Analytics application has a dependency on the following ServiceNow applications, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home):
    -   Health Log Analytics, Version 22.0.12 - December 2021 and later releases.
    -   Agent Client Collector -Framework, Version 2.7.0 - December 2021 and later releases.
-   Verify that a MID Server is installed and configured. For more information, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).
-   The MID Server must be configured to work with the Agent Client Collector. For more information, see [Enable Agent Client Collector monitoring on the MID Server](../../agent-client-collector/task/acc-monitoring-setup.md).

**Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

**Note:** Currently, this setup only supports basic authentication with the MID Server. mTLS is not supported.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **ACC Log Analytics** &gt; **ACC Data Inputs**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For a description of the fields, see [ACC data input configuration fields](../../agent-client-collector/reference/accl-data-input-conf-ref.md).

4.  Select **Advanced** to set additional configuration fields.

5.  Select **Save**.

    Health Log Analytics adds the data input record to the Data Inputs table.

6.  Ensure that the data input is configured correctly by selecting **Test connection**.

    Health Log Analytics tries to connect the MID Server to the data repository.

    -   If the connection was established, the **Test connection** button is turned off and the **Publish** button is enabled.
    -   If the connection failed, the reason for the failure displays in the **Error message** field. This field displays only when a streaming error has occurred.

        Resolve the issue, select **Save** if you modified the configuration, and then select **Test connection** to test the connection again.

        **Note:** You can only publish the data input configuration when the connection is created successfully.

    **Note:** You can revert to the last published configuration by selecting **Revert Changes**. This option is available only when you're modifying a configuration that has been published previously.

7.  Select **Publish** to publish the data input to the MID Server.


## Result

The new data input is ready to stream logs.

**Note:** The data input record includes these related lists:

-   Agents – Lists all active agents connected to the MID Server for this data input.
-   Streaming Sources – Lists all sources for this data input and the MID Server that receives logs from it.

## What to do next

[Ensure that the data input is streaming data](../../agent-client-collector/task/accl-verify-log-streaming.md).

