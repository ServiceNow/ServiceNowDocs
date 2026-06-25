---
title: Use playbooks
description: Use a playbook to guide a retail store project through each stage of its life cycle, from initiation to go-live or closure. Playbooks provide step-by-step activities within each stage, confirming that required information is captured and governance processes are followed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/use-playbooks-spm-retail.html
release: australia
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 2
keywords: [playbooks, SPM retail suite, SPM Retail, retail project playbook, store lifecycle playbook]
breadcrumb: [Use, Retail Strategic Portfolio Management Suite, Strategic Portfolio Management]
---

# Use playbooks

Use a playbook to guide a retail store project through each stage of its life cycle, from initiation to go-live or closure. Playbooks provide step-by-step activities within each stage, confirming that required information is captured and governance processes are followed.

## Before you begin

Role required: sn\_spm\_retail.project\_manager

## About this task

A playbook defines the stages of a retail store project and includes action items to complete at each stage. The Retail Strategic Portfolio Management Suite, includes predefined playbooks for each store life cycle scenario and is triggered automatically when a project is created. For more information about the available playbooks, see [Explore playbooks for retail projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/playbooks-spm-retail-suite.md).

**Note:** The playbook presents project information in a guided, stage-based workflow.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace**.

2.  Open an existing retail project or create one.

    For more information on creating retail projects, see [Create a retail project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/spmr-create-retail-projects.md).

3.  Select **Playbooks** from the L-2 \(level 2\) navigation menu.

4.  Select a stage to view its activities.

    Each activity displays its status \(**In Progress**, **Pending**, or **Complete**\) and the fields or lists to update.

    **Note:** The default playbook is a stage-gate playbook, that is, a stage is unlocked only when its prior stages are marked as completed or skipped.

5.  Complete the activities within each stage.

    -   Select **Mark Complete** to mark the activity as done and move to the next activity.
    -   Select **Save** to save your progress without completing the activity.
    -   Select **Skip** to bypass the activity and move to the next one.
    **Note:** When all sections in a stage are marked complete or skipped, the system sends an approval request to members of the Retail HQ Governance group.

    Admins can create a playbook by defining the trigger condition in Workflow Studio. For more information, see [Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer-triggers.md).

    For more information on how to create and use playbooks, see [Building Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/building-a-process.md) and [Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-experience-admins.md).


**Related topics**  


[Explore playbooks for retail projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/playbooks-spm-retail-suite.md)

[Running Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-agents-and-fulfillers.md)

[Playbooks reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer-reference.md)

[Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-experience-admins.md)

