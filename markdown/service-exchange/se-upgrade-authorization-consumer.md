---
title: Upgrade authorization on a consumer instance
description: Upgrade a provider connection from the Resource Owner Password Credentials \(ROPC\) OAuth grant type to client credentials without off-boarding and re-onboarding the provider connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-upgrade-authorization-consumer.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Connect to a provider, Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Upgrade authorization on a consumer instance

Upgrade a provider connection from the Resource Owner Password Credentials \(ROPC\) OAuth grant type to client credentials without off-boarding and re-onboarding the provider connection.

## Before you begin

The provider and consumer instances must be on V2.5.X or later.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Providers Connections**.

2.  Select a provider connection number to open the record.

3.  Check that **Upgrade Auth** appears in the form header.

    If the option isn't shown, the connection already uses Client Credentials.

4.  In the Provider page form header, check the **Upgrade Auth**.

    -   The upgrade starts immediately. There is no confirmation dialog.
    -   The form reloads when the upgrade completes. This can take a few minutes.

## Result

The form displays the message `Authorization successfully upgraded to Client Credentials.` Outbound status and Inbound status show Active Replication, and the **Upgrade Auth** option no longer appears in the form header. If a different message appears, see Troubleshooting.

