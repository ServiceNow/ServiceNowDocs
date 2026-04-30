---
title: Revoke an OAuth token
description: You might want to revoke an OAuth access or refresh token for security reasons.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage OAuth tokens, OAuth Inbound, OAuth Inbound and Outbound authentication, Authentication, Access Management]
---

# Revoke an OAuth token

You might want to revoke an OAuth access or refresh token for security reasons.

## Before you begin

Role required: admin

## About this task

Revoking the token pertains to the situation where your instance acts as the OAuth resource server. You can revoke the token through a URL or by .

## Procedure

-   Access your instance using `oauth_revoke_token.do` and append the access or refresh token.

    For example: `https://[Your_ServiceNow_Instance]:[port]/oauth_revoke_token.do?token=[access or refresh token]` without the brackets `[ ]`.


## Result

This endpoint access does not require authentication. The token in this request is marked as expired.

