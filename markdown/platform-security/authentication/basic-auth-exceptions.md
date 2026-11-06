---
title: Basic authentication exceptions
description: The Basic Auth Exceptions table lists accounts that have been identified as using basic authentication on the instance, along with their assigned decision and usage details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/basic-auth-exceptions.html
release: australia
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [basic auth exceptions, basic authentication, identified users, enforcement]
breadcrumb: [Basic authentication, API authentication, Authentication, Access Management]
---

# Basic authentication exceptions

The Basic Auth Exceptions table lists accounts that have been identified as using basic authentication on the instance, along with their assigned decision and usage details.

**Important:** Basic authentication is being prepared for future deprecation. Starting with the Brazil release, migrate your integrations to OAuth 2.0, mutual TLS \(mTLS\), or federated token-based authentication. Basic authentication remains supported until a future release, subject to the restrictions described in the Basic authentication restriction topic. For guidance on identifying and migrating these integrations, see the [KB3220405](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3220405) article.

The Basic Auth Exceptions table displays accounts that have been identified as using basic authentication during the tracking period. Each row represents an identified account and shows its usage details and the decision assigned by the administrator.

Navigate to **All** &gt; **Basic Auth Restriction** &gt; **Basic Auth User Exceptions** to open the table.

## Table columns

|Column|Description|
|------|-----------|
|**User**|The account identified as using basic authentication.|
|**Department**|The department associated with the user record.|
|**Manager**|The manager associated with the user record.|
|**Usage Count**|The number of basic authentication requests recorded for the account during the tracking period.|
|**Decision**|The decision assigned to the account. Overrides the default decision set on the Basic Auth Restriction page.|
|**Last Seen**|The date and time of the most recent basic authentication request recorded for the account.|

