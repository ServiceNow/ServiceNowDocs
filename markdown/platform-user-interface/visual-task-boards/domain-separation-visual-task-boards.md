---
title: Domain separation and Visual Task Boards
description: Domain separation is supported in the Visual Task Boards application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Visual Task Boards
classification: visual-task-boards
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Visual Task Boards reference, Visual Task Boards, Configure UIs and portals, Configure user experiences]
---

# Domain separation and Visual Task Boards

Domain separation is supported in the Visual Task Boards application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## How domain separation works in Visual Task Boards

Visual Task Boards that are "data-driven" show the data from tables that are like Task tables. The data that is domain separated is also supported.

Condition-based criteria is used to filter that data. Free-form VTBs' use Private Tasks \(vtb\_task\), which supports domain separation as an extension of Task and inherits domain separation logic as a result.

**Parent Topic:**[Visual Task Boards reference](vis-task-boards-ref.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

