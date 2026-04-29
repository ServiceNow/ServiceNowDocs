---
title: Foundation data sync
description: Foundation data sync \(FDS\) enables structured, periodic data sharing from provider to consumer and consumer to provider instances. FDS ensures that both providers and consumers can share and receive accurate, up‑to‑date foundational data, supporting better service delivery and operational alignment.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Service Exchange]
---

# Foundation data sync

Foundation data sync \(FDS\) enables structured, periodic data sharing from provider to consumer and consumer to provider instances. FDS ensures that both providers and consumers can share and receive accurate, up‑to‑date foundational data, supporting better service delivery and operational alignment.

FDS is a data synchronization mechanism that enables a provider instance to share foundational data, such as server, hardware, network information with consumer instances and consumers instance to provider instances on a scheduled cadence \(daily, weekly, or monthly\).

FDS supports two separate unidirectional data flows, allowing both providers and consumers to act as either data source or recipient depending on the business need:

-   **Consumer-bound FDS**

    Provider shares data with consumer instances.

-   **Provider-bound FDS**

    Consumer shares data with provider instances.


**Note:** These are independent flows. Each flow must be configured separately. Establishing data sharing in one direction does not automatically enable data sharing in the reverse direction.

FDS supports all CMDB CI extended tables and the following non-CMDB tables: Asset, Company, User, Group, Location, Department, Stockroom, Product Model, Knowledge, Hardware Model, Consumable Model, Hardware, and Consumable. If you need support for any additional table, contact Support.

## Benefits of FDS

FDS supports the service life cycle by enabling providers to share foundational data with consumers in a structured, automated way. This data transfer provides the essential context for operational workflows, reduces manual effort, and eliminates the need to exchange data through external channels.

## FDS data flow scenarios

FDS provides two ways to collaborate by sharing date in either direction:

-   **Consumer-bound FDS \(Provider shares data\)**

    The provider creates FDS offering definitions and publishes them to make data available. Consumers browse available offerings and request the data they need. After validation and acceptance, data flows from the provider instance to the consumer instance on the defined schedule.

    The provider controls which tables, fields, and records are shared. Consumers configure how the incoming data maps to their instance tables.

    **Note:** Consumer-bound FDS \(Provider shares data\) is supported from Service Exchange version 2.2.x.

-   **Provider-bound FDS \(Consumer shares data\)**

    The consumer creates FDS offering definitions and publishes them to make data available. Providers browse available offerings and request the data they need. After validation and acceptance, data flows from the consumer instance to the provider instance on the defined schedule.

    The consumer controls which tables, fields, and records are shared. Providers configure how the incoming data maps to their instance tables.

    **Note:** Provider-bound FDS \(Consumer shares data\) is supported from Service Exchange version 2.3.x.


## Use Case Example

A telecom provider, XYZ company, does not own or manage its own servers. Instead, it relies on a third-party infrastructure provider, ABC company. ABC maintains the configuration data for the servers, including hardware specifications and network dependencies.

XYZ needs this data to assign users to the correct servers based on bandwidth requirements. FDS enables ABC to push this data to XYZ regularly, ensuring XYZ has the information it requires to deliver reliable services.

In this scenario, ABC is the provider, XYZ is the consumer, and the data flows from ABC to XYZ.

ABC company also needs visibility into XYZ to understand the consumption pattern. To enable ABC to provide better infrastructure support, XYZ needs to share data back to ABC. FDS enables XYZ company to share usage data with ABC regularly, enabling ABC to make informed decisions about capacity planning and infrastructure optimization.

**Related topics**  


[Configuring outbound foundation data sync as providers](service-bridge-v2-using-foundation-data-sync.md)

[Configuring inbound foundation data sync as providers](service-bridge-v2-configure-inboun-fds-providers.md)

[Configuring inbound foundation data sync as a consumer](service-bridge-v2-using-foundation-data-sync-for-consumer.md)

[Configuring outbound foundation data sync as consumers](using-provider-bound-fds-consumer.md)

