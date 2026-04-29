---
title: Set up the Shodan spoke
description: Integrate the Shodan account and your ServiceNow instance using the API keys.Add and configure Shodan connections to authenticate ServiceNow requests to the Shodan server.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Shodan Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Shodan spoke

Integrate the Shodan account and your ServiceNow® instance using the API keys.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Shodan spoke.
-   API key of your Shodan account.
-   Role required: admin.

## Configure a connection for Shodan spoke

Add and configure Shodan connections to authenticate ServiceNow® requests to the Shodan server.

### About this task

You must configure two connections: Shodan and Shodan Exploit.

### Before you begin

-   Role required: admin
-   Log in to your Shodan account and get the API Key.

### Procedure

1.  Configure the Shodan connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Select the **Integrations** tab.

    3.  In the Search all connections field, enter `Shodan`.

        The **Outbound** tab is active by default. If it's not active, toggle it to activate.

    4.  On the Shodan alias tile, select **View Details**.

        ![View Details button on the Shodan alias tile.](../image/shodan-conn-template.png)

    5.  Select **Configure**.

    6.  Fill the form.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Name to identify the connection. The default value is Shodan.|
        |Connection URL|URL to connect to Shodan. The default value is `https://api.shodan.io`|
        |Key|API key from your Shodan account.|

        ![Shodan alias connection form.](../image/shodan-alias-conn-form.png)

    7.  Select **Create Connection**.

2.  Configure the Shodan Exploit connection.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Select the **Integrations** tab.

    3.  In the Search all connections field, enter `Shodan Exploit`.

        The **Outbound** tab is active by default. If it's not active, toggle it to activate.

    4.  On the Shodan Exploit alias tile, select **View Details**.

        ![Connection template for Shodan Exploit.](../image/shodan-exploit-conn-template.png)

    5.  Select **Configure**.

    6.  Fill the form.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Name to identify the connection. The default value is Shodan.|
        |Connection URL|URL to connect to Shodan. The default value is `https://api.shodan.io`|
        |Key|API key from your Shodan account.|

        ![Shodan Exploit alias connection form.](../image/shodan-exploit-alias-conn-form.png)

    7.  Select **Create Connection**.


