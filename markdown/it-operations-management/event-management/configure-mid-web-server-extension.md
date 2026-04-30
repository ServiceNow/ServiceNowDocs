---
title: Configure the MID Web Server extension
description: The MID Web Server is a MID Server extension that enables developing REST APIs to send events and metrics to the MID Server. The extension is leveraged by other MID Server extensions, such as Metric Intelligence, MID WebService Event Listener, and the Agent Client Collector websocket endpoint extension.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the MID Web Server extension

The MID Web Server is a MID Server extension that enables developing REST APIs to send events and metrics to the MID Server. The extension is leveraged by other MID Server extensions, such as Metric Intelligence, MID WebService Event Listener, and the Agent Client Collector websocket endpoint extension.

## Before you begin

-   Deploy and start a MID Server.
-   Enable the MID Web Server \[com.snc.sa.mid.webserver\] plugin.

Role required: agent\_admin.

## About this task

Agent Client Collector supports the following authentication strategies:

-   **Keybased**: For backwards \(pre-Zurich release\) compatibility only. See [Configure key-based MID Web Server authentication](configure-mid-web-server-extension-metric-data.md).
-   **API key**: See [Configure MID Web Server API key authentication](mid-web-server-api-key-authentication.md).
-   **mTLS**: See [MID Web Server and agent mTLS Authentication](../concept/mid-web-server-mTLS-authentication.md).

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Extensions** &gt; **MID Web Server**.

2.  In the MID Web Server Contexts list, click **New**.

3.  Fill in the values on the [Event Management MID Web Server extension form](../reference/configure-midwebserver-extension-form.md).

4.  Click **Save** to save the data.

5.  Restart the MID Web Server extension to apply your changes.

6.  Navigate to **All** &gt; **MID Server** &gt; **Extensions** &gt; **MID Web Server** and select the MID Server you just created.

7.  In the **Related Links** section, click **Start** to start the extension.


