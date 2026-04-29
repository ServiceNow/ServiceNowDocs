---
title: Enable Engagement Messenger on a website when third-party application cookies are blocked
description: Configure a custom URL for the ServiceNow instance that helps prevent web browsers from blocking Engagement Messenger when cross-origin iframes and third-party cookies are blocked.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up Engagement Messenger, Enable communication channels, Configure, Customer Service Management]
---

# Enable Engagement Messenger on a website when third-party application cookies are blocked

Configure a custom URL for the ServiceNow instance that helps prevent web browsers from blocking Engagement Messenger when cross-origin iframes and third-party cookies are blocked.

## Before you begin

You must activate the Custom URL \(com.snc.customurl\) plugin. For more information, see [Activate custom URLs](https://www.servicenow.com/docs/access?context=activate-custom-url-plugin&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Role required: admin

## About this task

The latest versions of browsers including Safari and Chrome have enhanced browser security features. By default, the browser security features block third-party cookies that help prevent the loading of a third-party application on a website. If you don’t use a custom URL, the browser treats the messenger as a third-party application when embedded inside a parent website. To prevent messenger from getting blocked by the browser, you need to set a custom URL for the ServiceNow instance to match the messenger domain with the website domain. Using custom URL, browser treats messenger as a first-party application rather than a third-party application. The web browser's security restrictions block messenger for the following reasons:

-   Web browser blocks cross-origin iframes when the domain of the URL used in the iframe does not match the domain of the website itself.

    **Note:** Engagement Messenger uses an iframe to load messenger’s  interface on a third–party website.

-   Web browser treats messenger’s cookies as the third-party cookies and blocks them.

    **Note:** Engagement Messenger uses cookies to enable features like authentication, recommendations, proactive help and so on.


**Note:** Custom URL is primarily configured to get a branded URL for the ServiceNow instance, Portals, and EM module that matches with your domain URL.

You must add a CNAME record to your website domain’s DNS records where Engagement Messenger is embedded and set it as your ServiceNow instance URL. For example, in the name server for `acme.com`, create an entry

```
support.acme.com 300 IN CNAME acme.servicenow.com
```

where `acme.service-now.com` is the ServiceNow instance and `acme.com` is your website on which Engagement Messenger is integrated.

## Procedure

1.  Navigate to **All** &gt; **Custom URL** &gt; **Custom URLs**.

2.  Select **New**.

3.  On the Custom URL form, in the **Domain name** field, enter the CNAME record \(your custom URL\) that you have set as the ServiceNow instance URL.

4.  Select **Create**.

    **Note:** The new custom URL takes approximately six hours for activation.

5.  After the custom URL is active, on the Custom URL form, select the **Set instance URL** check box to enable the custom URL as an instance URL.

6.  In a text editor, open the HTML file of the web page on your website where you integrate Engagement Messenger.

7.  In the code, replace the existing website URL with a custom URL.

8.  Save the file.


## Result

Engagement Messenger loads on a third-party website.

## Example

The following code includes a sample URL that contains `support.acme.com` as a custom URL.

![Custom url](../image/em-custom-URL-in-code.png "Custom URL in code")

**Related topics**  


[Set a custom URL as the instance URL](https://www.servicenow.com/docs/access?context=configure-custom-url&version=australia&pubname=australia-platform-security&ft:locale=en-US)

[Custom URLs association to your instance](https://www.servicenow.com/docs/access?context=custom-url&version=australia&pubname=australia-platform-security&ft:locale=en-US)

[Custom URL errors and fixes](https://www.servicenow.com/docs/access?context=custom-url-error-fix&version=australia&pubname=australia-platform-security&ft:locale=en-US)

