---
title: Legacy - Update a custom application record
description: You can update a custom application record to add new features or change application functionality.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Update a custom application record

You can update a custom application record to add new features or change application functionality.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Role required: admin or a delegated developer role granting full access

## About this task

You can only update applications in development on your local instance. You cannot edit applications downloaded from your company application repository or the ServiceNow Store.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Applications** &gt; **Studio**.

2.  Click the application name or the **Edit** button for the application you want to update.

    The system displays the application and application files in Studio.

3.  Click **File** &gt; **Settings**.

    Studio opens a tab containing the Custom Application record for the current application.

4.  Fill in the fields, as appropriate.

<table id="table_CustomApplicationForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

\[Required\] Enter a label for the application. Changing the name does not change any other field value derived from the application name such as the **Scope**, **Menu**, or **User role** fields.

</td></tr><tr><td>

Version

</td><td>

Enter version information for the application. Both the ServiceNow application repository and the store use this value to determine whether updates are available to your application users.**Note:** To publish the application in the ServiceNow Store, the version must conform to the application certification standards.

</td></tr><tr><td class="sub-head" colspan="2">

Application Scoping

</td></tr><tr><td>

Scope

</td><td>

\[Read Only\] Displays the unique application scope set during the creation process. You can change this value only by deleting and recreating the application with a new value. For more information about the protections offered, see [Application scope](../concept/c_ApplicationScope.md).

</td></tr><tr><td>

Application administration

</td><td>

Select whether to protect sensitive application data by restricting how users acquire application-specific roles. See [Application administration](../concept/application-administration.md).

</td></tr><tr><td class="sub-head" colspan="2">

Design and Runtime

</td></tr><tr><td>

JavaScript Mode

</td><td>

The JavaScript standard that the application supports. Select **ECMAScript 2021 \(ES12\)** to support features in ECMAScript 12th edition or **ES5 Standards Mode** to support features in ECMAScript 5th edition. Select **Compatibility Mode** to support earlier ECMAScript editions. For more information, see [Set the JavaScript mode for an application](https://www.servicenow.com/docs/access?context=set-javascript-mode-application&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Runtime Access Tracking

</td><td>

Select how the application handles script access requests to resources in other applications. Select **None** to authorize all access requests to cross-scope resources without logging them. Select **Tracking** to log and authorize all access requests to cross-scope resources. Select **Enforcing** to log access requests to cross-scope resources but require an administrator to authorize each request.

</td></tr><tr><td>

Restrict Table Choices

</td><td>

Clear the option to allow the application to see tables from other application scopes. Select the option to restrict design choices to only tables in the same application.

</td></tr><tr><td class="sub-head" colspan="2">

Subscription Management

</td></tr><tr><td>

Licensable

</td><td>

Specifies whether the application is tracked by the Subscription Management application.

</td></tr><tr><td>

Subscription requirement

</td><td>

Not applicable for ServiceNow customers who build custom applications for their own use. Used only by partners who sell and monitor the usage of resellable applications on the ServiceNow Store.Specifies whether the application requires a separate subscription \(**Required**\) or is monitored only.

</td></tr><tr><td>

Subscription model

</td><td>

Not applicable for ServiceNow customers who build custom applications for their own use. Used only by partners who sell and monitor the usage of resellable applications on the ServiceNow Store.Specifies how the Subscription Management application tracks usage. See [Types of subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=types-subscription-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td class="sub-head" colspan="2">

Primary Menu

</td></tr><tr><td>

Menu

</td><td>

Select the application menu where you want to display modules. For more information about menus and modules, see [Create an application menu](../../../administer/auto-test-framework/reference/test-steps-app-navigator-category.md#).

</td></tr><tr><td class="sub-head" colspan="2">

End user access

</td></tr><tr><td>

User role

</td><td>

Select the user role required to access the application menu. For more information about user roles, see [Create a role](https://www.servicenow.com/docs/access?context=t_CreateARole&version=australia&pubname=australia-platform-administration&ft:locale=en-US) [Create a role](https://www.servicenow.com/docs/access?context=t_CreateARole&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Short description

</td><td>

Enter a description of the application purpose or usage.

</td></tr><tr><td>

Logo

</td><td>

Select the image the system displays in the applications list and ServiceNow Store.

</td></tr><tr><td>

Application Files

</td><td>

View configuration records associated with this application in platform feature tables.

</td></tr><tr><td>

Dependencies

</td><td>

View or add tables or applications on which this application depends. The system automatically adds records to this list when you extend tables or when another application creates application files for this application. Add script-based dependencies. See [Dependencies for custom applications](../concept/c_ApplicationDependencies.md).

</td></tr><tr><td>

Cross scope privileges

</td><td>

View or create cross-scope privilege records to determine which script operations and targets the system allows to run. See [Cross-scope privilege record](../reference/c_CrossScopePrivilegeRecord.md).

</td></tr><tr><td>

Design Access

</td><td>

View or specify which other applications have design access to tables or records in this application. See [Application design access record](../concept/c_ApplicationDesignAccessRecord.md).

</td></tr></tbody>
</table>5.  Click **Update**.


**Parent Topic:**[Legacy - ServiceNow Studio](../concept/c_ServiceNowStudio.md)

