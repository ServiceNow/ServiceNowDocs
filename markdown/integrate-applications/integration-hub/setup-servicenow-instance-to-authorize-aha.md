---
title: Set up ServiceNow instance for Aha!
description: Set up your ServiceNow instance to add the Aha! Client ID and Client Secret keys.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Aha! Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up ServiceNow instance for Aha!

Set up your ServiceNow instance to add the Aha! Client ID and Client Secret keys.

## Before you begin

ServiceNow Role required: admin

## Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **Connection &amp; Credentials** &gt; **Connection &amp; Credentials Aliases**.

    Connection &amp; Credentials Aliases page appears and shows the list of apps.

3.  Locate and open the Connection &amp; Credentials record for Aha!.

4.  Click the **Create New Connection &amp; Credential** related link.

5.  On the Create Connection and add Credential form, fill in the details.

    |Fields|Descriptions|
    |------|------------|
    |Connection Name|Name of the integration profile.|
    |Connection URL|Connection URL for Aha!.|
    |OAuth Client ID|OAuth2 key that you received while creating an OAuth2 authentication from the Aha! site.|
    |OAuth Client Secret|OAuth Client Secret key that you received while creating an OAuth2 authentication from the Aha! site.|
    |OAuth Redirect URL|ServiceNow redirect URL.|

6.  Click **Configure and get OAuth Token** and then click **Authorize**.


