---
title: Admin APIs: Managed tables
description: Legacy information about APIs that interact with managed tables
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API overview and resources, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Admin APIs: Managed tables

Legacy information about APIs that interact with managed tables

We highly recommend leveraging [Admin API keys](cpq-admin-api-keys.md) to interact with the CPQ APIs for managed tables. Bulk-level permissions are necessary for your admin API key to authenticate calls related to managed tables. For more information on these APIs, see the full API documentation:

[CPQ API documentation](https://api-docs.logik.io/#introduction)

The following Postman collection demonstrates how to retrieve and manipulate table metadata and data using the deprecated JWT authorization noted below:

[Postman Collection\_Logik managed tables APIs](https://drive.google.com/file/d/1V4c1SbBsIDwlJ0bZ7UPF2tO1-_R2Xegk/view?usp=share_link)

The following operations are demonstrated in this collection:

-   Retrieving a list of all tables defined in an environment
-   Manipulating table metadata \(schema\)
    -   Retrieving table metadata
    -   Uploading table metadata
    -   Adding table metadata
    -   Deleting table metadata
-   Manipulating table data
    -   Retrieving table data
    -   Adding a table data row
    -   Updating a table data row
    -   Deleting a table data row
    -   Uploading table data via CSV
    -   Exporting table data to CSV
    -   Getting the status of an export job
    -   Replacing a table

All calls leverage JWT authorization. The bearer token is stored in the global variable `{{logik_admin_BearerToken}}`. For instructions for generating JWT, see:

[Admin APIs: Authentication using a Salesforce-connected app](admin-apis-authentication-via-salesforce-connected-app.md)

