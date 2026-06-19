---
title: API implementation
description: You can use JavaScript APIs to extend application server and client functionality. Use web services to connect ServiceNow applications to other software applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/api-implementation.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API implementation and reference]
---

# API implementation

You can use JavaScript APIs to extend application server and client functionality. Use web services to connect ServiceNow applications to other software applications.

<table id="table_iwv_lpv_klb" class="nav-card"><tbody><tr><td>

[Scripts\[Omitted image "bus-start-developing.svg"\] Alt text: Extend application server and client functionality.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_Script.md)

</td><td>

[Web services \[Omitted image "bus-rocketship.svg"\] Alt text: Communicate between ServiceNow and third-party applications.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_AvailableWebServices.md)

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

