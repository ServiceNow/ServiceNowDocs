---
title: Entity-based record access rules
description: The entity-based record access rules let admins apply restrictions automatically to new and changed records. This configuration ensures that access settings stay enforced. No manual updates are needed when records are created, modified, or when users are added to user fields or user group fields.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Entity-based record access rules

The entity-based record access rules let admins apply restrictions automatically to new and changed records. This configuration ensures that access settings stay enforced. No manual updates are needed when records are created, modified, or when users are added to user fields or user group fields.

Entity-based record access rules apply access restrictions on newly created and modified records. These rules can be configured and activated in the Core UI, for a specific primary record type such as Risk or Issue. After activation, any associated secondary records, such as Risk Response Task or Remediation Task, inherit access restrictions from their corresponding primary records. The rule applies when records are linked to entities with active configurations.

To ensure users referenced on records continue to have access when entity-based access restrictions are applied, administrators must configure record attribute user access. This configuration allows access for users and groups referenced in user fields or user group fields. It is set up per table and doesn't apply automatically to secondary records, so each secondary record type must be configured separately. For more information, see [Configure entity-based record access rules](../task/configure-continuous-eba-monitoring-on-record-types.md).

To support entity-based access restrictions, the system applies the access restrictions on new records based on the activated rules:

-   Entity class and entity type adjustments are assessed, and access implications are handled automatically.
-   Users who are part of user groups or user fields on a record continue to have access to that record.
-   The system automatically assesses and enforces access when entities are added, removed, or moved within an entity based access governed hierarchy.

    This enforcement helps maintain the correct access settings for downstream records, keeping them aligned with the new structure.


## Key Benefit

Enabling record attribute user access ensures that users and groups referenced on records retain access even when entity-based access restrictions are applied. This prevents disruption and maintains seamless access control during data segregation.

**Parent Topic:**[Entity Based Access](entity-based-access.md)

