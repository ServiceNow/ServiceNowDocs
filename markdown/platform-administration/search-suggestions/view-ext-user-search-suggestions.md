---
title: Use the GraphQL REST API to view suggestions created from external user searches
description: Submit a request to the GraphQL REST API endpoint to retrieve search suggestions created from searches by self-registered external users. This endpoint allows access by non-authenticated guest users.
locale: en-US
release: australia
product: Search Suggestions
classification: search-suggestions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Search Suggestions, Search Suggestions, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Use the GraphQL REST API to view suggestions created from external user searches

Submit a request to the GraphQL REST API endpoint to retrieve search suggestions created from searches by self-registered external users. This endpoint allows access by non-authenticated guest users.

## Before you begin

Ensure that the following conditions are met in your instance:

-   The Domain Separation plugin isn't activated. For details on this plugin, see Domain separation plugin.
-   The Explicit Roles plugin \(com.glide.explicit\_roles\) is activated. To learn more about this plugin, see Explicit Roles.
-   External users with the snc\_external role have submitted searches in search applications that generate search suggestions, such as ServiceNow® Service Portal, Now Mobile, or ServiceNow® Virtual Agent.
-   The **glide.search.suggestions.allow\_guest\_user** system property is set to **true**. For details on setting a system property value, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).

Obtain the sys\_id of the search application that you want to retrieve external user search suggestions for.

**Note:** Users with the search\_application\_admin, agent\_workspace\_user, or workspace\_user roles can obtain this sys\_id by copying it from the search application record in the Search Application Configuration \[sys\_search\_context\_config\] table.

Download a third-party GraphQL client, such as the GraphiQL, Insomnia, or Postman client.

Role required: none

## About this task

Search Suggestions creates suggestions for searches performed by self-registered external users. When the **glide.search.suggestions.allow\_guest\_user** system property is set to **true**, non-authenticated guest users can access the GraphQL REST API endpoint for your instance to retrieve external user search suggestions for a search application.

No authentication is required or enforced for this GraphQL REST API endpoint.

**Note:** Non-authenticated guest users can only retrieve search suggestions from the Global domain. If domain separation is enabled in your instance, guest users can't retrieve any search suggestions.

## Procedure

1.  In your third-party GraphQL client, configure a new request that uses the HTTP POST method.

2.  Set the endpoint for the request to the GraphQL REST API endpoint for your instance, `https://<instance name>.service-now.com/api/now/graphql`.

3.  Set the request body to the following GraphQL query, replacing `<search_application_sys_id>` with the sys\_id of the search application that you want to retrieve external user search suggestions for:

    ```
    {
      GlideSearch_Query {
        suggestions(searchContextConfigId: "<search_application_sys_id>", searchTerm: "") {
          term
          data {
            name
            records {
              type
              columns {
                label
                fieldName
                value
                displayValue
              }
            }
          }
        }
      }
    }
    ```


## Result

The system returns search suggestions from application searches by self-registered external users as a JSON object, as shown in this example:

```
{
  "data": {
    "GlideSearch_Query": {
      "suggestions": {
        "term": "",
        "data": [
          {
            "records": [
              {
                "type": "POPULAR_QUERY",
                "columns": [
                  {
                    "label": "name",
                    "displayValue": "automatic replies",
                    "value": "automatic replies",
                    "fieldName": "name"
                  }
                ]
              },
              {
                "type": "POPULAR_QUERY",
                "columns": [
                  {
                    "label": "name",
                    "displayValue": "contact group",
                    "value": "contact group",
                    "fieldName": "name"
                  }
                ]
              },
              {
                "type": "POPULAR_QUERY",
                "columns": [
                  {
                    "label": "name",
                    "displayValue": "tablet",
                    "value": "tablet",
                    "fieldName": "name"
                  }
                ]
              },
              {
                "type": "POPULAR_QUERY",
                "columns": [
                  {
                    "label": "name",
                    "displayValue": "laptop",
                    "value": "laptop",
                    "fieldName": "name"
                  }
                ]
              },
              {
                "type": "POPULAR_QUERY",
                "columns": [
                  {
                    "label": "name",
                    "displayValue": "new email account",
                    "value": "new email account",
                    "fieldName": "name"
                  }
                ]
              }
            ],
            "name": "Popular searches"
          }
        ]
      }
    }
  }
}
```

