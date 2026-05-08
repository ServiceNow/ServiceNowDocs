---
title: JSON Web token grant workflow
description: Configuring an OAuth JSON Web Token \(JWT\) bearer grant secures token-based authentication without user interaction.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [JWT Grant, Inbound integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# JSON Web token grant workflow

Configuring an OAuth JSON Web Token \(JWT\) bearer grant secures token-based authentication without user interaction.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## About this task

The client application generates a signed JWT with identity-related claims such as the user or system it represents. The client application sends the JWT to the ServiceNow instance to request an access token.

-   -   **When acting on behalf of a user:**

    The token represents a previously authenticated user. It enables secure, seamless access without prompting the user for credentials or consent. ServiceNow trusts the request by validating the user's identity from the signed token, eliminating the need for real-time user interaction.

-   -   **When acting as itself:**

    The token identifies and authenticates the client application. Instead of using a shared secret, the application signs the token with a private key. This offers a more secure alternative to the client credentials grant.


![JWT Grant Workflow](../images/mic-jwt-grant-workflow.png "JWT Grant workflow")

## Procedure

1.  The client application sends a token request to ServiceNow, with a JWT signed with its private key.

2.  ServiceNow validates the JWT using the corresponding public key.

    It maps the `sub` \(subject\) claim in the token to a `sys_user` record.

3.  ServiceNow validates the JWT, and issues the access token.

4.  The client includes the access token in the API requests to ServiceNow.

5.  ServiceNow validates the access token, and returns the appropriate API response.


