---
title: ValidateLowestCommonTable
description: The ValidateLowestCommonTable validator reports the lowest table in the Glide hierarchy that the workflow uses.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# ValidateLowestCommonTable

The **ValidateLowestCommonTable** validator reports the lowest table in the Glide hierarchy that the workflow uses.

For example, the Requested Item \[sc\_req\_item\] table is the lowest table in a workflow containing a **Catalog Task** activity. This information is significant to a designer who wants to change the table against which an existing workflow runs after adding activities to the canvas.

**Note:** This validator provides information only. It does not indicate an error or warning condition.

## Validation summary

-   Risk: This validator informs only and has no risk associated with it.
-   Severity Level: Data/Information
-   Valid Result: Valid
-   Valid Message: The lowest common table in this workflow is &lt;&lt;table\_name&gt;.
-   Invalid Result: N/A \(informational only\)
-   Invalid Message: N/A \(informational only\)
-   Suggested Action: None
-   Publishable: Yes
-   Runnable: Yes
-   Related Information: [Workflow activities](../../using-workflows/concept/c_WorkflowActivities.md)

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

