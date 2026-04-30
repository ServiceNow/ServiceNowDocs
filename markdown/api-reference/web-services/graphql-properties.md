---
title: GraphQL system properties
description: Configure GraphQL API framework behavior. For example, you can configure whether to allow introspective queries into your schema.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Query record data using the GraphQL API framework, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# GraphQL system properties

Configure GraphQL API framework behavior. For example, you can configure whether to allow introspective queries into your schema.

Navigate to **System Web Services** &gt; **GraphQL** &gt; **Properties** to change your GraphQL settings.

<table id="table_o42_dx1_dlb"><thead><tr><th>

Label

</th><th>

Details

</th><th>

System property

</th></tr></thead><tbody><tr><td>

Enable/Disable introspective queries for the GlideRecord Schema

</td><td>

Enabling this option allows the GraphQL Explorer to show the GlideRecord schema in the documentation pane and as auto-complete suggestions.

 -   Type: Boolean
-   Default: False

</td><td>

**glide.graphql.glide\_record\_schema.introspection\_enabled**

</td></tr><tr><td>

Enable/Disable debug logging for GraphQL

</td><td>

-   Type: Boolean
-   Default: False

</td><td>

**glide.graphql.debug**

</td></tr><tr><td>

Enable/Disable introspective queries for users to discover the supported GraphQL queries and types. Introspection request require graphql\_schema\_admin role.

</td><td>

Enabling this option allows the GraphQL Explorer to show the GraphQL schema in the documentation pane and as auto-complete suggestions.

 -   Type: Boolean
-   Default: False

</td><td>

**glide.graphql.introspection\_enabled**

</td></tr></tbody>
</table>**Parent Topic:**[Query record data using the GraphQL API framework](../concept/scripted-graph-ql.md)

