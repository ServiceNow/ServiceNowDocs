---
title: Basic authentication restriction
description: Basic authentication restriction is a security feature that controls which accounts can use basic authentication on a ServiceNow instance. Administrators can review identified users and assign per-account decisions before enforcement begins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-security/authentication/basic-auth-restriction.html
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-06-18"
reading_time_minutes: 2
keywords: [basic authentication restriction, basic auth, enforcement, snc\_basic\_auth\_api\_access]
breadcrumb: [Basic authentication, API Authentication, Authentication, Access Management]
---

# Basic authentication restriction

Basic authentication restriction is a security feature that controls which accounts can use basic authentication on a ServiceNow instance. Administrators can review identified users and assign per-account decisions before enforcement begins.

The Basic Auth Restriction page provides guidance on available actions and controls the enforcement configuration. Administrators are prompted to review the identified users and take action before the enforcement period begins.

**Important:** The Basic Auth Restriction page is read-only based on its protection policy. The `security_admin` role is required to make any changes.

Navigate to **All** &gt; **Basic Auth Restriction** &gt; **Properties** to open the page.

## Actions available for identified users

Review the **Identified Users** table and set a decision for each account. The following decisions are available:

-   **Maintain current login — Basic Auth API and UI login allowed**

    The `snc_basic_auth_api_access` role is granted to the account. Basic authentication access continues when enforcement begins.

-   **Revoke Basic Auth API login — Basic Auth API login blocked and UI login allowed**

    The account is not granted the exception role. Basic auth access fails when enforcement begins.

-   **Convert to web service access only account — Basic Auth API login allowed and UI login blocked**

    The account is converted to a web service access only account. The account can't make UI logins, but basic authentication continues to work past the enforcement period. No roles are assigned.

-   **Apply default from system property**

    Basic auth access is granted or denied based on the decision configured in the global property `glide.authenticate.basic_auth.restriction.default_decision`. Review or change this on the property page.


Administrators should also review and adjust the start of the enforcement period from the **enforcement schedule job**.

## How enforcement works

Once enforcement is enabled, basic authentication requests are blocked unless the requesting account matches one of the following:

-   Accounts having Web Services Access Only \(WSAO\).
-   Accounts presenting a valid MFA one-time password.
-   Accounts having the `snc_basic_auth_api_access` role.

## Basic Auth Restriction settings

The Basic Auth Restriction page includes the following configurable settings:

-   **Default value**

    The default decision applied to new rows in the Basic Auth Exception table during the tracking period. Per-row decisions in the Basic Auth Exception table override this default.

-   **Feature toggle**

    A feature toggle for the Basic Authentication restriction feature on the instance. When unchecked \(false\), no enforcement occurs regardless of the value of `glide.authenticate.basic_auth.restriction.enforce`. Use this as an emergency disable to halt the feature without changing other settings.

-   **Enforcement toggle**

    Controls whether enforcement is active. When unchecked \(false\), accounts using basic authentication are recorded but no requests are blocked — tracking mode. When checked \(true\), basic authentication requests are blocked unless the requesting account is on the allow-list — enforcing mode. Has no effect when the feature toggle is set to false.


