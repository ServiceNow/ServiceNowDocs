---
title: Upgrade Change Management
description: Activate Change Management core and update your change types and customizations when you upgrade an instance that used Change Management before the Geneva release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/migrate-change-mgmt-pre-geneva.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Explore, Change Management, IT Service Management]
---

# Upgrade Change Management

Activate Change Management core and update your change types and customizations when you upgrade an instance that used Change Management before the Geneva release.

## Before you begin

Prior to Geneva, Change Request installed the Conflict Detection, Best Practice Change Risk Calculator, Change Risk Assessment, and Bulk CI Changes plugins by default.

Role required: admin

## About this task

Before the Geneva release, Change Management installed the Conflict Detection, Best Practice Change Risk Calculator, Change Risk Assessment, and Built CI Changes plugins by default. New instances from Geneva onward also install the Standard change catalog, State Model, and Mass updates CI plugins by default.

## Procedure

1.  Activate the Change Management core, State Model, Standard change catalog, and Mass updates CI plugins.

    -   If you are upgrading from a release prior to Geneva, you can choose to activate Change Management core, State Model, Standard change catalog, and Mass updates CI plugins. The State Model, and Standard change catalog plugins are dependent on the Change Management core plugin. Hence, activating either the [State model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/t_ActivateStateModel.md) or the [Standard change catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/t_ActivateStandardChangeCatalog.md) plugins results in the activation of the Change Management core plugin.

        Also consider the following consequences of activating Change Management core and the subsequent changes you might need to make to best suit your organization's requirements:

        -   The previous change types are updated from routine, comprehensive, and emergency to standard, normal, and emergency respectively. Analyze customizations that you may have performed that reference old change type values since they are affected and require updating.
        -   When Change management core is activated, the change types are updated.
    -   Update your change types and customizations.

        -   The change types are updated from routine, comprehensive, and emergency to standard, normal, and emergency. Update any customizations that reference the old change type values.
        -   If you created change types and the default change types, customize them based on the new change types.
        -   A new ACL, **change\_request.type**, prevents users from updating the change type. To allow a role to update the change type, for example from **Normal** to **Emergency**, remove **nobody** from the **Requires role** list of the ACL and add the role.
        -   If you had the Bulk CI plugin installed, then install the Mass updates CI plugin.

## Result

Change Management uses the standard, normal, and emergency change types and the state model, and your customizations reference the new change type values.

**Parent Topic:**[Exploring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/exploring-change-management.md)

