---
title: Configure ServiceNow
description: Configure ServiceNow with Azure AD details to use SSO.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Azure AD Integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Configure ServiceNow

Configure ServiceNow with Azure AD details to use SSO.

## Before you begin

Plugin: `Integration - Multiple Provider single sign-on Installer`

Enable the Multi Provider SSO properties:

-   -   Select **Enable multiple provider SSO**.
-   Select **Enable Auto Importing of users from all identity providers into the user table**.
-   Select **Enable debug logging for the multiple provider SSO integration**.
-   Enter **email**, The field on the user table that.….

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  On the Identity Providers page, select **New**.

3.  On the Identity Providers windows, select **SAML**.

4.  On the Import Identity Provider Metadata, you can either:

    -   **URL**: App Federation Metadata URL to auto-populate the details on the Identity Provider configuration page.
    -   **Import**: Import the XML to import the details on the Identity Provider configuration page.
5.  Right click on the top of the screen, click **Copy sys\_id**, and use this value to the **Sign on URL** in **Basic SAML Configuration** section.

6.  On the form, fill in the fields.

<table id="table_lf5_c3d_4z"><thead><tr><th>

Property

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Yes

</td><td>

Name for the IdP. This IdP is the auto redirect sys id.

</td></tr><tr><td>

Active

</td><td>

Yes

</td><td>

Active should be set to true for the IdP to be used for authentication.**Note:** The option to set this property only comes after a successful test connection.

</td></tr><tr><td>

Default

</td><td>

No

</td><td>

Auto Redirect IdP, formerly known as the Primary IdP, automatically redirects users to access the base instance URL. This property sets this IdP configuration as the default.

</td></tr><tr><td>

Auto Redirect IdP

</td><td>

No

</td><td>

IdP configuration that you can set as the Auto Redirect IdP.**Note:** If you make a new Auto Redirect IdP configuration active, the**glide\_sso\_id** cookie updates with the new Auto Redirect IdP. The **glide.authenticate.sso.update.idp.cookie** system property, automatically enabled, controls this feature.

</td></tr><tr><td>

Identity Provider URL

</td><td>

Yes

</td><td>

URL to your IdP. Each IdP URL must be unique.

</td></tr><tr><td>

Identity Provider's AuthnRequest

</td><td>

Yes

</td><td>

URL to the HTTP-Redirect binding obtained from the SingleSignOnService element.

</td></tr><tr><td>

Identity Provider's SingleLogoutRequest

</td><td>

No

</td><td>

URL obtained from the SingleLogoutService element.

</td></tr><tr><td>

ServiceNow Homepage

</td><td>

Yes

</td><td>

URL, including the login page, of the instance for which the IdP authenticates. For example: https://yourinstance.service-now.com/navpage.do

</td></tr><tr><td>

Entity ID/Issuer

</td><td>

Yes

</td><td>

Base URL, excluding the login page of the instance for which the IdP authenticates. For example: https://yourinstance.service-now.com/

</td></tr><tr><td>

Audience URI

</td><td>

Yes

</td><td>

Base URL, excluding the login page of the instance for which the IdP authenticates. For example: https://yourinstance.service-now.com/

</td></tr><tr><td>

NameID Policy

</td><td>

Yes

</td><td>

Value of the NameIDFormat element the integration uses.

</td></tr><tr><td>

External logout redirect

</td><td>

No

</td><td>

URL where the integration redirects users after they log out.

</td></tr><tr><td>

Failed Requirement Redirect

</td><td>

No

</td><td>

URL for redirecting failed authentication requests. By default, this is the URL endpoint of an error page or logout page configured in the IdP. You can populate this value in the glide.authenticate.failed\_requirement\_redirect field.

</td></tr></tbody>
</table>7.  Encryption And Signing tab

    **Note:** Use your own certificates for the encryption and signing.

    ![Encryption and Signing tab](../../authentication/images/encryption-signing.png)

    |Property|Description|
    |--------|-----------|
    |Signing/Encryption Key Alias|Alias of the key entry stored in [SAML 2.0 SP Keystore](t_CreatingAServiceProviderKeyStore.md).|
    |Signing Key Password|Password of the key entry stored in [SAML 2.0 SP Keystore](t_CreatingAServiceProviderKeyStore.md).|
    |Encrypt Assertion|Check box to encrypt the assertion in the SAML response. The metadata generated for the IDP embeds the x509 certificate, which the IDP uses to encrypt the assertion in the SAML response that it generates.|
    |Signing Signature Algorithm|URL that points to the SAML 2.0 Identity Provider AuthnRequest Consumer for eSignature Authentication.|
    |Sign AuthnRequest|Check box to enable the IdP single-sign on service to receive a signed AuthnRequest.|
    |Sign LogoutRequest|Check box to enable the IdP single-sign on service to receive a signed LogoutRequest.|

8.  User Provisioning tab

    ![User Provisioning Tab.](../../authentication/images/user-provisioning.png)

    |Property|Description|
    |--------|-----------|
    |Auto Provisioning User|Automatic user provisioning, creates the users when user doesn't exists in the instance User Table based on the information provided by the IdP.|
    |Update User Record Upon Each Login|Update to user information in the instance User table with the information in the IdP each time that the user logs in using SAML.|

9.  Advanced tab

    ![Advanced tab](../../authentication/images/advanced.png)

<table id="table_aqk_mnd_4z"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Field

</td><td>

Field on the User table that contains the value that the IdP requires to identify the user. This unique id is part of the response. For example, a user name, employee id, and so on. In the sys user table, this unique id is matched with the user details.

</td></tr><tr><td>

NameID Attribute

</td><td>

Field that you leave empty unless you configure a new NameID policy. If you configure a new policy, the system requires the User table it must use to identify the user logging in. The system matches the NameID token to the name of that User table field.

</td></tr><tr><td>

Create AuthnContextClass

</td><td>

Check box to specify a particular context class such as Password Protected Transport. If the check box is cleared, the IdP selects the most appropriate context class.

</td></tr><tr><td>

AuthnContextClassRef Method

</td><td>

URN of the login mechanism that you want the IdP to use to authenticate users.

</td></tr><tr><td>

Force AuthnRequest

</td><td>

Check box to force AuthnRequests to occur.

</td></tr><tr><td>

Is Passive AuthnRequest

</td><td>

Check box if the AuthnRequest is passive.

</td></tr><tr><td>

Single Sign-On Script

</td><td>

Single Sign-On script. The default is MultiSSOV2\_SAML2\_custom.

</td></tr><tr><td>

Sign Logout Response

</td><td>

Logout response details in this field.

</td></tr><tr><td>

Clock Skew

</td><td>

Nnumber of seconds between the two attributes that make up the SAMLResponse nonce. The default is 60. A valid SAMLResponse must fall between the notBefore and notOnOrAfter date-time values. See Sample SAML 2 Response with the SubjectConfirmation and SubjectConfirmationData Elements and Sample SAML 2 Response with the AudienceRestrictions and Audience Elements for a sample SAMLResponse message.

</td></tr><tr><td>

Protocol Binding for the IDP's SingleLogoutReuqest

</td><td>

One of the supported values listed in the Binding attribute from the SingleLogoutService element.

</td></tr><tr><td>

Metadata URL from which IDP properties are imported

</td><td>

IdP properties import from this URL. If set, it enables the automatic import of SAML certificate from the IdP if the previous certificate has expired. **Note:** If you upgrade from SAML2 Update 1 to Multi-Provider SSO or if you manually set up your SSO connection, the IdP Metadata URL does not automatically populate.

</td></tr><tr><td>

Request

</td><td>

Unique id as part of request. The id can be a user name, employee id, and so on.**Note:** Both redirect and post binding is supported for request. The option to set this field only appears after a successful test connection. For more information, see [Test IdP connections](../../single-sign-on/task/t_TestIdPConnections.md).

</td></tr><tr><td>

Response

</td><td>

Unique id as part of response. The id can be a user name, employee id, and so on. **Note:** Both redirect and post binding is supported for response. The option to set this field only appears after a successful test connection. For more information, see [Test IdP connections](../../single-sign-on/task/t_TestIdPConnections.md).

</td></tr></tbody>
</table>10. Select **Test Connection** at the upper-right corner of the page.

11. Enter your credentials.

    The SSO Logout Test Results are displayed.

12. Select **Activate** to activate the configuration.


