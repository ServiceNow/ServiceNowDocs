---
title: Optional activities
description: Enable your agents and fulfillers to add additional activities as they go through a playbook.As a Playbooks administrator, add an optional activity to a playbook that Playbook Experience agents and fulfillers can choose to add and complete during the playbook runtime.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/optional-activities.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Optional activities

Enable your agents and fulfillers to add additional activities as they go through a playbook.

## Overview

Admins enable and add optional activities in the Workflow Studio Playbooks builder, while agents and fulfillers add and complete optional activities in Playbook Experience.

As an example, if you have a playbook for a Security Incident, a playbook admin could add an optional activity for a virus scan. When the activity runs, the optional virus scan activity would take the parent Security Incident record and run third-party virus scanning integrations on Configuration Management Database \(CMDB\) assets associated with the parent record. The security analyst can decide at runtime whether to run a virus scan based on their assessment of the situation.

The flow of working with optional activities:

1.  Turn on and add optional activities to a playbook in Workflow Studio.
2.  Optional activities are configured like other activities. To see [design an automated process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/design-automated-process.md).
3.  Agents add optional activities in Playbook Experience.

**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

## Add an Optional Activity to a playbook

As a Playbooks administrator, add an optional activity to a playbook that Playbook Experience agents and fulfillers can choose to add and complete during the playbook runtime.

### Before you begin

Role required: playbook.admin or pd\_author

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Open the playbook that you want to add an optional activity to.

3.  Switch to **Board view**.

    \[Omitted image "board-view.png"\] Alt text: Toggle for Diagram and Board views

4.  In the upper right-hand corner, toggle on **Optional activities**.

    \[Omitted image "optional-activities.png"\] Alt text: Toggle on Optional activities

    The optional activities swimlane opens.

5.  Add an optional activity.

    Global optional activities can be inserted by the agent or fulfiller anywhere in the playbook, while a stage-specific optional activity can only be inserted within its specific stage.

6.  Configure your activity the way that you would configure a regular activity.


