---
title: Configure the websocket server on the MID Server
description: Configure the websocket server on MID Servers to enable connections from agents to the MID Server. You can configure only one websocket server per MID Server.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector with a MID Server, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Configure the websocket server on the MID Server

Configure the websocket server on MID Servers to enable connections from agents to the MID Server. You can configure only one websocket server per MID Server.

## Before you begin

-   Ensure that you download and install curl \(or similar software\) on your MID Server Windows machine.
-   Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  Select the relevant MID Server name.

3.  In the **Related Links** section, click **Setup ACC Listener**.

    The **Agent Client Collector Setup** dialog box appears.

    ![Agent Client Collector Setup dialog box](../image/acc-setup.png)

4.  Enter the MID web server port \(**8800**\) in the displayed field.

    **Note:** You can change the default port, **8800**, as needed.

    -   To invoke secure TLS configuration, configure the following in the `acc.yml` file: `wss://<mid_ip>:<websocket_port>/ws/events`
    -   To invoke TLS 1.3 support on the MID Web Server, set the following parameter in the `wrapper-override.conf` file on the MID Server: `-Djdk.tls.server.protocols="TLSv1.3"`
    -   In a Linux environment, port numbers under 1024 can be used only with superuser privileges.
5.  Click **OK**.

    A confirmation message with the URL for the agent configuration file appears.

    The web server and websocket extension are configured for the MID Server. To verify that the configuration is working, you must navigate to the following menu options:

    -   **Agent Client Collector** &gt; **MID Web Server**. When editing the fields on the resulting form, you must restart the MID web server extension to save your changes.
    -   **Agent Client Collector** &gt; **Websocket Endpoint**
6.  Verify the validity of the websocket, using curl:

    1.  Enter the following command into a cmd or terminal window: `curl -Lk -H "Authorization: Key <API_KEY>" https://<mid_server_address>:<port>/api/mid/mon`

    2.  Verify that you receive a valid JSON response \(and not an error message\), such as the following:

        ![Successful installation JSON script](../image/ACC-websocket-JSON.png "Successful installation JSON script")


**Parent Topic:**[Configuring Agent Client Collector with a MID Server](../concept/acc-configuring-with-mid.md)

