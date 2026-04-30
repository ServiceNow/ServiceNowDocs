---
title: Optional activities
description: Enable your agents and fulfillers to add additional activities as they go through a playbook.As a Playbooks administrator, add an optional activity to a playbook that Playbook Experience agents and fulfillers can choose to add and complete during the playbook runtime.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Stages and activities, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Optional activities

Enable your agents and fulfillers to add additional activities as they go through a playbook.

## Overview

Admins enable and add optional activities in the Workflow Studio Playbooks builder, while agents and fulfillers add and complete optional activities in Playbook Experience.

As an example, if you have a playbook for a Security Incident, a playbook admin could add an optional activity for a virus scan. When the activity runs, the optional virus scan activity would take the parent Security Incident record and run third-party virus scanning integrations on Configuration Management Database \(CMDB\) assets associated with the parent record. The security analyst can decide at runtime whether to run a virus scan based on their assessment of the situation.

The flow of working with optional activities:

1.  Turn on and add optional activities to a playbook in Workflow Studio.
2.  Optional activities are configured like other activities. To see [design an automated process](../task/design-automated-process.md).
3.  Agents add optional activities in Playbook Experience.

**Parent Topic:**[Stages and activities](process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](../task/add-configure-stage.md)

[Activity definitions](activity-definitions.md)

[Add and configure an activity in a playbook](../task/add-configure-activity.md)

[Automation Assets](automation-assets.md)

[Start with delay input properties](../reference/start-with-delay-properties.md)

[Decision activities](../task/create-a-decision-activity.md)

[Questionnaire activity](../reference/questionnaire-activity.md)

[Parallel branches](../task/create-parallel-activity.md)

[Add dynamic inputs to an activity](../task/add-dynamic-inputs-to-activity.md)

## Add an Optional Activity to a playbook

As a Playbooks administrator, add an optional activity to a playbook that Playbook Experience agents and fulfillers can choose to add and complete during the playbook runtime.

### Before you begin

Role required: playbook.admin or pd\_author

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Open the playbook that you want to add an optional activity to.

3.  Switch to **Board view**.

    ![Toggle for Diagram and Board views](../images/board-view.png)

4.  In the upper right-hand corner, toggle on **Optional activities**.

    ![Toggle on Optional activities](../images/optional-activities.png)

    The optional activities swimlane opens.

5.  Add an optional activity.

    Global optional activities can be inserted by the agent or fulfiller anywhere in the playbook, while a stage-specific optional activity can only be inserted within its specific stage.

6.  Configure your activity the way that you would configure a regular activity.


