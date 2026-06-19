---
title: Workflow stage field icons and tooltips
description: A workflow stage field displays icons to indicate the workflow stage.Based on the stage renderer selected for a workflow, workflow stage icons may display tooltips with detailed information about a stage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/legacy-workflow/r\_WorkflowFieldIcons.html
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a workflow stage field, Workflow stages, Workflow management, Classic Workflow, Build workflows]
---

# Workflow stage field icons and tooltips

A workflow stage field displays icons to indicate the workflow stage.

Based on the stage renderer selected for the workflow, these icons may display a tooltip with additional information.

|Icon|Workflow stage|
|----|--------------|
|\[Omitted image "WorkflowActive.png"\] Alt text: Current active step icon|Current active step|
|\[Omitted image "WorkflowAwaiting.png"\] Alt text: Approval pending icon|Approval pending|
|\[Omitted image "WorkflowRejected.png"\] Alt text: Approval rejected icon|Approval rejected|
|\[Omitted image "WorkflowComplete.png"\] Alt text: Complete icon|Complete|
|\[Omitted image "WorkflowLate.png"\] Alt text: Late or Canceled icon|Late \(Change/Request\) or Canceled \(Catalog\)|
|\[Omitted image "WorkflowSkipped.png"\] Alt text: Skipped icon|Skipped \(Catalog only\)|

**Parent Topic:**[Create a workflow stage field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/legacy-workflow/t_CreateAWorkflowStageField.md)

## Stage tooltips

Based on the stage renderer selected for a workflow, workflow stage icons may display tooltips with detailed information about a stage.

<table id="table_zkz_1kh_hr"><thead><tr><th>

Renderer

</th><th>

Tooltip behavior

</th></tr></thead><tbody><tr><td>

Legacy

</td><td>

When a user points to a stage, the tooltip displays the name of the stage. In the expanded view, the activity status appears in parentheses next to the stage.

 \[Omitted image "stage-tooltip-no-approver.png"\] Alt text: Stage tooltip with no name of approver.

</td></tr><tr><td>

Other renderers

</td><td>

When a user points to a stage, the tooltip displays the name of the stage. If the stage is a gated approval, the tooltip also shows the name of the approver. In the expanded view, the activity status appears in parentheses next to the stage.

 \[Omitted image "stage-tooltip-includes-approver.png"\] Alt text: Stage tooltip that includes approver.

</td></tr></tbody>
</table>If you do not want the approver's name included in the tooltip, navigate to **System Properties** &gt; **Service Catalog** and clear the **Show the current pending approver's name in the stage widget mouseover** check box.

\[Omitted image "ApprovalHover2.png"\] Alt text:

