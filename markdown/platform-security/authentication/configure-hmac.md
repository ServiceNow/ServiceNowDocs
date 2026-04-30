---
title: Configure HMAC - Token-based authentication
description: Configure HMAC to support authentication for REST API endpoints.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [API Key and HMAC Authentication for inbound REST APIs, Token-based authentication, API authentication, Authentication, Access Management]
---

# Configure HMAC - Token-based authentication

Configure HMAC to support authentication for REST API endpoints.

## Before you begin

Role required: admin

Plugin required: API Key and HMAC Authentication \(`com.glide.tokenbased_auth`\)

**Note:** While configuring the HMAC, ensure the name of the script that starts with HMAC to populated in the script list view.

## Procedure

1.  Create an HMAC configuration.

    1.  Navigate to **All** &gt; **System Web Services** &gt; **API Access Policies** &gt; **HMAC Configuration**.

    2.  Select **New**.

        **Note:** You can also use the **Default HMAC SHA256 Base64 Encoding** which is created when installing the plugin.

    3.  On the form, fill the fields:

<table id="table_y3b_h1f_nzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the HMAC configuration.

</td></tr><tr><td>

Application

</td><td>

Scope of the configuration.

</td></tr><tr><td>

Description

</td><td>

Detailed description about the configuration.

</td></tr><tr><td>

Hash Algorithm

</td><td>

Choose the Hash Algorithm. Options available:-   HmacSHA256
-   HmacSHA384
-   HmacSHA512


</td></tr><tr><td>

HMAC util script

</td><td>

Utility script for HMAC.**Note:** If you validate HMAC authentication using Request body, Time stamp and Secret with no Key Id, then do the following:

-   Create a customized script include as HMAC util script
-   Use that script include util to interpret the passed in timestamp, and request body.
For every shared secret created in the ServiceNow® instance, there is a key ID. You need to configure the key ID into Default key id in HMAC auth profile.

</td></tr></tbody>
</table>        ![HMAC Configuration](../images/configure-hmac.png)

    4.  Submit the record.

2.  Create an inbound authentication profile.

    1.  Navigate to **All** &gt; **System Web Services** &gt; **API Access Policies** &gt; **Inbound Authentication Profiles**.

    2.  Select **New**.

        The system displays the message `What kind of authentication profile?`

    3.  Select **Create HMAC authentication profiles**.

        ![HMAC authentication profile](../images/hmac-profile.png)

    4.  On the form, fill in the fields.

<table id="table_nnk_yqx_mzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the authentication policy.

</td></tr><tr><td>

Application

</td><td>

Scope of the authentication policy.

</td></tr><tr><td>

Configuration for HMAC

</td><td>

Select the HMAC configuration that was created.

</td></tr><tr><td>

Auth Parameter

</td><td>

Select the auth parameter for the authentication request. You can select the default options or create a new auth parameter:-   x-sn-hmac-signature-256: Auth Header
-   x-sn-hmac-signature-256: Query Parameter


</td></tr><tr><td>

Default Key ID of Shared Secret

</td><td>

The token information that can be updated in this field for using HMAC.

</td></tr></tbody>
</table>        **Note:** The selected option has to be defined in the REST call as part of the Auth Header or Query Parameter.![HMAC Profile](../images/hmac-parameter.png)

    5.  Submit the form.

3.  Create an HMAC secret.

    1.  Navigate to **All** &gt; **System Web Services** &gt; **API Access Policies** &gt; **REST API HMAC Secret**.

    2.  Select **New**.

    3.  On the form, fill the fields:

<table id="table_tpz_x1f_nzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the REST API HMAC secret.

</td></tr><tr><td>

Description

</td><td>

Description for the REST API HMAC secret.

</td></tr><tr><td>

Active

</td><td>

Status of the REST API HMAC secret.

</td></tr><tr><td>

User

</td><td>

User associated to the REST API HMAC secret. Use the look-up icon to select the user.

</td></tr><tr><td>

Key ID

</td><td>

Key ID that must be sent as part of the REST call. Key ID is generated after submitting the form.

</td></tr><tr><td>

Shared Secret

</td><td>

Shared secrets of the user. For example, the password.

</td></tr><tr><td>

Source

</td><td>

Source of the record.

</td></tr><tr><td>

Expiry

</td><td>

Time after which the credential is no longer valid. Empty value means no expiration.**Note:** For more information, about expiry of token, see [Cleaning up token Expiry](../concept/token-expiry-api-and-hmac.md) .

</td></tr></tbody>
</table>    4.  Submit the form.

    5.  Open the record that was created.

        Find the Key ID generated by the ServiceNow AI Platform for the user.

        ![HMAC Key ID](../images/hmac-key.png)

        **Note:** You can add the Key ID that was generated during the Key ID in the Authentication Profile that was created for HMAC if you don't want to specify the Auth or Query parameter for the API call.

4.  Create a REST API access policy.

    1.  Navigate to **All** &gt; **System Web Services** &gt; **REST API Access Policies**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

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

Enable this field to apply auth policy to all methods, versions, and resources for the API.**Note:** Token Based Auth isn’t allowed in the Global REST API Policy.

</td></tr><tr><td>

Apply to all methods

</td><td>

Enable this field to apply the auth policy for the API to all the methods, versions, and resources for the API.

</td></tr><tr><td>

Apply to all resources

</td><td>

Enable this field to apply the auth policy for the API to all the versions.

</td></tr><tr><td>

Apply to all versions

</td><td>

Enable this field to apply the auth policy for the API to all the resources.

</td></tr></tbody>
</table>    4.  Add the API authentication profile that was created.

        ![HMAC Profile added to Access Policy](../images/hmac-profile-added.png)

    5.  Submit the form.

        You can send the REST API call:

        -   With the x-sn-hmac-signature-256 that was generated by ServiceNow® during the API Key creation within the Header or Query parameter based on the configuration for authentication.
        -   With pre-request Script with Shared Secret specified as part of the request.
        **Warning:** Use **POST** request when submitting any sensitive information to the server.


