---
title: Create a connection record
description: Create a connection record with all the details needed to integrate your ServiceNow instance to the Asana instance. When your ServiceNow instance requests a connection, the OAuth app you had set up authenticates the request based on the details in the connection record.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the Asana spoke, Asana Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a connection record

Create a connection record with all the details needed to integrate your ServiceNow instance to the Asana instance. When your ServiceNow instance requests a connection, the OAuth app you had set up authenticates the request based on the details in the connection record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select Connections.

3.  Turn on the Outbound tab.

4.  In the Search all connections field, enter `Asana`.

5.  On the Asana card, select **View Details**.

6.  Select **Configure**.

7.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection established with the Asana instance. The first connection's default name is automatically assigned to match the name specified in the Connections and Credentials form on the Connection &amp; Credential Aliases page. To provide your custom name, create a connection record by selecting **Add Connection**.|
    |Connection URL|The URL your ServiceNow instance uses to connect to the Asana instance.|
    |OAuth Client ID|The client ID that you had generated while you set up the OAuth application.|
    |OAuth Client Secret|The client secret that you had generated while you set up the OAuth application.|
    |OAuth Redirect URL|The redirect URL that the OAuth application uses to redirect to your ServiceNow instance. The URL must be in the format `https://<your instance name>.service-now.com/oauth_redirect.do`.|

8.  Select **Configure and Get OAuth Token**.

    The OAuth application authenticates the connection request and provides a temporary token to access the Asana instance.


