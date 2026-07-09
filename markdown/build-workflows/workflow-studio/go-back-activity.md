---
title: Go back activity
description: The Go back activity defines a conditional return point in a playbook, enabling the playbook to loop back to an earlier activity, stage, or the start of the playbook based on an outcome.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/go-back-activity.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 2
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Go back activity

The Go back activity defines a conditional return point in a playbook, enabling the playbook to loop back to an earlier activity, stage, or the start of the playbook based on an outcome.

The Go back activity lets you define a conditional return point in a playbook. When an agent or fulfiller reaches a Go back activity during runtime, the playbook returns to a target you define — the start of a specific activity, the start of a stage, or the start of the playbook — and continues from there.

Use a Go back activity when a process needs to loop back based on an outcome. For example, if a request is rejected, the playbook can return to an earlier data-gathering step instead of ending or requiring a full restart.

## How it works

The Go back activity is placed inside a decision branch. When the branch condition is met at runtime, the playbook returns to the configured target and resumes execution from that point.

You can configure the Go back activity to return to one of three targets:

-   Activity: Returns to the start of a specific activity earlier in the playbook.
-   Stage: Returns to the start of a specific stage.
-   Start of playbook: Returns to the beginning of the playbook.

## Design considerations

Workflow Studio enforces the following rules when you add a Go back activity. The playbook can't be activated if any rule is violated.

|Rule|Description|
|----|-----------|
|At least one forward path required|Every decision that contains a Go back activity must have at least one branch that continues forward in the playbook.|
|No parallel forward branches without a decision|You can't add a Go back activity if there is a parallel branch running forward that is not separated by a decision.|
|Single branch evaluation required|If a decision is set to evaluate all branches that are true, it can't contain a Go back activity. Change the evaluation mode to process only the first true branch.|
|Target required|The Go back activity must have a configured target. The target must appear before the Go back activity and the target can’t be another Go back activity.|
|Must be the last activity|A decision branch can contain only one Go back activity and the activity must be the last activity.|

-   **[Add a Go back activity to a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/add-go-back-activity.md)**  
Add a Go back activity to a decision branch in your playbook and configure where the playbook returns to when the activity runs.

**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

