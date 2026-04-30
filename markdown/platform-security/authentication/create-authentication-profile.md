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
breadcrumb: [REST API access policies, API access policy, Authentication, Access Management]
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

3.  Select **Create standard http authentication profiles**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the authentication policy.|
    |Description|Description of the authentication policy.|
    |Active|Option to make the authentication policy active.|
    |Application|Scope of the authentication policy.|
    |Type|Type of the authentication available. You can select **Basic Auth**, **ID Token**, **Certificate based Auth**, or **OAuth**.|
    |OAuth Entity|OAuth Entity profile. This field appears only when **ID Token** or **OAuth** is selected from **Type**.|

5.  Double-click **Insert a new row**.

6.  Select an authentication policy from the list and select the save icon ![save icon](../images/green-checkmark.png).

    **Note:** Don’t select Allow Access Policy or Deny Access Policy. These policies are meant only for user logins.

    You can add one or more authentication policies for an authentication profile.

    **Note:**

    Authenticate Header \[WWW-Authenticate\].

    When REST API Access Policy is active we will return the most recently mapped authentication profile in the authenticate header. In the case you want the server to return all the authentication schemes, use the `glide.security.response.authenticate.header.auth_profile.first_scheme_only` property and set it to **false**. The response is returned with multiple header. For example:

    ```
    < WWW-Authenticate: BEARER realm="Service-now"
    < WWW-Authenticate: BASIC realm="Service-now"
    ```


