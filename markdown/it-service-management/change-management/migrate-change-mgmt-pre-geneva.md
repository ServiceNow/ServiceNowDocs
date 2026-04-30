---
title: Upgrade Change Management
description: Follow these instructions to upgrade your Change Management system.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Change Management, IT Service Management]
---

# Upgrade Change Management

Follow these instructions to upgrade your Change Management system.

## Before you begin

Prior to Geneva, Change Request installed the Conflict Detection, Best Practice Change Risk Calculator, Change Risk Assessment, and Bulk CI Changes plugins by default.

For new instances from Geneva onwards, the Standard change catalog, State Model, and Mass updates CI plugins are also installed by default.

Role required: admin

## Procedure

1.  Choose one of the following options.

    -   If you are upgrading from a release prior to Geneva, you can choose to activate Change Management core, State Model, Standard change catalog, and Mass updates CI plugins. The State Model, and Standard change catalog plugins are dependent on the Change Management core plugin. Hence, activating either the [State model](t_ActivateStateModel.md) or the [Standard change catalog](t_ActivateStandardChangeCatalog.md) plugins results in the activation of the Change Management core plugin.

        Also consider the following consequences of activating Change Management core and the subsequent changes you might need to make to best suit your organization's requirements:

        -   The previous change types are updated from routine, comprehensive, and emergency to standard, normal, and emergency respectively. Analyze customizations that you may have performed that reference old change type values since they are affected and require updating.
        -   When Change management core is activated, the change types are updated.
    -   Perform the following tasks after you activate Change management core to ensure that change types and customizations are updated if you already upgraded from a release prior to Geneva.

        -   If you had created newer change types in addition to the default change types, then you must customize them based on the new change types being introduced.
        -   Modify the customizations that are affected to use the new change type values.
        -   A new ACL, **change\_request.type**, prevents users from updating the change type. If you allow any roles to update the type of a change request, for example, from **Normal** to **Emergency**, modify the ACL. Remove **nobody** from the **Requires role** list and add the roles allowed to update the change type.
        -   If you had the Bulk CI plugin installed, then install the Mass updates CI plugin for enhanced user experience and alignment with the new plugins.

**Parent Topic:**[Exploring Change Management](../concept/exploring-change-management.md)

