---
title: Create a global API access policy to protect SOAP APIs
description: Create a single global API access policy to protect all the SOAP APIs.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create SOAP API access policy, SOAP API access policies, API access policy, Authentication, Access Management]
---

# Create a global API access policy to protect SOAP APIs

Create a single global API access policy to protect all the SOAP APIs.

## Before you begin

-   Role required: admin
-   Install the **Processor Access policy** \(`com.glide.processor.policy`\) plugin
-   Make sure that an authentication profile is created. For more information, see [Create an authentication profile](../../authentication/task/create-authentication-profile.md).

The following steps describes how to create a single global access policy to protect all the SOAP APIs.

**Note:** The policies defined at the individual SOAP API levels overrides the **SOAPProcessor** level global access policy.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Process Access Policies**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Processor|Name to identify the authentication policy. For example select, **SOAPProcessor** \(Authentication profile\).|
    |Application|Scope of the authentication policy. Default: Global|
    |Authentication Profile|Type of the authentications profile. Select, **Global SOAP Auth Profile**.|

    ![Create a global API access policy to protect SOAP APIs](../image/protect-soap-api.png)

3.  Select **Submit**.


