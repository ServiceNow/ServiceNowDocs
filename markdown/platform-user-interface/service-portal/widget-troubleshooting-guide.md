---
title: Widget troubleshooting guide
description: Use the following tools to investigate and resolve unexpected behavior in your custom Service Portal widgets.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Widget troubleshooting guide

Use the following tools to investigate and resolve unexpected behavior in your custom Service Portal widgets.

Provides debugging tips for troubleshooting Service Portal configuration issues.

-   **Reduce complexity**

    Deactivate widgets unrelated to the widget you are troubleshooting to isolate parts of the page that may be causing errors or unexpected behavior. Set the active field to false on a widget record to hide the widget on the page, and prevent associated scripts from executing.

-   **Use the browser developer console**

    All supported desktop browsers have built in developer tools. Access your browsers developer tools to view console messages and errors thrown by client-side JavaScript. Many of the logging tools detailed below output information to this console.

    If you experience performance issues, check the JavaScript console to see if there are errors, a large number of HTTP requests, or HTTP requests that take a long time to resolve. You can use the console to identify any widgets that load slowly. For more information, see the [How to identify a slow widget on a page \[KB0744521\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0744521) article in the Now Support Knowledge Base.

-   **Determine the cause of performance issues**

    The following tips can help determine the cause of performance issues in portals:

    -   Determine if the issue is related to the portal or platform-wide by comparing the functionality in both interfaces. For more information about platform performance issues, see Platform performance.
    -   Determine if the issue affects the entire portal or specific pages. If all pages in the portal are slow, check if scripted menu items in the header menu or themes with large font or image files could be the cause. If a specific page is slow, use the browser developer console to determine which widget could be the cause.
    -   Check the Log \[syslog\] table for warnings related to large JSON objects causing slowness. If these warnings are appear with the action that causes slowness, this indicates that a widget is using too much data.
    For more information, see the [Six common performance pitfalls in Service Portal and how to avoid them \[KB0634588\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0634588) article in the Now Support Knowledge Base.

-   **Use the widget context menu to access information and options**

    CTRL+right-click a widget to access configuration options for the widget. There are also options to output the scope and scope data object to the browser console. For more detail on this menu, see [Using portal widgets](../concept/service-portal-widgets.md).

-   **Use script methods to capture debugging output**

    Several methods are available to output debugging information within your server and client-side code.

<table id="table_dfp_xc3_ldb"><thead><tr><th>

Method

</th><th>

Availability

</th><th>

Description

</th></tr></thead><tbody><tr><td>

console.log\(\)

</td><td>

Server and client

</td><td>

Logs output to the browser developer console.

</td></tr><tr><td>

$sp.log\(\)

</td><td>

Server

</td><td>

Logs output to the Service Portal Log Entries \[sp\_log\] table, when the logged in user has the `sp_admin` or `admin` role.

</td></tr><tr><td>

[gs.log\(\)](https://www.servicenow.com/docs/access?context=c_GlideSystemAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Server

</td><td>

Logs output to the Log \[syslog\] table.**Note:** gs.log creates records on the syslog table. Excessive use can adversely affect performance.

</td></tr><tr><td>

[gs.warn\(\)](https://www.servicenow.com/docs/access?context=c_GlideSystemScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Server

</td><td>

Produces warning level output in the Log \[syslog\] table.

</td></tr><tr><td>

[gs.error\(\)](https://www.servicenow.com/docs/access?context=c_GlideSystemScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Server

</td><td>

Produces error level output in the Log \[syslog\] table.

</td></tr><tr><td>

[gs.addInfoMessage\(\)](https://www.servicenow.com/docs/access?context=c_GlideSystemScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Server

</td><td>

Displays a green information message at the top of the browser window.

</td></tr><tr><td>

[gs.addErrorMessage\(\)](https://www.servicenow.com/docs/access?context=c_GlideSystemScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Server

</td><td>

Displays a red error message at the top of the browser window.

</td></tr><tr><td>

[spUtil.addErrorMessage\(\)](https://www.servicenow.com/docs/access?context=spUtilAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Client

</td><td>

Displays an error message within the browser window.

</td></tr><tr><td>

[spUtil.addInfoMessage\(\)](https://www.servicenow.com/docs/access?context=spUtilAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Client

</td><td>

Displays an Info message within the browser window.

</td></tr><tr><td>

[spUtil.addTrivialMessage\(\)](https://www.servicenow.com/docs/access?context=spUtilAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Client

</td><td>

Displays a message which automatically disappears after a short time.

</td></tr><tr><td>

[debugger](https://www.servicenow.com/docs/access?context=script-debugger&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

</td><td>

Client

</td><td>

Sets a break point in Chrome and Firefox browsers, allowing you to step through a script line by line in the browsers developer console.

</td></tr><tr><td>

\{\{data\|json\}\}

</td><td>

HTML

</td><td>

This code can be added to the HTML code of a page to output the data object to the portal page in JSON format.

</td></tr></tbody>
</table>-   **Check for security restrictions**

    Often, widget display issues are caused by access rules or user criteria rather than the widget script. Check the user criteria for records and verify that any records that are not accessible within a widget are accessible using the platform UI. Use the ACL debugger to ensure that your users have the expected access to records used by your widgets. For more detail on the debugger, see [ACL debugging tools](https://www.servicenow.com/docs/access?context=c_AccessControlRulesDebug&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

    Service Catalog items can also be restricted to not appear in Service Portal. If you get a `You are either not authorized or record is not valid` error message for a Service Catalog widget, check that the item is not hidden from Service Portal.

-   **Check the associated Angular Providers**

    Verify that the necessary Angular Providers are associated with widgets. Removing the default Angular Providers associated with a base system widget can cause unexpected behavior. For example, removing the scToggleData or scBindHtmlCompile Angular Providers from the SC Catalog Item widget.

-   **Create a reference to the widgets scope in the console**

    Use reference to a widget to manipulate scope data or manually run the widgets client and server scripts. Use the following steps to create the reference.

    -   1. Right-click the widget and choose **Inspect**.
    -   2. In dev tools Elements tab, click to highlight the element with attribute widget=`widget`. You can find it a few elements above the currently inspected element. This element points the $0 scripting tool at the widget.
    -   In the Javascript console, run the following code:

        ```
        var scopeRef = angular.element($0).scope();
        ```

    Use the reference to your widget to change data within the console. See the following example. Remember to run `AngularJS $apply()` on the scope to apply changes to the page.

    ```
    scopeRef.data.prop1 = "Pear";
    scopeRef.$apply();
    ```

    Run any function defined in the widgets client controller from your reference using the syntax below.

    ```
    scopeRef.exampleFunction();
    ```

    Use the refresh command to manually execute the widgets server script.

    ```
    scopeRef.server.refresh();
    ```


**Parent Topic:**[Developing custom widgets](../concept/widget-dev-guide.md)

