---
title: Configure the ServiceNow Otto webhook connection
description: Configure the otto\_webhook Connection &amp; Credential Alias so ServiceNow can deliver webhook events to the ServiceNow Otto listener.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/t\_configure-moveworks-webhook.html
release: brazil
topic_type: task
last_updated: "2025-07-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Break-Fix and Store Audit overview, ServiceNow Otto for Retail Service Management \(RSM\), Retail]
---

# Configure the ServiceNow Otto webhook connection

Configure the otto\_webhook Connection &amp; Credential Alias so ServiceNow can deliver webhook events to the ServiceNow Otto listener.

## Before you begin

Obtain the listener endpoint URL and the API key from the ServiceNow Otto team. The webhook connection supports API key authentication only.

Role required: admin

## Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases** and open `otto_webhook`.

2.  In the **Connections** related list, click **New**.

    Set **Connection URL** to the ServiceNow Otto listener endpoint and save.

3.  In the **Credentials** related list, select **New** and then select **API Key Credentials**.

    Set **API Key** to the key from the ServiceNow Otto team, set **API Key Header Name** to `Authorization`, and set **API Key Prefix** to `Bearer`. Leave **MID Servers** blank.

4.  Save the credential.

5.  Open the connection record, set its **Credential** field to the new credential, and save.

6.  On a non-production instance, transition a BF case \(with `contact_type = otto`\) to Resolved and verify the payload appears in the ServiceNow Otto listener logs.

    If the call does not arrive, check **System Logs** &gt; **Outbound HTTP Requests**.


**Parent Topic:**[ServiceNow Otto for Break-Fix and Store Audit overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-breakfix-storeaudit-overview.md)

