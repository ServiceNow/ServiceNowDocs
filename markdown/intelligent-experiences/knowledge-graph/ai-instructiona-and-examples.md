---
title: Improving Natural Language Queries with Tag configuration
description: AI instructions add more business context to natural language queries. They guide users and promote responses that more closely align with their needs and expectations.
locale: en-US
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2026-03-17"
reading_time_minutes: 5
breadcrumb: [Tagging in Knowledge Graph Designer, Using Enterprise graph schema, Knowledge Graph, Enable AI experiences]
---

# Improving Natural Language Queries with Tag configuration

AI instructions add more business context to natural language queries. They guide users and promote responses that more closely align with their needs and expectations.

## AI instructions

AI instructions help clarify how the knowledge graph interprets user queries and accesses data. When a user submits a query, relevant instructions at all applicable levels like node, property, and edge are considered.

AI Instructions are persistent, declarative guidance applied at three levels:

-   Node \(entity/table\) level
-   Property \(column/attribute\) level
-   Edge \(relationship\) level

## The Always Include flag

The option to set an **Always include** flag enables users to indicate that a particular instruction should be considered unconditionally. This is useful for enforcing critical business filters, such as always excluding certain asset statuses unless requested otherwise.

Instructions:

-   Use **Always include** for business-critical filters that must apply regardless of user query phrasing.
-   Omit **Always include** for context-sensitive instructions that should only apply when relevant.
-   Verify that flagged instructions do not conflict with each other or produce duplicate results.

The following table shows common scenarios where AI instructions improve query accuracy and provide better business context.

<table id="ai-instructions-examples-table"><thead><tr><th>

No.

</th><th>

Instruction Pattern

</th><th>

Example Query

</th><th>

Behavior without AI instruction

</th><th>

Sample AI instructions

</th><th>

Behavior with AI instruction

</th></tr></thead><tbody><tr><td>

1

</td><td>

Preventing incorrect traversal paths

</td><td>

Which companies are located in New York?

</td><td>

When no instructions are added, the query goes from core\_company to cmn\_location table and filters on city field by default. But if your use case requires to query location from city field of core\_company table, you need to write an AI instruction to guide the system on the traversal path.

</td><td>

Table Instruction on `core_company` table: `For company-city queries, always use core_company.city directly. Do NOT traverse through cmn_location.` This instruction avoids the system from using cmn\_location path for city-based company queries.

</td><td>

When instruction is added, the query matches with city field in core\_company table and then filters city=New York and returns all matching companies.

</td></tr><tr><td>

2

</td><td>

Providing column specific context

</td><td>

Who hosted BBS0000013 brown bag session?

</td><td>

When there is no AI instruction, the system will return sys\_id without traversing to host\_s. You need to add an instruction on host\_s column to provide business context to use this column when query is about host.

</td><td>

Column Instruction on `host_s` of `x_snc_brown_bags_sessions` table: `Use s.host_s or :host_s relationship for the host of a brown bag session, NOT s.sys_created_by`

</td><td>

When instructions are added, the query correctly returns the name from host\_s column.

</td></tr><tr><td>

3

</td><td>

Providing column specific context

</td><td>

What is Kelsey Rodriguez's tenure in current role \(months\)?

</td><td>

When there is no AI instruction, the system may not give accurate result as it may provide incorrect information for tenure column. You need to add an instruction to guide the system to refer right column for such queries.

</td><td>

Column instruction on `time_in_current_role` column: `Prioritize this column when query contains 'tenure in current role'`

</td><td>

When instructions are added, the query correctly returns the time from `time_in_current_role` column.

</td></tr><tr><td>

4

</td><td>

Providing context on what to prioritize in case of similar tables

</td><td>

Give me name of Allison Hill's reports having goals pastdue &gt;0?

</td><td>

When there is no AI instruction, LLM will directly refer to “sys\_user” table to fetch user details instead of traversing to WDF table where this information is stored.

 We need to add an instruction to guide LLM to refer right table when there are similar tables.

</td><td>

Table instruction on WDF table – “x\_snc\_wdf\_user”

 *“Always give more priority to "* x\_snc\_wdf\_user”*over sys\_user and other glide tables”*

</td><td>

When instructions are added, the query correctly refers to WDF table and return results.

</td></tr><tr><td>

5

</td><td>

Providing context on what to prioritize in case of similar tables

</td><td>

What is your job title?

</td><td>

When there is no AI instruction, LLM will directly refer to “*sn\_hr\_core\_job*” table to fetch job details instead of traversing to*sn\_hr\_core\_profile"* table where this information is stored.

 We need to add an instruction to guide LLM to refer right table when there are similar tables.

</td><td>

Table instruction on table – “*sn\_hr\_core\_profile*”

 *“Always give more priority to "sn\_hr\_core\_profile" over “sn\_hr\_core\_job” when user specifically asks about job titles.*

</td><td>

When instructions are added, the query correctly refers to “sn\_hr\_core\_profile” table and return results.

</td></tr><tr><td>

6

</td><td>

Disambiguate among multiple similar and confusing choice values

</td><td>

What are the hardware models that are in normalized state?

</td><td>

When there is no AI instruction, LLM will refer to “normalized” choice value of “normalization status” column which could confuse LLM whether to use other choice values or not as “normalization status” field has 5 choice values \(normalized, manufacturer normalized, manually normalized, partially normalized, match not found\).

 We need to add instruction to guide LLM on which all choices to include in normalization status.

</td><td>

Column instruction on “Column- normalization status”:

 *“Always consider normalization status as normalized when choice values is any of the following choices: “normalized, manufacturer normalized, manually normalized”*

</td><td>

When instructions are added, the query correctly considers all 3 choices “normalized, manufacturer normalized, manually normalized” as normalized state and return results.

</td></tr></tbody>
</table>## Best practices for AI instructions

Follow these guidelines when creating AI instructions to verify optimal performance and accuracy:

-   Write clear, unambiguous, and actionable instructions tied to business logic. Always reference the correct tables \(nodes\), columns \(properties\), and relationships \(edges\). Use flags like Always include only when enforcing true default business behavior.
-   Avoid vague or contradictory instructions. Instructions that do not align with the underlying data model can confuse the system and lead to incorrect results. For example, an instruction like "Filter by manufacturer" without specifying the column or condition is ambiguous.
-   Use conditions to control when logic applies. Clearly state when an instruction should be applied \(for example, only when the user asks for host information\), rather than applying logic universally.
-   Keep instructions focused and generalized. Instructions should guide intent interpretation across similar queries, not solve a single one-off case.
-   Do not duplicate logic already handled elsewhere. Avoid restating filters or constraints that are already enforced through data filters to avoid conflict.

## Support for Synonyms, Data Filters and hidden columns

Synonyms:

Knowledge Graph supports configuring synonyms for tables, columns, edges, and reverse edges to enhance flexibility and user-friendliness. Synonyms enable users to define alternate names for these entities, accommodating different terminologies.

-   Each entity can have up to five synonyms.
-   Synonyms promote broad coverage for commonly used alternate terms.
-   Maintaining a manageable synonym set reduces ambiguity in query resolution.

Data Filters:

Data filters are applied deterministically as post-processing rules to refine query results. After initial Cypher generation, filters are systematically applied to promote consistency and reliability of outcomes.

-   Filters are applied after Cypher generation, not during.
-   Dynamic filters enable real-time adaptation based on user context.
-   Improves precision and relevance of returned data. Does not modify the core graph query.

Hidden columns:

Hidden columns cannot be queried and do not appear in the result.

For example: add Employee number as hidden columns for sys\_user table to hide the employee number from query results.

