---
title: Basic authentication exceptions
description: The Basic Auth Exceptions table lists accounts that have been identified as using basic authentication on the instance, along with their assigned decision and usage details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-security/authentication/basic-auth-exceptions.html
release: yokohama
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 1
keywords: [basic auth exceptions, basic authentication, identified users, enforcement]
breadcrumb: [Basic authentication, API Authentication, Authentication, Access Management]
---

# Basic authentication exceptions

The Basic Auth Exceptions table lists accounts that have been identified as using basic authentication on the instance, along with their assigned decision and usage details.

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

