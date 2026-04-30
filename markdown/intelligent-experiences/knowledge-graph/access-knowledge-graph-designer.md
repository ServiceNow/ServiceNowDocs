---
title: Access Knowledge Graph Schemas
description: Use Knowledge Graph Designer to create, edit, and manage Knowledge Graph schemas.
locale: en-US
release: xanadu
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Knowledge Graph, Knowledge Graph, Now Assist, Enable AI experiences]
---

# Access Knowledge Graph Schemas

Use Knowledge Graph Designer to create, edit, and manage Knowledge Graph schemas.

## Before you begin

Role required: kg\_admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Graph** &gt; **Knowledge Graph Designer**.

    The Knowledge Graph Designer landing page displays a list of all the Knowledge Graph schemas available for users.

    ServiceNow some provides prebuilt schema that are non-editable. Currently, the following prebuilt schemas are available:

    -   User graph schema: Used to provide logged in user's details to Virtual Agent for personalised response. The profile section is used by AI agents for additional user context.

        The details of the user context passed by default are as below:

<table id="table_qsd_3hx_42c"><thead><tr><th>

Entry

</th><th>

Attributes

</th></tr></thead><tbody><tr><td>

Grouped as Profile

</td><td>

sys\_user table's columns:

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
-   Time format
-   date format
-   Time zone
 cmn\_location

-   city
-   state
-   country
 cmn\_department

-   name
-   headcount
 core\_company: name

</td></tr><tr><td>

Grouped as manager

</td><td>

sys\_user table's columns:

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
-   Time format
-   date format
-   Time zone
-   zip code
-   city
-   state


</td></tr><tr><td>

Grouped as reportees

</td><td>

sys\_user table's columns:

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
-   Time format
-   date format
-   Time zone
-   zip code
-   city
-   state


</td></tr><tr><td>

Grouped as assets

</td><td>

alm\_asset table's columns:

-   display name
-   purchase date
-   retired date


</td></tr></tbody>
</table>    -   NLQ graph Scheme: Helps requesters with personalized responses on people queries and Natural Language queries. Also supports people citation card. By default the user NLQ graph is connected which is used for people queries but you also have sample graph schema for other employee queries. For more details see [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2069778).
    ![Knowledge Graph Designer landing page.](../Images/knowledge-graph-landing-page.png)

    You can also create a Knowledge Graph schema from the landing page.


