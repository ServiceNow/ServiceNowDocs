---
title: Model script editor role
description: This role grants write access to the scripted condition fields on model state transition conditions and model condition types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/model-script-editor-roles.html
release: australia
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create a Change model, Configure, Change Management, IT Service Management]
---

# Model script editor role

This role grants write access to the scripted condition fields on model state transition conditions and model condition types.

## Role required to edit scripted condition fields

|Role|Description|Elevated privilege|Grants write access to|
|----|-----------|------------------|----------------------|
|`change_model_script_admin`|Enables modification of the scripted condition fields on transition conditions and transition condition types.|false|Scripted condition fields on change model state transition conditions and change model condition types.|

No existing role inherits either of these roles, so assign the applicable role directly. For information on assigning a role to a user, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AssignARoleToAUser.md).

## Where the role applies

The same scripted condition field appears in several places, and the role protects all of them:

-   Model state transition conditions, where **Requires** is set to **Transition Script**. To edit the script, see [Configure change model states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/configure-change-model-states.md).
-   Model condition types, where **Condition type** is set to **Script**. To edit the script, see [Create predefined transition condition types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-predefined-transition-condition-type.md).

**Note:** A user who doesn't have the role can still open the record and read the script. The script editor is displayed in read-only mode, and pointing to the editor displays the message `Cannot edit in read-only editor`. All other fields on the record continue to follow the existing access controls.

**Parent Topic:**[Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-change-model.md)

