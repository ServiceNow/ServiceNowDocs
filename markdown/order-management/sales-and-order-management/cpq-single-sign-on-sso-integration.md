---
title: Single sign-on \(SSO\) integration
description: If you intend to use CPQ for a headless use case \(such as exposing CPQ on a website or eCommerce platform\), please fill out and submit an SSO Setup Request Form that details the identity provider \(IdP\) you are using for single sign-on \(SSO\).
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, price, quote apps, Configure, Sales and Order Management]
---

# Single sign-on \(SSO\) integration

If you intend to use CPQ for a headless use case \(such as exposing CPQ on a website or eCommerce platform\), please fill out and submit an SSO Setup Request Form that details the identity provider \(IdP\) you are using for single sign-on \(SSO\).

This process involves:

-   Creating an app for CPQ in your IdP tool of choice. See the steps and links below.
-   Sharing parameters and users from the app with the CPQ team. The team will complete the provisioning process using the parameters that you send.
-   Testing and confirming that the SSO redirect works as expected.

Note the following considerations:

-   CPQ can now support SSO with any IdP that supports OAuth2 with OpenID Connect \(OIDC\).
-   CPQ is not compatible with SAML.
-   Your IdP client must be up to date.
-   Users who have been added to CPQ before SSO was implemented may need to be added again.
-   These steps are not required if you are using CPQ with Salesforce.

## Configuring Google SSO

CPQ supports Google for both personal and business single sign-on. If you use Google IdP for identity verification, all we need are the names and email addresses of your users.

## Configuring Okta SSO

To set up an application that supports the Authorization code flow for CPQ, start by following the Okta Developer instructions: [Implement authorization by grant type: set up your app](https://developer.okta.com/docs/guides/implement-grant-type/authcode/main/#set-up-your-app)

For the redirect URL, specify your CPQ URL, append `/login/oauth2/code/`, and then append your `-okta` subdomain. So if your URL is `example.test.logik.io`, your redirect URL would be `https://example.test.logik.io/login/oauth2/code/example-okta`.

Note your client ID, client secret, redirect URL, and Okta domain.

**Note:** To confirm that your Okta domain is accurate, you can confirm that the OpenID connection metadata is visible by visiting `https://{oktaDomain}/.well-known/openid-configuration`. You should see a JSON file with information about the authorization server endpoints.

Provide these values together with any user details, such as name and email, for users that you want to test with. The CPQ team will schedule a brief call with you to obtain your client secret. The team will complete the provisioning process from there.

**Note:** Users' email addresses will be used for authentication. These are case sensitive, so make sure that the email addresses you provide are accurate.

When your CPQ point of contact has confirmed that setup is complete, try to visit your tenant-specific CPQ URL. You should see a redirect flow that brings you to an Okta consent screen to allow access to your CPQ app.

## Configuring Entra ID SSO

Register an app by following the instructions on the following Microsoft Entra documentation website:

[Register an application in Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app)

In the **Redirect URI** section of the Microsoft Entra registration page, in the **Select a platform** menu, select **Web**. For the redirect URI, enter your tenant-specific URL, append `/login/oauth2/code/`, and then append `<your subdomain>-entra`. For example, if your URL is `example.test.logik.io`, your redirect URI is `https://example.test.logik.io/login/oauth2/code/example-entra`.

Make sure to select **ID tokens** on the Authentication tab of your app. For more information about OIDC, see the following Microsoft Entra documentation website: [OpenID Connect on the Microsoft identity platform](https://learn.microsoft.com/en-us/entra/identity-platform/v2-protocols-oidc).

Note your client ID, client secret, and your Authority URL.

**Note:** Make sure you note the client secret at this time. It won't be available to you later.

For information about how to validate your Authority URL, see "Find your app's OpenID configuration document URI" at the Microsoft Entra documentation website: [OpenID Connect on the Microsoft identity platform](https://learn.microsoft.com/en-us/entra/identity-platform/v2-protocols-oidc). To get the correct issuer in the metadata, make sure to include `/v2.0` at the end. You should be able to see the metadata and validate your issuer URL by visiting it in a browser with `/.well-known/openid-configuration` appended to it. For example: `https://login.microsoftonline.com/c7dd9346-1cfc-4bd8-a34c-a066c8bc0477/v2.0/.well-known/openid-configuration`.

**Note:** It may be possible to directly associate your users with the application via the **Manager** &gt; **Users and groups** &gt; **Add user/group** option in your application.

![Users and groups interface](../../servicenow-cpq/images/cpq-single-sign-on-integration.png)

Optionally, add an app role for the users whom you wish to test with. For more information, see "Add a user account to your directory, and add that account to an appRole" on the following Microsoft Entra documentation website: [Add sign-in with Microsoft Entra account to a Spring web app](https://learn.microsoft.com/en-us/azure/developer/java/spring-framework/configure-spring-boot-starter-java-app-with-entra?toc=%2Fentra%2Fidentity-platform%2Ftoc.json&bc=%2Fentra%2Fidentity-platform%2Fbreadcrumb%2Ftoc.json#create-microsoft-entra-instance)

On the SSO Setup Request Form, provide the client ID, Authority URL, and redirect URl together with user details \(email, name\) for the users you wish to test with. The CPQ team will schedule a brief call with you to obtain your client secret.

By default, each user’s emails will act as their identifiers, but it may be possible to use a different identifier in a user profile. The fields that can be used as identifiers are limited by what’s available at the `user_info` endpoint defined in the well-known/openid-configuration URL described above. For more information about the `user_info` endpoint, see the following Microsoft Entra documentation website: [Microsoft identity platform UserInfo endpoint](https://learn.microsoft.com/en-us/entra/identity-platform/userinfo).

Once your CPQ point of contact has confirmed that setup is complete, try to visit your tenant-specific CPQ URL. You should see a redirect flow that brings you to an Entra ID consent screen to allow access to your CPQ app.

<table id="table_rhp_c2y_23c"><thead><tr><th>

Issue

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

The issuer does not match the expected value. For example, the issue is `sts.microsoft.net` instead of `login.microsoftonline.com`.

</td><td>

-   Make sure that your issuer URL includes `/v2.0` after the tenant ID.
-   Update the application manifest to set the **accessTokenAcceptedVersion** to **2**.

</td></tr><tr><td>

Admin is redirected to http://logik.ai, despite being set up correctly.

</td><td>

In your manifest, set the **acceptMappedClaims** parameter to **true** in your manifest.

</td></tr></tbody>
</table>## Configuring another IdP

CPQ can now support SSO with any IdP that supports OAuth2 with OpenID Connect \(OIDC\). In the SSO Setup Request Form, provide details about your preferred IdP tool and our team will connect with you to ensure it is properly integrated with CPQ.

