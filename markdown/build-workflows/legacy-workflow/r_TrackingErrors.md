---
title: Workflow error tracking features
description: Error handling provides visual cues within the workflow, such as error descriptions for activities in pop-ups, and detailed log records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/legacy-workflow/r\_TrackingErrors.html
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workflow error handling, Workflow administration, Classic Workflow, Build workflows]
---

# Workflow error tracking features

Error handling provides visual cues within the workflow, such as error descriptions for activities in pop-ups, and detailed log records.

## Banners

Look for an activity with a red banner, indicating that a syntax error has occurred in a script field. All activities that provide error handling, with the exception of **Catalog Task** and **Create Task**, display a red banner for this error.

\[Omitted image "ErrorHandlingBanner.png"\] Alt text:

## Tooltips

Point to the activity displaying a red banner to view information about the error. A tooltip shows the **State** and **Result** of the activity and provides a brief **Fault Description** \(except for task activities\). Note that this approval continued as skipped despite the error given in the fault description. See [Workflow error handling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/legacy-workflow/c_WorkflowErrorHandling.md) for the information available to each activity.

\[Omitted image "ErrorHandlingHover.png"\] Alt text:

## Execution order

Tooltip text in the Workflow Context graphical view displays the execution order of individual activities, which assists in troubleshooting.

To view the order in which a workflow activity was executed:

1.  Navigate to **Workflow** &gt; **Live Workflows** &gt; **Active Contexts** or **All Contexts**.
2.  Open the context you want to examine.
3.  Click **Show Workflow**.
4.  Hover the cursor over a finished or executing activity.

    A tooltip appears showing error data, execution time, and the order in which that activity executed in the workflow. You can use this data to help troubleshoot activities in an error state.

    \[Omitted image "ExecutionOrderWorkflow.png"\] Alt text: Activity execution order


## Workflow log

View the log in the Workflow Context form for more information about the syntax error in the activity. Since task activities do not display a red banner when a syntax error has occurred, you must view the log if you suspect the workflow has not run properly. Examine the error description in the log, and then inspect the script in the activity named in the log.

To view the activity by name, navigate to **Workflow** &gt; **Administration** &gt; **Properties** and enable the **Log workflow debug messages** property.

In this example, an SSH activity named File Read specifies an invalid MID Server.

\[Omitted image "ErrorHandlingLog.png"\] Alt text: Error handling log

If the credentials used by an activity in the workflow fail, and the activity cannot authenticate on the target, a message describing the failure appears in the **Workflow Log** related list. The message displays the target IP address and the credential details.

\[Omitted image "CredDebugWorkflowLog.png"\] Alt text: Credential debugging in the workflow log

**Parent Topic:**[Workflow error handling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/legacy-workflow/c_WorkflowErrorHandling.md)

