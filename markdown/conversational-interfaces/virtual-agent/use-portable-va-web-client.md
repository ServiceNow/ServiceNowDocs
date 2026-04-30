---
title: Configuring the portable Virtual Agent chat widget
description: The portable chat widget can run on third-party web pages, in the service portal, or in UI Builder portals.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-11-14"
reading_time_minutes: 3
breadcrumb: [Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Configuring the portable Virtual Agent chat widget

The portable chat widget can run on third-party web pages, in the service portal, or in UI Builder portals.

The portable chat widget is a new Seismic component that makes it easy to add Virtual Agent chat to your page. It simplifies configuration and provides the following features:

-   Easily configurable
-   Simpler single sign-on \(SSO\) authentication flow
-   Connect to Service Portal Agent Chat
-   System parameters and context variables work the same as before

## Prerequisites for using the Portable Virtual Agent chat widget

The Portable chat widget uses an inline frame element \(iframe\). The third-party website must be under the same parent domain as your ServiceNow® instance. For example, `site1.company.com` and `site2.company.com` share the same parent domain. If you're embedding the chat widget on any subdomain that is not shared with your ServiceNow instance, the URL must be a custom instance URL. Due to increased browser security, the chat widget may fail to load if you don't use a custom URL.

Before you begin, do the following:

1.  [Activate the custom URL plugin \(com.snc.customurl\) in your instance.](https://www.servicenow.com/docs/access?context=activate-custom-url-plugin&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)
2.  [Add the custom URL \(that you previously purchased and registered\) to your instance.](https://www.servicenow.com/docs/access?context=configure-custom-url&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

**Note:** To learn more about using custom URLs, see [Associating custom URLs to your instance](https://www.servicenow.com/docs/access?context=custom-url&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Using SSO authentication with the Portable Virtual Agent chat widget

After you embed the Virtual Agent client, you can optionally trigger SSO authentication from the chat widget, but only when your instance is set up to use an external SSO provider. Your hosting site must also use the same SSO provider as your instance. For details on setting SSO providers, see [External single sign-on \(SSO\)](https://www.servicenow.com/docs/access?context=c_MultipleProviderSingleSignOn&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

To trigger SSO authentication, create a JavaScript script that defines conditions for running authentication and redirects users to a chat widget page that you specify. You also specify the allowed URLs that can be passed in this script, by identifying them in the **com.glide.cs.web\_client\_login\_redirect\_urls** system property. Specify the full redirect URLs or the host part of the URL, such as `https://example.com`.

This procedure requires that you set values for the following two system properties:

-   **com.glide.cs.embed.csp\_frame\_ancestors**
-   **com.glide.cs.embed.xframe\_options** \(IE 11 only\)

These properties determine the security policy for the embedded chat widget, namely how browsers render and secure HTML content for Virtual Agent and Live Agent chat, in an iframe, before you embed the web chat client. The HTTP header directives that you specify tell the browser whether a page can be embedded on certain domains to mitigate clickjacking attempts. Setting both properties ensures that there are security directives for major browsers and also older browsers, such as Internet Explorer.

**Note:** If you're using the Content Management System \(CMS\) application to create custom interfaces for the ServiceNow AI Platform and ServiceNow® applications, be aware that it does not support Virtual Agent.

-   **[Configure the Portable Virtual Agent chat widget](../task/configure-portable-va-web-client.md)**  
Configure the Portable Virtual Agent chat widget to run Virtual Agent on third-party web pages.
-   **[Add the Portable Virtual Agent Chat Widget to a third-party website](../task/add-portable-va-client-website.md)**  
To use the Portable Chat Widget for Virtual Agent on third-party web pages, add the necessary code to your web page.
-   **[Embed the Virtual Agent chat widget in an external web page \(legacy method\)](../task/create-va-standalone-client.md)**  
Load the Virtual Agent chat widget interface in an external web page by using an inline frame element \(iframe\). You can also optionally enable the single sign-on \(SSO\) authentication process to run automatically for guest users who are using the chat widget and are not logged in.

**Parent Topic:**[Configuring Virtual Agent](configure-virtual-agent.md)

**Related topics**  


[Configure the Portable Virtual Agent chat widget](../task/configure-portable-va-web-client.md)

[Add the Portable Virtual Agent Chat Widget to a third-party website](../task/add-portable-va-client-website.md)

