---
title: Enable log monitoring in a Windows environment
description: To enable monitoring logs in a Windows environment, select the relevant policy and assign specific check parameters to the policy. When log monitoring is enabled and a specified string is discovered in the log being monitored, the system creates an event.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Agent Client Collector logs, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Enable log monitoring in a Windows environment

To enable monitoring logs in a Windows environment, select the relevant policy and assign specific check parameters to the policy. When log monitoring is enabled and a specified string is discovered in the log being monitored, the system creates an event.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

2.  Select the **Windows log monitoring** policy.

3.  On the **Check Instances** tab, select **os.windows.check-log** to enable monitoring Windows log files.

4.  On the **Check Parameters** tab, specify the log parameters to be monitored by the check, as described in the following table:

<table id="table_qp2_vht_44b"><thead><tr><th>

Name

</th><th>

Value

</th></tr></thead><tbody><tr><td>

warning

</td><td>

Number of times the specified pattern strings are found in the log which generates a **warning** event. Default = 1.For example, if the **pattern** value is **Exception** and one Exception event is located in the log, a **warning** event is generated.

</td></tr><tr><td>

critical

</td><td>

Number of times the specified pattern strings are found in the log which generates a **critical** event. Default = 2.For example, if the **pattern** value is **Exception** and two Exception events are located in the log, a **critical** event is generated.

</td></tr><tr><td>

file

</td><td>

Location of the log file.

</td></tr><tr><td>

pattern

</td><td>

Strings which are being searched for in the log. Default values are **Severe** and **Exception**. Other possible values include **404** and **Error**.Ensure that you separate multiple patterns with a pipe \(\|\) and pass it as a parameter inside quotes. For example: `"SEVERE|404"`.

</td></tr></tbody>
</table>
**Parent Topic:**[Using Agent Client Collector logs](../concept/logs-acc.md)

