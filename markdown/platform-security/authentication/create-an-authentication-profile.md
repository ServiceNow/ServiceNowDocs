---
title: Create an authentication profile
description: Create an authentication profile and add one or more authentication policies to the profile. You can also configure the ID Token and OAuth Token authentication profiles that are available by default.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SOAP API access policies, API access policy, Authentication, Access Management]
---

# Create an authentication profile

Create an authentication profile and add one or more authentication policies to the profile. You can also configure the **ID Token** and **OAuth Token** authentication profiles that are available by default.

## Before you begin

Role required: admin

**Note:** You can apply authentication policies, IP range, role-based, user-based, and so on with mutual authentication and customized authentication.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **API Access Policies** &gt; **Inbound Authentication Profiles**.

2.  Select **New**.

    The system displays the message. `What kind of authentication profile?`

3.  Choose **What Kind of authentication profiles?**.

    -   **Create standard http authentication profiles**
    -   **Create WSSE authentication profiles**
    ![Authentication profile](../../inbound-soap/image/auth-profile.png)

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the authentication policy.|
    |Description|Description of the authentication policy.|
    |Active|Option to make the authentication policy active.|
    |Application|Scope of the authentication policy.|
    |Type|Type of the authentication available. You can select **Basic Auth**, **ID Token**, **Certificate based Auth**, **OAuth**, or **WSSE** \(In case of WSSE Authentication profile\).|
    |OAuth Entity|OAuth Entity profile. This field appears only when **ID Token** or **OAuth** is selected from **Type**.|

5.  Double-click **Insert a new row**.

6.  Select an authentication policy from the list and select the save icon ![save icon](../images/green-checkmark.png).

    **Note:** Don’t select **Allow Access Policy** or **Deny Access Policy**. These policies are meant only for user logins.

    You can add one or more authentication policies for an authentication profile.

    When there’s a change in the authentication profile, the Authorization header returns a value specific to the changes made at that time. To have the ability to get all the authentication schemes returned in the \`WWW-Authenticate\` header, you must activate `glide.security.response.authenticate.header.auth_profile.first_scheme_only` to **false**. The response is returned with multiple headers. For example:

    ```
    < WWW-Authenticate: BEARER realm="Service-now"
    < WWW-Authenticate: BASIC realm="Service-now"
    ```


