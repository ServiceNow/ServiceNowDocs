---
title: Third party token workflow for user accounts
description: This workflow is based on the token federation concept. It allows client applications to obtain tokens directly from an IdP and use them to access ServiceNow APIs.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Third Party Token Grant, Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Third party token workflow for user accounts

This workflow is based on the token federation concept. It allows client applications to obtain tokens directly from an IdP and use them to access ServiceNow APIs.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## About this task

The third-party client application requests tokens directly from your identity provider \(IdP\). The authentication method between the client and the IdP is flexible and can be configured to meet your specific requirements. After successful authentication, the IdP issues an ID token or access token, and optionally a refresh token. These tokens are sent directly to the client application, which then uses them to access ServiceNow APIs.

**Note:** ServiceNow validates the token using the public key configured during setup and grants access to the requested APIs. Ensure that the token is in JSON Web Token \(JWT\) format.

![User Account Workflow](../images/mic-third-party-user-account.png "User Account Workflow")

**Note:** This diagram is for illustrative purpose. It shows the Authorization code grant flow between your client application and the identity provider. The workflow is flexible. You can use a different flow based on your requirements.

## Procedure

1.  Configure your third party client application.

    Set up your third party client application to request tokens directly from your identity provider \(IdP\). Select an authentication method that best fits your security and integration requirements.

2.  Create an OAuth client in ServiceNow.

    Provide the required details to enable validation of incoming tokens from your identity provider \(IdP\). For more information on how to configure, see [Configure a third party ID token](configure-a-third-party-id-token.md)


