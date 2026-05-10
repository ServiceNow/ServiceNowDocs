---
title: SAML 2.0 configuration using Multi-Provider SSO
description: You can create or update a SAML 2.0 SSO configuration from the Multi-Provider SSO feature.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# SAML 2.0 configuration using Multi-Provider SSO

You can create or update a SAML 2.0 SSO configuration from the Multi-Provider SSO feature.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## About this task

**Note:** New to the Jakarta release, you must validate your configuration by using the Test Connection functionality before you can activate your IdP configuration. You can still use the Update functionality to save your configuration data, but it is not an active configuration without a successful test connection.

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Do one of the following options.

    -   To update a configuration, click an SSO configuration record.
    -   To create a new configuration, click **New** &gt; **SAML**.
3.  Enter the IdP information by one of the following methods.

<table id="choicetable_okg_pdd_4z"><tbody><tr><td id="d226129e119">

**Using a metadata descriptor URL**

</td><td>

Click the URL check box and enter the URL of the IdP that you are using.

</td></tr><tr><td id="d226129e128">

**Using metadata descriptor XML file**

</td><td>

Click the XML check box and paste in the XML data generated from the IdP you are using.

</td></tr><tr><td id="d226129e137">

**Entering metadata manually**

</td><td>

Close the popup window and manually enter the data in the property fields.

</td></tr></tbody>
</table>    **Note:** All required fields must be filled-in on the Identity Provider form.

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

Enter the name for the IdP. This IdP is the auto redirect sys id.

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

The Auto Redirect IdP, formerly known as the Primary IdP, automatically redirects users to access the base instance URL. This property sets this IdP configuration as the default.

</td></tr><tr><td>

Auto Redirect IdP

</td><td>

No

</td><td>

Sets this IdP configuration as the Auto Redirect IdP.**Note:** If you make a new Auto Redirect IdP configuration active, the**glide\_sso\_id**cookie updates with the new Auto Redirect IdP. The **glide.authenticate.sso.update.idp.cookie** system property, automatically enabled, controls this feature.

</td></tr><tr><td>

Identity Provider URL

</td><td>

Yes

</td><td>

Enter the URL to your IdP. Each IdP URL must be unique.

</td></tr><tr><td>

Identity Provider's AuthnRequest

</td><td>

Yes

</td><td>

Enter the URL to the HTTP-Redirect binding obtained from the SingleSignOnService element.

</td></tr><tr><td>

Identity Provider's SingleLogoutRequest

</td><td>

No

</td><td>

Enter the URL obtained from the SingleLogoutService element.

</td></tr><tr><td>

ServiceNow Homepage

</td><td>

Yes

</td><td>

Enter the URL, including login page, of the instance for which the IdP authenticates. For example: https://yourinstance.service-now.com/navpage.do

</td></tr><tr><td>

Entity ID/Issuer

</td><td>

Yes

</td><td>

Enter the base URL, excluding login page. of the instance for which the IdP authenticates. For example: https://yourinstance.service-now.com/

</td></tr><tr><td>

Audience URI

</td><td>

Yes

</td><td>

Enter the base URL, excluding login page. of the instance for which the IdP authenticates. For example: https://yourinstance.service-now.com/

</td></tr><tr><td>

NameID Policy

</td><td>

Yes

</td><td>

Enter the value of the NameIDFormat element the integration uses.

</td></tr><tr><td>

External logout redirect

</td><td>

No

</td><td>

Enter the URL where the integration redirects users after they log out.

</td></tr><tr><td>

Failed Requirement Redirect

</td><td>

No

</td><td>

Enter the URL for redirecting failed authentication requests. By default, this is the URL endpoint of an error page or logout page configured in the IdP. You can populate this value in the glide.authenticate.failed\_requirement\_redirect field.

</td></tr><tr><td>

Client Type

</td><td>

No

</td><td>

Choose the client type, based on the type of your client. Options:**Iframe Embedded**.**Note:** If client type field is required for your configuration, you can edit the form and add the field. To know more, see [Configure client type for OAuth and SSO records](../../authentication/concept/client-type.md).

</td></tr></tbody>
</table>4.  Encryption And Signing tab

    **Note:**

    -   You should use your own self-signed or CA-signed certificate. The following types of certificates are supported:
        -   [BCFKS \(FIPS-compliant\) keystore](../../saml/task/create-fips-certificate-for-saml.md) \(Recommended\)
        -   Java keystore
    -   The **FIPS approved mode** requires different certificates for **Encryption** and **Signing**.
    -   Use different certificates for **Encryption** and **Signing** for a better security posture.
    -   While using the certificates, make sure to update the following system properties with the sys\_id of the certificates \(x.509 Certificates\):
        -   **Signing** \(`glide.authenticate.sso.saml2.keystore`\)
        -   **Encryption** \(`glide.authenticate.sso.saml2.encryption.keystore`\)
    -   Make sure to update the key alias and key password of the **Signing** and **Encryption** keystores in the Identity Provider record and generate the metadata \(Select **Generate Metadata**\).
    -   Upload the signing and encryption certificates present in the generated metadata \(XML\) to the Identity Provider.
    -   To configure certificate expiry notification, use **Notify on expiration** and **Groups to notify on expiration**, and set the notification timing using **Warn in days to expire** and **Frequency**.
    ![Encryption And Signing](../../authentication/images/encryption-signing.png)

    |Property|Description|
    |--------|-----------|
    |Signing Key Alias|Enter the Signing alias of the key entry stored in [SAML 2.0 SP Keystore](../../saml/task/t_CreatingAServiceProviderKeyStore.md).|
    |Signing Key Password|Enter the Signing password of the key entry stored in [SAML 2.0 SP Keystore](../../saml/task/t_CreatingAServiceProviderKeyStore.md).|
    |Encryption Key Alias|Enter the Encryption alias of the key entry stored in [SAML 2.0 SP Keystore](../../saml/task/t_CreatingAServiceProviderKeyStore.md).|
    |Encryption Key Password|Enter the Encryption password of the key entry stored in [SAML 2.0 SP Keystore](../../saml/task/t_CreatingAServiceProviderKeyStore.md).|
    |Encrypt Assertion|Select the check box to encrypt the assertion in the SAML response. The metadata generated for the IDP embeds the x509 certificate, which the IDP uses to encrypt the assertion in the SAML response that it generates.|
    |Signing Signature Algorithm|Enter the URL that points to the SAML 2.0 Identity Provider AuthnRequest Consumer for eSignature Authentication.|
    |Sign AuthnRequest|Select the check box to enable the IdP single-sign on service to receive a signed AuthnRequest.|
    |Sign LogoutRequest|Select the check box to enable the IdP single-sign on service to receive a signed LogoutRequest.|
    |Sign Logout Response|Select the check box to enable the IdP single-sign on service to receive a signed Logout Response.|

5.  User Provisioning tab

    |Property|Description|
    |--------|-----------|
    |Auto Provisioning User|Enable automatic user provisioning, creates the users when user doesn't exists in the instance User Table based on the information provided by the IdP.|
    |Update User Record Upon Each Login|Updates user information in the instance User table with the information in the IdP each time the user logs in using SAML.|

6.  Advanced tab

    ![Advanced tab](../../authentication/images/advanced.png)

<table id="table_aqk_mnd_4z"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Field

</td><td>

Enter the field on the User table that contains the value the IdP requires to identify the user. This is a unique id as part of the response. For example, user name, employee id, and so on. In the sys user table, this unique id is matched with the user details.

</td></tr><tr><td>

NameID Attribute

</td><td>

Leave this field blank unless you configure a new NameID policy. If you configure a new policy, the system requires the User table it must use to identify the user logging in. The system matches the NameID token to the name of that User table field here.

</td></tr><tr><td>

Create AuthnContextClass

</td><td>

Select the check box to specify a particular context class such as Password Protected Transport. If the check box is cleared, the IdP selects the most appropriate context class.

</td></tr><tr><td>

AuthnContextClassRef Method

</td><td>

Enter the URN of the login mechanism you want the IdP to use to authenticate users.

</td></tr><tr><td>

Force AuthnRequest

</td><td>

Select the check box to force AuthnRequests to occur.

</td></tr><tr><td>

Is Passive AuthnRequest

</td><td>

Select the check box if the AuthnRequest is passive.

</td></tr><tr><td>

Single Sign-On Script

</td><td>

Select the Single Sign-On script. The default is MultiSSOV2\_SAML2\_custom.

</td></tr><tr><td>

Sign Logout Response

</td><td>

Enter the logout response details in this field.

</td></tr><tr><td>

Clock Skew

</td><td>

Enter the number of seconds between the two attributes that make up the SAMLResponse nonce. The default is 60. A valid SAMLResponse must fall between the notBefore and notOnOrAfter date-time values. See Sample SAML 2 Response with the SubjectConfirmation and SubjectConfirmationData Elements and Sample SAML 2 Response with the AudienceRestrictions and Audience Elements for a sample SAMLResponse message.

</td></tr><tr><td>

Protocol Binding for the IDP's SingleLogoutReuqest

</td><td>

Enter one of the supported values listed in the Binding attribute from the SingleLogoutService element.

</td></tr><tr><td>

Metadata URL from which IDP properties are imported

</td><td>

The IdP properties import from this URL. If set, it enables the automatic import of SAML certificate from the IdP if the previous certificate has expired. **Note:** If you upgrade from SAML2 Update 1 to Multi-Provider SSO or if you manually set up your SSO connection, the IdP Metadata URL does not automatically populate.

</td></tr><tr><td>

Request

</td><td>

An unique id as part of request, the id can be user name, employee id, and so on.**Note:** Both redirect and post binding is supported for request. The option to set this field only appears after a successful test connection. For more information see, [Test IdP connections](t_TestIdPConnections.md).

</td></tr><tr><td>

Response

</td><td>

An unique id as part of response, the id can be user name, employee id, and so on. **Note:** Both redirect and post binding is supported for response. The option to set this field only appears after a successful test connection. For more information see, [Test IdP connections](t_TestIdPConnections.md).

</td></tr></tbody>
</table>7.  On the Continuous Authentication tab, configure the following fields:

    **Note:**

    -   The Continuous Authentication tab appears only when you install the **Zero Trust - Continuous Authentication** \(`com.snc.zero_trust_continuous_authentication`\) plugin that requires license.
    -   If you're using continuous authentication policy to protect access to table or data class, see [Continuous Authentication \(CA\)](../../authentication/concept/ca-homepage.md).
    ![Continuous Authentication - tab information](../../authentication/images/ca-tab.png)

<table id="table_vvj_d5x_4dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Continuous Authentication Configured

</td><td>

Select the check-box to set the configuration active.

</td></tr><tr><td>

Continuous Authentication Consumer URL

</td><td>

Provide the Consumer URL from the Identity Provider.

</td></tr><tr><td>

Continuous Authentication Script

</td><td>

Select the look-up icon to choose the script provided from the platform. In this configuration, for SAML: **MultiSSOv2\_SAML2\_ContinuousAuth\_custom**

</td></tr></tbody>
</table>
