---
title: Service provider reference architecture for hybrid
description: Use the hybrid service provider \(SP\) reference architecture for a customized solution. Your customers require a dedicated instance for a specific service. They can still use the shared SP instance for other services, but it requires integration of each instance.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service provider reference architecture, Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Service provider reference architecture for hybrid

Use the hybrid service provider \(SP\) reference architecture for a customized solution. Your customers require a dedicated instance for a specific service. They can still use the shared SP instance for other services, but it requires integration of each instance.

## Hybrid architecture

Your customer may be responsible for delivering this additional service directly. You need to build a hybrid solution of several attributes for your customer to provide.

## Attributes

-   You can share and leverage the administration of the instance. This means that there is no overhead, and you can optimize licenses.
-   If there is a new instance for a decentralized environment, the program team is responsible and funded accordingly as dedicated administrator users for that instance. In a centralized environment where all instances stem from a blueprint, you need duplicate administration licenses.
-   You do not assign fulfillers to a domain. Instead, you can share them across domains.
-   If a customer is sharing both a shared environment and a dedicated environment, they require a fulfiller in both environments. This means more work for each team because the processes for shared and dedicated instances require different work for each instance.
-   The number of users on the instance can change when you get a new customer. A new customer can result in tens or even hundreds of thousands of new users on the system. The number of total users is virtually unlimited in one shared environment.
-   Each instance has a finite number of requesters and fulfillers. When you get a new customer, you must procure an instance that is based on the size and scale of your customer's company.



**Parent Topic:**[Service provider reference architecture](bp-sp-reference-arch-ds.md)

