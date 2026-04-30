---
title: Nginx default checks and policies
description: Agent Client Collector provides the following policies for Nginx health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for both Windows and Linux.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Nginx default checks and policies

Agent Client Collector provides the following policies for Nginx health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for both Windows and Linux.

<table id="table_y3r_2qd_2tb"><thead><tr><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Command

</th><th>

Output

</th></tr></thead><tbody><tr><td>

nginx.check-nginx-alive

</td><td>

Verifies whether Nginx server is alive.**Note:** Use basic authentication for events.

</td><td>

`check-nginx-status.rb` -   **-h, --host**

Nginx hostname

-   **-p, --port**

Nginx port


 **Note:** Use basic authentication for events.

</td><td>

``

</td><td>

Successful

 `CheckNginxStatus OK: Nginx is Alive and healthy` Failure

 `CheckNginxStatus CRITICAL: Nginx is Down`

</td></tr></tbody>
</table><table id="table_mqy_xzd_2tb"><thead><tr><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Command

</th><th>

Output

</th></tr></thead><tbody><tr><td>

nginx.metrics-nginx-server

</td><td>

Retrieves the following information:

-   **nginx.active\_connections**

Total number of active connections on server.

-   **nginx.accepts**

The accepted connections.

-   **nginx.handled**

Handled connections, which normally equals the number of accepted connections.

-   **nginx.requests**

Total number of handled requests by the server.

-   **nginx.read**

Shows whether the server is reading requests.

-   **nginx.writing**

Shows whether the server is writing responses to the client.

-   **nginx.waiting**

Idle connections waiting for a request.


 **Note:** Use basic authentication for metrics.

</td><td>

`metrics-nginx.rb` Options:

 `-u --url` Full URL to the server status page. For example: `https://yoursite.com/nginx_status`

</td><td>

``

</td><td>

```
ws19-INC0047517.nginx.active_connections 1 1640135552 
ws19-INC0047517.nginx.accepts 5746 1640135552 
ws19-INC0047517.nginx.handled 5746 1640135552 
ws19-INC0047517.nginx.requests 9603 1640135552 
ws19-INC0047517.nginx.reading 0 1640135552 
ws19-INC0047517.nginx.writing 1 1640135552 
ws19-INC0047517.nginx.waiting 0 1640135552 
```

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

