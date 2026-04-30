---
title: Connect the agent to the MID Web Server using TLS
description: Connect the agent to the MID Web Server to enable configuring mTLS on your MID Web Server and agent.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [MID Web Server and agent mTLS Authentication, Configure the MID Web Server extension, MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Connect the agent to the MID Web Server using TLS

Connect the agent to the MID Web Server to enable configuring mTLS on your MID Web Server and agent.

## Before you begin

Ensure that you have installed the .pem file and set up the MID Web Server. For details, see [Install the .pem file in the MID unified keystore and set up the MID Web Server](set-mid-web-server.md).

Role required: agent\_client\_collector\_admin

## Procedure

1.  Add the `labcacert.pem` file to your agent host's truststore.

    ```
    sudo cp -a /<path>/<to>/labcacert.pem /etc/pki/ca-trust/source/anchors/; 
    sudo update-ca-trust extract 
    openssl verify /<path>/<to>/labcacert.pem
    ```

    The generated output is `/<path>/labcacert.pem: OK`

2.  Configure the `acc.yml` file to use TLS.

    1.  Set the **insecure-skip-tls-verify** property to **false**.

    2.  Set the **backend-url** property to use the MID Server's FQDN.

        `backend-url="wss://<mid server fqdn>:<mid web server port>/ws/events"`

3.  Restart the agent.

    ```
    systemctl restart acc;
    ```

4.  Verify in the logs that the agent is connected to the MID Server.


## What to do next

[Configure mTLS authentication for a MID Web Server](../../event-management/task/configure-mid-web-server-extension-mTLS.md).

**Parent Topic:**[MID Web Server and agent mTLS Authentication](../../event-management/concept/mid-web-server-mTLS-authentication.md)

