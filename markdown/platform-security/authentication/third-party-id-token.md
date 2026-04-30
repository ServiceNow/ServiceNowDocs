---
title: Third party token grant
description: The third party token grant enables ServiceNow to accept identity tokens from trusted external identity providers, such as Azure AD or Okta. Third party token grant provides secure, token-based access. This method supports secure access and single sign-on \(SSO\) in federated authentication scenarios.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Third party token grant

The third party token grant enables ServiceNow® to accept identity tokens from trusted external identity providers, such as Azure AD or Okta. Third party token grant provides secure, token-based access. This method supports secure access and single sign-on \(SSO\) in federated authentication scenarios.

The client application requests an ID or access token from a trusted external identity provider, such as Azure AD or Okta, and includes it in the `Authorization` header of API requests to ServiceNow®. ServiceNow® validates the token and, if trusted, grants access based on the asserted identity.

You can use accounts from a third-party identity provider \(IdP\) to access the ServiceNow® API for:

-   [Third party token workflow for user accounts](third-party-token-worflow-for-user-accounts.md)
-   [Third party token workflow for service accounts](third-party-token-workflow-for-service-accounts.md)

