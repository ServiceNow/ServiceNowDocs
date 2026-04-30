---
title: Scheduled jobs for Governance, Risk, and Compliance
description: Scheduled jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule. GRC administrators run the scheduled jobs on demand to automate the tasks such as setting an entity class on the entities depending on the entity class rule.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Entity classes, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Scheduled jobs for Governance, Risk, and Compliance

Scheduled jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule. GRC administrators run the scheduled jobs on demand to automate the tasks such as setting an entity class on the entities depending on the entity class rule.

Starting with the Xanadu release, the following scheduled jobs are provided for GRC:

-   **GRC set entity class on entities based on entity class rule**: Use this scheduled job to populate the entity class rule for multiple entities at a time. The scheduled job script checks all the entity class rules, checks all the entities where the entity class field is empty, and updates the entity class for multiple entities.

-   **GRC set entity class on entities same as pillar**: This scheduled job is provided for the GRC: Operational Resilience application users.

    The Operational Resilience base system includes five pillars. Pillars are the categories that are used to organize risk data that is pulled from their associated entity types. If the GRC: Operational Resilience application is installed in the instance, the **Pillar** field displays the pillar in the application to which an entity type is assigned. If an entity class is not defined for the entity type, it is mapped to the value that is displayed in the **Pillar** field using the **GRC set entity class on entities same as pillar** job.


**Parent Topic:**[Entity classes](../../grc-common-workspace/concept/entity-class-in-risk-ws.md)

