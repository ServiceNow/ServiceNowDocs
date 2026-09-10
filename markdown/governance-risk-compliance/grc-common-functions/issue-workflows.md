---
title: Issue workflows
description: Issue workflows define the lifecycle, layout, guided activities, approval requirements, and routing rules for different types of issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/issue-workflows.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 3
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Issue workflows

Issue workflows define the lifecycle, layout, guided activities, approval requirements, and routing rules for different types of issues.

Different types of issues can require different states, layouts, guidance, and approval controls. Issue workflows allow multiple issue-management processes to operate on the same table, with each workflow configured for a particular type of issue. As a result, supporting a new issue-management process no longer requires customizing the issue table.

## Key benefits

-   Support different issue-management processes on the same table.
-   Configure lifecycle behavior without customizing the issue table.
-   Guide people through the activities required at each lifecycle stage.
-   Require approval before specified state changes or due date extensions.
-   Route new issues automatically by using trigger conditions and priority.

## Workflow components

An issue workflow brings together several components.

-   **Table and identity**

    Defines the workflow's name, description, and the exact issue table it serves.

-   **Layout**

    Defines the fields, sections, header information, and vertical navigation available for an issue.

-   **State model**

    Defines the lifecycle states and the permitted transitions between them.

-   **Playbook**

    Provides optional activities that guide people through the work associated with lifecycle stages.

-   **State-to-stage mapping**

    Synchronizes lifecycle states with corresponding playbook stages.

-   **Approval definitions**

    Specify the state changes or due date extensions that require approval.

-   **Trigger condition**

    Determines which new issues qualify for the workflow.

-   **Priority**

    Determines which workflow is selected when more than one active workflow matches an issue.


The playbook and approval definitions are optional. A workflow can define a layout and lifecycle without guided activities or approval requirements.

## Workflow assignment

When a new issue is created, the system evaluates active workflows configured for its table, beginning with the lowest priority number. The first workflow with a matching trigger condition is assigned. A workflow without a trigger condition applies to any new issue on its table that reaches it during evaluation. Active workflows on the same table can't share a priority number, so a new issue is never routed ambiguously.

If no active workflow matches, the issue is created without a workflow configuration and continues to use the existing issue behavior. The vertical layout remains available, but workflow-specific playbooks and approval definitions do not apply. Existing issues are not evaluated retrospectively.

The assigned workflow does not change automatically if the issue later matches another workflow's conditions. An issue without an assigned workflow cannot be moved to a configured workflow. For an issue that already has a workflow, the **Change workflow** action is available when more than one active workflow exists. See [Reassign an issue's workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/reassign-an-issue-s-workflow.md).

-   **[Access issue workflow administration from a workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/access-issue-workflow-administration-from-a-workspace.md)**  
Reach issue workflow configuration from within a product workspace, such as Risk Workspace, instead of navigating to the base GRC admin console.
-   **[Create an issue workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-an-issue-workflow.md)**  
Set up a workflow so a specific category of issues, such as vendor risk or compliance issues, follows its own states, layout, and trigger condition.
-   **[Add the layout, state model, and playbook to a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-the-layout-state-model-and-playbook-to-a-workflow.md)**  
Attach a layout, state model, and playbook to a workflow to define what it captures, its lifecycle, and how users are guided through it.
-   **[Create a GRC state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-a-grc-state-model.md)**  
Create a GRC state model to define the states a table's records move through so an issue workflow can use it to control its lifecycle.
-   **[Add a state to a GRC state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-a-state-to-a-grc-state-model.md)**  
Add a state to a GRC state model and configure its stepper display, transitions, and attributes.
-   **[Map states to playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/map-states-to-playbook-stages.md)**  
Map workflow states to playbook stages so that the issue state and guided activities remain synchronized as an issue moves through its lifecycle.
-   **[Set the trigger condition and priority for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/set-the-trigger-condition-and-priority-for-a-workflow.md)**  
Define which issues a workflow applies to and determine the order in which it is evaluated relative to other workflows on the same table.
-   **[Configure approvals for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/configure-approvals-for-a-workflow.md)**  
Attach approvals to a workflow so issues or remediation tasks require approval before certain actions can be completed.
-   **[Review and activate a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/review-and-activate-a-workflow.md)**  
Review the workflow configuration and activate the workflow so it can be applied to new issues.
-   **[Deactivate an issue workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/deactivate-an-issue-workflow.md)**  
Stop an active workflow from being evaluated for new issues on its table.
-   **[Clone an issue workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/clone-an-issue-workflow.md)**  
Create a copy of an existing workflow to use as a starting point for a new workflow.
-   **[Reassign an issue's workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/reassign-an-issue-s-workflow.md)**  
Change the workflow assigned to an issue when more than one active workflow exists for the issue's table.

**Parent Topic:**[Common Governance, Risk, and Compliance features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/common-grc-features.md)

