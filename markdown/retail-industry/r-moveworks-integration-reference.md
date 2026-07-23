---
title: Components for Moveworks integration for break-fix
description: Technical reference for webhook events, authentication types, platform artifacts, and troubleshooting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/r-moveworks-integration-reference.html
release: australia
topic_type: reference
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components for Moveworks integration for break-fix

Technical reference for webhook events, authentication types, platform artifacts, and troubleshooting.

## Webhook events

|Event|State transition|Condition|Extra payload field|
|-----|----------------|---------|-------------------|
|`case_assigned`|New \(1\) → Open \(10\)|`contact_type = moveworks`|None|
|`case_resolved`|Any → Resolved \(6\)|`contact_type = moveworks`|Resolution code|
|`case_awaiting_info`|Any → Awaiting Info \(18\)|`contact_type = moveworks`|None|

**Note:** No event is dispatched if the `opened_by` user has no email address. The call is skipped silently and a warning is written to the system log.

**Note:** Bearer token, OAuth 2.0 Client Credentials, and JWT-OAuth are the supported credential types. HMAC-SHA256 and HMAC-SHA512 are not supported.

## Moveworks AI Agent Marketplace

Customize your Moveworks AI Assistant with installable agents from the AI Agent Marketplace.

-   Create: [Create a break-fix case](https://marketplace.moveworks.com/plugins/servicenow-retail-create-breakfix-case#how-to-implement)
-   Update: [Update break-fix case details](https://marketplace.moveworks.com/plugins/servicenow-retail-update-breakfix-case-details#how-to-implement)
-   Notify: [Get notified on break-fix case updates](https://marketplace.moveworks.com/plugins/servicenow-retail-notify-on-breakfix-case-updates#how-to-implement)
-   Get: [Get break-fix case details](https://marketplace.moveworks.com/plugins/servicenow-retail-get-breakfix-case-details#how-to-implement)

## Troubleshooting

|Symptom|Where to check / action|
|-------|-----------------------|
|Webhook call not arriving at the Moveworks listener|Navigate to **System Logs** &gt; **Outbound HTTP Requests** and filter by URL or time. Confirm the `moveworks_webhook` connection URL is set correctly|
|No event dispatched despite a qualifying state change|Verify `contact_type = moveworks` on the case and that `opened_by` has a non-empty email address|
|Authentication error in outbound logs|Confirm the credential type is not HMAC. Re-enter credential values in the `moveworks_webhook` alias and retest|
|ServiceNow dispatches the event but Moveworks does not act on it|Verify all four side plugins from Moveworks are installed in the Moveworks environment \(see [Moveworks integration overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)\)|

**Parent Topic:**[Components installed with plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-components-installed-with-plugins.md)

