---
title: OAuth issues
description: Learn how to fix OAuth token refresh issues.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Troubleshoot synthetic monitors, Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# OAuth issues

Learn how to fix OAuth token refresh issues.

## Condition

OAuth token doesn't refresh as expected.

## Cause

Your OAuth provider and server have different refresh time periods. Refresh time periods are based on the OAuth provider. When creating an OAuth connection, you configure it to have an x-amount of time before needing reauthentication. If that configured amount of time isn't the same as your provider's, your token might require a refresh sooner or later than expected.

## Remedy

Refer to your OAuth provider's documentation when configuring OAuth. See [OAuth Inbound and Outbound authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/api-inbound-and-outbound.md) for more information.

**Parent Topic:**[Troubleshoot synthetic monitors](troubleshoot-synthetic-monitors.md)

