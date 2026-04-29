---
title: Manage OAuth tokens
description: Open OAuth tokens to provide access to restricted resources.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Manage OAuth tokens

Open OAuth tokens to provide access to restricted resources.

## Before you begin

Role required: any user or oauth\_admin

## About this task

OAuth tokens issued by the instance and third party OAuth provider are stored in oauth\_credential table.

Some of the important columns in this table:

-   Token: Value of the token issued by ServiceNow instance.
-   Type: Determines if the token is Access Token or Refresh Token.
-   Expires: Data/Time when the Access or Refresh Token expire.
-   Token Received: Value of the token issued by a 3rd party OAuth Provider. This value is in encrypted format.

Token Expiration and Validity is as follows:

-   Access Token: By default, an instance issues access tokens with a 30-minute lifespan in the scenario where the instance is the OAuth provider.
-   Refresh Token: By default, an instance issues refresh tokens with a 100-day lifespan in the scenario where the instance is the OAuth provider.

## Procedure

1.  Navigate to one of the following menu options:

    -   **Self-Service** &gt; **My Connected Apps** to see the tokens that the instance created when you granted access to a resource on the instance.
    -   **System OAuth** &gt; **Manage Tokens** to see all tokens. Only administrators can access this module.
2.  Click the **Name** to open the token.

3.  Click **Revoke Access** to prevent access to the restricted resource.

    You can also view other information about the token, including the scope it allows access to and the expiration date.

    You can select the **Clean Expired OAuth Credentials** record from the Schedule page \(`sys.trigger.list`\) and configure the following:

    -   **com.snc.platform.security.oauth.is.active**: By default, the value is set true.
    -   **com.snc.platform.security.oauth.hours.expired.credential.is.kept**: Set the value based on your requirement to determine the number of hours you want the keep the expired `oauth` credential in the system.
    -   **com.snc.platform.security.oauth.day.old.credential.is.kept**: Set the value based on your requirement to determine the number of days you want the keep the expired `oauth` credential in the system.

