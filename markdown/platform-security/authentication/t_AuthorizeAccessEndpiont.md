---
title: Authorize access to an OAuth endpoint using auth code flow
description: End users who own a protected resource on the ServiceNow instance must authorize access to the resource before the instance can provide the access token.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [OAuth authorization code grant flow, OAuth Inbound, OAuth Inbound and Outbound authentication, Authentication, Access Management]
---

# Authorize access to an OAuth endpoint using auth code flow

End users who own a protected resource on the ServiceNow instance must authorize access to the resource before the instance can provide the access token.

## Before you begin

Role required: none. You must already be logged in to the instance that holds the protected resource. Alternatively, you can log in using the authentication method \(such as multi-factor authentication or SAML\) that your ServiceNow administrator already set up.

## Procedure

1.  Click the link or button on the client application where you are requesting access to the protected resource on the instance.

    This kicks off the token request. If you are making a REST call from one instance to another, this link is **Get OAuth Token** on the REST Message form.

2.  If you are not logged in, log in now.

    If you are not the same user as the user specified in the upper-right corner, click **Not You?** and log in.

3.  Click account permissions to open the list of access tokens that you have already issued.

    This is the same as the **Self-Service** &gt; **My connected** apps token list.

4.  Click **Allow** to allow access and have the instance issue the authorization code \(if using auth code flow\) or the access token \(if using implicit grant type\).

    If you click **Deny**, the authorization is not allowed, but you are not logged out of the instance.

    ![Allow access](../image/allow_access.png)

    A message that confirms access should appear. If you are requesting access from the REST Message form on an instance, the following message appears at the top of the form: OAuth Refresh token is available and will expire at \{date\}.


