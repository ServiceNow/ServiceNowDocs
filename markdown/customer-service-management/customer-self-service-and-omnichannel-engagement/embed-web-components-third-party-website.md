---
title: Embed ServiceNow components instance on the third-party website
description: Embed the global code and component code for configured components on your third-party website so customers can use them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-web-components-third-party-website.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Embed ServiceNow components instance on the third-party website

Embed the global code and component code for configured components on your third-party website so customers can use them.

## Before you begin

At least one ServiceNow component must be configured in your instance. For more information, see [Configure the ServiceNow component instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-servicenow-web-components-instance.md).

Role required: none

## About this task

When you select **Get embed code** for a component instance, your instance generates two blocks of code:

-   Global code connects your website to your instance. You add it once to your website.
-   Component code adds one component instance to a page. You add it for each component instance that you want to display.

This procedure outlines the high-level steps that you must follow to embed Web Embeddables component instance on your third-party website.

## Procedure

1.  In the HTML file of your third-party website, paste the global code that you copied.

    **Note:** The global code only needs to be added once to your third-party website, even if you embed more than one component.

2.  In the global code, update the `getTokenCallBack` and `getGuestJWTTokenCallBack` functions to return the authentication token and guest token for the current user.

    The generated functions contain placeholders. For more information about authentication, see [Authenticate the ServiceNow components using OIDC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/auth-sn-webcomponents-non-oidc.md).

3.  In the HTML file of the page or section where you want the component to appear, paste the component code that you copied.

    Use the page or section that matches the group that contains the component instance in your module. If you turned on the **Enable event handler** toggle when you copied the code, the component code also includes a script block with event handlers. Event handlers run your code when users interact with the component, for example when they select a record.

4.  Update the component code for your website.

    For example, replace the placeholder page URLs in the event handlers with the URLs of your own pages. For component-specific instructions, see:

    -   [Embed the Case create component instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-case-create-component-on-third-party-website.md)
    -   [Embed the Case list component instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-case-list-component-on-third-party-website.md)
    -   [Embed the Case view component instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-case-view-comp-on-third-party-website.md)
    -   [Embed the Catalog item component instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-catalog-item-component-on-third-party-website.md)
    -   [Embed the Catalog browse component on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-embed-catalog-browse-on-third-party-web.md)
    -   [Embed the Knowledge article view component instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-know-article-view-comp.md)
    -   [Embed the Playbook intake component instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-playbook-intake-comp.md)
    -   [Embed the Data visualization component instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-data-viz-comp.md)
    -   [Embed the Object list component on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-embed-object-list-comp-on-thirdparty-web.md)
5.  Open the website in a browser to verify that it launches the component.


## Result

The ServiceNow component instance that you embedded appears on your third-party website.

If the component doesn't appear on your website, check the following:

-   The `glide.uxf.lib.embeddables.enabled` system property is set to true. By default, the property is set to true. For more information, see [Properties installed with Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/properties-installed-with-web-embeddables.md).
-   You configured CORS rules for the domain of your website. For more information, see [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-cors-for-web-components.md).
-   The **External domain** field of your module matches the domain where you embedded the component. For more information, see [Create a module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/create-we-module.md).
-   The `authCallback` function in the global code returns the authentication token for the current user. For more information, see [Authenticate the ServiceNow components using OIDC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/auth-sn-webcomponents-non-oidc.md).
-   If your browser blocks third-party cookies, set up a custom URL for your instance. For more information, see [Set up a custom URL as the instance URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/set-up-custom-url.md).

