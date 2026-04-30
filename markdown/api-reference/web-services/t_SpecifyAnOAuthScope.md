---
title: Specify an OAuth scope
description: Specify the OAuth scopes that you get from the provider. Scopes can be any level of access specified by the provider, such as read, write, or any string, including a URL.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Profiles and scopes, Use a third-party OAuth provider, Configure a message with OAuth, Outbound REST authentication, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Specify an OAuth scope

Specify the OAuth scopes that you get from the provider. Scopes can be any level of access specified by the provider, such as read, write, or any string, including a URL.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System OAuth** &gt; **Application Registry** and open a third-party OAuth provider record.

2.  In the OAuth Entity Scopes embedded list, click **Insert a new row** and then enter a **Name** and **OAuth scope**.

    The OAuth scope is the scope that you are granted by the provider. Typical scopes are read and write. Scopes can be any string that the provider specifies.

    ![OAuth entity scopes embedded list](../image/OAuthEntityScope.png)

3.  Right-click the OAuth provider form header and select **Save**.

    The scope record is created.

4.  In the OAuth Entity Profiles embedded list, open a profile associated with the OAuth provider.

5.  In the OAuth Entity Profile Scopes embedded list, click **Insert a new row** and then select the scope you created.

6.  Click **Update**.

    The scope is added to the profile.


**Parent Topic:**[OAuth profiles and scopes](../concept/c_OAuthProviderAndScope.md)

