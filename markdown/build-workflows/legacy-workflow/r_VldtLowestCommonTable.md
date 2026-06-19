---
title: ValidateLowestCommonTable
description: The ValidateLowestCommonTable validator reports the lowest table in the Glide hierarchy that the workflow uses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/legacy-workflow/r\_VldtLowestCommonTable.html
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, Build workflows]
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
-   Related Information: [Workflow activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-activities/c_WorkflowActivities.md)

**Parent Topic:**[Workflow validator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/legacy-workflow/r_WorkflowValidator.md)

