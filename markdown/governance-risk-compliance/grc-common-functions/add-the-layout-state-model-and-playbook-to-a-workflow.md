---
title: Add the layout, state model, and playbook to a workflow
description: Attach a layout, state model, and playbook to a workflow to define what it captures, its lifecycle, and how users are guided through it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/add-the-layout-state-model-and-playbook-to-a-workflow.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 2
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Add the layout, state model, and playbook to a workflow

Attach a layout, state model, and playbook to a workflow to define what it captures, its lifecycle, and how users are guided through it.

## Before you begin

The issue workflow must exist, with its basic details saved. See [Create an issue workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-an-issue-workflow.md).

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

The layout defines the fields, sections, header information, and vertical navigation available for an issue. The state model defines the lifecycle stages an issue moves through and the rules for moving between them. The playbook provides the step-by-step guided experience users see while working through the issue lifecycle.

The Workflow components step opens automatically after you save the workflow's basic details.

## Procedure

1.  In the **Layout** field, select an existing issue layout, such as **Issue configuration** or **Advanced Issue configuration**.

    **Note:**

    Select **View all issue layouts** to browse existing layouts, filtered to the workflow's table, or select **New** on that list to create one. See [Table configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/table-configuration-fields.md).

2.  In the **State model** field, select an existing state model.

    Each option in the list previews the states included in that model.

    **Note:**

    Select **View all state models** to browse existing state models or create one. See [Create a GRC state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-a-grc-state-model.md).

3.  In the **Playbook** field, select an existing playbook, or leave the field set to **None**.

    **Note:**

    Select **View all playbooks** to browse existing playbooks or create one. To build a new playbook from scratch in Workflow Studio, see [Create a playbook](https://www.servicenow.com/docs/r/build-workflows/workflow-studio/create-process-definition.html).

4.  Save your selections by selecting **Save and continue**.


## Result

The step is marked Complete. If you selected a state model or playbook, their states and stages become available for mapping.

## What to do next

Continue the guided setup by mapping states to playbook stages. See [Map states to playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/map-states-to-playbook-stages.md).

-   **[Table configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/table-configuration-fields.md)**  
Fields on the Table configuration form, used to create an issue layout.

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

