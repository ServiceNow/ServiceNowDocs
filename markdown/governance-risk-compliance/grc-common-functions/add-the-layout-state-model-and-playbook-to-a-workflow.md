---
title: Add the layout, state model, and playbook to a workflow
description: Attach a layout, state model, and playbook to a workflow to define what it captures, its lifecycle, and how users are guided through it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/add-the-layout-state-model-and-playbook-to-a-workflow.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-16"
reading_time_minutes: 2
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Add the layout, state model, and playbook to a workflow

Attach a layout, state model, and playbook to a workflow to define what it captures, its lifecycle, and how users are guided through it.

## Before you begin

The issue workflow must exist, with its basic details saved. See [Create an issue workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/create-an-issue-workflow.md).

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

The layout defines the fields, sections, header information, and vertical navigation available for an issue. The state model defines the lifecycle stages an issue moves through and the rules for moving between them. The playbook provides the step-by-step guided experience users see while working through the issue lifecycle.

The **Workflow components** step opens automatically after you save the workflow's basic details.

## Procedure

1.  In the **Layout** field, select an existing issue layout, such as **Issue configuration** or **Advanced Issue configuration**.

    To browse the layouts available for the workflow's table, or to create one, select **View all issue layouts**.

2.  In the **State model** field, select an existing state model.

    Each option in the list previews the states included in that model.

    To browse the available state models, or to create one, select **View all state models**. See [Create a GRC state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/create-a-grc-state-model.md).

3.  In the **Playbook** field, select an existing playbook.

    The field can remain set to **None**.

    To browse the available playbooks, or to create one, select **View all playbooks**.

4.  Save your selections by selecting **Save and continue**.


## Result

-   The step is marked **Complete**.
-   If you selected a state model or playbook, their states and stages become available for mapping.

## What to do next

Continue the guided setup by mapping states to playbook stages. See [Map states to playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/map-states-to-playbook-stages.md).

**Note:**

If you change the state model or the playbook after states are mapped to playbook stages, the existing mappings are reset and a confirmation is required. Clearing the **Playbook** field also removes the existing state-to-stage mappings.

-   **[Table configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/table-configuration-fields.md)**  
Fields on the Table configuration form, used to create an issue layout.

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

