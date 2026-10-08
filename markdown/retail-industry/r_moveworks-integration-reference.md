---
title: Components for ServiceNow Otto integration for break-fix
description: Technical reference for webhook events, authentication types, platform artifacts, and troubleshooting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/r\_moveworks-integration-reference.html
release: brazil
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Break-Fix and Store Audit overview, ServiceNow Otto for Retail Service Management \(RSM\), Retail]
---

# Components for ServiceNow Otto integration for break-fix

Technical reference for webhook events, authentication types, platform artifacts, and troubleshooting.

## Webhook events

|Event|State transition|Condition|Extra payload field|
|-----|----------------|---------|-------------------|
|`case_assigned`|New \(1\) → Open \(10\)|`contact_type = otto`|None|
|`case_resolved`|Any → Resolved \(6\)|`contact_type = otto`|Resolution code|
|`case_awaiting_info`|Any → Awaiting Info \(18\)|`contact_type = otto`|None|

**Note:** No event is dispatched if the `opened_by` user has no email address. The call is skipped silently and a warning is written to the system log.

**Note:** API Key Credentials is the only supported credential type. The key is sent in a single header, by default `Authorization: Bearer <key>`. If the credential has no API key, the webhook call fails instead of being sent without authentication.

## ServiceNow Otto AI Agent Marketplace

Customize your ServiceNow Otto AI Assistant with installable agents from the AI Agent Marketplace.

-   Create: [Create a break-fix case](https://marketplace.otto.servicenow.com/plugins/servicenow-retail-create-breakfix-case#how-to-implement)
-   Update: [Update break-fix case details](https://marketplace.otto.servicenow.com/plugins/servicenow-retail-update-breakfix-case-details#how-to-implement)
-   Notify: [Get notified on break-fix case updates](https://marketplace.otto.servicenow.com/plugins/servicenow-retail-notify-on-breakfix-case-updates#how-to-implement)
-   Get: [Get break-fix case details](https://marketplace.otto.servicenow.com/plugins/servicenow-retail-get-breakfix-case-details#how-to-implement)

## Troubleshooting

|Symptom|Where to check / action|
|-------|-----------------------|
|Webhook call not arriving at the ServiceNow Otto listener|Navigate to **System Logs** &gt; **Outbound HTTP Requests** and filter by URL or time. Confirm the `otto_webhook` connection URL is set correctly|
|No event dispatched despite a qualifying state change|Verify `contact_type = otto` on the case and that `opened_by` has a non-empty email address|
|Authentication error in outbound logs|Confirm the credential on the `otto_webhook` connection is an API Key credential with the API key filled in and the header name and prefix set. Re-enter the API key and retest.|
|ServiceNow dispatches the event but ServiceNow Otto does not act on it|Verify all four side plugins from ServiceNow Otto are installed in the ServiceNow Otto environment \(see [ServiceNow Otto integration overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/c_moveworks-integration-overview.md)\)|

**Parent Topic:**[ServiceNow Otto for Break-Fix and Store Audit overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-breakfix-storeaudit-overview.md)

