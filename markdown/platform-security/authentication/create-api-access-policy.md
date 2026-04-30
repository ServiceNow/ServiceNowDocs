---
title: Create REST API access policy
description: Create an API access policy and map an authentication profile to restrict the authentication type for a REST API. For example, you can create an API access policy that allows only ID token authentication for a REST API.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [REST API access policies, API access policy, Authentication, Access Management]
---

# Create REST API access policy

Create an API access policy and map an authentication profile to restrict the authentication type for a REST API. For example, you can create an API access policy that allows only ID token authentication for a REST API.

## Before you begin

-   Role required: admin
-   Make sure that an authentication profile is created. For more information, see [Create an authentication profile](create-authentication-profile.md).

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST API Access Policies**.

2.  Click **New**.

3.  On the form, fill in the fields.

    ![API access policy fields](../images/rest-api-access-policy.png)

<table id="table_d4x_w45_d4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the API access policy.

</td></tr><tr><td>

Active

</td><td>

Option to make the API access policy active.

</td></tr><tr><td>

REST API

</td><td>

The REST API to which the access policy is applied. For example, **Attachment API**.

</td></tr><tr><td>

REST API PATH

</td><td>

API path of the REST API. This field is auto-populated based on the selected REST API. For example, **now/attachment**.

</td></tr><tr><td>

HTTP Method

</td><td>

Method used for interacting with the API. This field is auto-populated based on the selected REST API.

</td></tr><tr><td>

Version

</td><td>

Version of the API. For example, **v1**. This field is auto-populated based on the selected REST API.**Note:** If you want to create an authentication policy for all versions of a REST API, you must create individual policies for each version.

</td></tr><tr><td>

Resource

</td><td>

Child resource of the REST API. This field is auto-populated based on the selected REST API. For example, **/now/attachment**

</td></tr><tr><td>

Application

</td><td>

Scope of the application.

</td></tr><tr><td>

Global

</td><td>

Enable to apply auth policy to all methods, versions, and resources for the API.

</td></tr><tr><td>

Apply to all methods

</td><td>

Enable to apply auth policy for the API to all the methods, versions, and resources for the API.

</td></tr><tr><td>

Apply to all resources

</td><td>

Enable to apply auth policy for the API to all the versions.

</td></tr><tr><td>

Apply to all versions

</td><td>

Enable to apply auth policy for the API to all the resources.

</td></tr></tbody>
</table>    **Note:** To understand more about the API access policy prioritization, see [API access policy prioritization](../../inbound-rest/concept/api-access-policy-prioritization.md).

4.  Double-click **Insert a new row**.

5.  Select an inbound authentication profile from the list and click the save icon ![save icon](../images/green-checkmark.png).

    For example, you can add **Basic Auth**, **ID Token**, **Certificate based Auth**, **OAuth** or **WSSE Auth**.

    1.  To add one or more inbound authentication profiles, click **New** to create a new profile.

    2.  Choose **What Kind of authentication profiles?**.

        -   **Create standard http authentication profiles**
        -   **Create WSSE authentication profiles**
        ![Authentication profile](../../inbound-soap/image/auth-profile.png)

    3.  After creating the authentication profile, save the record.

6.  Click **Submit** to submit the REST API access policy.


