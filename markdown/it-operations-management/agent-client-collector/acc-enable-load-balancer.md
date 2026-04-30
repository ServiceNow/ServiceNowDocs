---
title: Enable the Agent Client Collector load balancer
description: Enable a load balancer to ensure that you have functional MID Servers. A load balancer distributes resources over multiple MID Servers to ensure that no single MID Server is overloaded.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC installation, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Enable the Agent Client Collector load balancer

Enable a load balancer to ensure that you have functional MID Servers. A load balancer distributes resources over multiple MID Servers to ensure that no single MID Server is overloaded.

## Before you begin

1.  Install the Agent Client Collector Framework.
2.  Configure the Agent Client Collector web server.
3.  Ensure that you have access to the internal application's load balancer configuration.
4.  Verify that the file `<mid_server_install_path>/static/hello.txt` was created during MID Server setup.

    `hello.txt` is an empty file that is created manually, to retrieve an HTTP response 200.


Role required: agent\_client\_collector\_admin

## About this task

Load balancers are not configured by default. Follow this procedure to configure a load balancer in your environment.

## Procedure

1.  Configure the load balancer so that it can be used in the **backend-url** parameter in the `acc.yml` configuration file.

2.  Perform the following setup actions on the load balancer:

    1.  Increase the idle timeout to 300 seconds.

    2.  Configure the load balancer target group with **https** and port 443.

        Configure all MID Servers behind the load balancer as targets.

    3.  Configure the load balancer health check to monitor the `<mid_server_install_path>/static/hello.txt` file created during MID Server setup.

        The health check ensures that there are no communication interruptions between the load balancer and the MID Server.

3.  Add the `<mid_server_install_path>/static/hello.txt` file to the static folder for each MID Server.

    You can place the file in another location that doesn't require credentials, to simplify the setup.

4.  Update the acc.yml configuration file with the appropriate FQDN \(**backend-url** value\) and port number, and turn off automatic MID Server selection.

    ```
    backend-url:
     - wss://<fqdn>:<port>/ws/events
    enable-auto-mid-selection: false
    ```

5.  Restart the Agent Client Collector.


## Result

The Agent Client Collector data flow proceeds as described in [Agent Client Collector architecture](../concept/acc-concept.md).

**Note:**

When working with SSL, all certificates or certificate chains used by the configured MID Servers must be signed by root certificate authorities whose certificates are bundled inside a single `.pem` file. To transfer the signed certificates to the agent, specify the `.pem` file in the **trusted-ca-file** property of the agent’s `.yml` configuration file. For information on enhancing security with SSL/TLS configuration, see the [ITOM Agent Client Collector documentation material](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1122613) article in the Now Support Knowledge Base.

