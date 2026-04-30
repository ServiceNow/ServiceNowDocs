---
title: MID Web Server
description: The MID Web Server is part of the common infrastructure of the MID Server.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# MID Web Server

The MID Web Server is part of the common infrastructure of the MID Server.

The MID Web Server extension provides options for authentication and data security, and runs for as long as it is enabled. The extension starts a web server on the MID Server to handle web requests from external systems. The raw data is pushed to the extension, either from a client or with a customized script. The data is collected by the MID Server and is transmitted to the ServiceNow instance.

The MID Web Server extension supports MID Server clusters that are configured for failover. When selecting a MID Server cluster option, an algorithm determines which MID Server in the cluster runs the extension. The extension can run on only one MID Server. If the MID Server in the cluster that runs the MID Web Server extension goes down, the extension automatically starts to run on the secondary MID Server, which is activated when the primary MID Server goes down.

-   **[Configure the MID Web Server extension](../task/configure-mid-web-server-extension.md)**  
The MID Web Server is a MID Server extension that enables developing REST APIs to send events and metrics to the MID Server. The extension is leveraged by other MID Server extensions, such as Metric Intelligence, MID WebService Event Listener, and the Agent Client Collector websocket endpoint extension.

**Parent Topic:**[Event Management setup](c_EMConfiguration.md)

**Related topics**  


[Configure the MID Web Server extension](../task/configure-mid-web-server-extension.md)

[Configure a secure MID Web Server extension](../task/configure-midwebserver-extension-secure.md)

