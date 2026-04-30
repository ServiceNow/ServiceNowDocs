---
title: Standard ticket page
description: Configure individual request types to display the request-specific information, while still having a consistent layout that is similar to other request types. This configuration ensures a consistent experience when viewing submitted requests.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Creating portal pages, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Standard ticket page

Configure individual request types to display the request-specific information, while still having a consistent layout that is similar to other request types. This configuration ensures a consistent experience when viewing submitted requests.

For new instances, the standard ticket page is available by default. For upgraded instances, you need to activate the Standard Ticket Route page route map. For information about activating this page route map, see [Activate the page route map for the standard ticket page](../task/config-pageroutemap-stpage.md).

The information displayed in each section of a standard ticket page depends on the individual request type. If a configurable section has no specified values or if a user does not have access to the information, it is not visible.

![Incident standard ticket page](../image/inci-in-service-portal.png "Standard ticket page for an incident")

## Header section

By default, this section displays the following information for a submitted request:

-   Identification number
-   Created and updated dates
-   State. Instead of the **State** field, you can also configure any other field that represents the state of the ticket.

## Info section

If configured, this section displays the following regions for a submitted request:

-   Ticket description region with the short description, and optionally the description.

    **Note:** You can map the **Description** field to any other field on the record.

-   Fields region where the associated fields are configured. A configured field is not visible when it has no value or when a user does not have access to the field.

    **Note:** A field of the Workflow type is not supported for any table. Only for the Requested Item \[sc\_req\_item\] table, the Workflow type field is supported, for example, the **Stage** field. This field is displayed at the last irrespective of the field position in the configuration.

-   Actions region

## Tabs section

If configured, this section displays the following types of tabs for a submitted request:

-   Activity
-   Attachments
-   Variable editor
-   Variable summarizer
-   Associated Requests. Displays all associated requests \(visible in the **My Requests** widget in Service Portal\) for which the current ticket is the parent. It is applicable in any of the following scenarios:

    -   If the current ticket is a universal request, then all requests associated \(through the **Parent** field on the task table\) with child tickets of the universal request are displayed.
    -   If the current ticket is not a universal request, then all requests associated \(through the **Parent** field on the task table\) with the current ticket are displayed.
    For information on defining filters for the My Requests widget, see [Define filters for My Requests](https://www.servicenow.com/docs/access?context=configure-my-requests&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   Custom tab

By default, the **Activity** and **Attachments** tabs are available.

## Configurations for a cross-scope application

For each request type of a cross-scope application, the following configurations are required:

-   Restricted caller access privileges for the following standard ticket page widgets so that these widgets can access the application tables. For information about these privileges, see [Application access settings](https://www.servicenow.com/docs/access?context=c_ApplicationAccessSettings&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
    -   Widget: Standard Ticket Header
    -   Widget: Standard Ticket Attachments
    -   Widget: Standard Ticket Tab
-   Restricted caller access privileges for the **Description** field in the application. This field is displayed on the standard ticket page header.
-   Page route map to route all the requests of that application to the standard ticket page

## Domain separation for a standard ticket page

Tab configurations are not domain-separated.

Ticket configurations are process domain-separated. For any request type record, when a user opens the standard ticket page, it checks for ticket configurations in the following order irrespective of the user's domain:

1.  In the record’s domain
    1.  Ticket configurations for the record table
    2.  Ticket configurations for the parent table of the record table
2.  In the record domain’s parent hierarchy
    1.  Ticket configurations for the record table
    2.  Ticket configurations for the parent table of the record table

**Note:** For a table, only one active configuration is allowed per domain.

-   **[Configure the standard ticket page](../task/configure-st-page.md)**  
Give Service Portal users a consistent way to view their submitted requests. You can configure the standard ticket page for different request types.
-   **[Activate the page route map for the standard ticket page](../task/config-pageroutemap-stpage.md)**  
If you have upgraded your instance, redirect the ticket page to standard\_ticket page in Service Portal and view requests on the standard ticket page.

**Parent Topic:**[Creating portal pages](c_Pages.md)

**Related topics**  


[Standard ticket page for a requested item](https://www.servicenow.com/docs/access?context=stpage-req-item&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

[Incident standard ticket page](https://www.servicenow.com/docs/access?context=incident-stnd-ticket-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

