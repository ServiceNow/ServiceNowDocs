---
title: Domain separation support for AI Data Explorer
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for AI Data Explorer. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Domain separation support for AI Data Explorer

Domain separation is supported for AI Data Explorer. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Overview of domain separation in AI Data Explorer

The goal of AI Data Explorer is to provide shared spaces, called "explorations," where collaborators can ask for and discuss AI-generated data visualizations with summaries. The AI also suggests follow-up questions. AI Data Explorer shows data only from domains that collaborators can access.

## How domain separation works in AI Data Explorer

When a user in an exploration asks a question of the AI, the answer is limited to data from domains that the user and other collaborators can access. Users from a child domain cannot see explorations from parent or sibling domains, but users from a parent domain can see explorations from child domains if those explorations are shared with them.

All AI Data Explorer tables have domain fields to associate explorations to domains and restrict access accordingly.

**Parent Topic:**[AI Data Explorer reference](now-assist-explorer-reference.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

