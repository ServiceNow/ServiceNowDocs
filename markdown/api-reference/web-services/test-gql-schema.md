---
title: Test GraphQL APIs with GraphQL Explorer
description: Test query your GraphQL APIs using an integrated GraphQL testing tool.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Query record data using the GraphQL API framework, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Test GraphQL APIs with GraphQL Explorer

Test query your GraphQL APIs using an integrated GraphQL testing tool.

## Before you begin

Create a schema for your GraphQL API. For more information, see [Create a GraphQL schema](build-graphql-scripted-schema.md#).

Enabling introspective queries allows GraphQL Explorer to show the schemas on the instance in the Documentation Explorer and as auto-complete suggestions, which makes finding queries and mutations easier. For more information, see [Enable introspective queries for GraphQL schemas](enable-introspective-queries-graphql-schemas.md).

**Note:** Don’t use introspective queries in a production environment.

Role required: graphql\_schema\_admin or admin

## About this task

The GraphQL Explorer integrates the GraphiQL IDE into the ServiceNow AI Platform. For additional information about the interface, see the [GraphiQL readme](https://github.com/graphql/graphiql/blob/main/packages/graphiql/README.md) in the GraphiQL GitHub repository.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **GraphQL** &gt; **GraphQL Explorer**.

2.  If you enabled introspection, in the left sidebar, select the Show Documentation Explorer icon \(![Show Documentation Explorer icon](../image/graphql-show-doc-explorer.png)\) to view and search for available queries or mutations.

3.  In the editor, enter a query to the schema.

    Include both the application and schema namespaces in the query. For information about directives you can apply, see [Directives and global functions](../concept/scripted-graph-ql.md#section_zdw_rnc_glb).

    This example shows using both the application and schema namespaces:

    -   Application namespace: `x_graph_scope`
    -   Schema namespace: `planet`
    ```
    query {
      x_graph_scope {
        planet {
          findAll {
            name
            mass
            distance
          }
        }
      }
    }
    ```

    This example shows using the @defer directive to stream results for the openedBy field after the initial incident response.

    ```
    query findIncidents {
      now {
        incident {
          findAll {
            description {
              displayValue
            }
            ...
            @defer(label: "my-label", if: true) {
              openedBy {
                firstName
                lastName
              }
            }
          }
        }
      }
    }
    ```

4.  At the bottom of the editor, select **Variables** and enter any necessary variables.

5.  Select the Execute query icon \(![Execute query icon](../image/graphql-execute-query.png)\).

    **Tip:** You can also use a keyboard shortcut. To see the list of available keyboard shortcuts, select the Open short keys dialog icon \(![Open short keys dialog icon](../image/graphql-keyboard-shortcuts.png)\).

    The result of your query returns in the right pane.

6.  Select the Add tab icon \(![Add tab icon](../image/graphql-add-tab.png)\) to run additional queries.


## What to do next

If you need to view a list of previous queries, in left sidebar, select the Show History icon \(![Show History icon](../image/graphql-show-history.png)\).

To access record data in a component, you can create a custom component and query your scripted GraphQL schema from the component. For more information, see [Query a GraphQL schema from a component](query-schema-from-component.md).

**Parent Topic:**[Query record data using the GraphQL API framework](../concept/scripted-graph-ql.md)

