---
title: MFA enforcement scope
description: FAQ related to MFA enforcement scope and why it’s important.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Frequently asked questions, MFA enforcement, Multi-factor authentication, Authentication, Access Management]
---

# MFA enforcement scope

FAQ related to MFA enforcement scope and why it’s important.

1.  Which user, login, and environment types require MFA?

    From the Yokohama release onwards, with the new default secure MFA policy MFA enforced for the following scenarios:

    -   All the users except the users having **snc\_external** role.
    -   All the users performing user name and password based local or Lightweight Directory Access Protocol \(LDAP\) authentication.
    -   All customer instances, including production, subprod, and test instances, that didn’t already have an active MFA policy before the upgrade.
    The instance admin can modify the enforcement scope by changing the MFA context policy, policy criteria, or policy conditions.

2.  Is MFA required for Single-Sign-On \(SSO\) logins?

    No. With the default secure MFA policy, MFA isn’t required for SSO \(SAML, OIDC, Certificate Based Authentication\) login.

    Customers can collaborate with their Single Sign-On \(SSO\) provider \(Identity Provider, or IdP\) to enforce multi-factor Authentication \(MFA\) on the IdP side. If enforcing MFA on the IdP side isn’t feasible, customers also have the option to enable the ServiceNow platform's MFA for SSO logins by following the instructions provided in [Multi-factor Authentication with Single Sign-On](mfa-sso.md).

3.  Is MFA required for external users?

    No. With the default secure MFA policy, MFA isn’t required for users having the snc\_external role.

    -   Admins can modify this behavior and enforce MFA for external users by updating the MFA policy conditions.
    -   External users who were already undergoing MFA before the upgrade to Yokohama or later release continues to have MFA.
    -   External users can visit their profile and self-enroll for MFA.
4.  Is MFA required for Mobile App login?

    Yes. The MFA policy is applied to both web and mobile app log in with user name and password based non-SSO login.

5.  Is MFA required for non-production and test environments?

    Yes. MFA is enforced for all customer instances, including production, non-production, dev, and test environments, if there's no active MFA policy existed on the instance before upgrading to Yokohama or later versions.

6.  Is MFA required for developer instances?

    Yes. MFA is enforced for all developer instances that are on Yokohama or later release versions.

7.  Is MFA required for API authentication?

    No. From Yokohama or a later release, MFA is only required for the user name and password-based interactive user logins. This means API authentication with basic auth works without requiring MFA. It’s recommended to customers use alternative secure API authentication methods such as OAuth or mTLS. More details here.

    1.  Clone
    2.  Update set retrieval
    3.  RPA
    **Note:** To enforce MFA for API authentication, set the `glide.authenticate.multifactor.for_integrations` system property to `true`. MFA is enforced only for users who have already enrolled in MFA. Users who have not enrolled are not affected.

8.  Is there any impact on the clone setup process due to MFA?

    No, the clone setup process continues to work with user name and password and doesn't require MFA.

9.  Is there any impact on the update set retrieval due to MFA?

    No, the update set retrieval continues to work with user name and password and doesn't require MFA.

10. Is there been any impact on RPA bots accessing ServiceNow instances?

    Yes, if the RPA bot uses the interactive user name and password login to access the ServiceNow instance, it must perform MFA. Admins can add RPA bot accounts to the **MFA Exempted User Group** if they want to relax MFA for RPA bot accounts.

11. Is MFA required for the OAuth-based integrations?

    The OAuth Resource owner password credential \(ROPC\) works with user name and password without requiring MFA. For Authorization code grant type MFA is required as part of the user login flow before giving the OAuth consent.


