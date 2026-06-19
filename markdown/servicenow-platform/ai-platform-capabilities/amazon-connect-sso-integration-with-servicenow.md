---
title: Amazon Connect SSO integration with ServiceNow
description: Single Sign-On \(SSO\) integration between Amazon Connect and ServiceNow eliminates duplicate authentication by using a shared identity provider \(IdP\) to authenticate agents automatically when they open the Amazon Connect softphone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/ai-platform-capabilities/amazon-connect-sso-integration-with-servicenow.html
release: australia
product: AI Platform Capabilities
classification: ai-platform-capabilities
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [Amazon Connect SSO, single sign-on, SAML, identity provider, Contact Control Panel]
breadcrumb: [Integrate ServiceNow Voice with Amazon Connect, Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Amazon Connect SSO integration with ServiceNow

Single Sign-On \(SSO\) integration between Amazon Connect and ServiceNow eliminates duplicate authentication by using a shared identity provider \(IdP\) to authenticate agents automatically when they open the Amazon Connect softphone.

## Amazon Connect SSO integration overview

When an agent authenticates into ServiceNow via configured IdP, an active IdP session is established. Opening the softphone forwards the SSO Login URL fromServiceNow to Amazon Connect, which initiates authentication. The IdP completes the SAML 2.0 flow using the existing session, and the Amazon Connect softphone loads without requiring any additional agent action.

If the SSO Login URL field is empty, the system falls back to standard Amazon Connect authentication. No custom code is required. The SSO capability is provided by the Streams API library, which is part of Amazon Connect, and works for both the standard Contact Control Panel \(CCP\) and the Interaction Controls Component \(ICC\) enabled voice controls.

**Note:** The SSO setup must be done in the IdP and AWS after the guided setup is completed and the basic login is working as expected.

For more information about Single Sign-On \(SSO\) configuration for ServiceNow Voice, see the [Single Sign-On configuration for ServiceNow Voice with Amazon Connect \[KB3025173\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3025173) article in the HI Knowledge Base.

## Benefits of the SSO authentication

Using the SSO authentication, agents using ServiceNow as the primary agent workspace and Amazon Connect as the contact center solution can address the following issues:

-   **Duplicate authentication**

    Agents can avoid authenticating twice, for ServiceNow and for Amazon Connect, even with both systems using the same IdP.

-   **Disruptive login popups**

    Without the SSO integration, the Amazon Connect opens an authentication pop-up, creating an inconsistent agent experience.


## SSO configuration sequence

The following configuration displays the one-time setup steps required across Okta, ServiceNow, and Amazon Connect to enable SSO.

**Note:** Okta has been used as an IdP example. The steps are similar for any other IdP.

The configuration steps are:

1.  **ServiceNow:** Install the SSO plugin and configure Okta as the IdP.
2.  **IdP: example Okta** Create a user and add the Amazon Web Services SAML application.
3.  **Amazon Connect:** Enable SAML federation and configure the IAM role and IdP.
4.  **IdP: example Okta** Retrieve the IdP-initiated SAML SSO Login URL.
5.  **ServiceNow**: Paste the SSO Login URL into the **SSO Login URL** field on the Amazon Connect instance record.

**Note:** After configuration, all three systems share the same IdP. User identity \(email or username\) must match exactly across ServiceNow and Amazon Connect for SSO to work.

The login parameter is generally the user email that must be mapped to the user name. Here's an example of how SSO is configured in Amazon Connect.

The following screen captures show the user identity fields across all three applications.



\[Omitted image "amazon-connect-instance-user.png"\] Alt text: Amazon Connect user list showing one record with login and name fields used for identity matching.



\[Omitted image "idp-okta-user.png"\] Alt text: Okta user profile showing name and email fields used for identity matching.



\[Omitted image "service-now-user.png"\] Alt text: Platform user form showing User ID, first name, last name, and email fields used for identity matching.

-   **[Configure SSO for Amazon Connect integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/ai-platform-capabilities/configure-sso-with-amazon-connect.md)**  
Configure Single Sign-On \(SSO\) between Amazon Connect and ServiceNow so that agents authenticated through a shared identity provider \(IdP\) are automatically signed into the Amazon Connect Softphone without a second login.

**Parent Topic:**[Integrate ServiceNow Voice with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/ai-platform-capabilities/integrate-ccc-amazonconnect.md)

