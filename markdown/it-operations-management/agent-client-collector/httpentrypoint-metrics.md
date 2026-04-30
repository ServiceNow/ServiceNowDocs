---
title: HTTP entry point metrics
description: The following table lists the metrics that are gathered as output from HTTP entry point checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# HTTP entry point metrics

The following table lists the metrics that are gathered as output from HTTP entry point checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

<table id="table_gsr_bc2_2tb"><thead><tr><th>

Metric type

</th><th>

Resource \(name of specific database, where relevant\)

</th><th>

Units

</th><th>

Metric type description

</th></tr></thead><tbody><tr><td>

http\_code \(featured metric\)

</td><td>

 

</td><td>

 

</td><td>

Status code of the request.

</td></tr><tr><td>

time\_total \(featured metric\)

</td><td>

 

</td><td>

milliseconds

</td><td>

The total time the operation lasted.

</td></tr><tr><td>

time\_namelookup \(featured metric\)

</td><td>

 

</td><td>

seconds

</td><td>

Time to resolve the name in the URL.

</td></tr><tr><td>

time\_connect \(featured metric\)

</td><td>

 

</td><td>

seconds

</td><td>

Time to complete the connection to the remote host or proxy.

</td></tr><tr><td>

time\_pretransfer \(featured metric\)

</td><td>

 

</td><td>

seconds

</td><td>

Time between start and beginning of file transfer. Includes all pre-transfer commands and negotiations.

</td></tr><tr><td>

time\_starttransfer \(featured metric\)

</td><td>

 

</td><td>

seconds

</td><td>

Time between the start and the transfer of the first byte. Includes **time\_pretransfer** and the time the server used to calculate the result.

</td></tr><tr><td>

time\_redirect \(featured metric\)

</td><td>

 

</td><td>

seconds

</td><td>

Time for all redirection steps including:-   name lookup
-   connect
-   pretransfer
-   transfer

Shows the complete execution time for multiple redirections.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

