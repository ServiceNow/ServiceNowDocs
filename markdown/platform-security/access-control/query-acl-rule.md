---
title: Query ACLs
description: Query ACLs allow you to define more granular access control by explicitly defining who can query the data.
locale: en-US
release: zurich
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure an ACL rule, Access Control List Rules, Access Management]
---

# Query ACLs

Query ACLs allow you to define more granular access control by explicitly defining who can query the data.

## What is a query ACL

A query ACLs have their operation set to either `query_range` or `query_match`. Query ACLs allow for more specific control of user queries, restricting or enabling access based on their setup. Query ACLs are powerful tools against blind query attacks, where an attacker blindly queries the data to extract information from results, even when they can't see the values.

## When to use a query ACL

Wherever a column contains sensitive values, and allows partial/conditional access to data a query ACL should be considered and implemented as necessary based on the sensitivity of the data. Wherever there is a partial/conditional access to rows and their columns in tables, especially where that access is not enforced by data filters, query ACLs should be implemented as necessary based on the sensitivity of the data.

**Note:** Consider query ACLs when some users have access to some rows or columns and not others .

## Payroll query control

I can see one row in payroll table with my salary, but there is no reason for me to be able to issue range queries to query users with a salary contained within 2 boundaries. A `query_range` ACL on salary would prevent me from issuing that query.

## HR query control

I can see all hr\_profiles, but can only see SSN for myself. I have no business querying SSN, and query ACLs should prevent me from running queries against SSN of other hr profiles to try to extract SSN mappings.

## Query ACL behavior

Query ACLs use `query_match` and `query_range` operations for secure and granular table querying behavior. Their behaviors are described below:

-   **`query_match`**

    `query_match` is composed of: EQUALS, NOT\_EQUALS, IN, NOT\_IN, SAMEAS, NSAMEAS, ANYTHING, ISEMPTYSTRING, ISEMPTY, ISNOTEMPTY, ISNULL, ISNOTNULL. `query_match` is made of the "safe operators", in a sense that they are built to fetch specific record\(s\), and can't be exploited to return others.

<table id="table_c3k_1zl_zbc"><thead><tr><th>

Evaluation outcome

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Pass

</td><td>

User can submit match queries

</td></tr><tr><td>

Fail

</td><td>

User will not be able to submit match queries:-   EQUALS
-   NOT\_EQUALS
-   IN
-   NOT\_IN
-   SAMEAS
-   NSAMEAS
-   ANYTHING
-   ISEMPTYSTRING
-   ISEMPTY
-   ISNOTEMPTY
-   ISNULL
-   ISNOTNULL


</td></tr></tbody>
</table>-   **`query_range`**

    `query_range` is composed of all the others \(STARTS\_WITH, CONTAINS, &gt;=, &lt;= etc\) which are more dangerous as they allow users to query for more records by adjusting the boundary values.

    |Evaluation outcome|Result|
    |------------------|------|
    |Pass|User can submit range queries and sorting is unrestricted|
    |Fail|The user will not be able to submit range queries with \(STARTS\_WITH, CONTAINS, &gt;=, &lt;=, etc. Sorting by column is restricted|


**Important:**

Query ACLs \(both query\_match and query\_range\) default to a star.star ACL that delegates to read access. This means, where ACLs are enforced on queries, if no query ACL was created then read access to the column is evaluated ; if query ACLs are defined then they override the default behavior.

