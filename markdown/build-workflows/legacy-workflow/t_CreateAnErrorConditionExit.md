---
title: Create an error condition exit
description: An administrator can reroute the workflow when a script error occurs by creating an error condition exit for specific activities within the workflow. This allows the workflow to process script errors in a predictable way and not create undesirable results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/legacy-workflow/t\_CreateAnErrorConditionExit.html
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow error handling, Workflow administration, Classic Workflow, Build workflows]
---

# Create an error condition exit

An administrator can reroute the workflow when a script error occurs by creating an error condition exit for specific activities within the workflow. This allows the workflow to process script errors in a predictable way and not create undesirable results.

## Procedure

1.  Open and check out a workflow.

2.  Right-click in the top portion of the activity for which you want to create an error exit.

3.  Select **Add condition** from the context menu.

4.  Add a condition exit with the following values:

    -   Name: `Error`
    -   Condition: `activity.state=='faulted'`
5.  Click **Submit**.

    The **Error** exit appears on the activity.

6.  Connect the **Error** exit to another activity for handling the error state, such as **Notification** or **Log Message**.

    \[Omitted image "ErrorHandlingExit2.png"\] Alt text: Error handling exit


**Parent Topic:**[Workflow error handling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/legacy-workflow/c_WorkflowErrorHandling.md)

