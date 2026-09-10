---
title: Live Connect configuration on your ServiceNow instance
description: Complete the three-step configuration that's required to enable Live Connect access.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/configure-sql-api-overview.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Live Connect configuration on your ServiceNow instance

Complete the three-step configuration that's required to enable Live Connect access.

Configuring Live Connect on your ServiceNow instance enables you to integrate your ServiceNow data with third-party BI tools and analytics platforms. You can connect to platforms such as Pyramid Analytics, Tableau, Power BI, DB Visualizer, or custom ODBC/JDBC clients to enhance your reporting and data analysis capabilities.

## Before you begin

Confirm the following prerequisites are in place before starting:

-   The Live Connect plugin is installed on your instance.
-   You have consulted your network team to identify the IP address range for your ODBC/JDBC client machines.
-   You have identified which ServiceNow tables must be accessible via the Live Connect.

Role required: admin

## Configuration steps

Complete the following procedures to configure Live Connect access on your instance:

1.  [Assign roles and create service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-service-account.md)
2.  [Create Access Control Lists \(ACLs\) for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-acls-sql-api.md)
3.  [Create IP filter criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-ip-filter-criteria.md)

## After configuration

After completing all the procedures, your user account \(personal or service account\) can connect to your ServiceNow instance via ODBC or JDBC. You can then query tables for which access has been granted.

Additional considerations:

-   You can assign roles to personal user accounts or create dedicated service accounts with different roles and access control settings to support different integrations or teams.

    **Note:** Service accounts are recommended for production reports and dashboards because they promote continuity. Personal accounts will break if the user loses access or leaves the organization.

-   Access is not granted globally. A user account can query a table only if it has explicit read access. Access is granted through table-level ACLs \(`egress_sql` and `read`\) or through a role with read permissions.
-   Live Connect supports both individual user accounts \(via OAuth\) and service accounts.
-   Non-interactive \(machine\) service accounts can't complete MFA challenges. If you're using non-interactive service accounts, turn off MFA for those accounts. Personal accounts using OAuth aren't subject to this limitation.

-   **[Assign roles and create service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-service-account.md)**  
Assign the **sn\_odbc\_rest\_access** or **sn\_jdbc\_rest\_access** role to users who need Live Connect access. You can assign these roles to personal user accounts or create dedicated non-interactive \(Machine\) service accounts.
-   **[Create Access Control Lists \(ACLs\) for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-acls-sql-api.md)**  
Configure table-level access control using the egress\_sql and read operations to grant user accounts \(personal and service accounts\) query access to specific tables through Live Connect.
-   **[Create IP filter criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-ip-filter-criteria.md)**  
Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the Live Connect ODBC/JDBC driver.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configuring-sql-api.md)

