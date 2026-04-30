---
title: Foundation data sync
description: Foundation data sync \(FDS\) enables structured, periodic data sharing from provider to consumer instances. It ensures that consumers have access to accurate, up-to-date foundational data from providers, supporting better service delivery, and operational alignment.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Service Exchange]
---

# Foundation data sync

Foundation data sync \(FDS\) enables structured, periodic data sharing from provider to consumer instances. It ensures that consumers have access to accurate, up-to-date foundational data from providers, supporting better service delivery, and operational alignment.

FDS is a data synchronization mechanism that enables a provider instance to share foundational data, such as server, hardware, network information with consumer instances on a scheduled cadence daily, weekly, or monthly.

FDS supports all CMDB CI extended tables and the following non-CMDB tables: Asset, User, Group, Location, Company, and Department.

## Benefits of FDS

FDS supports the service life cycle by enabling providers to share foundational data with consumers in a structured, automated way. This data transfer provides the essential context for operational workflows, reduces manual effort, and eliminates the need to exchange data through external channels.

## Use Case Example

A telecom provider, XYZ company, does not own or manage its own servers. Instead, it relies on a third-party infrastructure provider, ABC company. ABC maintains the configuration data for the servers, including hardware specifications and network dependencies.

XYZ needs this data to assign users to the correct servers based on bandwidth requirements. FDS enables ABC to push this data to XYZ regularly, ensuring XYZ has the information it requires to deliver reliable services. In this scenario, ABC is the provider, XYZ is the consumer, and the data flows from ABC to XYZ.

**Related topics**  


[Using foundation data sync as a provider](service-bridge-v2-using-foundation-data-sync.md)

[Using foundation data sync as a consumer](service-bridge-v2-using-foundation-data-sync-for-consumer.md)

