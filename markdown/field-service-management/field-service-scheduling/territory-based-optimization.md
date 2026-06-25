---
title: Territory-Based Optimization
description: Enable the Field Service Territory model to focus optimization on territories rather than assignment groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/territory-based-optimization.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Territory-Based Optimization

Enable the Field Service Territory model to focus optimization on territories rather than assignment groups.

You must [Configure Territory Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/configuring-territory-planning-fsm.md). When implementing Schedule Optimization based on territories, consider the following points:

-   **Plugin dependencies**

    Territory-based optimization requires the Territory Planning plugin. The following conditions apply:

    -   If the Territory Planning plugin is not installed or the Territory Model is inactive, optimization continues using assignment groups.
    -   If both the Territory Planning and Schedule Optimization plugins are installed but the Territory Model is inactive, tasks are optimized based on assignment groups. Keep territory-related batches inactive until you activate the Territory Model.
    -   If both plugins are installed and the Territory Model is active, tasks are optimized exclusively based on territories. You can create scopes specifically for territories.
-   **Activation prerequisite**

    Before [Enabling the territory model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/enable-territory-model.md), confirm that batches optimized by assignment groups are inactive and batches optimized by territories are active.

-   **Post-activation**

    After activating the Territory Model, tasks require a territory selection for Schedule Optimization to assign them to technicians.

-   **Territory membership evaluation**

    Schedule Optimization evaluates territory membership at the day level. If a technician belongs to multiple territories during a single day, the system treats them as a member of all those territories for the entire day. Membership is based on technician membership records, not optimization horizon dates. The optimization job does not check for date overlaps regardless of when assignments take effect.

-   **Overlapping Territories management**

    Territories can overlap geographically or share technicians.

-   **Agent start location**

    When using the Territory Model, you can temporarily assign a technician a different start location with a specified start and end date. The system uses this temporary location when assigning tasks. When the end date passes or no temporary location is set, the technician's location reverts to their home location. During relocation, you can also adjust technician membership and availability attributes. For more information, see [Move agents between territories in the Territory Planning console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-manager-workforce/relocate-agents-territories.md).


