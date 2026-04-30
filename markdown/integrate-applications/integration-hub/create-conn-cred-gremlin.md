---
title: Create Connection and Credential record for the Gremlin spoke
description: Authorize the Gremlin spoke actions by creating connection and credential record for the application registered in Gremlin. The Gremlin spoke connection and credential alias uses these connections and credentials to authorize actions.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Gremlin Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Create Connection and Credential record for the Gremlin spoke

Authorize the Gremlin spoke actions by creating connection and credential record for the application registered in Gremlin. The Gremlin spoke connection and credential alias uses these connections and credentials to authorize actions.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Gremlin spoke.
-   Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Connection &amp; Credential Alias**.

2.  Open the record, **Gremlin**.

3.  Click the **Create New Connection &amp; Credential** related link.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record. By default, this is `Gremlin Connection`. You may change it as per your requirement.|
    |Connection URL|URL to connect to Gremlin. By default, this is `https://api.gremlin.com`.|
    |API Version|API version of the Gremlin platform. By default, this is `v1`.|
    |Team ID|Team ID of your team.|
    |API Key|API Key of your team.|
    |Credential Name|Name to identify the credential record. By default, this is `Gremlin Credentials`. You may change it as per your requirement.|

5.  Click **Create**.


