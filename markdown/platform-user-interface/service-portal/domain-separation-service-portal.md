---
title: Domain separation and Service Portal
description: Domain separation is unsupported in Service Portal. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Portal reference, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Domain separation and Service Portal

Domain separation is unsupported in Service Portal. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: No support

-   The domain field may exist on data tables but there is no business logic to manage the data.
-   This level is not considered domain-separated.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Overview

Domain separation provides complete data isolation for domain-specific users.

## How domain separation works in Service Portal

Elements of the Service Portal platform such as settings, portals, pages and widgets are not domain-separated. However, the data within widgets does display when based on the appropriate domain. To provide different experiences, admins should create separate service portals, each with unique URLs, that they can redirect users to.

**Parent Topic:**[Service Portal reference](reference-service-portal.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

