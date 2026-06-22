---
title: ServiceNow Studio supported file types using code search
description: Reference the file types that ServiceNow Studio supports when using code search to locate scripts and metadata across an instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sn-studio-file-types.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: reference
last_updated: "2026-05-29"
reading_time_minutes: 4
breadcrumb: [Reference, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio supported file types using code search

Reference the file types that ServiceNow Studio supports when using code search to locate scripts and metadata across an instance.

Code search in ServiceNow Studio uses the default code search group. The following table lists the file types supported by the default ServiceNow Studio code search.

**Tip:** To expand the list of supported file types, an administrator can create a new code search group that includes additional file types. For more information, see [Expand code search tables](https://developer.servicenow.com/connect.do#!/share/contents/3024956_expand_code_search_tables?v=1&t=PRODUCT_DETAILS).

**Note:** File types must extend the sys\_metadata table to be searchable in code search. Other file types, such as scheduled items \(sys\_trigger records\), are not searchable in ServiceNow Studio.

<table id="table_lcj_1bh_qcc"><thead><tr><th>

File type

</th><th>

Code search table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td><td>

sys\_security\_acl

</td><td>

Determines whether access is granted for a specified operation to a specific entity, such as:

-   Type of entity being secured
-   Operation being secured
-   Unique identifier describing the object

</td></tr><tr><td>

[Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/business-rules-classic/c_BusinessRules.md)

</td><td>

sys\_script

</td><td>

Customize system behavior. -   [Business Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/business-rules-classic/c_BusinessRules.md) run when a database action occurs \(query, insert, update, or delete\).
-   The script can run:
    -   before or after the database action is performed \(runs as part of the database operation\).
    -   asynchronously \(at some point after the database operation\).
    -   on display \(when displaying the data in a form\).

</td></tr><tr><td>

[Client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/client-scripts.md)

</td><td>

sys\_script\_client

</td><td>

Change the appearance of forms and display fields based on entered values or other custom display options.

-   onLoad: The client script runs when the form or page loads.
-   onChange: The client script runs when a specific field changes and also when the form or page loads.
-   onSubmit: The client script runs when the form is submitted.

 Client scripts can also be called by other scripts or modules, including UI policies.

</td></tr><tr><td>

[Email templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/c_EmailTemplates.md)

</td><td>

sysevent\_email\_template

</td><td>

Create reusable content for the subject line and message body of email notifications.

</td></tr><tr><td>

[Inbound email actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/actions-inbound-email.md)

</td><td>

sysevent\_in\_email\_action

</td><td>

Script how the system responds to inbound emails.

</td></tr><tr><td>

[Map pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/c_MapPages.md)

</td><td>

cmn\_map\_page

</td><td>

Display ServiceNow data graphically on a Google map page based on location data that you provide.

</td></tr><tr><td>

[Map transforms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/c_CreatingNewTransformMaps.md)

</td><td>

sys\_transform\_map

</td><td>

Import data by defining mapping relationships between tables. Transform maps:

-   Define mapping relationships between tables.
-   Can use business rules, other scripts, or other options to import data.

</td></tr><tr><td>

[Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateANotification.md)

</td><td>

sysevent\_email\_action

</td><td>

Determine how an application communicates with users and alerts them about important application-related events.

</td></tr><tr><td>

[Processors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_Processors.md)

</td><td>

sys\_processor

</td><td>

Provide customizable URL endpoints that execute server-side JavaScript code and produce output such as TEXT or JSON.

</td></tr><tr><td>

[Relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/table-relationships.md)

</td><td>

sys\_relationship

</td><td>

Extend tables, reference records in another table, create many-to-many relationships, and join tables in a database view.

</td></tr><tr><td>

[Scheduled script executions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_ScheduledJobs.md)

</td><td>

sysauto\_script

</td><td>

Define automated, server-side script logic that executes at a specific time or on a recurring basis. Scheduled script executions are also referred to as scheduled jobs.

</td></tr><tr><td>

[Script actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/system-events/r_ScriptActions.md)

</td><td>

sysevent\_script\_action

</td><td>

Contain scripts that run when an event occurs, for example:

-   Approval is canceled
-   Change is approved
-   Problem is assigned

</td></tr><tr><td>

[Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ScriptIncludes.md)

</td><td>

sys\_script\_include

</td><td>

Contain reusable functions or classes that run only when called by other scripts, often business rules. Any server script that is complicated or reusable should be a Script Include, especially complicated business rules.

</td></tr><tr><td>

[Schedule items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_ViewAScheduleItem.md)

</td><td>

sys\_trigger

</td><td>

Contain the back-end data for the [System scheduler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_SystemScheduler.md), where scheduled jobs are created, queued up, and executed. Schedule items can execute scheduled jobs, business rules, inactivity monitors, service level agreement \(SLA\) calculations, metric events, upgrades, and more. Access schedule item records to troubleshoot scheduling.

</td></tr><tr><td>

[Defining UI actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/c_UIActions.md)

</td><td>

sys\_ui\_action

</td><td>

Include the buttons, links, and context menu items on forms and lists. Configure UI actions to make the UI more interactive, customized, and specific to user activities.

</td></tr><tr><td>

[UI macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_UIMacros.md)

</td><td>

sys\_ui\_macro

</td><td>

Contain discrete scripted components that administrators can add to the user interface. UI macros are typically controls that provide inputs or information not provided by existing field types. By default, the system provides UI macros for a variety of user interface elements.

</td></tr><tr><td>

[UI pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/r_UIPages.md)

</td><td>

sys\_ui\_page

</td><td>

Create and display forms, dialogs, lists, and other UI components.

</td></tr><tr><td>

[Using UI policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAUIPolicy.md)

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

[UI scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_UIScripts.md)

</td><td>

sys\_ui\_script

</td><td>

Store client scripts for reuse. Run only when called from other scripts.

</td></tr><tr><td>

[UI style](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_DefineFieldStyles.md)

</td><td>

sys\_ui\_style

</td><td>

Declare individual CSS styles for a field in a list or form.

</td></tr><tr><td>

[Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/c_NestedWidgets.md)

</td><td>

sp\_widget

</td><td>

Describe objects that contain content and can be added to or embedded in portal pages. Use the base system widgets provided with the Service Portal, clone and modify widgets, or develop custom widgets to fit your own needs.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Studio reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-reference.md)

