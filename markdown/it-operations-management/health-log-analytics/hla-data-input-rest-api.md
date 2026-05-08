---
title: Configure a REST API data input in Health Log Analytics manually
description: Set up a REST API data input for streaming log data to your ServiceNow instance.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration]
breadcrumb: [Manual data input configuration, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure a REST API data input in Health Log Analytics manually

Set up a REST API data input for streaming log data to your ServiceNow instance.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see MID Server system requirements.

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

    On the MID Web Server Context form, in the **Execute on** field, select Specific MID Server and not the cluster option. In the **MID Server** field, select the specific MID Server to which the log data is pulled.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see Create a MID Server property. If the MID Server and external clients are on the same network, connections can be made using the private IP address.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the REST API data input.

4.  On the form, fill in the fields.

    For a description of the fields, see [REST API data input configuration fields](../reference/hla-data-input-rest-api-ref.md).

5.  Select **Save**.

    -   Health Log Analytics adds the data input record to the **Data Inputs** table.
    -   The system automatically generates the REST API data input URL for sending logs to the MID Server. The generated URL will be in this format: `http://(MID_SERVER_IP):(MID_WEB_SERVER_PORT)/ap1/mid/hla/raw`. HLA replaces `(MID_SERVER_IP)` and `(MID_WEB_SERVER_PORT)` with the values you configured.
6.  Copy the generated URL.

7.  Instruct your API client to send log messages to the MID Server.

    1.  In the API client, configure a request with the following parameters:

        -   HTTP Method: POST.
        -   URL: The URL you copied in the previous step.
        -   Authentication: The required authentication credentials. For example, Basic authentication \(username and password\).

            **Note:** The authentication method must be the same as the method configured on the MID Web Server.

        -   Headers: Set the `Content-Type` header to match your payload format.
            -   For JSON: `application/json`.
            -   For raw text: `text/plain`.
        -   Body: The logs payload in JSON or raw text.
    2.  Send the request.

        A successful response indicates that the MID Server has received the payload. When the MID Server has processed the log messages, the data input streams them to your ServiceNow instance using the REST protocol.


**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

