---
title: Configure REST API Auth scope
description: Link the OAuth entity with an auth scope to manage the token to access the REST APIs that are linked with the auth scope.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [REST API Auth Scope, REST API access policies, API access policy, Authentication, Access Management]
---

# Configure REST API Auth scope

Link the OAuth entity with an auth scope to manage the token to access the REST APIs that are linked with the auth scope.

## Before you begin

Install the following plugins:

-   OAuth 2.0
-   REST API Provider
-   Authentication scope
-   REST API Auth Scope

**Note:** The **REST API Auth Scope** plugin is added as part of the Tokyo release.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **API Auth Scopes** &gt; **REST API Auth Scope**.

    The REST API Auth Scopes page is displayed.

2.  To configure a new REST API Auth Scope, click **New**.

3.  On the form, fill in the fields.

<table id="table_sss_z55_4tb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name that identifies the REST API Auth Scope.

</td></tr><tr><td>

Active

</td><td>

Select the check box to make the configuration active.

</td></tr><tr><td>

Application

</td><td>

Read-only application scope.

</td></tr><tr><td>

REST API

</td><td>

The REST API to which the auth scope is applied. For example, the Table API.

</td></tr><tr><td>

Auth Scope

</td><td>

Select the auth scope from the lookup icon.

</td></tr><tr><td>

REST API PATH

</td><td>

API path of the REST API. This field is auto-populated based on the selected REST API. For example, now/table.

</td></tr><tr><td>

HTTP Method

</td><td>

Method used for interacting with the API. Select the method from drop-down list. You can disable the **Apply auth scope to all http methods in this API** field on the form manually to select the method.

</td></tr><tr><td>

REST API Version

</td><td>

Version of the API. For example, v1. This field is auto-populated based on the selected REST API. You can disable the **Apply auth scope to all versions in this API** field on the form manually to select the version.

</td></tr><tr><td>

Resource

</td><td>

Child resource of the REST API. This field is auto-populated based on the selected REST API. For example, /now/table.You can disable the **Apply auth scope to all resources in this API** field on the form manually to select the resources.

</td></tr><tr><td>

Apply auth scope to all http methods in this API

</td><td>

When enabled, applies the auth scope to all the http methods in the API.

</td></tr><tr><td>

Apply auth scope to all versions in this API

</td><td>

hen enabled, applies the auth scope to all versions in the API.

</td></tr><tr><td>

Apply auth scope to all resources in this API

</td><td>

When enabled, applies the auth scope to all resources in the API

</td></tr></tbody>
</table>4.  Click **Submit**.

    Based on the selected REST API and Auth Scope, the APIs retrieves information that is particular to the scope.


## Consider creating three REST API Auth Scope for Table API

The first auth scope is mapped to the **Table API** with all the http methods, versions, and resources enabled.

![REST API Auth Scope3](../image/auth-scope3.png)

The second auth scope is mapped to the **Table API** with all the versions and resources enabled. But, you choose the HTTP Method, in this example, the **GET** method.

![REST API Auth Scope2](../image/auth-scope2.png)

The third auth scope is mapped to the **Table API** without the http methods, versions, and resources enabled. But, you choose the HTTP Method, Version, and Resource manually. In this example, HTTP Method is **GET**, REST API Version is **latest**, and Resource is `/now/table/{tableName}`.

![REST API Auth Scope1](../image/auth-scope1.png)

If all these auth scopes are created, you can use **GET** method with all the three scopes, but for **POST**, **PUT**, **DELETE**, or **PATCH** methods only **scope3** can be used.

