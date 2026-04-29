---
title: Deactivating entity-based access configuration
description: Deactivating entity-based access \(EBA\) not only disables the configuration but also streamlines admin workflows by automating record-level access evaluation.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Deactivating entity-based access configuration

Deactivating entity-based access \(EBA\) not only disables the configuration but also streamlines admin workflows by automating record-level access evaluation.

When you initiate the deactivation of an EBA configuration, the system performs an evaluation. It assesses whether the selected configuration is the only active one influencing the access restrictions of associated entity records. If it’s identified as the sole active configuration, the system automatically disables the corresponding EBA restrictions at the record-level. This action removes outdated access controls and saves administrators from performing manual updates.

If other active configurations exist, the system retains EBA restrictions and restricts access only for users linked to the configuration being deactivated. This conditional approach helps ensure that deactivation actions don’t inadvertently affect other active access controls.

## Benefits of automating deactivation process

-   Reduces manual administrative effort by automating impact evaluation.
-   Enhances consistency in releasing record-level access restrictions where applicable.
-   Minimizes the risk of unintentional data exposure or access gaps during configuration changes.

**Parent Topic:**[Entity Based Access](entity-based-access.md)

