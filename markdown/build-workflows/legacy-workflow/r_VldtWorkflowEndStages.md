---
title: ValidateWorkflowEndStages
description: The ValidateWorkflowEndStages validator checks that in workflows with stages, the end activity of the workflow has a stage named Complete or Completed.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, Build workflows]
---

# ValidateWorkflowEndStages

The **ValidateWorkflowEndStages** validator checks that in workflows with stages, the end activity of the workflow has a stage named Complete or Completed.

If the workflow has stages associated with it, but does not have the completed stage on the end activity, then the stage indicator will not show that the workflow completed.

## Validation summary

-   Risk: The stage indicator will not show the workflow is completed.
-   Severity Level: Warning
-   Valid Result: Valid
-   Valid Message: Workflow end stages are valid.
-   Invalid Result: invalid
-   Invalid Message: End activity A found with invalid stage "S."
-   Suggested Action: If this is not by design, make the appropriate changes.
-   Publishable: Yes
-   Runnable: Yes
-   Related Information: [Workflow activities](../../using-workflows/concept/c_WorkflowActivities.md)

## Troubleshooting

Check the workflow for an end activity. Ensure that this activity assigns a stage named Complete or Completed.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

