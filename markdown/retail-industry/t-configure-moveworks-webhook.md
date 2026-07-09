---
title: Configure the Moveworks webhook connection
description: Configure the moveworks\_webhook Connection &amp; Credential Alias so ServiceNow can deliver webhook events to the Moveworks listener.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/t-configure-moveworks-webhook.html
release: australia
topic_type: task
last_updated: "2025-07-01"
reading_time_minutes: 1
breadcrumb: [Moveworks integration overview, Configure, Retail]
---

# Configure the Moveworks webhook connection

Configure the moveworks\_webhook Connection &amp; Credential Alias so ServiceNow can deliver webhook events to the Moveworks listener.

## Before you begin

Obtain from the Moveworks team: listener endpoint URL, credential type, and credential values.

**Warning:** HMAC-SHA256 and HMAC-SHA512 are not yet implemented. Contact the support team before configuring if HMAC is required.

Role required: `admin`

## Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases** and open `moveworks_webhook`.

2.  In the **Connections** related list, click **New**.

    Set **Connection URL** to the Moveworks listener endpoint and save.

3.  In the **Credentials** related list, click **New** and select the credential type.

    Use Bearer token when Moveworks provides a static token.

4.  Enter the credential values and save.

    Then open the connection record, set its **Credential** field to the new credential, and save.

5.  On a non-production instance, transition a BF case \(with `contact_type = moveworks`\) to Resolved and verify the payload appears in the Moveworks listener logs.

    If the call does not arrive, check **System Logs** &gt; **Outbound HTTP Requests**.


