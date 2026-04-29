---
title: Source document import tasks
description: The Regulatory Change Management application processes the alerts that are externally sourced. Source document import tasks are automatically created whenever a source document alert record is marked as applicable. The source document can refer to the legislative and regulatory materials.
locale: en-US
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Source document import tasks

The Regulatory Change Management application processes the alerts that are externally sourced. Source document import tasks are automatically created whenever a source document alert record is marked as applicable. The source document can refer to the legislative and regulatory materials.

When a source document type of regulatory alert is received, it provides the citation title and the number of the citation. The citation may already be available in the GRC library or it can be a newly created citation. Each alert record contains metadata about the source document that helps the key stakeholders to import the record into the regulatory library. The metadata includes the citation name and other information.

Source document alerts are used to create source document import tasks. A source document import task is used to ingest a particular source document that is received from the provider into the regulatory library. This task is performed by the Compliance team members. They import a source document into the regulatory library in ServiceNow as a citation object.

A source document import task is created from a regulatory alert record. The task goes through the source document import workflow or life cycle.

1.  All the unassigned alert records that are of source document type are assessed for applicability.
2.  If a source document alert record is marked as applicable, a source document import task is automatically created.

The source document import life cycle starts from the regulatory alert record. When the manager with the sn\_grc\_reg\_change.manager role marks an unassigned source document alert as applicable, a source document import task gets created.

Users can view the import document task in the Ready to Import state, evaluate the citation associated with the alert, and decide the future course of action for the import document task.

-   **[Users, associated actions, and states for the source document import tasks](../reference/import-doc-tasks-users-actions.md)**  
Managers with the sn\_grc\_reg\_change.manager role and the users with the sn\_grc\_reg\_change.user, or sn\_grc\_reg\_change.admin role can view and perform certain actions on the source document import tasks.
-   **[Manage the source document import tasks](../task/manage-source-document-import-tasks.md)**  
Manage the source document tasks, the associated source document alerts, and other relevant details in the Regulatory Change Tasks module. Use these tasks to identify and comply with the source document changes.

**Parent Topic:**[Regulatory Change Management Core UI](using-rcm-classic-ui.md)

