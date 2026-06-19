---
title: Custom URL with Identity Provider
description: Set your custom URL with the Identity Provider to enable the user to login with their IdP's.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/custom-url-with-multiple-identity-providers.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Custom instance URLs, Authentication, Access Management]
---

# Custom URL with Identity Provider

Set your custom URL with the Identity Provider to enable the user to login with their IdP's.

## Before you begin

Role required: custom\_url\_admin

## Procedure

1.  Navigate to **All** &gt; **Custom URL** &gt; **Custom URLs**.

2.  Click **New**.

3.  Provide the details of the IdP in the **Identity Provider** field.

    For information about other fields, see [Set a custom URL as the instance URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configure-custom-url.md). \[Omitted image "new-custom-url-idp.png"\] Alt text: A Custom URL"configuration interface with fields for domain name, status, service portal, and identity provider \(set to "GOOGLE OIDC"\), along with helpful setup links.

4.  Click **Create**.

    The record is created and displayed on the Custom URL page.

    \[Omitted image "custom-url-with-odp.png"\] Alt text: Custom URL record with Identity Provider

    When the custom URL is accessed, the user is redirected to the Identity Provider that is configured. In this case, accessing the `snowtest.com`, the user is navigated to the **Employee Center**, and then redirected to the Google Identity Provider.

    **Note:**

    -   If the Service Portal field is empty and the Identity Provider field is defined, when the user accesses the custom URL, the user is directly navigated to the configured Identity Provider.
    -   If both the Service Portal and Identity Provider field is defined, when the user accesses the custom URL with the Service Portal that is defined, the user is navigated to the configured Identity Provider.
    -   If both the Service Portal and Identity Provider field is defined, when the user accesses the custom URL with the different portal that is not defined, the user is navigated to the auto-redirect Identity Provider if configured on the instance.
5.  Use the credentials to login to the application.


