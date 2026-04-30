---
title: Domain Separation release notes
description: The ServiceNow Domain Separation application enables you to separate data, processes, and administrative tasks into logically defined domains. Domain Separation is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Domain Separation release notes

The ServiceNow® Domain Separation application enables you to separate data, processes, and administrative tasks into logically defined domains. Domain Separation is a new application in the Zurich release.

## Domain Separation highlights for the Zurich release

-   Changes to the domain table are queued sequentially and batched into a single background job. This helps simplify domain table updates.
-   Domain Admins can delete by domain to efficiently manage domains and reduce storage overhead.

See [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

## Domain Separation features

-   ****

    Domain Admins may now delete by domain to efficiently manage domains and reduce storage overhead. The tool also includes data recovery and retention, enabling rollbacks and retention policy setting.

-   ****

    Changes to the domain table are now queued sequentially and batched into a single background job. This helps simplify domain table updates. Users are notified when a job needs to be delayed as well when a job needs to start.


## Activation information

Domain Separation is a ServiceNow AI Platform feature that is available with activation of the com.glide.domain.activation\_utility. For details, see [Domain separation plugin](https://www.servicenow.com/docs/access?context=domain-sep-plugin&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

