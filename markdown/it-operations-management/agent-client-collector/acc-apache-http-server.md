---
title: Configure Agent Client Collector Apache HTTP server monitoring
description: To configure the Agent Client Collector to perform Apache HTTP server monitoring, set the following configurations in the Apache HTTP server application.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Operating system and application monitoring using ACC, Exploring ACC Framework, Agent Client Collector, IT Operations Management]
---

# Configure Agent Client Collector Apache HTTP server monitoring

To configure the Agent Client Collector to perform Apache HTTP server monitoring, set the following configurations in the Apache HTTP server application.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  On the Apache HTTP Server host, navigate to one of the following locations:

    -   In a Linux environment:
        -   `/etc/httpd`
        -   `/etc/httpd/conf`
        -   `/etc/apache2`
        -   `/etc/apache2/conf`
    -   In a Windows environment: The `conf` directory in the Apache installation location.
2.  Locate either the `httpd.conf` or `apache2.conf` file.

3.  Ensure that the following line is uncommented:

    `LoadModule status_module modules/mod_status.so`

4.  Configure the check instance port to be identical to the port on which Apache is listening \(default for both is **80**\).

5.  To ensure a secure connection, configure SSL, as follows:

    1.  Ensure that the following line is uncommented:

        `LoadModule ssl_module modules/mod_ssl.so`

    2.  Activate the **ssl\_secure\_connection** parameter in the check instance.

    3.  Configure the check instance port to be identical to the port on which Apache is listening to secure connections \(default is **443**\).


**Parent Topic:**[Operating system and application monitoring using Agent Client Collector](../concept/itom-monitoring-for-acc.md)

**Related topics**  


[Apache Module](https://httpd.apache.org/docs/current/mod/mod_status.html#enable)

[Apache SLL/TLS Strong Encryption: How-to](https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html)

