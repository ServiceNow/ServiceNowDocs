---
title: Create SOAP API access policy
description: Create an API access policy and map an authentication profile to restrict the authentication type for a SOAP API. For example, you can create an API access policy that allows only ID token authentication for a SOAP API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/create-soap-api-access-policy.html
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SOAP API access policies, API access policy, Authentication, Access Management]
---

# Create SOAP API access policy

Create an API access policy and map an authentication profile to restrict the authentication type for a SOAP API. For example, you can create an API access policy that allows only ID token authentication for a SOAP API.

## Before you begin

-   Make sure that an authentication profile is created. For more information, see [Create an authentication profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/create-authentication-profile.md).
-   Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **API Access Policies** &gt; **SOAP API Access Policies**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of the API access policy.|
    |SOAP API|SOAP API to which the access policy is applied. For example, **GetProperty API**.|
    |Application|Scope of the application.|
    |Active|Option to make the API access policy active.|

4.  In the Inbound Authentication section, double-click **Insert a new row**.

5.  Select an inbound authentication profile from the list and click the save icon \[Omitted image "green-checkmark.png"\] Alt text: save icon.

    For example, you can add **Basic Auth**, **ID Token**, **Certificate based Auth**, **OAuth** or **WSSE Auth**.\[Omitted image "create-soap-api-policy.png"\] Alt text: SOAP API Access Policy

    1.  To add one or more inbound authentication profiles, click **New** to create a new profile.

    2.  Choose **What Kind of authentication profiles?**.

        -   **Create standard http authentication profiles**
        -   **Create WSSE authentication profiles**
        \[Omitted image "auth-profile.png"\] Alt text: Authentication Profile

    3.  To create a WSSE authentication profile, on the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name of the API access policy.|
        |Description|Description of the authentication profile.|
        |Application|Scope of the application.|
        |Active|Option to make the API access policy active.|
        |Type|WSSE Auth as authentication profile WSSE \(Web Security\).|

        \[Omitted image "wsse-profile.png"\] Alt text: WSSE Authentication Profile

    4.  After creating the authentication profile, save the record.

6.  Click **Submit** to submit the SOAP API access policy.


