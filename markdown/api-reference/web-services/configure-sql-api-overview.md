---
title: Configure SQL API plugin on your ServiceNow instance
description: Overview of the three-step configuration process required to enable SQL API access including prerequisites and expected outcomes.
locale: en-us
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure SQL API plugin on your ServiceNow instance

Overview of the three-step configuration process required to enable SQL API access including prerequisites and expected outcomes.

Configuring the SQL API on your instance enables you to integrate your ServiceNow data with external BI tools and analytics platforms such as Power BI, DB Visualizer, or custom ODBC/JDBC clients, enhancing your reporting and data analysis capabilities.

This configuration requires a system administrator to complete three sequential procedures. Complete each procedure before proceeding to the next.

## Before you begin

Verify the following prerequisites are in place before starting:

-   You have system administrator access to your ServiceNow instance.
-   The SQL API plugin is installed on your instance.
-   You consulted your network team to identify the IP address range for your ODBC/JDBC client machines.
-   You identified which ServiceNow tables must be accessible via the SQL API.

## Configuration steps

Complete the following three procedures to configure SQL API access on your instance:

|Step|Procedure|Description|
|----|---------|-----------|
|1|[Create a Service Account and assign Roles](create-service-account.md)|Create a dedicated non-interactive \(Machine\) Service Account in User Administration. Assign it the `sn_odbc_rest_access` or `sn_jdbc_rest_access` role. You can create multiple Service Accounts, each with different roles and security restrictions, to support different integrations or teams. By default, the SQL API checks access at the table, row, and field level for every query. You can turn them off by assigning the `sn_sql_api_privileged_mode` role to the service account.|
|2|[Create Access Control Lists \(ACLs\) for SQL API](create-acls-sql-api.md)|Configure table-level access using the `egress_sql` operation. For each table the Service Account needs to query, create two ACLs. Create one for `egress_sql` \(SQL API data export\) and one for `read` \(record-level access\). Repeat this for each table and each role combination.|
|3|[Create IP filter criteria](create-ip-filter-criteria.md)|Define which IP addresses or IP ranges are permitted to connect via the ODBC/JDBC driver. By default, all incoming IPs are blocked. Configure the SQL API Authentication Policy with an IP filter and policy condition. This allows access only from trusted client machines.|

## What to expect

After completing all three procedures, your Service Account will be able to connect to your ServiceNow instance via ODBC or JDBC and query the tables for which access has been granted.

Keep the following in mind:

-   Multiple Service Accounts: You can create multiple Service Accounts with different roles and access control settings. This allows different BI tools or teams to have separate, independently managed access.
-   Table-level access via egress\_sql: Access is not granted globally. Each table requires its own `egress_sql` and `read` ACL. A Service Account can only query tables for which both ACLs are explicitly configured.
-   Use Service Accounts: Personal user accounts are not supported. Reports and dashboards will break if the associated user loses access or leaves the organization. Service Accounts promote continuity.
-   Turn off MFA: Non-interactive \(Machine\) users cannot complete MFA challenges. Confirm that MFA is turned off for all SQL API Service Accounts.

-   **[Create a Service Account and assign Roles](create-service-account.md)**  
Create a dedicated non-interactive Service Account in User Administration and assign the appropriate SQL API access role to enable secure, programmatic access for BI tools and analytics platforms.
-   **[Create Access Control Lists \(ACLs\) for SQL API](create-acls-sql-api.md)**  
Configure table-level access control using the egress\_sql and read operations to grant Service Accounts query access to specific tables through the SQL API.
-   **[Create IP filter criteria](create-ip-filter-criteria.md)**  
Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the SQL API ODBC/JDBC driver. By default, all incoming IPs are blocked until you configure the SQL API Authentication Policy with an IP filter and policy condition to allow access only from trusted client machines.

**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)

