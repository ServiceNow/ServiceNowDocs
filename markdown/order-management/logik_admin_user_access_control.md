---
title: CPQ: User Access Control
description: View access types, access areas, and user roles that can be managed via the User Access utility.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ admin settings, CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# CPQ: User Access Control

View access types, access areas, and user roles that can be managed via the User Access utility.

**Note:** This feature must be enabled by support request.

Use the User Access utility to manage access to CPQ Admin. Admin users have full admin access unless their access level is modified via CSV import.

For basic user access in CPQ, see [User access](please_share_your_feedback_on_admin_assist_responses.md).

## Access levels

-   NONE
-   READ
-   EDIT
-   ADMIN

## Access areas

-   END\_USER
-   CONFIG

    Users with ADMIN can use the Matrix Loader, including product filters and the catalog enrichment script MANAGED\_TABLES.

-   TRANSACTION

    Users with ADMIN can use the Matrix Loader.

-   MANAGED\_TABLES
-   TABLE

    Applies permissions for an individual table listed in addition to any MANAGED\_TABLES access level. Examples:

    -   EX: MANAGED\_TABLES: NONE + TABLE “myTable” Edit = ability to edit “myTable” only
    -   EX: MANAGED\_TABLES: READ + TABLE “myTable” Edit = ability to read all tables and edit "myTable"
-   DEPLOY
    -   Applies all blueprint, transaction, product catalog enrichment, and product filter deploys
    -   Roles are either NONE or ADMIN UTILITIES
-   UTILITIES
    -   Logs, user access, runtime clients, admin API keys, external connections, settings, webhooks, connections
    -   Products \(for Ecommerce tenants\)

## Tables

User access can be limited to specific tables via CSV or API.

**Note:** These are additive permissions with the overall tables permission set, so if the user has read access for all tables, the individual permission of NONE would have no effect.

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

## Modifying access controls

Admin users can modify access via CSV upload \(Admin &gt; Utilities &gt; User Access\). The User Access list shows existing users.

![Admin: User Access Control](../images/cpq-user-access-control-list.png)

Steps:

1.  Hover a tooltip to view a userʼs access.

    ![Admin: User Access Control](../images/cpq-user-access-control-list-tooltip.png)

2.  Create a CSV file to add users, make changes to users, or delete users. \(See below for sample CSV files.\)

    ![Admin: User Access Control](../images/cpq-user-access-control-list-sample-csv.png)

3.  Import the CSV file.

    ![Admin: User Access Control](../images/cpq-user-access-control-csv-import.png)

    You will receive a message confirming success or failure.

    ![Admin: User Access Control](../images/cpq-user-access-control-csv-import-status.png)


Changes to user list are now made.

![Admin: User Access Control](../images/cpq-user-access-control-list-updated.png)

## Sample CSVs

Default all-access admin CSV:

```
name,userName,area,access,action
User,email@example.com,DEPLOY,ADMIN,
User,email@example.com,UTILITIES,ADMIN,
User,email@example.com,CONFIG,ADMIN,
User,email@example.com,TRANSACTION,ADMIN,
User,email@example.com,MANAGED_TABLES,ADMIN, 
```

Example complex-access CSV:

```
name,userName,area,access,action
User 1,user.one@example.com,DEPLOY,ADMIN
User 2,user.two@example.com,UTILITIES,ADMIN
User 2,user.two@example.com,CONFIG,ADMIN
User 2,user.two@example.com,TRANSACTION,ADMIN
User 3,user.three@example.com,END_USER,END_USER
User 4,user.four@example.com,END_USER,END_USER,DELETE
User 5,user.five@example.com,CONFIG,ADMIN
User 5,user.five@example.com,TRANSACTIONS,ADMIN
User 5,user.five@example.com,MANAGED_TABLES,READ
User 5,user.five@example.com,UTILITIES,ADMIN
User 5,user.five@example.com,DEPLOY,ADMIN
User 6,user.six@example.com,CONFIG,ADMIN 
```

CSV adding user to the table "sampleTable":

```
name,userName,area,access,variableName,action
John Smith,john.smith@example.com,CONFIG,ADMIN,,UPSERT
John Smith,john.smith@example.com,TRANSACTIONS,ADMIN,,UPSERT
John Smith,john.smith@example.com,TABLE,ADMIN,sampleTableName,UPSERT
Jane Doe,jane.doe@example.com,MANAGED_TABLES,READ,,DELETE
Jane Doe,jane.doe@example.com,UTILITIES,,NONE
```

