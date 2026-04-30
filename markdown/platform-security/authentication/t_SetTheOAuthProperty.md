---
title: Set the OAuth property
description: To generate OAuth 2.0 tokens to registered applications, the com.snc.platform.security.oauth.is.active property must be active for the instance.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [OAuth 2.0, OAuth authentication, Authentication, Access Management]
---

# Set the OAuth property

To generate OAuth 2.0 tokens to registered applications, the `com.snc.platform.security.oauth.is.active` property must be active for the instance.

## Before you begin

Role required: admin

## Procedure

1.  To use OAuth 2.0, enter **sys\_properties.list** in the navigator and select **New**.

    You can also open the system properties list by navigating to **All** &gt; **System Properties** &gt; **All Properties** &gt; ****.

2.  Fill out the form with the following settings:

    -   **Name**: com.snc.platform.security.oauth.is.active
    -   **Type**: true \| false
    -   **Value**: true

