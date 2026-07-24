---
title: Third party token grant
description: The third party token grant enables ServiceNow to accept identity tokens from trusted external identity providers, such as Azure AD or Okta. Third party token grant provides secure, token-based access. This method supports secure access and single sign-on \(SSO\) in federated authentication scenarios.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/third-party-id-token.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Inbound Integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Third party token grant

The third party token grant enables ServiceNow to accept identity tokens from trusted external identity providers, such as Azure AD or Okta. Third party token grant provides secure, token-based access. This method supports secure access and single sign-on \(SSO\) in federated authentication scenarios.

-   **Ideal for:**

    Federated authentication scenarios where ServiceNow trusts identity tokens issued by external identity providers such as Azure AD or Okta.

-   **How it works:**

    The client application obtains an ID token from a trusted third-party identity provider and includes it in the Authorization header when making API requests to the ServiceNow instance to validate the token and, if trusted, grants access based on the identity it asserts—enabling seamless single sign-on \(SSO\) and federated authentication across systems.


To know more about how to use accounts from a third-party identity provider \(IdP\) to access the ServiceNow API, see [Third party token workflow for user accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/third-party-token-worflow-for-user-accounts.md).

