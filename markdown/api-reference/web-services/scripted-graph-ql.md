---
title: Query record data using the GraphQL API framework
description: Create a custom GraphQL API to query record data from a component or a third-party system.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Query record data using the GraphQL API framework

Create a custom GraphQL API to query record data from a component or a third-party system.

For example, you can create a component that displays the cases associated with an SLA. You can use the Next Experience UI Framework to develop the component you need, and access case data from the platform by creating a GraphQL schema that defines data in the Case table.

To learn more about developing components, see [Developing components for Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/custom-components.md).

## Benefits of GraphQL

GraphQL is a web query language optimized for client-side development. Using scripted GraphQL, you can:

-   Discover fields and objects available to query through introspection.
-   Query the exact data you need from a component.
-   Manage multiple possible queries from a single API, as opposed to multiple endpoints for a REST request.
-   Integrate with third-party systems by making the schema public.
-   Generate the GraphQL query from your component and handle the response.

## What to know before you begin

Before you start creating custom GraphQL APIs, make sure you have:

-   GraphQL knowledge to create a schema.
-   JavaScript knowledge to define the API behavior.
-   General knowledge of web component concepts.
-   A custom Workspace component to consume record data.
-   Understanding of the ServiceNow data model that you want to expose in the schema.
-   GlideRecord knowledge to map fields to record data in your resolver scripts.

## GraphQL overview

Creating a scripted GraphQL API includes these parts:

-   **GraphQL Schema Definition Language \(SDL\)**

    Define the structure and data type of fields available in a GraphQL query. You can define the SDL using the **Schema** script field in the GraphQL Scripted Schemas \[sys\_graphql\_schema\] table. The SDL only supports Query and Mutation operations.

-   **Resolvers**

    Define the data returned by each field. You can define the resolvers for each field in the GraphQL Scripted Resolvers related list on the GraphQL Scripted Schemas form.

-   **Typeresolvers**

    Resolve interfaces and unions into concrete GraphQL types. For example, you might define a union between an `incident` type and a `problem` type. Use the typeresolver script to define when to return which. You can define the typeresolvers in the GraphQL Scripted Typeresolvers related list on the GraphQL Scripted Schemas form.

-   **Resolver mappings**

    Map resolvers to fields in the schema. You can define resolver mappings in the GraphQL Scripted Resolver Mappings related list on the GraphQL Scripted Schemas form.


To learn more about the GraphQL query language, see the [GraphQL website](https://graphql.org/).

To test queries to your GraphQL APIs, you can use the GraphQL Explorer, an integrated GraphQL testing tool. For more information, see [Test GraphQL APIs with GraphQL Explorer](../task/test-gql-schema.md).

## Limitations

The following GraphQL features aren't supported:

-   Subscription operations
-   Custom scalar types

## Introspection

By default, introspective queries into your custom schemas aren’t enabled. To turn on introspection, see [Enable introspective queries for GraphQL schemas](../task/enable-introspective-queries-graphql-schemas.md).

## Namespaces

GraphQL APIs have two different namespaces:

-   **Application namespace**

    The namespace for the custom application. To learn more about application namespaces, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationScope.md).

-   **Schema namespace**

    The namespace for the schema to ensure that all queries are unique. You can have multiple schema namespaces in a single application.


When querying data, you must include both namespaces in your query. For example, the following query is searching for data with the following namespaces:

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

## Directives and global functions

-   **`@source` schema directive**

    Maps a GraphQL field to the value of a property of the parent object. If the field has a separate resolver script, the system uses the record that it resolves to instead of the parent object.

    Use the `@source` directive in your schema script.

-   **`@defer` query directive**

    Defer processing of a GraphQL fragment until later in the query. Use this query directive to delay returning data for slow-responding fields within a fragment. Stream the field results of the deferred fragment as a multi-part response.

    **Note:** To use the `@defer` directive, your GraphQL client must accept multipart/mixed HTTP headers. For example, set the HTTP headers to `Accept: multipart/mixed; boundary="-"`.

    Use the `@defer` directive to improve user time to interaction. Avoid applying this query directive indiscriminately as it can also cause performance degradations. Conduct performance testing to determine which fields can be deferred for better performance.

-   **Resolver functions**

    These functions are available on the global env object.

    -   getArguments\(\): Returns the arguments of the previous field.
    -   getSource\(\): Returns the parent object.
    Use in your resolver script.

-   **Typeresolver functions**

    These functions are available on the global env object.

    -   getArguments\(\): Returns the arguments of the previous field.
    -   getObject\(\): Returns the parent object.
    -   getTypeName\(\): Returns the name of the interface or union type.
    Use in your typeresolver script.


## Demo application

To see a demo GraphQL PTO calendar schema with mutations and queries, enable the GraphQL Framework Demo Application plugin \(com.glide.graphql.framework.demo\).

-   **[Create a GraphQL schema](../task/build-graphql-scripted-schema.md#)**  
Create a GraphQL schema to make data available to GraphQL queries.
-   **[Enable introspective queries for GraphQL schemas](../task/enable-introspective-queries-graphql-schemas.md)**  
Discover the queries and mutations supported by schemas on your instance by enabling introspection.
-   **[Test GraphQL APIs with GraphQL Explorer](../task/test-gql-schema.md)**  
Test query your GraphQL APIs using an integrated GraphQL testing tool.
-   **[Query a GraphQL schema from a component](../task/query-schema-from-component.md)**  
Access record data in a component by querying your scripted GraphQL schema.
-   **[GraphQL system properties](../reference/graphql-properties.md)**  
Configure GraphQL API framework behavior. For example, you can configure whether to allow introspective queries into your schema.

**Parent Topic:**[Additional integration resources](../../outbound-web-services/concept/additional-integration-resources.md)

