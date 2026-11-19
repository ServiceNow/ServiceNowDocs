---
title: Optional activities
description: Enable your agents and fulfillers to add additional activities as they go through a playbook.As a Playbooks administrator, add an optional activity to a playbook that Playbook Experience agents can choose to add and complete during the playbook runtime.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/optional-activities.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-11-06"
reading_time_minutes: 2
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Optional activities

Enable your agents and fulfillers to add additional activities as they go through a playbook.

## How optional activities work

Admins enable and add optional activities in the Playbooks designer, while agents add and complete optional activities in Playbook Experience. For more information about optional activities in Playbook Experience, see [Add an optional activity to a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-add-optional-activity.md).

The flow of working with optional activities:

1.  Turn on and add optional activities to a playbook in Workflow Studio.
2.  Optional activities are configured like other activities. For more information, see [Add and configure an activity in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/add-configure-activity.md).
3.  Agents add optional activities in Playbook Experience.

## Optional activities in a change request playbook

A playbook for a change request can include two optional activities. A global optional activity escalates the change to the CAB chair at any point in the run. A stage-specific optional activity requests more information from the requester while the review stage is active. The agent adds either activity only when a particular change calls for it.

**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

## Add an Optional Activity to a playbook

As a Playbooks administrator, add an optional activity to a playbook that Playbook Experience agents can choose to add and complete during the playbook runtime.

### Before you begin

Role required: playbook.admin or pd\_author

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Open the playbook that you want to add an optional activity to.

3.  Switch to **Board view**.

    \[Omitted image "board-view.png"\] Alt text: Toggle for Diagram and Board views

4.  In the upper right-hand corner, toggle on **Optional activities**.

    \[Omitted image "optional-activities.png"\] Alt text: Toggle on Optional activities

    The optional activities swimlane view opens.

5.  Add an optional activity.

    Global optional activities can be inserted by the agent or fulfiller anywhere in the playbook, while a stage-specific optional activity can only be inserted within its specific stage.

6.  Configure your activity the way that you would configure a regular activity.

    For more information, see [Add and configure an activity in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/add-configure-activity.md).


### What to do next

Agents and fulfillers can now add this activity while the playbook is running in Playbook Experience. For more information, see [Add an optional activity to a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-add-optional-activity.md).

