---
title: Upgrade Change Management
description: Activate Change Management core and update your change types and customizations when you upgrade an instance that used Change Management before the Geneva release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/migrate-change-mgmt-pre-geneva.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, Change Management, IT Service Management]
---

# Upgrade Change Management

Activate Change Management core and update your change types and customizations when you upgrade an instance that used Change Management before the Geneva release.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Activate the Change Management core, State Model, Standard change catalog, and Mass updates CI plugins.

    -   If you are upgrading from a release prior to Geneva, you can choose to activate Change Management core, State Model, Standard change catalog, and Mass updates CI plugins. The State Model, and Standard change catalog plugins are dependent on the Change Management core plugin. Hence, activating either the [State model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_ActivateStateModel.md) or the [Standard change catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_ActivateStandardChangeCatalog.md) plugins results in the activation of the Change Management core plugin.

        Also consider the following consequences of activating Change Management core and the subsequent changes you might need to make to best suit your organization's requirements:

        -   The previous change types are updated from routine, comprehensive, and emergency to standard, normal, and emergency respectively. Analyze customizations that you may have performed that reference old change type values since they are affected and require updating.
        -   When Change management core is activated, the change types are updated.

## Result

**Parent Topic:**[Exploring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/exploring-change-management.md)

