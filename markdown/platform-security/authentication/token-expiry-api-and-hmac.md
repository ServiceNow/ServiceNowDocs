---
title: Cleaning up token Expiry
description: Details about how to clean up token expiry by using different system properties.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API Key and HMAC Authentication for inbound REST APIs, Token-based authentication, API Authentication, Authentication, Access Management]
---

# Cleaning up token Expiry

Details about how to clean up token expiry by using different system properties.

Once the API Key or HMAC secret expires, the details is retained for 7 days. A scheduled job `Clean expired Token Auth Credentials` deletes the expired API Keys or HMAC Secrets after that. You can configure this behavior and control the deletion using the following properties:

-   **com.snc.platform.security.token.auth.cleanup**: Use this property if you want to delete expired API Keys and HMAC tokens. By default `true`.
-   **com.snc.platfrom.security.token.auth.days.expired.api\_key.is.kept**: Set the value based on your requirement to determine the number of days you want the keep the expired `API` token in the system. By default 7.
-   **com.snc.platfrom.security.token.auth.days.expired.hmac\_key.is.kept**: Set the value based on your requirement to determine the number of days you want the keep the expired `HMAC` token in the system. By default 7.

To navigate to the token expiry property, enter `sys_properties.list` in the navigation bar and then search for the following properties. Change the expiry based on your requirement.

