---
title: Agent Client Collector log rotation parameters
description: If Agent Client Collector logs get too large, they can drain system resources. To ensure system efficiency, configure parameters in the acc.yml file by which to rotate logs out of the system's storage \(Windows default location = C:\\ProgramData\\ServiceNow\\agent-client-collector\\config\\acc.yml. Linux default location = /etc/servicenow/agent-client-collector/acc.yml\).
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector log rotation parameters

If Agent Client Collector logs get too large, they can drain system resources. To ensure system efficiency, configure parameters in the `acc.yml` file by which to rotate logs out of the system's storage \(Windows default location = `C:\ProgramData\ServiceNow\agent-client-collector\config\acc.yml`. Linux default location = `/etc/servicenow/agent-client-collector/acc.yml`\).

<table id="table_hw3_21d_ymb"><thead><tr><th>

Parameter

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

log-file-and-stdout

</td><td>

Write logs to the `stdout` file.Default: **false**

</td></tr><tr><td>

log-retention-duration

</td><td>

Maximum age, in days, of the log file before it is rotated out of the system's storage.Default: **72h** \(3 days\)

</td></tr><tr><td>

log-retention-files

</td><td>

Maximum number of log files that can be stored before being rotated out of the system.Default: **3**

</td></tr><tr><td>

log-max-size

</td><td>

Maximum size, in MB, of the log file before it is rotated out of the system's storage.Default: **10**

</td></tr><tr><td>

log-level

</td><td>

The log level to be measured by the logs. Available options are: **Panic, Fatal, Error, Warn, Info, Debug**.Default: **Info**

The specified log level represents the lowest level of events displayed in the log. For example, a user who specifies **Error** sees all Error events, as well as Fatal and Panic events.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

