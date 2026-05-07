---
title: Natural language queries use cases and examples
description: View example use cases of some natural language queries used in Knowledge Graph and Enterprise Graph.
locale: en-US
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Exploring Knowledge Graph, Knowledge Graph, Enable AI experiences]
---

# Natural language queries use cases and examples

View example use cases of some natural language queries used in Knowledge Graph and Enterprise Graph.

Natural Language Query support in Knowledge Graph and Enterprise Graph allows users to interact with structured data using human-like language. This feature enhances the user experience by enabling more intuitive and flexible search capabilities within the ServiceNow platform.

## Supported Queries

Knowledge Graph and Enterprise Graph, understand and process queries that reference specific tables, columns, choice values, and conditions. It also handles queries involving system-generated identifiers \(sys-ids\), person names, dates, and contextual pronouns. Additionally, it supports aggregate and sorting queries, enabling users to perform simple statistical analysis and order results.

Here are some examples of the supported query types:

## Queries with specific reference

Queries having reference to all table names, column names, or choice values and conditions required are supported. Ensure that the conditions are specified exactly.

Here are some example queries and description of how they works in Knowledge Graph.

|Example|Description|
|-------|-----------|
|Show all stories which are ready for acceptance.|Stories refers to stories table and ready for acceptance refer to choice.|
|Find details of CI associated with P1 priority incident.|CI refers to look at configuration table and find those CI which are liked to incident with priority 1.|
|List all change requests with high risk.|Change request refers to change\_request table, risk refers to column, and high refers to choice.|
|Give details of CI named "AppleMacBookPro15".|CI refers to configuration item table and named refers to name column. The exact name of CI is also specified.|
|Show all incidents which are open.|Incident refers to the table; "in progress," "new," and "on hold" are choice value in state column options that correspond to open.|
|Share all case task assigned to "Dev – Knowledge Graph" group.|Case task is reference to table, group is a reference to assignment group column, and exact condition to look for is specified exactly.|
|Find Configuration items where manufacturer = Lenovo.|Configuration item is reference to cmdb\_ci table, manufacturer is column, and the exact name of manufacturer is specified.|
|Show me assets assigned to &lt;Person Name&gt;.|Assets refer to asset table, assigned to is column and person name is well specified.|
|Find details of CI associated with P1 priority incident.|CI refers to look at configuration table and P1 indicated the choice value of the priority column.|

## Queries with Sys-IDs, Person Names, and Date References

Queries having person names or references to dates such as yesterday, last month and contextual pronouns to the right person. Queries using system-generated identifiers \(sys-ids\) also works and can identify the table based on sys-ids.

Here are some example queries and description of how they works in Knowledge Graph.

|Example|Description|
|-------|-----------|
|Find details of request items linked to REQ0010144.|The request item refers to sc\_req\_item table and REQ sys-id refers to to sc\_request table.|
|Show details for INC0000044.|INC as sys-id refers to Incident table.|
|Get status for CHG000567.|CHG as sys-id refers to change request table and the status refers to the status column for that record.|
|Find department for person who requested RITM0010144.|The RITM sys-id refers to sc\_request\_item and department refers to department column from cmn\_department which is linked to the person who requested RITM0010144.|
|Find details of problem linked to INC0000047.|This query requests the details of problem record linked to incident INC0000047.|
|Show incidents assigned to Fred Luddy.|Finds Incident table with user in assigned to column.|
|List tasks created by Beth Anglin.|Task refers to task table and User name refers to created by column.|
|Find approvals pending for Joe’s reportees.|Find approvals from the sysapproval\_approver table for approval that are pending for the user's reportees.|
|Display incidents created more than 3 days ago and are not resolved yet.|Uses Incident table, created date, and state column to fetch the details.|
|Find certificates expiring in the next 30 days.|Certificates refer to table name, the next 30 days reference can be converted to date related condition and can be understood from the date reference in query.|
|Find case task created in last 30 minutes.|Case task refers to table, created refers to created column and time related condition can be understood from time reference in query.|
|What are the Problems open with my group?|Problem refers to problem table, group refers to column, ‘my’ reference will be resolved to the person asking the query.|
|Show my open incidents.|Uses Incident table and 'my' reference is the person asking the query.|
|What is the status of my request?|Uses request table and 'my' reference is the person asking the query.|
|What are their pending approvals?|Uses `sysapproval_approver` table and 'their' reference is the person who was referred to in previous turn of conversation.|

## Aggregate or Sorting Queries

These queries let users perform simple statistics and sorting directly in the Virtual Agent or Now Assist panel.

Here are some example queries and description of how they works in Knowledge Graph.

|Example|Description|
|-------|-----------|
|Count of incidents grouped by priority.|Counts the records in incident table grouped by priority column.|
|Count of problems grouped by stage.|Counts the records in problem table grouped by stage column.|
|Count case task assigned to group “Dev - Knowledge Graph ”.|Counts the records in case task table that are assigned to assignment group = Dev – Knowledge Graph.|
|List in progress hr cases by ordered by created date.|Lists the HR cases from HR cases table ordered by the created date field.|
|Show top 5 users by number of incident assigned to them.|Lists the top 5 user by number of incidents from the incident table assigned to them.|

## Unsupported Query Categories

Knowledge Graph does not support the following types of queries:

## Queries Missing References or with Misspellings

Queries that lack references to table, columns, choice values, or conditions, or contain misspellings, are not supported.

Here are a few examples of unsupported queries that will work if rephrased, as suggested below:

|Example|Rephrase to:|
|-------|------------|
|Find incidents about SAP login issue.|Find incidents where short description = SAP login issue.|
|Find CI where manufacturer is Orrange.\(Incorrect spelling\)|Find CI where manufacturer is Orange.|
|Find CI in SanDiego city.|Find CI in San Diego city.|
|Locate changes related to patch upgrade.|Locate change request where description contains patch upgrade.|
|Change request for Abel Tuter.|Change request assigned to Abel Tuter or Change request opened by Abel Tuter.|
|Problem by Mark Andrew.|Problem updated by Mark Andrew or Problem closed by Mark Andrew.|

## Queries on Journal Fields or Document IDs

Queries involving journal entries, document IDs, or glidelist references are not supported.

Here are a few examples of unsupported queries:

-   Show latest comments added to INC0000044.
-   What comments or work notes were added in the approval of change request CHG0000046.
-   Show tasks with ‘urgent’ in comments.
-   Find incident where Joe commented about email resolution steps.

## Keyword Queries or Queries Requiring KB Resolution

Keyword-based queries or those requiring resolution from the Knowledge Base \(KB\) are handled by AI Search, not the Knowledge Graph.

Here are a few examples of unsupported queries:

-   VPN issue
-   Password reset
-   Incident SLA
-   How can I request a windsurf license?
-   How to install global protect for PC?

## CMDB query support

Knowledge Graph supports CI Relationship \(Rel CI\) queries, enabling natural language questions about CMDB configuration item dependencies and infrastructure topology. For more details see [Configuration item relationships and Knowledge Graph](ci-relationships-knowledge-graph.md)

