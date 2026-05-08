---
title: Set up OAuth
description: Set up and activate OAuth, enable the OAuth system property, create an OAuth application endpoint for external client applications to access the instance, and set OAuth parameters.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OAuth 2.0, OAuth authentication, Authentication, Access Management]
---

# Set up OAuth

Set up and activate OAuth, enable the OAuth system property, create an OAuth application endpoint for external client applications to access the instance, and set OAuth parameters.

## Before you begin

Role required: oauth\_admin

## Procedure

1.  Make sure the [OAuth plugin](t_ActivateOAuth.md) is active and the [OAuth activation property](t_SetTheOAuthProperty.md) is set to true.

2.  Create an OAuth application registry using one of the following methods:

    -   [Create an endpoint for external clients](t_CreateEndpointforExternalClients.md) that want to access your instance. This creates an **OAuth client application** record and generates a client ID and client secret that the client needs to access the restricted resources on the instance.
    -   Use a third-party OAuth provider that provides the authorization for access to your instance.

        Specify an OAuth profile and Specify an OAuth scope when you are connecting to another OAuth provider.

3.  Configure your client applications to create an HTTP POST that requests an OAuth token.

    The application must also be able to parse the JSON response to use the returned access token and refresh token.


