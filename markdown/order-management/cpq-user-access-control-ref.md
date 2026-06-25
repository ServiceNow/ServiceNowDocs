---
title: User Access Control reference
description: Control Admin access levels using CSV imports. Assign NONE, READ, EDIT, or ADMIN permissions to specific areas.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-user-access-control-ref.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ admin settings, CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# User Access Control reference

Control Admin access levels using CSV imports. Assign NONE, READ, EDIT, or ADMIN permissions to specific areas.

**Note:** The User Access utility is enabled via a support request. Open a ticket by using the [ServiceNow Support portal](https://support.servicenow.com). For step-by-step instructions, see [Create a case on Now Support for CPQ \(Logik.ai\) Customers](https://support.servicenow.com/kb?sys_kb_id=d67d3e71475d7a90f64de825126d4326&id=kb_article_view).

## Access levels

-   NONE
-   READ
-   EDIT
-   ADMIN

## Access areas

-   END\_USER
-   CONFIG

    Users with ADMIN can use the Matrix Loader.

-   TRANSACTION

    Users with ADMIN can use the Matrix Loader, including product filters and the catalog enrichment script.

-   MANAGED\_TABLES
-   TABLE

    Applies permissions for an individual table listed in addition to any MANAGED\_TABLES access level. Examples:

    -   MANAGED\_TABLES: NONE + TABLE “myTable” Edit = ability to edit “myTable” only
    -   MANAGED\_TABLES: READ + TABLE “myTable” Edit = ability to read all tables and edit "myTable"
-   DEPLOY
    -   Applies all blueprint, transaction, product catalog enrichment, and product filter deploys
    -   Roles are either NONE or ADMIN
-   UTILITIES
    -   Logs, user access, runtime clients, admin API keys, external connections, settings, webhooks, connections
    -   Products \(for Ecommerce tenants\)
-   Access to specific resources

    Tables: Users can be limited to specific tables they have access to. This is done via CSV as well as API.


## User roles

-   END\_USER: This is the only permission for the runtime
-   CONFIG\_NONE / CONFIG\_READ / CONFIG\_EDIT / CONFIG\_ADMIN
    -   READ correlates to GET endpoints
    -   EDIT additionally correlates to POST PUT PATCH DELETE endpoints
    -   ADMIN additionally correlates to Matrix Loader endpoints
-   TRANSACTION\_NONE / TRANSACTION\_READ / TRANSACTION\_EDIT / TRANSACTION\_ADMIN
    -   READ correlates to GET endpoints
    -   EDIT additionally correlates to POST PUT PATCH DELETE endpoints
    -   ADMIN additionally correlates to Matrix Loader endpoints
-   MANAGED\_TABLES\_NONE / MANAGED\_TABLES\_READ / MANAGED\_TABLES\_EDIT / MANAGED\_TABLES\_ADMIN
    -   READ correlates to GET endpoints
    -   EDIT additionally correlates to POST PUT PATCH DELETE endpoints
    -   ADMIN additionally correlates to Matrix Loader endpoints
-   DEPLOY\_NONE / DEPLOY\_ADMIN \(no EDIT or READ\): ADMIN everything deployment related, including Product Filter Rules and Product Catalog Enrichment Deployments
-   UTILITIES\_NONE / UTILITIES\_READ / UTILITIES\_ADMIN \(no EDIT\)
    -   READ correlates to GET endpoints
    -   ADMIN correlates to everything else

**Related topics**  


[Using CPQ user access management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-using-uam.md)

[User access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

