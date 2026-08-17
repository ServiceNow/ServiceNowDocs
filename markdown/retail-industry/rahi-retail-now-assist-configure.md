---
title: Configure ServiceNow Otto for Retail Service Management \(RSM\)
description: The collection comprises of ServiceNow Otto for Retail Service Management \(RSM\) and RSM AI agent collection. The ServiceNow Otto for Retail Service Management \(RSM\) and RSM AI agent collection together enable the store inquiry AI agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/retail-industry/rahi-retail-now-assist-configure.html
release: zurich
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Retail Service Management \(RSM\), Retail]
---

# Configure ServiceNow Otto for Retail Service Management \(RSM\)

The collection comprises of ServiceNow Otto for Retail Service Management \(RSM\) and RSM AI agent collection. The ServiceNow Otto for Retail Service Management \(RSM\) and RSM AI agent collection together enable the store inquiry AI agent.

-   The HQ agent can leverage the store inquiry AI agent either manually or by enabling or configuring the trigger.
-   A trigger allows the AI agent to launch automatically without requiring a HQ agent request when the trigger condition is met.
-   The trigger that is shipped with this release is configured to launch for the HQ agent when the case state changes to Open from New and Assigned to field is not empty.
-   By default, the trigger being shipped is disabled and HQ agent can navigate to the AI agent and enable the trigger.

