---
title: Edge Encryption MID Server integration
description: Configure the MID Server to route data through an Edge Encryption proxy server.To pass data from the MID Server through the Edge Encryption proxy server, update the MID Server configuration file to point the MID Server to the Edge Encryption proxy server.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Data integration with Edge Encryption, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Edge Encryption MID Server integration

Configure the MID Server to route data through an Edge Encryption proxy server.

When integrated with the MID Server, the Edge Encryption proxy server acts as the MID Server's endpoint. The Edge Encryption proxy server then encrypts and decrypts data passing between the ServiceNow instance and the MID Server.

## Limitations when integrating with the MID Server

When MID Server data is configured to pass through the Edge Encryption proxy server, the following limitations apply:

-   Encryption of ECC Queue fields is not supported.
-   Encrypted data cannot be used with Discovery or Service Mapping.

**Parent Topic:**[Data integration with Edge Encryption](data-integration.md)

## Point the MID Server to the Edge Encryption proxy server

To pass data from the MID Server through the Edge Encryption proxy server, update the MID Server configuration file to point the MID Server to the Edge Encryption proxy server.

### Before you begin

Role required: admin

### About this task

When configuring the MID Server to pass through the Edge Encryption proxy server, you cannot use the web proxy properties in the MID Server configuration file to route traffic through the Edge Encryption proxy server to your instance. Instead, you must set the Edge Encryption proxy server as the MID Server's endpoint.

### Procedure

1.  Navigate to your local MID Server directory and open the `config.xml` file.

2.  Find the element `<parameter name="url" value="https://YOUR_INSTANCE.service-now.com" />` and change the value property to the URL of your Edge Encryption proxy server.

    For example, `http://hostname.mycompany.com:8081`

    This step directs the MID Server to pass traffic to the Edge Encryption proxy server instead of the instance. The Edge Encryption proxy server in turn encrypts any necessary fields and passes the payload to the instance.

3.  Save and close the file.

4.  If running, restart the MID Server.


