---
title: Query ACLs
description: Query ACLs enable more granular access control by defining who can query the data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/access-control/query-acl-rule.html
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Configure an ACL, Access Control Lists \(ACLs\), Access Management]
---

# Query ACLs

Query ACLs enable more granular access control by defining who can query the data.

## What is a query ACL

A query ACL is a record-type ACL that has its operation set to either `query_range` or `query_match`. Query ACLs allow for more specific control of user queries, restricting or enabling access based on their setup. Query ACLs restrict who can query the data, preventing attackers from extracting information from query results even when they can't see the values.

## When to use a query ACL

Wherever a column contains sensitive values, and allows partial or conditional access to data, a query ACL should be considered and implemented as necessary based on the sensitivity of the data. Wherever there is a partial/conditional access to rows and their columns in tables, especially where that access is not enforced by data filters, query ACLs should be implemented as necessary based on the sensitivity of the data.

**Note:** Consider query ACLs when some users have access to some rows or columns and not others.

## Payroll query control

A user can see one row in the payroll table for their own salary, but has no reason to issue range queries for users with a salary within two boundaries. A `query_range` ACL on salary would prevent them from issuing that query.

## HR query control

A user can see all hr\_profiles, but can only see their own SSN. Query ACLs prevent users from running queries against the SSN of other hr profiles to extract SSN mappings.

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

Users can't submit match queries:-   EQUALS
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

    `query_range` is composed of all the others \(STARTS\_WITH, CONTAINS, &gt;=, &lt;=, and similar operators\) which are more dangerous as they allow users to query for more records by adjusting the boundary values.

    |Evaluation outcome|Result|
    |------------------|------|
    |Pass|User can submit range queries and sorting is unrestricted|
    |Fail|Users cannot submit range queries with STARTS\_WITH, CONTAINS, &gt;=, &lt;=, and similar operators. Sorting by column is restricted.|


**Warning:**

Query ACLs \(both query\_match and query\_range\) default to a star.star ACL that delegates to read access. This means, where ACLs are enforced on queries, if no query ACL was created then read access to the column is evaluated ; if query ACLs are defined then they override the default behavior.

