---
title: ValidateWorkflowStageColumn
description: The ValidateWorkflowStageColumn validator detects and reports when the stage field \(stage column\) for a workflow is not correct or is unusable.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, Build workflows]
---

# ValidateWorkflowStageColumn

The **ValidateWorkflowStageColumn** validator detects and reports when the stage field \(stage column\) for a workflow is not correct or is unusable.

## Validation summary

-   Risk: The stage indicators may not display appropriate information.
-   Severity Level: Warning
-   Valid Result: Valid
-   Valid Message:Workflow stage values are valid.
-   Invalid Result: Warning
-   Info Summary: Stage warnings found.
-   Invalid Messages:
    -   Table T does not have a column named C.
    -   Workflow for table T has stages, but no stage column.
    -   Table T has a stage column "C," but no stages are set by activities.
    -   Workflow on table T has stage column "C" that is not type=workflow.
-   Suggested Action: If this is not by design, make the appropriate changes.
-   Publishable: Yes
-   Runnable: Yes
-   Related Information: [Workflow activities](../../using-workflows/concept/c_WorkflowActivities.md), [Workflow stages](../../using-workflows/concept/c_WorkflowStages.md)

## Troubleshooting

To check the stage column:

1.  Open and check out a workflow.
2.  Open the workflow version properties dialog by clicking the menu icon and selecting **Properties**.
3.  View the **Stages** tab or section.
4.  Check that the assigned stage column is actually a column in the table to which the workflow is associated.
5.  Check that the column is type=workflow.

Tip: Stage columns should not be choice lists. If they are, the list appears read-only in form views, since changing that column value outside the workflow engine does not ensure safe tracking of stage states.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

