---
title: ITIL change process assignment for change models
description: The change model specifies which ITIL change process it represents: Normal, Standard, or Emergency. The change is still governed by the model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/itil\_change\_process\_models.html
release: brazil
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [ITIL change process, change model, Change Management]
breadcrumb: [Configure, Change Management, IT Service Management]
---

# ITIL change process assignment for change models

The change model specifies which ITIL change process it represents: Normal, Standard, or Emergency. The change is still governed by the model.

## ITIL change process assignment

Previously, the ChangeRequest API methods newNormal, newStandard, and newEmergency each created a change request from one specific out-of-the-box change model for the corresponding ITIL change process. The system provided the Normal, Standard, and Emergency change models as base system data. Change managers could create additional custom change models, but the API methods remained fixed to those original base system data models regardless of any customizations.

The ITIL change process assignment removes this fixed dependency. A change manager can designate any active change model, including a custom one, to represent the Normal, Standard, or Emergency ITIL change process. The ChangeRequest API then uses whichever model is currently designated for that process.

## Benefits

Assigning an ITIL change process to a change model provides the following benefits:

-   Change managers can choose which change model represents each ITIL change process without customizing the ChangeRequest API.
-   The ChangeRequest API automatically uses the designated change model when it creates a Normal, Standard, or Emergency change request.
-   Change request creation continues to work as before for any ITIL change process that doesn't have a change model designated for it.

## How it works

Each change model record includes an **ITIL change process** field that a change manager sets to **Standard**, **Normal**, or **Emergency**, or leaves the field at the default value of **None**.

The system enforces the following rules when a change manager assigns a process to a change model:

-   Only one active change model per domain can be designated for a given ITIL change process at a time. If a change manager activates a second change model designated for a process that's already represented by another active model, the system blocks the change.
-   A change manager cannot designate a change model for a process if they don't have write access to the change model that's already assigned to that process.

When the ChangeRequest API creates a new Normal, Standard, or Emergency change request, it resolves the change model to use as follows:

1.  The API searches for an active change model designated for the matching ITIL change process.
2.  If it finds a designated change model, the API creates the change request using that model.
3.  If no change model is designated for the process, the API falls back to the default change model for that process.

-   **[Assign an ITIL change process to a change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/assign_itil_change_process_model.md)**  
Assign an ITIL change process to a change model so the ChangeRequest API uses that model when it creates a matching change request.

**Parent Topic:**[Configuring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-change-management.md)

**Related topics**  


[Assign an ITIL change process to a change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/assign_itil_change_process_model.md)

