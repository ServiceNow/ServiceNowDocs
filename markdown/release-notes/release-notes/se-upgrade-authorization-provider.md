---
title: Upgrade authorization on a provider instance
description: Upgrade a consumer connection from the Resource Owner Password Credentials \(ROPC\) OAuth grant type to the client credentials grant type without offboarding or re-onboarding the connection.
locale: en-US
release: brazil
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
---

# Upgrade authorization on a provider instance

Upgrade a consumer  connection from the Resource Owner Password Credentials \(ROPC\) OAuth grant type to the client credentials grant type without offboarding or re-onboarding the connection.

## Before you begin

The provider and consumer instances must be on V2.5.X or later.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Consumers**.

2.  Select a consumer connection number to open the record.

3.  Check that **Upgrade Auth** appears in the form header.

    If the option isn't shown, the connection already uses Client Credentials.

4.  In the Consumer page form header, check the **Upgrade Auth**.

    -   The upgrade starts immediately. There is no confirmation dialog.
    -   The form reloads when the upgrade completes. This can take a few minutes.

## Result

The form displays the message `Authorization successfully upgraded to Client Credentials.` Outbound status and Inbound status show Active Replication, and the **Upgrade Auth** option no longer appears in the form header. If a different message appears, see Troubleshooting.

