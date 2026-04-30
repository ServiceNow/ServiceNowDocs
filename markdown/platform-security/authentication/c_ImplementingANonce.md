---
title: Implementing a nonce
description: You can implement a nonce to be used with single sign-on digest authentication.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Local Authentication, Authentication, Access Management]
---

# Implementing a nonce

You can implement a nonce to be used with single sign-on digest authentication.

To use a nonce with the unencrypted token or encrypted token methods of single sign on, these steps apply with only a few minor changes.

**Note:** The nonce is used only for login requests, not for any other type of request. If the system receives a nonce value after login, the nonce is not consumed.

## Benefits

The usage of a nonce prohibits a malicious user from performing a replay attack in order to log into your system.

