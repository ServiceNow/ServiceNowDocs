---
title: Intro to admin API keys
description: You can use admin API calls to access Admin functionality without using the Admin UI interface and a browser.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 2
breadcrumb: [API overview and resources, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Intro to admin API keys

You can use admin API calls to access Admin functionality without using the Admin UI interface and a browser.

ServiceNow CPQ provides admin API keys that you can use to access admin functionality via API calls instead of using a browser and the ServiceNow CPQ Admin interface.

For an introduction to ServiceNow CPQ admin API keys, view the following video:

[Admin API keys](https://www.youtube.com/watch?v=8BwQgKw4Dak)

## Admin API keys page

To get to the Admin API Keys page in ServiceNow CPQ, click the arrow to expand the Utilities section in ServiceNow CPQ Admin. The Admin API Keys tab appears in the menu.

![Admin keys](../images/cpq-apis-admin-keys-page.png)

## Add a new admin API key

To add a new admin API key, click **New** at the top of the screen.

![Add Admin Key](../images/cpq-apis-admin-new-key.png)

All parameters are required.

1.  Name: the name of the admin API key
2.  User ID
3.  Expiration Date: the expiration date of the key
4.  Permissions: the permissions assigned to the key

Choose the permissions that fit your use case before clicking **Save**.

## Admin API key permissions

![API key Permissions](../images/cpq-apis-admin-permissions.png)

1.  Read \(required, default\): read-only access, typically for GET requests
2.  Edit: create, read, update, and delete access for most objects, including fields and rules
3.  Deploy: allows the deployment of blueprints and access to deployment history
4.  Bulk: allows importing and exporting data, such as managed tables, to and from ServiceNow CPQ
5.  Admin: full permissions to all Admin functionality
6.  End User Data: access to end user data APIs

When you are finished assigning permissions, click **Save**. The dialog box updates to show the new admin API key.

![Add API key](../images/cpq-apis-admin-new.png)

1.  View the admin API key
2.  Copy the key to the clipboard
3.  Close the dialog box

**Important:** You can copy an admin API key only when it is created. Make sure to copy and store the key.

## Accessing admin APIs by using API keys

To use an admin API key in API requests, use the API key with Bearer Token authentication.

-   Header: Authorization Header
-   Key: authorization
-   Value: Bearer &lt;Admin API key&gt;

Example header:

`authorization: Bearer Qda_UdoiYipb15Le11En8axEuN71FA6Vt_cw`

When you use an admin API key, you use different endpoints to access the admin APIs.

-   For general Admin endpoints \(`/a/Admin/…`\) the endpoint to use is \(`/api/Admin/…`\).

    For example \(retrieving a list of rules\):

    -   API call in Admin UI: `/a/Admin/v3/rules?page=0&size=100&sort=modified%2CDESC`
    -   API call using Admin Keys: `/api/Admin/v3/rules?page=0&size=100&sort=modified%2CDESC`
-   For managed table endpoints \(`/a/managed_tables/…`\) the endpoint to use when accessing with an API key is \(`/api/managedTables/…`\)

    For example \(retrieving the schema of a managed table\):

    -   API call in Admin UI: `/a/managed_tables/v1/managedTables/{tableName}/metadata`
    -   API call using Admin Keys: `/api/managedTables/v1/managedTables/{tableName}/metadata`

**Related topics**  


[https://logikio.atlassian.net/wiki/spaces/CS/pages/1614479620/Setting+up+a+Google+IdP+JWT+Token+for+Headless+Admin+API+Authentication](https://logikio.atlassian.net/wiki/spaces/CS/pages/1614479620/Setting+up+a+Google+IdP+JWT+Token+for+Headless+Admin+API+Authentication)

[Admin APIs: Authentication using a Salesforce-connected app](admin-apis-authentication-via-salesforce-connected-app.md)

