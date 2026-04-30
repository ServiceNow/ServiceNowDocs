---
title: Audiences
description: Target portal content and lifecycle event activities to specified audiences with audience records.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reusable components, Setup employee communications, Configure, Employee Center, Employee Service Management]
---

# Audiences

Target portal content and lifecycle event activities to specified audiences with audience records.

|For|Use case|
|---|--------|
|Portal content|Defines the conditions or criteria that a user must meet to see content in the portal. See [Scheduling the delivery of content](../task/ecpro-schedule-content.md) for more information.|
|Org chart page and my team widget|Defines when new hires display on the org chart page and my team widget in the portal.|
|Lifecycle event activity|\(Enterprise Onboarding and Transitions\) Defines whether the activity should trigger for the lifecycle event case.|

-   **Scoped cache**

    You can add scoped cache for HR criteria to optionally save the evaluation results in cache. This is an optional feature that is available by passing a Boolean "true" as the "useCache" parameter.

    You can also define how long in minutes to retain the cached entries via the sn\_hr\_core.cache.hrcriteria.ttl system property.


