---
title: Domain separation and Proactive Triggers
description: Domain separation is supported for Proactive Triggers. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Proactive Triggers reference, Proactive Triggers, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Proactive Triggers

Domain separation is supported for Proactive Triggers. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Overview

The Proactive Triggers rich text pop-up messages provide users with actions according to real-time Proactive Triggers data. Domain separation is enabled and supported at the basic level.

## How domain separation works in Proactive Triggers

Each domain has its own set of rules and trigger types that are evaluated independently of other domains.

**Parent Topic:**[Proactive Triggers reference](../reference/proactive-triggers-reference.md)

**Related topics**  


[Domain separation explained](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

