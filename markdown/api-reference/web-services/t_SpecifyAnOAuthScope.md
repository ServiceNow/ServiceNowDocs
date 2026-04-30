---
title: Specify an OAuth scope
description: Specify the OAuth scopes that you get from the provider. Scopes can be any level of access specified by the provider, such as read, write, or any string, including a URL.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [OAuth profiles and scopes, Use a third-party OAuth provider, Configure a REST message with OAuth, Outbound REST authentication, Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Specify an OAuth scope

Specify the OAuth scopes that you get from the provider. Scopes can be any level of access specified by the provider, such as read, write, or any string, including a URL.

## Before you begin

Role required: admin

## Procedure

1.  Open a third-party OAuth provider record.

2.  Open a profile associated with the provider.

3.  In the OAuth Entity Profile Scopes embedded list, click **Insert a new row** and then enter a **Name** for the profile.

4.  Right-click the **OAuth Entity Profile** form header and select **Save**.

    The profile record is created.

5.  Click the name of the scope that you created and then fill in the form fields.

    ![OAuth Entity Scope](../image/OAuthEntityScope.png)

    |Field|Description|
    |-----|-----------|
    |Name|Enter a descriptive name.|
    |OAuth provider|Verify the provider associated with this scope.|
    |OAuth scope|The scope that you are granted by the provider. Typical scopes are read and write. Scopes can be any string that the provider specifies.|

6.  Click **Update**.


**Parent Topic:**[OAuth profiles and scopes](../concept/c_OAuthProviderAndScope.md)

