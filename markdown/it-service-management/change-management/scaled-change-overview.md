---
title: Scaled change
description: Scaled Change extends change management to complex environments with many configuration items. A single Scaled Change generates and coordinates child change records for every affected configuration item. It uses scheduling intelligence, conflict detection, and approval workflows to keep large-scale changes on track from planning through closure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/scaled-change-overview.html
release: brazil
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [scaled change, Primary change, child change, change management]
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Scaled change

Scaled Change extends change management to complex environments with many configuration items. A single Scaled Change generates and coordinates child change records for every affected configuration item. It uses scheduling intelligence, conflict detection, and approval workflows to keep large-scale changes on track from planning through closure.

Use scaled change when a single change affects many CIs and you need to track implementation for each CI separately. Add all affected CIs to one Primary change request. When the Primary change reaches its configured trigger state, one Child change is generated for each CI. For example, a Primary change with 20 affected CIs generates 20 Child changes.

**Important:**

Activate the Major Change \(**com.sn\_major\_change**\) plugin to trigger the Child change creation. For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateAPlugin.md).

## Generate child changes using Scaled change

Scaled change generates Child changes in the following sequence:

1.  A Primary change is created using a change model configured to allow Child change creation on a configured trigger state. For example, if the configured trigger state is Assess, Child changes are generated when the Primary change enters Assess.
2.  When the Primary change enters the configured trigger state, one Child change is generated for each CI in the Affected CIs list. Each Child change's configuration item is set to the corresponding CI. Its short description, category, description, justification, implementation plan, risk and impact analysis, backout plan, and test plan are copied from the Primary change.
3.  While generation is in progress, the Primary change's `child_changes_creation_status` field is set to `in_progress`.
4.  When all child changes are generated, `child_changes_creation_status` is set to `completed`, or `completed_with_errors` if any child change failed to generate.

## Scaled change implementation

To implement scaled change, complete the following tasks in order:

1.  Create a Primary change model and configure a trigger state with the Allow Child Change Creation attribute. For more information, see [Configure a Primary change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-primary-change-model.md).
2.  Create a Child change model. For more information, see [Configure a Child change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-child-change-model.md).
3.  Create a flow to configure child change creation on the Primary change model. The flow triggers when the Primary change reaches the configured state. For more information, see [Create a scaled change flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-scaled-change-flow.md).

    **Note:** To configure the system properties related to child change creation, see [Components installed with Scaled Change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/installed-with-scaled-change.md).


## Scaled change tracking fields

The following fields track the relationship and generation status between Primary changes and Child changes.

<table id="table_scaled_change_attributes"><thead><tr><th>

Field

</th><th>

Applies to

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`child_changes_creation_status`

</td><td>

Primary change

</td><td>

Tracks the overall Child change generation status. Values: `in_progress`, `completed`, `completed_with_errors`. **Note:** This field remains always empty in a Child change request.

</td></tr><tr><td>

`primary_change`

</td><td>

Child change

</td><td>

Stores a reference to the Primary change. This field is not on the Change Request form; view its value in the record's XML.

</td></tr><tr><td>

`type` = Child change requests creation

</td><td>

Worker record \(chg\_mgt\_worker\)

</td><td>

Identifies a worker record created to track the asynchronous, batched creation of child change requests for a primary change. Each worker holds a batch of affected CIs and a reference to the primary change. The worker progresses through in-progress, complete, or error states as its child change requests are generated.

</td></tr></tbody>
</table>-   **[Configure a Primary change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-primary-change-model.md)**  
Configure a Primary change model so that a change using this model generates one Child change for each affected configuration item \(CI\).
-   **[Configure a Child change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-child-change-model.md)**  
Configure a Child change model to define the states required by the Child change requests.
-   **[Create a scaled change flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-scaled-change-flow.md)**  
Create a flow to configure child change creation on the primary change model. The flow triggers when the primary change reaches the configured state.
-   **[Components installed with Scaled Change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/installed-with-scaled-change.md)**  
Several components are installed with the Major Change \(**com.sn\_major\_change**\) plugin. These include system properties and a data retention rule for Child changes.

**Parent Topic:**[Configuring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-change-management.md)

