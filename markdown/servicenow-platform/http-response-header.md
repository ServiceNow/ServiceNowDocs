---
title: HTTP Response Headers
description: A response header is a simple name-value pair used in an HTTP response to provide additional information about page content or how the client should process it.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Extend ServiceNow AI Platform capabilities]
---

# HTTP Response Headers

A response header is a simple name-value pair used in an HTTP response to provide additional information about page content or how the client should process it.

You can configure HTTP response headers for all, or specific types of pages, which include Service Portal, UI Page, or UX applications. The ability to configure and pass response headers enables special handling of the page content by a client, most typically a browser.

To learn more about what an HTTP header is, and about configuring the name-value pair for specific HTTP response headers, see:[https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)

When configuring response headers, you must look at the definition for the HTTP header to determine how the client would handle the page content.

-   For example, you configure an HTTP header for a specific page or all the pages with a Content-Security-Policy: frame-ancestors 'self' https://www.servicenow.com.
-   When you invoke the page in a browser such as Chrome, you can review it in the Response Headers section of Chrome Developer Tools.

    ![HTTP header with Content-Security-Policy: frame-ancestors 'self'](../image/CSP-frame-ancestors-Response-Header.png)


To learn more about how browsers handle a page with frame-ancestors, see [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors).

**Warning:** When using URLs with custom name-value pairs, proceed with caution because there is a potential security risk when doing so. The signed security amendment to the ServiceNow AI Platform contract has implied security. You may potentially or accidentally override it when you use custom name-value pairs in the resulting URLs.

-   If you want to entirely disable HTTP response header configuration functions, set the **glide.http.headers\_config.enabled** property to **false**.
-   Once you set it to false, ServiceNow AI Platform does not use any of the header configurations you defined in the sys\_response\_header table.

## Special handling of the Content-Security-Policy: frame-ancestor header

Normally, the ServiceNow AI Platform automatically includes the X-Frame-Options: SAMEORIGIN header.

-   It supports use of this header in all types of browsers, based on the setting of the **glide.set\_x\_frame\_options** global property, which is enabled by default.
-   When you configure a page with a Content-Security-Policy: frame-ancestor 'self' URL1 URL2 header, the ServiceNow AI Platform does not automatically include the X-Frame-Options: SAMEORIGIN header. Excluding it prevents the browser from being confused, because Content-Security-Policy: frame-ancestor 'self' already has a similar effect.

## Special handling of Content-Security-Policy: frame-ancestor header for Internet Explorer

Using the Content-Security-Policy: frame-ancestor 'self' URL1 URL2 header enables you to configure multiple URL sources to include the page from within an iFrame rendered from a third-party site. However, Internet Explorer does not support this type of header.

-   Instead, the Internet Explorer only supports the X-Frame-Options: ALLOW-FROM URL \(ALLOW-FROM\) directive in this header, although the restriction is for a single host URL.
-   If you configure the frame-ancestor 'self' URL1 URL2 header, and Internet Explorer is in use, the ServiceNow AI Platform automatically uses the X-Frame-Options: ALLOW-FROM URL \(ALLOW-FROM\) header instead.

If the Internet Explorer request includes the referrer URL header:

-   It attempts to match it with the host URLs \(full or wildcard http://\*.example.com type URL format only\) configured in the Content-Security-Policy: frame-ancestor 'self' URL1 URL2 header.
-   If there is a match, include the matched URL as X-Frame-Options: ALLOW-FROM URL1.
-   If there is no referrer header, it uses the first non-wildcard based host URLs configured in the Content-Security-Policy: frame-ancestor 'self' URL1 URL2 header.

**Note:** When configuring URLs, do not include a forward slash at the end of the URL.

-   This example of an incorrect configuration that may not work properly with this special handling:
    -   Name: Content-Security-Policy
    -   Value: frame-ancestors 'self' https://microsoft.com/
-   Use this correct syntax instead:
    -   Name: Content-Security-Policy
    -   Value: frame-ancestors 'self' https://microsoft.com

**Related topics**  


[Control request and response content type](https://www.servicenow.com/docs/access?context=c_SpecifyContentType&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

[bundle-psec.cache-control-http-header-value]

[Content-Security-Policy: frame-ancestor 'self' URL1 URL2](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors)

[X-Frame-Options: SAMEORIGIN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options)

[X-Frame-Options: ALLOW-FROM URL](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options)

