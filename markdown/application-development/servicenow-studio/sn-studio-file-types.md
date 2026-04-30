---
title: ServiceNow Studio supported file types using code search
description: ServiceNow Studio supports the following file types when using code search.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: reference
last_updated: "2024-09-06"
reading_time_minutes: 4
breadcrumb: [ServiceNow Studio reference, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio supported file types using code search

ServiceNow Studio supports the following file types when using code search.

When using code search in ServiceNow Studio, the application uses the default code search group. The following table outlines the file types that are supported when using the default ServiceNow Studio code search.

**Tip:** If your company wants to expand the list of supported file types used in code search, an administrator can create a new code search group that includes additional file types. For more information about expanding code search, see [Expand code search tables](https://developer.servicenow.com/connect.do#!/share/contents/3024956_expand_code_search_tables?v=1&t=PRODUCT_DETAILS).

<table id="table_lcj_1bh_qcc"><thead><tr><th>

File type

</th><th>

Code search table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Access control](https://www.servicenow.com/docs/access?context=sc-access-control&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

</td><td>

sys\_security\_acl

</td><td>

Determines whether access is granted for a specified operation to a specific entity, such as:

-   Type of entity being secured
-   Operation being secured
-   Unique identifier describing the object

</td></tr><tr><td>

[Business rules](../../../script/business-rules/concept/c_BusinessRules.md#)

</td><td>

sys\_script

</td><td>

Customize system behavior. -   [Business Rules](../../../script/business-rules/concept/c_BusinessRules.md#) run when a database action occurs \(query, insert, update, or delete\).
-   The script can run:
    -   before or after the database action is performed \(runs as part of the database operation\).
    -   asynchronously \(at some point after the database operation\).
    -   on display \(when displaying the data in a form\).

</td></tr><tr><td>

[Client scripts](../../../script/client-scripts/concept/client-scripts.md)

</td><td>

sys\_script\_client

</td><td>

Used for changing the appearance of forms, displaying different fields based on values that are entered or other custom display options.

-   onLoad means that the Client Script runs when the form or page is loaded
-   onChange means that the Client Script runs when something specific gets changed AND also when the form or page loads
-   onSubmit means that the Client Script runs when the form is submitted

 Client Scripts can also be called by other scripts or modules, including UI policies.

</td></tr><tr><td>

[Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td><td>

sysevent\_email\_template

</td><td>

Enable administrators to create reusable content for the subject line and message body of email notifications.

</td></tr><tr><td>

[Inbound email actions](https://www.servicenow.com/docs/access?context=actions-inbound-email&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td><td>

sysevent\_in\_email\_action

</td><td>

Script how the system responds to inbound emails.

</td></tr><tr><td>

[Map pages](https://www.servicenow.com/docs/access?context=c_MapPages&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

</td><td>

cmn\_map\_page

</td><td>

Display ServiceNow data graphically on a Google map page based on location data that you provide.

</td></tr><tr><td>

[Map transforms](https://www.servicenow.com/docs/access?context=c_CreatingNewTransformMaps&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)

</td><td>

sys\_transform\_map

</td><td>

Used for importing data. Transform maps:

-   Define mapping relationships between tables.
-   Can use business rules, other scripts, or other options to import data.

</td></tr><tr><td>

[Notifications](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td><td>

sysevent\_email\_action

</td><td>

Determine how an application communicates with users and alerts them about important application-related events.

</td></tr><tr><td>

[Processors](../../../script/processors/concept/c_Processors.md)

</td><td>

sys\_processor

</td><td>

Provide customizable URL endpoints that can execute arbitrary server-side JavaScript code and produce output such as TEXT or JSON.

</td></tr><tr><td>

[Relationships](https://www.servicenow.com/docs/access?context=table-relationships&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td><td>

sys\_relationship

</td><td>

Used to extend tables, reference records in another table, create many-to-many relationships, and join tables in a database view.

</td></tr><tr><td>

[Scheduled script executions](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td><td>

sysauto\_script

</td><td>

Define automated, server-side script logic that executes at a specific time or on a recurring basis. Scheduled script executions are also referred to as scheduled jobs.

</td></tr><tr><td>

[Script actions](https://www.servicenow.com/docs/access?context=r_ScriptActions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

</td><td>

sysevent\_script\_action

</td><td>

Contain scripts that run when an event occurs, for example:

-   Approval is canceled
-   Change is approved
-   Problem is assigned

</td></tr><tr><td>

[Script includes](../../../script/server-scripting/concept/c_ScriptIncludes.md#)

</td><td>

sys\_script\_include

</td><td>

Contain scripts that can be functions or classes. These scripts run only when called by other scripts, often business rules.Any server script that is complicated or reusable should be a Script Include, especially complicated business rules.

</td></tr><tr><td>

[Schedule items](https://www.servicenow.com/docs/access?context=t_ViewAScheduleItem&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td><td>

sys\_trigger

</td><td>

Contain the back-end data for the [System scheduler](https://www.servicenow.com/docs/access?context=c_SystemScheduler&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US), where scheduled jobs are created, queued up, and executed. Schedule items can execute scheduled jobs, business rules, inactivity monitors, service level agreement \(SLA\) calculations, metric events, upgrades, and more. You can access schedule item records to troubleshoot scheduling.

</td></tr><tr><td>

[UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td><td>

sys\_ui\_action

</td><td>

Include the buttons, links, and context menu items on forms and lists. Configure UI actions to make the UI more interactive, customized, and specific to user activities.

</td></tr><tr><td>

[UI macros](../../../script/server-scripting/concept/c_UIMacros.md#)

</td><td>

sys\_ui\_macro

</td><td>

Contain discrete scripted components that administrators can add to the user interface. UI macros are typically controls that provide inputs or information that is not provided by existing field types. By default, the system provides UI macros for a variety of user interface elements.

</td></tr><tr><td>

[UI pages](../../../script/server-scripting/reference/r_UIPages.md#)

</td><td>

sys\_ui\_page

</td><td>

Used to create and display forms, dialogs, lists, and other UI components.

</td></tr><tr><td>

[UI policies](https://www.servicenow.com/docs/access?context=t_CreateAUIPolicy&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td><td>

sys\_ui\_policy

</td><td>

Define the behavior and visibility of fields on a form. Fields can be one of the following:-   Mandatory
-   Visible
-   Read only

The following apply to usage:

-   UI policies are always attached to one table.
-   UI policies often have a condition that must be true for them to run.

</td></tr><tr><td>

[UI scripts](../../../script/client-scripts/concept/c_UIScripts.md#)

</td><td>

sys\_ui\_script

</td><td>

Contains client scripts stored for reuse. Only used when called from other scripts.

</td></tr><tr><td>

[UI style](https://www.servicenow.com/docs/access?context=t_DefineFieldStyles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td><td>

sys\_ui\_style

</td><td>

Enables you to declare individual CSS styles for a field in a list or form.

</td></tr><tr><td>

[Widgets](https://www.servicenow.com/docs/access?context=c_NestedWidgets&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

</td><td>

sp\_widget

</td><td>

Describe objects that contain content and can be added to or embedded in portal pages. You can use the base system widgets provided with the Service Portal, clone and modify widgets, or develop custom widgets to fit your own needs.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Studio reference](../concept/servicenow-studio-reference.md)

