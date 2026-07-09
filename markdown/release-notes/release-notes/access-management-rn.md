---
title: Access Management release notes
description: The ServiceNow Access Management provides robust tools to manage security data on the ServiceNow platform. It includes access control lists \(ACLs\), security attributes, contextual security manager, data filtration, and many more controls. These controls provide granular control and improve security for managing data access. Access Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Access Management release notes

The ServiceNow® Access Management provides robust tools to manage security data on the ServiceNow platform. It includes access control lists \(ACLs\), security attributes, contextual security manager, data filtration, and many more controls. These controls provide granular control and improve security for managing data access. Access Management was enhanced and updated in the Yokohama release.

## Access Management highlights for the Yokohama release

-   Security Data Filters are a powerful new feature designed to restrict access to sensitive records based on roles or security attributes. This ensures only authorized users can view data, regardless of how the data is accessed.
-   Related Record Access allows enforcement of consistent access rules across related tables, ensuring that users only see records associated with the data they are authorized to access.

See [Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/access-control-rules.md) for more information.

## New in the Yokohama release

-   **[Security data filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/security-data-filters.md)**

    Security data Filters enable you to control who can access sensitive data by restricting access to authorized users, regardless of how the data is accessed. Security data filters are applied before query execution, ensuring restricted data never leaves the database and prevents data leakage at the query level. Filters integrate into queries for GlideRecordSecure, GlideRecordSandbox, and GlideAggregateSandbox by default.

-   **[Related record access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/related-record-access.md)**

    Related record access integrated into the ACL framework enhances access management by enabling administrators to enforce specific ACLs for related tables. This ensures users can only access records in related tables, such as costs, estimations, or tasks, based on their permissions for the parent table, like projects or cases. Combined with broader ACL capabilities, Related record access ensures consistent, granular, and enforceable


## Activation information

Access Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-security-rn-landing.md)

