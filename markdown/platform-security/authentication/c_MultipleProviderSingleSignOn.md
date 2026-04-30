---
title: Multi-Provider Single sign-on \(SSO\)
description: External SSO allows organizations to use several SSO identity providers \(IdPs\) to manage authentication as well as retain local database \(basic\) authentication.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Access Management]
---

# Multi-Provider Single sign-on \(SSO\)

External SSO allows organizations to use several SSO identity providers \(IdPs\) to manage authentication as well as retain local database \(basic\) authentication.

The integration supports any combination of local and external authentication methods on a single instance:

-   SAML 2.0
-   Digest Authentication
-   OpenID Connect

You must perform several steps to set up Multi-Provider SSO, including configuring properties, creating identity providers \(IdPs\), and configuring users to use SSO.

For example, a globally dispersed corporation might require one SSO provider for their employees, a different one for their vendors, and local database authentication for their administrators. Alternatively, a company might implement SAML 2.0 and a digest token authentication solutions on the same instance.

