---
title: Set up a REST API integration for Health Log Analytics
description: Set up an integration for streaming log data to your ServiceNow instance for processing by Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [REST API, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up a REST API integration for Health Log Analytics

Set up an integration for streaming log data to your ServiceNow instance for processing by Health Log Analytics.

## Before you begin

-   Verify that the Health Log Analytics application is installed and provisioned on your instance. For more information, see [Install Health Log Analytics \(HLA\)](install-health-log-analytics.md).
-   Verify that a service instance is available.
-   Verify that the Health Log Analytics AI Engine is up and running.

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see MID Server system requirements.

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

    On the MID Web Server Context form, in the **Execute on** field, select Specific MID Server and not the cluster option. In the **MID Server** field, select the specific MID Server to which the log data is pulled.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see Create a MID Server property. If the MID Server and external clients are on the same network, connections can be made using the private IP address.

**Note:** REST API integrations support only UTF-8 encoding for incoming data.

Role required: evt\_mgmt\_admin

## About this task

You set up integrations through the Integrations Launchpad in Service Operations Workspace, which you access from the ITOM AIOps configuration center. The AIOps configuration center is a centralized workspace for configuring and managing AIOps features from a single place. The integrations setup process reduces implementation time compared to manual data input setup in the classic interface in Health Log Analytics. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](../../service-operations-workspace-itom/concept/integrations-launchpad.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  From the Integrate section, under Integrations, select **Add integration**.

    The Integrations Launchpad appears.

4.  In the **Browse integrations** tab, enter `REST` in the search field.

5.  Select the REST API integration tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can cancel the setup and complete the prior requirements first. Alternatively, you can continue in draft mode and complete the requirements later. Note that you can't activate the integration until you have completed all the prerequisites.

6.  On the **Provide details** form, fill in the fields.

    For a description of the fields, see [REST API integration configuration fields](../reference/il-connector-hla-restapi-fields.md).

7.  Select **Next**.

8.  In the **Set-up instruction** screen, copy the provided URL to the clipboard.

    The format of the URL is: `http://(MID_SERVER_IP):(MID_WEB_SERVER_PORT)/ap1/mid/hla/raw`, where `/aps/mid/hla/raw` is the endpoint. HLA has replaced `(MID_SERVER_IP)` and `(MID_WEB_SERVER_PORT)` with the values you configured on the **Provide details** form.

9.  Do one of the following:

    -   If you completed all the prerequisites before starting the configuration, select **Activate**.

        When the integration is activated successfully, the **Overview** tab is displayed. On the Integrations Launchpad, the integration tile is available in the **Installed integrations** tab.

    -   If you didn't complete all the prior requirements, select **Save draft**.

        The system saves the integration as a draft in the Integrations Launchpad. It appears in the **Installed integrations** tab, under **Waiting for your action**. You can complete the prerequisites and activate the integration later. For more information, see [Activate a draft integration in Health Log Analytics](il-connector-hla-activate-draft.md).


## What to do next

Instruct your API client to send log messages to the MID Server.

1.  In the API client, configure a request with the following parameters:
    -   HTTP Method: POST.
    -   URL: The URL you copied in the **Set-up instruction** screen.
    -   Authentication: The required authentication credentials. For example, Basic authentication \(username and password\).

        **Note:** The authentication method must be the same as the method configured on the MID Web Server.

    -   Headers: Set the `Content-Type` header to match your payload format.
        -   For JSON: `application/json`.
        -   For raw text: `text/plain`.
    -   Body: The logs payload in JSON or raw text.
2.  Send the request.

    A successful response indicates that the MID Server has received the payload. When the MID Server has processed the log messages, the data input streams them to your ServiceNow instance using the REST protocol.


**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

