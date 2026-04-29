---
title: Domain separation and Contextual Search
description: Domain separation is supported in Contextual Search. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Contextual Search
classification: contextual-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Domain separation and Contextual Search

Domain separation is supported in Contextual Search. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## How domain separation works in Contextual Search

By default, Contextual Search Suggestions results that appear use the domain of the currently logged-in user.

## Search as a different user

In addition to being able to search for results using the domain of the logged-in user, the administrator can also configure Contextual Search to [Search as a different user](../task/t_SearchAsDifferentUser.md) .

When **Search as** is configured, two tabs appear in the search results:

1.  **My Results** tab searches using the currently logged-in user domain.
2.  The **Search as** user tab searches using the domain of the User Reference field selected by the administrator. For example, selecting a request's **Opened by** or **Caller** field searches using the domain of the user who made the request.

**Note:**

-   The **Search as** user results apply security access to display results that are common to both the logged-in user and the **Search as** user. Hence, the search result view for that user may have fewer entries than what that user can actually view.
-   Record producers only support searching as the currently logged-in user.

Example: An Incident displaying search results for the currently logged-in user on the **My Results** tab.

![My Results tab showing search results for the currently logged-in user.](../image/ContextualSearch-MyResults.png)

Example: The same Incident displaying search results for the user from the **Caller** reference field on a second tab.

![Beth Anglin Results tab showing search results for the user specified as the Incident record's Caller.](../image/ContextualSearch-CallerResults.png)

**Parent Topic:**[Contextual search](c_ContextualSearch.md)

**Related topics**  


[Enable viewing of search results for the current and another selected user](../task/t_SearchAsDifferentUser.md)

