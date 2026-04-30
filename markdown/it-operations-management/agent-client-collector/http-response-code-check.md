---
title: HTTP response code check
description: Agent Client Collector provides the following additional check for HTTP response code. This check is not associated with any policy.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# HTTP response code check

Agent Client Collector provides the following additional check for HTTP response code. This check is not associated with any policy.

<table id="table_k2q_bwj_g5b"><thead><tr><th>

Type

</th><th>

Name

</th><th>

Description

</th><th>

Usage and usage example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Event

</td><td>

util.check-http-response-code

</td><td>

Raises a critical event if the URL response code doesn’t match the regex.Pass credentials \(username and password\) using secure parameters.

</td><td>

```
-u, --url  URL needs to be updated in the Monitoring HTTP Entrypoint/cmdb_ci_endpoint_http_list.do for the CI
-r, --response-code  Regex string to match the response code. Otherwise, a critical event is raised. Default: 200
-f, --follow_redirects Follows redirect URLs

```

 Usage example: `command: check-response-code.rb -u 'https://servicenow.com' -r 2.. -f`

</td><td>

`CheckResponseCode OK : URL is in OK state. HTTP Response code is 200, matches regex`

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

