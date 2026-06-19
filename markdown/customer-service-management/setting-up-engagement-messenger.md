---
title: Set up Engagement Messenger
description: Understand the stages involved in setting up Engagement Messenger before you add it to your customer service web portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/setting-up-engagement-messenger.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Enable communication channels, Configure, Customer Service Management]
---

# Set up Engagement Messenger

Understand the stages involved in setting up Engagement Messenger before you add it to your customer service web portal.

After you install the Engagement Messenger application in your instance, you’re ready to configure it. You can also watch the [academy video](https://www.youtube.com/watch?v=uViv-3bcg3k&list=PLkGSnjw5y2U79gjQuQW-2GBqzEccwFkWH&index=20) to understand the overall functionality of Engagement Messenger.

The configuration process involves the following tasks:

1.  [Install the Engagement Messenger application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/install-engagement-center-app.md) from the ServiceNow® Store.
2.  Create Engagement Messenger module.

    -   Configure the theme and styling of how Engagement Messenger appears to your customers
    -   Configure how Engagement Messenger behaves when your customer uses it
    -   Configure how Engagement Messenger works for your customers
    For more information, see [Configure Engagement Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-engagement-messenger-module.md).

3.  Create identity providers to enable an authenticated user experience. See [Create an identity provider \(IdP\) for Engagement Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-identity-providers-for-engagement-messenger.md).

    If you want to enable only a guest user experience for your customer service portal, you can ignore this step and move on to step 4.

4.  Create cross-origin resource sharing \(CORS\) rules for the REST API. See [Configure a CORS rule for Engagement Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-cors-for-rest-api-ec.md).
5.  Add HTTP response headers for your Engagement Messenger. See [Create HTTP response headers for Engagement Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-http-response-headers-for-ec.md).
6.  Configure the system properties to enable virtual agent chat, multi-provider SSO, and to set a user session time-out value. For more information, see [Engagement Messenger properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/additional-config-for-engagement-messenger.md).
7.  Configure a custom URL to load Engagement Messenger on third-party websites. For more information, see [Enable Engagement Messenger on a website when third-party application cookies are blocked](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/allowlist-em-third-party-website.md).
8.  Configure the deep linking feature to launch a specified feature in Engagement Messenger. For more information, see [Deep linking feature in Engagement Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/contextual-launch-engagement-messenger.md).
9.  [Activate an Engagement Messenger module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/activate-engagement-messenger-module.md).
10. [Embed Engagement Messenger in your web application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/embed-engagement-messenger-code-in-your-web-application.md).
11. Embed messenger in your native iOS mobile app using Now Mobile® SDK. For information, see the [Embed Engagement Messenger in a native iOS app using Now Mobile SDK \[KB1587276\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1587276) article in the Now Support Knowledge Base.
12. Embed messenger in your native android mobile app using Now Mobile® SDK. For more information, see the [Embed Engagement Messenger in a native android app using Now Mobile SDK \[KB1587611\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1587611) article in the Now Support Knowledge Base.

