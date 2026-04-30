---
title: Azure AD Integration with SAML 2.0
description: Integrate ServiceNow with Azure Active Directory \(Azure AD\).
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating SAML 2.0 with other features, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Azure AD Integration with SAML 2.0

Integrate ServiceNow with Azure Active Directory \(Azure AD\).

Integrating ServiceNow with Azure AD enables you to:

-   Control in Azure AD who has access to ServiceNow.
-   Enable users to automatically sign-in to ServiceNow with their Azure AD accounts.
-   Manage your accounts in the Azure portal.

## Prerequisities

To get started, you need the perform the following:

-   An Azure AD subscription. If you don't have a subscription, you can get a free account.
-   A ServiceNow single sign-on \(SSO\) enabled.
-   A ServiceNow instance or tenant of ServiceNow that supports San Diego versions or later.
-   A ServiceNow tenant must have the Multiple Provider Single Sign On Plugin enabled.
-   For automatic configuration, enable the multi-provider plugin for ServiceNow.

## Set of Actions for Configuration

Following are the set of actions that needs to performed to configure Azure AD:

-   Add ServiceNow from the gallery to Azure AD.
-   Configure Azure AD SSO
-   Create an Azure AD test user
-   Assign the Azure AD test user
-   Configure ServiceNow

