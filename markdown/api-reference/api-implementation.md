---
title: API implementation
description: You can use JavaScript APIs to extend application server and client functionality. Use web services to connect ServiceNow applications to other software applications.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [API implementation and reference]
---

# API implementation

You can use JavaScript APIs to extend application server and client functionality. Use web services to connect ServiceNow applications to other software applications.

<table id="table_iwv_lpv_klb" class="nav-card"><tbody><tr><td>

[Scripts![](../../../reuse/icons/brand-icons/bus-start-developing.svg) Extend application server and client functionality.](../../../script/topic/c_Script.md)

</td><td>

[Web services ![](../../../reuse/icons/brand-icons/bus-rocketship.svg) Communicate between ServiceNow and third-party applications.](../../../integrate/web-services/reference/r_AvailableWebServices.md)

</td></tr></tbody>
</table>## Scripts

Use Server JavaScript APIs in scripts to change application functionality or create applications. Use client-side JavaScript APIs to control aspects of how an instance is displayed and functions within the web browser.

Common use cases:

-   Calculate durations to give users a way to specify when a task or process is due.
-   Display prompts with alerts, confirmations, or other messages.
-   Implement event logging at different output levels, such as debug, info, warning, and error.
-   Query, update, create, and delete records.
-   Validate the input of all date and time fields.

## Web services

Use inbound \(provider\) and outbound \(consumer\) web services enable diverse applications to exchange information.

Common use cases:

-   Use REST API request information from ServiceNow instances in third-party applications.
-   Create scripted REST APIs for custom requests that aren’t available in the provided ServiceNow REST APIs.
-   Create a custom GraphQL API to query record data from a component or a third-party system.
-   Use the open database connectivity \(ODBC\) driver for read-only access to the database associated with your instance.
-   Use domain separation to separate data, processes, and administrative tasks into logical groups.

