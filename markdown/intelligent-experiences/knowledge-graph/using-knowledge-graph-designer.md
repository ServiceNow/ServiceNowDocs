---
title: Using Knowledge Graph Designer
description: Use Knowledge Graph Designer to create customized Knowledge Graph schemas that consist of nodes and edges.
locale: en-US
release: xanadu
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Knowledge Graph, Now Assist, Enable AI experiences]
---

# Using Knowledge Graph Designer

Use Knowledge Graph Designer to create customized Knowledge Graph schemas that consist of nodes and edges.

Knowledge Graph schemas are the customized Knowledge graphs that consist of nodes and edges.

Like tables, nodes also denote and store details about entities such as user, location, department. You can add nodes to the Knowledge Graph schema so that the system can reach out to all the relevant tables to fetch the data. You can also edit node properties such as data source, start node, end node, and connected nodes.

Knowledge Graph enables you to select the node columns that can be queried.

The relationship or connections between these nodes are referred to as edges. You can select and edit the connecting edges and available edges for each node.

With Knowledge Graph Designer, you can create, edit, duplicate, or delete a Knowledge Graph schema.

There’s an option to test a Knowledge Graph schema by generating and running a query.

## View Knowledge Graph schemas

By default,ServiceNow published Knowledge Graph schemas are available with the product. View the prebuilt schemas provided by ServiceNow, or the schemas created by your organization admin. There are currently two prebuilt schemas available that are read-only but can be cloned and edited:

1.  User profile schema
2.  HRSD schema \(available only if you have the Now Assist for HRSD plugin\)

## User profile schema

The User profile schema is the default schema that is used for passing the in-session user profile context to the OOTB integration with Virtual Agent for Context. This integration helps with personalized responses.

This schema details the attributes related to a user and comprises the following details:

<table id="table_qsd_3hx_42c"><thead><tr><th>

Schema

</th><th>

Attributes

</th></tr></thead><tbody><tr><td>

sys\_user

</td><td>

-   name
-   first name
-   last name
-   user name
-   employee number
-   email
-   business phone
-   mobile phone
-   title
-   preferred language
-   time format
-   date format
-   timezone
-   zip code
-   city
-   state

</td></tr><tr><td>

cmn\_location

</td><td>

-   city
-   state
-   country

</td></tr><tr><td>

cmn\_department

</td><td>

-   name
-   headcount

</td></tr><tr><td>

core\_company

</td><td>

name

</td></tr><tr><td>

manager

</td><td>

-   name
-   first name
-   last name
-   user name
-   employee number
-   email
-   business phone
-   mobile phone
-   title
-   preferred language
-   time format
-   date format
-   timezone
-   zip code
-   city
-   state

</td></tr><tr><td>

reportees

</td><td>

-   name
-   first name
-   last name
-   user name
-   employee number
-   email
-   business phone
-   mobile phone
-   title
-   preferred language
-   time format
-   date format
-   timezone
-   zip code
-   city
-   state

</td></tr><tr><td>

assets

</td><td>

-   display name
-   purchase date
-   retired date

</td></tr></tbody>
</table>