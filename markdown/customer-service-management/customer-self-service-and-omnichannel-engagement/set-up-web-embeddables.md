---
title: Set up Web Embeddables
description: Learn how to set up the Web Embeddables on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/set-up-web-embeddables.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Set up Web Embeddables

Learn how to set up the Web Embeddables on your ServiceNow instance.

## Setup tasks

Before you configure a component instance, complete the following tasks:

1.  Activate the plugins that enable Web Embeddables. See [Activate Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/act-web-embeddables.md).
2.  Set up a custom URL so that embedded components remain accessible when third-party cookies are turned off. See [Set up a custom URL as the instance URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/set-up-custom-url.md).
3.  Authenticate the components. Use OpenID Connect \(OIDC\) to log users in and out automatically. If your website doesn't use OIDC, use a JSON Web Token \(JWT\). See [Authenticate the ServiceNow components using OIDC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/auth-sn-webcomponents-non-oidc.md).
4.  Configure the component instance. See [Configure the ServiceNow component instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-servicenow-web-components-instance.md).
5.  Configure CORS rules so that your website can make requests to your instance. See [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-cors-for-web-components.md).

To see a component on a test page before you finish the setup, see [Test the ServiceNow components in a sandbox environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/test-sn-comp-we.md).

## Topics by scenario

|Scenario|Topics|
|--------|------|
|Your website uses OIDC to sign in users|[Activate Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/act-web-embeddables.md), [Set up a custom URL as the instance URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/set-up-custom-url.md), [Authenticate the ServiceNow components using OIDC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/authenticate-sn-webcomponents-oidc.md), [Configure the ServiceNow component instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-servicenow-web-components-instance.md), and [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-cors-for-web-components.md)|
|Your website doesn't use OIDC|[Activate Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/act-web-embeddables.md), [Set up a custom URL as the instance URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/set-up-custom-url.md), [Non OIDC authentication for ServiceNow components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/auth-sn-webcomponents-non-oidc.md), [Configure the ServiceNow component instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-servicenow-web-components-instance.md), and [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-cors-for-web-components.md)|
|You want to test components on a sandbox instance|[Test the ServiceNow components in a sandbox environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/test-sn-comp-we.md)|

## Next steps

Create a module and add components. See [Configure module in Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-module.md) and [Configure web components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/config-web-componts.md).

