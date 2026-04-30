---
title: Create a GraphQL schema
description: Create a GraphQL schema to make data available to GraphQL queries.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Querying data using GraphQL, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create a GraphQL schema

Create a GraphQL schema to make data available to GraphQL queries.

## Before you begin

Role required: graphql\_schema\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **GraphQL** &gt; **GraphQL APIs**.

2.  Select **New**.

3.  Complete these fields.

<table id="table_d5n_3vc_qkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the schema.

</td></tr><tr><td>

Schema namespace

</td><td>

Must be unique within the name of the application.

</td></tr><tr><td>

Application

</td><td>

Read-only application that the schema is a part of.

</td></tr><tr><td>

Application namespace

</td><td>

Read-only. Works with the **Schema namespace** to avoid conflict with schemas with the same name.

</td></tr><tr><td>

Active

</td><td>

Option to turn the GraphQL schema on or off.

</td></tr><tr><td>

Schema

</td><td>

Schema definition that adheres to the GraphQL SDL format. Must be valid GraphQL syntax. Otherwise, error messages appear on save to indicate the syntax problem.**Note:** The following GraphQL features aren’t supported:

-   Subscription operations
-   Custom scalar types


</td></tr></tbody>
</table>    You can use this directive in your schema:

    `@source`: Maps a GraphQL field to the value of a property of the parent object. If the field has a separate resolver script, the system uses the record that it resolves to instead of the parent object.

    This example defines an Incident object type in the schema and uses a resolver script to map the type to a GlideRecord from the Incident table. Using the `@source` directive maps the fields within the Incident type to the `value` or `display_value` in the Incident GlideRecord.

    ```
    type Incident {
        id: String @source(value: "sys_id.value")
        active: Boolean @source(value: "active.display_value")
        state: String @source(value: "state.display_value")    
        priority: String @source(value: "priority.display_value")
        severity: String
        description: DisplayableString
        resolvedBy: User @source(value: "resolved_by.value")
        openedBy: User @source(value: "opened_by.value")
        child_incidents: String
        opened_at: String
        resolved_at: String
        closed_at: String
        work_notes: String    
        comments: String @source(value: "comments.display_value")
        parent_incident: String
    }
    ```

4.  In the **Security** section, fill in the fields.

<table id="table_ql2_rlb_5kb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requires authentication

</td><td>

Select this option to require authentication to access the schema. Clearing this option makes the schema available publicly.

</td></tr><tr><td>

Requires ACL authorization

</td><td>

Select this option to require ACL authorization of the entire API. In the **ACLs** field, select ACLs with the GraphQL type.To use ACL authorization for specific paths only, leave this option cleared and specify the level to evaluate ACLs against in the **Path ACL depth** field.

</td></tr><tr><td>

Requires SNC internal

</td><td>

Select this option if the schema requires the SNC internal role. This option appears only if the Explicit Roles plugin \(com.glide.explicit\_roles\) is enabled.

</td></tr><tr><td>

Path ACL depth

</td><td>

Specify the level of the GraphQL API to which to apply ACLs. Setting the path depth to 3 or lower uses fewer resources and helps with returning query responses.To specify the ACLs to use for the path, you must create an ACL with the GraphQL type and add the exact API path beginning with the schema namespace in the **Name** field. For example: `/<planet>/<findAll>/<name>`. Wildcards aren’t supported. For more information, see [Configure an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Note:** The **ACLs** field applies to the entire API and is independent of the ACLs applied to specific paths.

</td></tr><tr><td>

ACLs

</td><td>

Select ACLs with the GraphQL type to check incoming queries against. The ACLs you select apply to the entire API. This option appears only if **Requires ACL authorization** is selected.

</td></tr></tbody>
</table>    **Note:** The API returns clear error messages to users who don’t have access to a schema, or who aren’t authenticated when the API requires authentication to access.

5.  Save the form.

6.  Create a resolver script to define what value the schema returns when a component queries a field.

    If you don't define a resolver for a field, the query returns any matching field value from the parent object type. For example, suppose you have an Incident object type in your schema with a worknotes field. The Incident object type has a resolver that maps to a GlideRecord from the Incident table. If you don’t create a resolver mapping for the worknotes field, the system searches the parent object's data source, which is the GlideRecord from the Incident table, for a worknotes field and assigns the associated value.

    1.  Select the GraphQL Scripted Resolvers tab and select **New**.

    2.  Complete the form.

<table id="table_lzp_tpd_qkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the resolver.

</td></tr><tr><td>

Schema

</td><td>

Read-only schema namespace.

</td></tr><tr><td>

Application

</td><td>

Read-only application that the schema is a part of.

</td></tr><tr><td>

Script

</td><td>

Define the value returned when the field is queried. Functions available on the global env object: -   getArguments\(\): Returns the arguments of the previous field.
-   getSource\(\): Returns the parent object.
 This script has access to GlideRecord.

</td></tr></tbody>
</table>        This example returns a record from the User table when the associated field is queried:

        ```
        (function process(/*ResolverEnvironment*/ env) {
        
            var userid = env.getArguments().id != null ? env.getArguments().id : env.getSource();
            var now_GR = new GlideRecord('sys_user');
            gr.addQuery('sys_id', userid);
            gr.queryO;
            return gr;
        
        })(env);
        ```

    3.  Select **Submit**.

7.  Define the type resolvers for your schema to resolve interfaces and unions into concrete types.

    1.  Select the GraphQL Scripted Type Resolvers tab and select **New**.

    2.  Complete the form.

<table id="table_tg2_r4d_qkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schema

</td><td>

Read-only schema namespace.

</td></tr><tr><td>

Type

</td><td>

The interface or union type defined in the schema.

</td></tr><tr><td>

Application

</td><td>

Read-only application that the schema is a part of.

</td></tr><tr><td>

Script

</td><td>

Define the value returned for union and interface types. Functions available on the global env object: -   getArguments\(\): Returns the arguments of the previous field.
-   getObject\(\): Returns the parent object.
-   getTypeName\(\): Returns the name of the interface or union type.
 This script has access to GlideRecord.

</td></tr></tbody>
</table>    3.  Select **Submit**.

8.  Map the resolver and type resolver records to fields in the schema.

    This mapping tells the system what value to return when a component queries a field.

    1.  Select the GraphQL Scripted Resolver Mappings tab and select **New**.

    2.  Complete the form.

        |Field|Description|
        |-----|-----------|
        |Path|Path to the field in the schema you want to map.|
        |Resolver|Resolver to use to define the data returned by the field.|
        |Application|Read-only application that the schema is a part of.|
        |Schema|Read-only schema namespace.|

    3.  Select **Submit**.


**Parent Topic:**[Query record data using the GraphQL API framework](../concept/scripted-graph-ql.md)

