---
title: Set up multiple provider SSO with Edge Encryption
description: Set up multiple provider SSO to enable logging in through the Edge Encryption proxy server URL or the instance URL. If you are implementing multiple provider single sign-on \(SSO\) with Edge Encryption enabled, some users might need to log in to your instance through the Edge Encryption proxy server, while other users might not.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Set up multiple provider SSO with Edge Encryption

Set up multiple provider SSO to enable logging in through the Edge Encryption proxy server URL or the instance URL. If you are implementing multiple provider single sign-on \(SSO\) with Edge Encryption enabled, some users might need to log in to your instance through the Edge Encryption proxy server, while other users might not.

## Before you begin

-   Enable the Integration - Multiple Provider Single Sign-On Installer plugin \(com.snc.integration.sso.multi.installer\).
-   Enable the Edge Encryption plugin \(com.glide.edgeencryption\) and ensure that one or more proxy servers are set up in your network.
-   Determine the URL for the Edge Encryption proxy server that users will log in through using multiple provider SSO. To determine the URL of an Edge Encryption proxy server, see [Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md).

Role required: admin

## About this task

The user logging in will need to use the appropriate URL to log in, either using the Edge Proxy or not using the Edge Proxy.

-   If routing all users through the Edge Encryption proxy server, set up your identify provider record and define the proxy server URL in the **ServiceNow Homepage**, **Entity ID / Issuer**, and **Audience URI** fields.
-   To route some users through the proxy server and some users to the instance, create two identify provider records. Both records use the same value in the **Identity Provider URL** field. However, one of the records routes through the proxy server, while the other routes to the instance.
    -   Login via instance name:`https://<instance name>.service-now.com/login_with_sso.do?glide_sso_id=<sys_id` of IdP record for non-Edge Proxy
    -   Log in via Edge Proxy: `https://<edge hostname>:<port>/login_with_sso.do?glide_sso_id=<sys_id` of the IdP record for the Edge Proxy

## Procedure

1.  Enable the duplication of identity provider URLs in identity provider records.

    A unique constraint prevents duplication of the identity provider URL in two different identity provider records. You can enable duplication of the identity provider URL in multiple IdP records by setting a field to false.

    1.  Navigate to **System Definition** &gt; **Dictionary**.

    2.  Open the definition record for the **idp** field of in the Identity Providers table \[saml2\_update1\_properties\].

    3.  Configure the form to add the **Unique** field.

    4.  Ensure that the value of the **Unique** field is set to **false**.

2.  Navigate to **Multi-Provider SSO** &gt; **Identity Providers**.

3.  Create two identity provider records for the same identity provider: one using the instance URL and one using the Edge Encryption proxy server URL.

    To create an identity provider record, see [Create an external identity provider](../../../integrate/single-sign-on/task/t_CreateUpdateIdentityProvider.md).

    1.  For the Edge Encryption proxy server URL, complete the form using these values.

<table id="table_btz_ysl_pbb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Identity Provider URL

</td><td>

Imported from IdP metadata.

</td></tr><tr><td>

ServiceNow Homepage

</td><td>

The URL for your proxy server homepage. For example: `https://<proxy hostname>:<port>/navpage.do`

</td></tr><tr><td>

Entity ID / Issuer

</td><td>

`https://<proxy hostname>:<port>`

</td></tr><tr><td>

Audience URI

</td><td>

`https://<proxy hostname>:<port>`

</td></tr></tbody>
</table>    2.  Click **Submit**.

    3.  For the instance URL, complete the form using these values.

<table id="table_bgh_xvl_pbb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Identity Provider URL

</td><td>

Imported from IdP metadata.

</td></tr><tr><td>

ServiceNow Homepage

</td><td>

`https://<instance>.service-now.com/navpage.do`

</td></tr><tr><td>

Entity ID / Issuer

</td><td>

`https://<instance>.service-now.com/navpage.do`

</td></tr><tr><td>

Audience URI

</td><td>

`https://<instance>.service-now.com/navpage.do`

</td></tr></tbody>
</table>    4.  Click **Submit**.

4.  If using more than one identity provider, modify the MultiSSO installation exit.

    1.  Navigate to **System Definition** &gt; **Installation Exits**.

        The system displays the current list of installation exits.

    2.  Open the **MultiSSO** installation exit.

    3.  Locate the following statement in the **Script** field.

        ```
        var samlResponseTxt = request.getParameter("SAMLResponse");
        if (!GlideSession.get().isLoggedIn() && GlideStringUtil.notNil(samlResponseTxt)) {
            var idpRecord = this.getIdPRecord(request);
            if (idpRecord) {
                SSO_Helper.debug("IdP found based on SAML response: " + idpRecord.getUniqueValue());
                return new SSO_Helper(idpRecord.getUniqueValue(), false, null, true);
            }
        }
        ```

    4.  Replace the statement with the following code.

        ```
        var samlResponseTxt = request.getParameter("SAMLResponse");
        if (!GlideSession.get().isLoggedIn() && GlideStringUtil.notNil(samlResponseTxt)) {
           /* // You have two profiles that use the same IdP entity id it cannot use
           // the IdP issuer / entity id from the response otherwise it may result in the
           // wrong IdP profile. IdP initiated login will not work
           var idpRecord = this.getIdPRecord(request);
           if (idpRecord) {
              SSO_Helper.debug("IdP found based on SAML response: " + idpRecord.getUniqueValue());
              return new SSO_Helper(idpRecord.getUniqueValue(), false, null, true);
              }*/
           return new SSO_Helper(null, true);
           }
        ```

        **Note:** IdP initiated login does not work in this configuration.

    5.  Click **Update**.

5.  If using more than one company, configure users for multi-provider SSO and update sys\_id of the identity provider record depending on the user.

    For more information, see [Configure users for Multi-Provider SSO](../../../integrate/single-sign-on/task/t_ConfigureUsersMultiProviderSSO.md).

    -   To configure a user to log in through the Edge Encryption proxy server, use the sys\_id of the identity provider record that uses the Edge Encryption proxy server URL.
    -   To configure a user to log in to the instance, use the sys\_id of the identity provider record that uses the instance URL.
    |URL|Login destination|
    |---|-----------------|
    |`https://<proxy hostname>:<port>/login_with_sso.do?glide_sso_id=<sys_id of the IdP record for the proxy server URL>`|Logs in through the proxy server.|
    |`https://<instance name>.service-now.com/login_with_sso.do?glide_sso_id=<sys_id of IdP record for the instance URL>`|Logs in through the instance.|


**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)

