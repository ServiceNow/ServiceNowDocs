---
title: Enable viewing HAProxy metrics
description: Configure the HAProxy metrics stats page to enable monitoring your system devices by viewing HAProxy metrics.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Monitoring, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Enable viewing HAProxy metrics

Configure the HAProxy metrics stats page to enable monitoring your system devices by viewing HAProxy metrics.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

HAProxy provides load balancing and reverse proxy capabilities for both HTTP and TCP requests. The HAProxy checks remove backend servers that fail several health checks in a row, and transfer incoming traffic to backend servers as part of load balancing.

## Procedure

1.  Access the HAProxy configuration file, located at: `/etc/haproxy/haproxy.cfg`.

2.  Add the following to the bottom of the file:

    ```
    listen frontend *:8080       #Haproxy 
    Monitoring run on port 8080
    mode http
    option forwardfor
    option httpclose
    stats enable
    stats show-legends
    stats refresh 5s
    stats uri /stats        #URL for HAProxy monitoring
    stats realm Haproxy\Statistics.   #Title for pop up window
    stats auth admin:admin     #User and Password for login to the monitoring dashboard
    stats admin if TRUE
    default_backend backend       #This is optional for monitoring backend 
    
    ```

3.  Run the following command to restart the HAProxy:

    `sudo service haproxy restart`

4.  View the HAProxy metrics on your system by viewing the HAProxy metrics stats page, accessible from the following URL:

    `http://<HAProxyServer>:8080/stats`


**Related topics**  


[HAProxy default checks and policies](../reference/haproxy-checks-policies.md)

