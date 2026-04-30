---
title: Pre-work for Continuous Authentication
description: Ensure to perform the following pre-work before using Continuous Authentication \(CA\).
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Continuous Authentication, Zero Trust Access, Access Management]
---

# Pre-work for Continuous Authentication

Ensure to perform the following pre-work before using Continuous Authentication \(CA\).

CA is built on ServiceNow's zero trust access security architecture that aims to enhance security by ensuring that the user remains who they claim to be, even after the initial authentication process.

**Note:** You must install the **Zero Trust - Continuous Authentication** \(`com.snc.zero_trust_continuous_authentication`\) for opting CA which requires a license.

CA configuration can be performed based on the following:

-   [LDAP or Local login \(Username and Password\)](pre-work-ca.md#section_jqr_nhw_ycc)
-   [SSO login \(SAML or OIDC\)](pre-work-ca.md#section_plh_4hw_ycc).

## CA for Local login

When the users are performing local login and to verify the Identity of the users, MFA is used as an authentication mechanism. If the users haven't setup MFA, it is compulsory to complete the setup.

**Note:**

-   From Yokohama, MFA is enforced to users for every login to ServiceNow performing local login.
-   Make sure the MFA properties are Active and configured based on your requirement. To know more about MFA properties, see [Multi-factor authentication system properties](../reference/mfa-properties.md).

To know more, see [High Assurance session for non-SSO login](high-assurance-non-sso-logins.md).

## CA for SSO login

When the users are performing SSO based login \(SAML or OIDC\). To verify the Identity of the users, the same SSO used during initial login is shown as the re verification with re-authentication or IdP's MFA.

**Note:**

-   You must install the **Zero Trust - Continuous Authentication** \(`com.snc.zero_trust_continuous_authentication`\) for opting CA which requires a license.
-   Activate the Integration - Multiple Provider Single Sign-On Installer \(**com.snc.integration.sso.multi.installer**\) plugin.

You must configure the IDP for CA as follows:

-   Enable the check box that is required to be set on a given multi SSO record to validate that set ready for using CA.![Continuous Authentication - tab information](../images/ca-tab.png)
-   For OIDC, CA relies on redirecting back to the `api/now/continuous_authentication/high_assurance/oidc/consumer` endpoint, which must be configured on the IDP. Both re-authentication and IdP's MFA options are available.
-   For SAML, the SSO records use the default re-athentication script for all Identity Providers \(IdP\) to support re-authentication.

    **Note:**

    -   To configure step up for **Okta** you can use the **ContinuousAuth\_Okta\_StepUp\_Script** in the IdP record. To know more, see this [documentation](https://developer.okta.com/docs/guides/step-up-authentication/main/).
    -   To configure step up for **Entra ID** or **Azure** you can use the **ContinuousAuth\_Azure\_StepUp\_Script** and add the required claim. To know more, see this [documentation](https://learn.microsoft.com/en-us/entra/identity-platform/developer-guide-conditional-access-authentication-context).

To know more, see [High Assurance for SSO Login](high-assurance-sso-logins.md).

**Related topics**  


[Exploring Continuous Authentication](explore-continuous-auth.md)

[Activating Continuous Authentication](../task/activate-continuous-authentication.md)

[Configuring Continuous Authentication](../task/configure-ca.md)

