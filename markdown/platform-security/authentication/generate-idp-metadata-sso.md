---
title: Generate SP metadata for SAML/SSO custom URL installations
description: A SAML or SSO installation needs the SP metadata generated for the IdP before the custom URL instance generates.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Custom instance URLs, Authentication, Access Management]
---

# Generate SP metadata for SAML/SSO custom URL installations

A SAML or SSO installation needs the SP metadata generated for the IdP before the custom URL instance generates.

## Before you begin

Role required: custom\_url\_admin

The IdP needs SP metadata for the instance to authenticate and forward requests.

**Note:** Adding the Assertion Consumer Service URL \(SP login URL\) might be different for each IdP \(Azure, ADFS, or Okta\).

## Procedure

1.  Choose your installed SSO plugin:

<table id="choicetable_eqz_pd4_pdb"><tbody><tr><td id="d35811e84">

**Multi-Provider SSO**

</td><td>

Navigate to **Multi-Provider SSO** &gt; **Identity Providers**. Choose an IdP and click the **Generate Metadata** button. The integration automatically generates the instance's SP metadata from the system property settings.

</td></tr><tr><td id="d35811e105">

**SAML 2 SSO**

</td><td>

Navigate to **SAML 2 Single Sign-on** &gt; **Metadata**. The integration automatically generates the instance's SP metadata from the system property settings.

</td></tr></tbody>
</table>2.  Copy the SP metadata in the text box.

    For example:

    ```
    <EntityDescriptor xmlns="urn:oasis:names:tc:SAML:2.0:metadata" entityID="https://yourinstance.service-now.com">
     	<SPSSODescriptor AuthnRequestsSigned="false" WantAssertionsSigned="true" protocolSupportEnumeration="urn:oasis:names:tc:SAML:2.0:protocol">
    		<SingleLogoutService Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect" Location="https://yourinstance.service-now.com/navpage.do" />
    		<NameIDFormat>urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress</NameIDFormat>
    		<AssertionConsumerService isDefault="true" index="0" Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST" Location="https://yourinstance.service-now.com/navpage.do" />
    		<AssertionConsumerService index="1" Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST" Location="https://yourinstance.service-now.com/consumer.do"/>
    	</SPSSODescriptor>
    </EntityDescriptor>
    ```

3.  Provide the instance SP metadata to the IdP.

    For example, SSOCircle allows a user to provide the SP metadata online.

4.  To set up custom URLs in Azure:

    1.  Go to **App Registrations**.

    2.  Select **All apps** from the menu.

    3.  Select the **ServiceNow App**.

    4.  Click settings to configure the URL.

5.  To set-up custom URLs in Okta:

    1.  Create two ServiceNow UD Okta Applications.

    2.  One Okta Application for the "service-now.com" instance URL.

    3.  One Okta Application for the custom URL.

        **Note:**

        -   Disable the **Disable Force Authentication** within the Okta configuration for the **Test Connection** to run successfully.
        -   If you're testing the Identity Provider record associated with the base URL, ensure you've to login to the instance with the base URL.
        -   If you're testing the Identity Provider associated with the Custom URL, ensure you've to login to the instance with the Custom URL.
6.  To use OAuth authentication, set up the redirect URL as all the registered custom URLs in the OAuth application endpoint configuration for the external client applications.

    The redirect URL is synonymous with the callback URL that the authorization server redirects to.

7.  To use Google reCAPTCHA service, [set up an API key pair.](https://www.servicenow.com/docs/access?context=t_ConfigureGoogleRecaptcha&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)


