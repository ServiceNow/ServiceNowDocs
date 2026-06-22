---
title: Configuring Now Mobile
description: Configure options for the Now Mobile app. For example, you can link the app with a service catalog and knowledge base, personalize the greeting for the home page, and specify which records appear under My Requests in the For Me tab.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-mobile-employee-experience/setup-mobile-employee.html
release: zurich
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Now Mobile app, Unified Employee Experience, Employee Service Management]
---

# Configuring Now Mobile

Configure options for the Now Mobile app. For example, you can link the app with a service catalog and knowledge base, personalize the greeting for the home page, and specify which records appear under **My Requests** in the **For Me** tab.

**Note:** Offline mode is not supported in the Now Mobile app.

## For Me

This page includes these configuration options:

-   **Greeting**

    Configure the greeting that your users see when they log in to the Now Mobile app. For example, you can add a hello message that includes the user's first and last name.

-   **My To-Dos**

    Users can view items that are assigned to them and complete their tasks. By default, My To-Dos show the user things that they need to approve from the Requests \[sc\_request\] and Requested Items \[sc\_req\_item\] tables. Other applications, such as HR Service Delivery, might include other types of tasks.


\[Omitted image "mobile\_home.png"\] Alt text: Configure a personalized welcome greeting.

## My Requests

Specify which records that you want your users to see under **My Requests** so that they can track their work assignments. For example, you can add a filter to display records that are opened by the user from the Problem table. By default, the app displays records that are opened by the user from the Incident and Requested Item tables.

\[Omitted image "my-requests-2-me.png"\] Alt text: Set the base table and filter from the request\_filter table.

## Search

Search includes these configuration options:

-   **People search**

    Configure whether users can search for other users in the system. By default, people search is enabled. For people search to display results, your users must have read-only access to the User \[sys\_user\] table. You can test people search by logging in as a user without any roles and searching for another user. If search results do not include meaningful data, for example, locations and phone numbers, update the access control lists \(ACLs\) on the User table to allow read access. For more information, see [Access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/access-control/access-control-rules.md).

-   **Analytics and suggestions**

    The Now Mobile app collects search data and analytics that generate search suggestions. If you are upgrading from a previous release, the search analytics do not contain any data yet. To immediately provide suggestions to your users, you can populate the search suggestions using knowledge, catalog, and user search records from the Text Searches \[text\_search\] table.

    Search Suggestions is a ServiceNow AI Platform feature. For more information, see [Search Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/search-suggestions/search-suggestions-overview.md).


## Items and services

Service Catalog items and services include these configuration options.

-   **Catalog**

    Enable your users to view and request their associated items in the Now Mobile app. If no catalogs are selected, users can view and request items from all catalogs in the system. By default, the app uses Service Catalog.

    For more information, see [Now Mobile for Service Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/service-catalog/now-mobile-catalog.md).

-   **Quick actions**

    Select catalog items to display as additional user menu actions. For example, add the **Report an Incident** catalog item to enable users to quickly navigate to the form. Users can only see items if they have the required user criteria permissions.


\[Omitted image "mobile\_catalogs.png"\] Alt text: Service catalog associated with the app.

## Knowledge

Enable users to view knowledge articles from the mobile app. If no knowledge bases are selected, users can view articles from all knowledge bases in the system. By default, the app uses the IT knowledge base.

For more information, see [Now Mobile for Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management/mobile-experience-for-km.md).

\[Omitted image "mobile\_knowledge\_bases.png"\] Alt text: Knowledge bases associated with the application.

## Siri shortcuts

In the base system, iOS users can use Siri shortcuts to open these pages in the app:

-   Open a chat window.
-   Browse items and services.
-   Open my tasks.
-   Open my requests.

