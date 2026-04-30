---
title: Service provider reference architecture for dedicated instances
description: Service provider \(SP\) customers can access SP services by using a portal to a dedicated instance. SPs use these dedicated instances to manage their service delivery.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service provider reference architecture, Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Service provider reference architecture for dedicated instances

Service provider \(SP\) customers can access SP services by using a portal to a dedicated instance. SPs use these dedicated instances to manage their service delivery.

## Dedicated instances

![Dedicated instance](../image/bp-sp-reference-architecture-dedicated.png)

## Attributes

-   Dedicated instances require that you have separate administration and dedicated teams. You need multiple licenses for the administrators and developers who log in to multiple instances.
-   Each instance has a finite number of requesters and fulfillers. When you get a new customer, you must procure an instance that is based on the size and scale of your customer's company.

## Shared instance

![Dedicated vs shared](../image/bp-dedicated-vs-shared.png "Dedicated vs.shared instance")

![Reference architecture](../image/bp-dedicated-ds-hybrid-siam.png "SP reference architecture comparison")

**Parent Topic:**[Service provider reference architecture](bp-sp-reference-arch-ds.md)

