---
title: Using formatters
description: A formatter is a form element used to display information that is not a field in the record. Add formatters to a form by configuring the form.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Using formatters

A formatter is a form element used to display information that is not a field in the record. Add formatters to a form by configuring the form.

<table id="table_pjt_gpn_t4"><thead><tr><th>

Formatter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity formatter

</td><td>

Displays the list of activities, or history, on a task form.

 For an example of an activity formatter, see [Activity formatter](c_ActivityFormatter.md#).

</td></tr><tr><td>

Process flow formatter

</td><td>

Displays the different stages in a linear process flow across the top of a record.

 For an example of a process flow formatter, see [Process flow formatter](../reference/r_ProcessFlowFormatter.md#).

</td></tr><tr><td>

Parent breadcrumbs formatter

</td><td>

Provides breadcrumbs to show the parent or parents of the current task.

 For an example of a parent breadcrumbs formatter, see [Parent breadcrumbs formatter](../task/t_TaskParentBreadcrumbsFormatter.md#).

</td></tr><tr><td>

Approval summarizer formatter

</td><td>

Displays dynamic summary information about the request being approved.

 For an example of an approval summarizer formatter, see [Approval summarizer formatter](../../service-administration/reference/r_ApprovalSummarizerFormatter.md).

</td></tr><tr><td>

CI relations formatter

</td><td>

Displays on the CI form a toolbar for viewing the relationships between the current CI and related CIs.

 For an example of CI relations formatter icons, see [CI relations formatter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_CIRelationsFormatterNG.md).

</td></tr></tbody>
</table>**Note:** Formatter elements cannot be exported to PDF. When exporting PDF data from a form, any formatter elements added to the form are not displayed in the PDF output.

To create a custom formatter, create a UI macro to define content for the formatter, then create a formatter that refers to the UI macro. You can then add the formatter to a form.

-   **[Create a UI macro for a formatter](../task/t_CreateAUIMacro.md)**  
Create a UI macro to define the content that the formatter displays.
-   **[Create a formatter and add it to a form](../task/t_CreateAFormatter.md)**  
Create the formatter after creating the UI macro that defines the content.
-   **[Activity formatter](c_ActivityFormatter.md#)**  
The activity formatter provides an easy way to track items not saved with a field in the record, for example, journal fields like comments and work notes.
-   **[Process flow formatter](../reference/r_ProcessFlowFormatter.md#)**  
The process flow formatter provides a graphical summary of the stages in a process. The formatter is typically shown at the top of forms that are part of a process.
-   **[Parent breadcrumbs formatter](../task/t_TaskParentBreadcrumbsFormatter.md#)**  
The parent breadcrumbs formatter on the Task table provides breadcrumbs that show the parent or parents of the current task. This formatter can be used also on any table that extends Task.
-   **[Approval summarizer formatter](../../service-administration/reference/r_ApprovalSummarizerFormatter.md)**  
The approval summarizer formatter creates the summary at the bottom of an approval form.
-   **[Override a formatter with macros](../task/t_UIMacroOverride.md)**  
The system uses formatters to handle complex rendering of specific form elements.
-   **[Limit the number of activity stream entries](../task/limit-activity-stream-entries.md)**  
You can set a system property to limit the number of entries allowed in an activity stream.

**Parent Topic:**[Administering forms on the ServiceNow AI Platform](form-administration.md)

