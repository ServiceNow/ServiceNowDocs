---
title: Map states to playbook stages
description: Map workflow states to playbook stages so that the issue state and guided activities remain synchronized as an issue moves through its lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/map-states-to-playbook-stages.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Map states to playbook stages

Map workflow states to playbook stages so that the issue state and guided activities remain synchronized as an issue moves through its lifecycle.

## Before you begin

The workflow's state model and playbook must already be selected on the Workflow components step. See [Add the layout, state model, and playbook to a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-the-layout-state-model-and-playbook-to-a-workflow.md). The playbook must contain the stages that you want to map.

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

Each non-terminal state in the workflow's state model maps to one corresponding playbook stage. When the issue enters a mapped state, the playbook moves to the corresponding stage. When the final activity in a stage is completed, the system proposes the corresponding state change for confirmation.

Terminal states, such as Closed or Cancelled, aren't mapped, because no further guided activity is required.

## Procedure

1.  In the **Playbook stage** column, double-click the cell for the state that you want to map.

2.  Select the corresponding playbook stage.

    **Note:**

    If the list contains many stages, enter text to search for the stage.

3.  Map a playbook stage to each remaining nonterminal state.

4.  Save the state-to-stage mappings by selecting **Save and continue**.


## Result

The selected playbook stages appear in the **Playbook stage** column. The state-to-stage mappings are saved for the workflow.

## What to do next

Set the trigger condition and priority for the workflow. See [Set the trigger condition and priority for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/set-the-trigger-condition-and-priority-for-a-workflow.md).

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

