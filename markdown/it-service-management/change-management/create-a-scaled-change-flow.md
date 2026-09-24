---
title: Create a scaled change flow
description: Create a flow to configure child change creation on the primary change model. The flow triggers when the primary change reaches the configured state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/create-a-scaled-change-flow.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [flow, Child change creation, scaled change]
breadcrumb: [Scaled change, Configure, Change Management, IT Service Management]
---

# Create a scaled change flow

Create a flow to configure child change creation on the primary change model. The flow triggers when the primary change reaches the configured state.

## Before you begin

Role required: `sn_change_write or itil`

-   Activate the Major Change \(**com.sn\_major\_change**\) plugin. For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateAPlugin.md). This plugin includes the Child change requests creation action that the flow uses.
-   Create a Primary change model. For more information, see [Configure a Primary change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-primary-change-model.md).
-   Create a Child change model. For more information, see [Configure a Child change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-child-change-model.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  To create a new flow, select the **New** button, and select Flow.

    For more information about Flow Designer, see [Create a flow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/create-flow.md)

3.  Enter a name in the **Flow name** field, and select **Build flow**.

4.  Configure the flow trigger.

    |Setting|Value|
    |-------|-----|
    |Trigger type|Record Created or Updated|
    |Table|Change Request \[**change\_request**\]|
    |Condition|\[**Model**\] \[**is**\] \[**Scaled change**\] and \[**State**\] \[**is**\] \[**Assess**\]|
    |Run Trigger|Only if not currently running|

    Use the name of your own Primary change model in the **Model** condition.

5.  Add the **Child change requests creation** action, and set its change model input to your Child change model.

    This action creates one Change Management Worker record for each batch of CIs that does not already have a Child change. It also sets the Primary change's `child_changes_creation_status` field to `in_progress`.

6.  Add a condition that ends the flow if the **Child change requests creation** action reports that the request was not processed.

7.  Add a **Wait For Condition** action on the Change Request table where **Child changes creation status** is **Completed**, or **Completed with Errors**.

8.  Add the **Evaluate Change Model** action.

    This base-system action evaluates the next available state for the change based on its change model. It moves the Primary change to the next state after Child change generation completes.

9.  Select **Publish**.


## Result

When a change using the Primary change model enters the configured state, the flow creates one Child change for each configuration item \(CI\) in the Affected CIs list. Each Child change copies category, description, justification, implementation plan, risk and impact analysis, backout plan, test plan, and software model from the Primary change.

To view child changes on a primary change request, select **Configure**, select **Related Lists**, and add the related list driven by the `primary_change` field. This related list displays the child changes generated for a primary change. It is hidden until child changes are created and does not appear on a child change.

Child changes generated from a Parent change have the `Configuration item` and `Model` fields set to read-only

**Parent Topic:**[Scaled change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/scaled-change-overview.md)

