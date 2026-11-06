---
title: Pre-work for Continuous Authentication
description: Perform the following pre-work before using Continuous Authentication \(CA\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/pre-work-ca.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Continuous Authentication \(CA\), Zero Trust Access, Access Management]
---

# Pre-work for Continuous Authentication

Perform the following pre-work before using Continuous Authentication \(CA\).

CA is built on ServiceNow's zero trust access security architecture that aims to enhance security by verifying that the user remains who they claim to be, even after the initial authentication process.

**Note:** You must install the **Zero Trust - Continuous Authentication** \(`com.snc.zero_trust_continuous_authentication`\) to opt in to CA, which requires a license.

CA configuration can be performed based on the following:

-   [LDAP or Local login \(Username and Password\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/pre-work-ca.md)
-   [SSO login \(SAML or OIDC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/pre-work-ca.md).

## CA for local login

When the users are performing local login and to verify the identity of the users, MFA is used as an authentication mechanism. If the users haven't set up MFA, it is compulsory to complete the setup.

**Note:**

-   From Yokohama, MFA is enforced for users for every login to ServiceNow performing local login.
-   Make sure the MFA properties are Active and configured based on your requirement. To learn more about MFA properties, see [Multi-factor Authentication system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/mfa-properties.md).

To learn more, see [High assurance session for non-SSO login](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/high-assurance-non-sso-logins.md).

## CA for SSO login

When the users are performing SSO based login \(SAML or OIDC\). To verify the identity of the users, the same SSO used during initial login is shown as the reverification with re-authentication or IdP's MFA.

**Note:**

-   You must install the **Zero Trust - Continuous Authentication** \(`com.snc.zero_trust_continuous_authentication`\) to opt in to CA, which requires a license.
-   Activate the Integration - Multiple Provider Single Sign-On Installer \(**com.snc.integration.sso.multi.installer**\) plugin.

You must configure the identity provider \(IdP\) for CA as follows:

-   Enable the check box that must be set on a given multi SSO record to validate that the set is ready for using CA.\[Omitted image "ca-tab.png"\] Alt text: Continuous Authentication - tab information
-   For OIDC, CA relies on redirecting back to the `api/now/continuous_authentication/high_assurance/oidc/consumer` endpoint, which must be configured on the IdP. Both re-authentication and IdP's MFA options are available.
-   For SAML, the SSO records use the default re-authentication script for all Identity Providers \(IdP\) to support re-authentication.

    **Note:**

    -   To configure step up for **Okta** you can use the **ContinuousAuth\_Okta\_StepUp\_Script** in the IdP record. To learn more, see this [documentation](https://developer.okta.com/docs/guides/step-up-authentication/main/).
    -   To configure step up for **Entra ID** or **Azure** you can use the **ContinuousAuth\_Azure\_StepUp\_Script** and add the required claim. To learn more, see this [documentation](https://learn.microsoft.com/en-us/entra/identity-platform/developer-guide-conditional-access-authentication-context).

To learn more, see [High assurance for SSO login](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/high-assurance-sso-logins.md).

**Related topics**  


[Exploring Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/explore-continuous-auth.md)

[Activate Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/activate-continuous-authentication.md)

[Configure Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/configure-ca.md)

