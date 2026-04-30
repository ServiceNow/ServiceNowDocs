---
title: Common browser issues while using ServiceNow CPQ
description: When cookies are blocked by the browser or by browser extensions, it can interfere with the use of ServiceNow CPQ.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [ServiceNow CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Common browser issues while using ServiceNow CPQ

When cookies are blocked by the browser or by browser extensions, it can interfere with the use of ServiceNow CPQ.

If attempting to configure in ServiceNow CPQ results in an error \(configurator not loading, a 403 error is returned, or similar\) and using another browser resolves the issue, then the issue must be with the settings of the original browser.

ServiceNow CPQ uses [authentication cookies](https://en.wikipedia.org/wiki/HTTP_cookie) to track active sessions across browser tabs. These cookies do not track the user and are deleted when the user closes their web browser. Their only purpose is to validate the user and their organization for the use of our software.

If cookies are not enabled in the browser, ServiceNow CPQ cannot configure products. The browser itself or the extensions used by the end user in this browser could be inhibiting this active cookie.

Here are some reasons this issue might occur.

## Cookie blocking by the browser

By default, Safari and Firefox block all cross-site cookies. This behavior interferes with the authentication cookie that jumps across ServiceNow CPQ and Salesforce. If either of these browsers is your \(or your end userʼs\) default browser, cookies must be allowed to use the configurator.

If you have no control over what browsers end users use to access the ServiceNow CPQ Configurator, and you use easyXDM, submit a support case requesting a “runtimeAPI” parameter. Once the runtime clients are updated to include this parameter, the browsers should work with their default settings.

Consult your browser's documentation to find the settings that affect whether cookies are blocked. These settings are often found in the privacy options sections of the browser settings.

## Cookie-blocking extensions

Cookies can also be blocked by browser extensions that are installed by the user. Some third-party cookie-blocking browser extensions include:

-   uBlock Origin
-   Privacy Badger
-   Ghostery
-   Disconnect
-   Cookie AutoDelete

Other extensions such as email templates or crypto wallets can also cause issues with cross-site third-party cookies. These extensions include:

-   Briskine
-   BNB Chain Wallet MetaMask
-   WalkMe

Review your browser's plugins to check whether any other extensions could be interfering while using ServiceNow CPQ. If the end user can configure after all browser extensions are disabled, one of the extensions must be causing the issue. If you identify an extension that causes the issue and is not in the list above, please let us know.

**Parent Topic:**[ServiceNow CPQ reference](../reference/servicenow-cpq-reference.md)

