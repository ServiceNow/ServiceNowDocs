---
title: Explore Digest token authentication
description: 
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Digest token authentication, Token based authentication \(User logins\), Authentication, Access Management]
---

# Explore Digest token authentication

The instance reads the HTTP header value and compares its computed hash value of the digest token. If the computed hash value matches the digest token value, then the instance searches for a matching value in the User table. If there is a matching value in the User table, the instance considers the user pre-authenticated and logs the user in.

Digest token authentication is more secure than simple unencrypted HTTP headers because any accidental or intentional change to the unencrypted HTTP header produces a different hash value. If the hash value fails to match, the instance denies the user access to the requested instance. This prevents users from attempting to login with another user's credentials.

To know more about digest link expiry, see this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1186365).

**Note:** Use Time Limited Authentication \(TLA\) to configure time based expiry links. To know more, see [Time limited authentication](time-limited-authentication.md).

## Integration requirements

A Digest Token Authentication integration requires:

-   A web server
-   SiteMinder or another single sign-on application to pre-authenticate the user on the local network
-   A web page or portal that passes user credentials to the target instance in one of these formats
    -   HTTP Header
    -   URL parameter
    -   Cookie
-   A web page or portal that creates and passes a digest token to the target instance using one of these encoding techniques
    -   SHA1
    -   MD5
    -   SHA 256 \(recommended\)

