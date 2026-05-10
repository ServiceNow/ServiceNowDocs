---
title: Third party token workflow for user accounts
description: This workflow can be used to integrate third-party identity providers \(IdPs\) with ServiceNow for secure API access. It allows client applications to obtain tokens directly from an IdP and use them to access ServiceNow APIs.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Third Party Token Grant, Inbound integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Third party token workflow for user accounts

This workflow can be used to integrate third-party identity providers \(IdPs\) with ServiceNow® for secure API access. It allows client applications to obtain tokens directly from an IdP and use them to access ServiceNow APIs.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## About this task

The third-party client application requests tokens directly from your identity provider \(IdP\). The authentication method between the client and the IdP is flexible and can be configured to meet your specific requirements. After successful authentication, the IdP issues an ID token or access token, and optionally a refresh token. These tokens are sent directly to the client application, which then uses them to access ServiceNow APIs.

**Note:** ServiceNow validates the token using the public key configured during setup and grants access to the requested APIs. Ensure that the token is in JSON Web Token \(JWT\) format.

![User Account Workflow](../images/mic-third-party-user-account.png "User Account Workflow")

## Procedure

1.  Configure your third party client application.

    Set up your third party client application to request tokens directly from your identity provider \(IdP\). Select an authentication method that best fits your security and integration requirements.

2.  Create an OAuth client in ServiceNow.

    Provide the required details to enable validation of incoming tokens from your identity provider \(IdP\).


