---
title: Retiring a service instance can affect tangible/physical CIs
description: Because a service instance might depend on a hardware \(tangible/physical\) device that other service instances depend on, you must take care when retiring a service instance.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tangible/physical life cycle, Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Retiring a service instance can affect tangible/physical CIs

Because a service instance might depend on a hardware \(tangible/physical\) device that other service instances depend on, you must take care when retiring a service instance.

## Considerations

A service instance is the logical representation of the underlying tangible/physical and software CIs that work together to implement a business application or system. The service instance represents an instance of the business application or system.

Tangible/physical and software CIs are managed using the tangible/physical life-cycle value pairs. Because a service instance is a logical representation, it is managed as using the intangible/logical life-cycle value pairs. The tangible/physical CIs that are part of the service map under a service instance have their own life cycles, but they are related through the service instance as a specific set of dependencies or decomposition.

-   **Example 1: A tangible/physical CI is not retired when the service instance is retired**

    When a service instance is retired, the associated tangible/physical device might not be retired. For example, the device might remain idle, unrelated to any service instance, until it is reallocated for use by a different service instance.

-   **Example 2: A tangible/physical CI is shared by multiple service instances**

    In the common scenario of a shared database, multiple service instances \(each with a unique database schema\) share a single database service. The database service runs on a single physical host.

    When one of the service instances is retired, the database service and host cannot be retired. All other service instances still depend on the database service that is running on the host.


See [Use Service instance \(Application Services\) dashboard to monitor health](../../configuration-management/task/app-service-dashboard.md).

**Parent Topic:**[Life cycle of tangible/physical CIs](../concept/csdm-lifecycle-hardware.md)

