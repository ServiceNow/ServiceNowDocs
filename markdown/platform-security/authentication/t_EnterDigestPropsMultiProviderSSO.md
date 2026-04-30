---
title: Configuring the digest properties for multi-provider single sign-on \(SSO\)
description: After enabling a digest installation exist script, configure properties for multi-provider SSO.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Digest token authentication, Token based authentication \(User logins\), Authentication, Access Management]
---

# Configuring the digest properties for multi-provider single sign-on \(SSO\)

After enabling a digest installation exist script, configure properties for multi-provider SSO.

## Before you begin

Role required: admin

## About this task

If you are not using multi-provider single sign-on, configure standard single sign-on properties.

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Fill in the fields of Digest Properties form.

<table id="choicetable_sf3_clr_xkb"><tbody><tr><td id="d38521e78">

**__Name__**

</td><td>

Enter the name of the digest token.

</td></tr><tr><td id="d38521e90">

**__User__**

</td><td>

Enter the sys\_user field that contains the matching data for the incoming header.

</td></tr><tr><td id="d38521e102">

**__HTTP Digest header name__**

</td><td>

Enter the HTTP header you generated. For example, `DE_USER`.

</td></tr><tr><td id="d38521e117">

**__HTTP header name__**

</td><td>

Enter the HTTP header you generated for your created digested token. For example, `SM_USER`.

</td></tr><tr><td id="d38521e132">

**__Secret Passphrase__**

</td><td>

Enter the secret key to use for encoding digest keys. For example, `32 or more characters`.

</td></tr><tr><td id="d38521e148">

**__Failed SSO Redirect field__**

</td><td>

Enter the URL to redirect users after a failed authentication.

</td></tr><tr><td id="d38521e160">

**__External logout redirect__**

</td><td>

Enter the URL to redirect users after a logout.

</td></tr><tr><td id="d38521e172">

**__Single Sign-on Script__**

</td><td>

Select **MultiSSO\_DigestedToken**.

</td></tr><tr><td id="d38521e187">

**__Client Type__**

</td><td>

Choose the client type, based on the type of your client. Options:**Iframe Embedded**.**Note:** If client type field is required for your configuration, you can edit the form and add the field. To know more, see [Configure client type for OAuth and SSO records](../../authentication/concept/client-type.md).

</td></tr></tbody>
</table>3.  Click **Update**.

4.  Set your Digested Token default to true.

    When you set the default to true, this overwrites the system default digest token record associated to SSO. Once the first multi-provider SSO related IdP record activates, only records associated to multi-provider SSO will be used.

    Digest token records which exist in digest properties table can be individually called by appending the Sys\_ID of the IdP. For example, a digest token record in the following authentication URL: `https://<instance_name>.service-now.com/login_with_sso.do?glide_sso_id=<sys_id_of_Digest_token_record>&SM_USER=<user_name>&DE_USER=<digested_token>`


