---
title: Connect the agent to the MID Web Server using TLS
description: Connect the agent to the MID Web Server to enable configuring mTLS on your MID Web Server and agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/agent-mid-connect.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MID Web Server and agent mTLS Authentication, Configure the MID Web Server extension, MID Web Server, Event Management setup, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Connect the agent to the MID Web Server using TLS

Connect the agent to the MID Web Server to enable configuring mTLS on your MID Web Server and agent.

## Before you begin

Ensure that you have installed the .pem file and set up the MID Web Server. For details, see [Set up the MID Web Server with a .pem file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/set-mid-web-server.md).

**Note:** This procedure includes commands for both CentOS 7/Linux and Windows Server environments. Select the commands relevant for your host operating system. If working with another Linux distribution, adapt the commands as needed for your specific OS.

Role required: agent\_client\_collector\_admin

## Procedure

1.  In a Linux environment:

    1.  Add the `labcacert.pem` file to your agent host's trust store.

        ```
        sudo cp -a /<path>/<to>/labcacert.pem /etc/pki/ca-trust/source/anchors/;
        sudo update-ca-trust extract
        openssl verify /<path>/<to>/labcacert.pem
        ```

        The generated output is: `/<path>/labcacert.pem: OK`

    2.  Configure the `acc.yml` file to use TLS.

        1.  Set the **insecure-skip-tls-verify** property to `false`.
        2.  Set the **backend-url** property to use the MID Server's FQDN.
        ```
        backend-url="wss://<mid server fqdn>:<mid web server port>/ws/events"
        ```

    3.  Restart the agent.

        ```
        systemctl restart acc;
        ```

    4.  Verify in the logs that the agent is connected to the MID Server.

2.  In a Windows environment:

    1.  Add the `labcacert.pem` file to your agent host's trust store by importing it into the Windows Certificate Store.

        ```
        certutil -addstore -f "Root" <path>\labcacert.pem
        openssl verify -CAfile <path>\labcacert.pem <path>\labcacert.pem
        ```

        The generated output is: `<path>\labcacert.pem: OK`

    2.  Configure the `acc.yml` file \(`C:\ProgramData\servicenow\agent-client-collector\config\acc.yml`\) to use TLS.

        1.  Set the **insecure-skip-tls-verify** property to `false`.
        2.  Set the **backend-url** property to use the MID Server's FQDN:

            ```
            backend-url:
             - "wss://<mid server fqdn>:<mid web server port>/ws/events"
            ```

    3.  Restart the agent using one of the following methods:

        -   Command line:

            ```
            net stop AgentClientCollector
            net start AgentClientCollector
            ```

        -   Services app: Select and hold the **Agent Client Collector** entry and select **Restart**.
    4.  Verify in the logs that the agent is connected to the MID Server.

        Logs are located at: `C:\ProgramData\ServiceNow\agent-client-collector\log\acc.log` \(or the location set by the **log-file** configuration parameter\).


## What to do next

[Configure mTLS authentication for a MID Web Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/configure-mid-web-server-extension-mTLS.md).

