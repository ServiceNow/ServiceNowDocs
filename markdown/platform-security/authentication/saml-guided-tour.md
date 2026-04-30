---
title: SAML Guided Tour
description: Use the SAML Guided Tour to configure SAML for single sign-on.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# SAML Guided Tour

Use the SAML Guided Tour to configure SAML for single sign-on.

SAML Guided tour helps you to get trained and configure the SSO for your ServiceNow® instance. Admins can select the guided tour to quickly know the required actions when configuring SSO for the instances.

Before using the guided tour, you must configure a SAML application in your preferred Identity Provider, such as Okta, Microsoft Azure, ADFS, and so on. To learn how to configure a SAML application, refer the following documentation:

-   Okta: For Okta, you must perform the following:
    -   [Add an Okta SAML application](https://help.okta.com/oag/en-us/Content/Topics/Access-Gateway/add-app-saml-pass-thru-add-okta.htm)
    -   [Configure SAML 2.0 for ServiceNow®](https://saml-doc.okta.com/SAML_Docs/How-to-Configure-SAML-2.0-for-ServiceNow.html)
-   Microsoft Azure: [Single sign-on \(SSO\) integration with ServiceNow®](https://learn.microsoft.com/en-us/azure/active-directory/saas-apps/servicenow-tutorial)
-   Ping: [Configuring SAML SSO with ServiceNow®](https://docs.pingidentity.com/bundle/configuration_guides/page/dqw1619131345786.html)
-   ADFS: [Integration with SAML 2.0](../../saml/concept/c_ADFSIntegrationWithSAML2.0.md)

To use the SAML Guided tour, activate the Integration - Multiple Provider Single Sign-On Installer plugin. For more information see, [Activate Multi-Provider SSO plugin](../task/t_ActivateMultipleProviderSSO.md).

To use the SAML Guided Tour, follow these steps:

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Provider**.
2.  Click **New**.
3.  Select **SAML**.
4.  Click the **Help** icon.
5.  Click **Take a Tour**.

SAML Guided tour use a series of steps that span across multiple pages to complete the configuration, following the steps and instructions provided as part of the tour and complete the tour. To know more about SAML configuration, see [SAML 2.0 configuration using Multi-Provider SSO](../task/t_CreateASAML2Upd1SSOConfigMultiSSO.md).

