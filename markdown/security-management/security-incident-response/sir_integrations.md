---
title: Security Incident Response integrations
description: All the Security Operations core applications and non-core third-party integrations are available from the ServiceNow Store. This section provides instructions for activating the integrations and configuring both ServiceNow and third-party integrations. Also included are some basic guidelines for developing your own integrations, as well as details on specific integrations included in the base system.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response integrations

All the Security Operations core applications and non-core third-party integrations are available from the ServiceNow Store. This section provides instructions for activating the integrations and configuring both ServiceNow and third-party integrations. Also included are some basic guidelines for developing your own integrations, as well as details on specific integrations included in the base system.

## Integration Configurations

The base system includes a series of "cards" for each of the integration implementations you can activate and use. Also, cards are displayed for any integrations posted on the ServiceNow Store that have dependencies on Security Operations plugins. The integration cards can be viewed by selecting **Security Operations** &gt; **Integration Configurations**.

![Configuration tiles for integrations](../image/config_tiles.png)

You can filter the visible integrations using the **Category** drop-down menu. The **Show Configurations** drop-down menu lets you see multiple instances of implementations that allow their creation.

## Buttons on integration cards

Integration cards display different buttons depending on the current state of the integration and the source of the card.

|Button|Description|
|------|-----------|
|Install Plugin|Click this button to install the applicable plugin to activate the integration. After the plugin is installed, the button changes to **Configure**.|
|Configure|Click this button to enter information for configuring the integration. For some integrations, you may need to enter API keys or URLs acquired from the website of the third-party integration.|
|New|Certain integrations, such as Carbon Black and IBM QRadar, allow you to define multiple implementations of the same integration. For those integrations, click **New** after the plugin is activated. The cards allow you to install plugins \(where applicable\) and configure the implementations for use.|
|Open Page|In the base system, your instance performs a query to the ServiceNow Store for any applications that have dependencies on Security Operations plugins. When those applications are found, and the associated application plugins are activated, integration cards for them are displayed with the other security integration cards. Click **Open Page** to access the website of the third-party application to configure the integration. After you have completed the configuration, the **Open Page** button changes to **Configure**.|

