---
title: AppConfig for Mobile Apps
description: Use AppConfig to define a default instance and browser for your managed mobile apps.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# AppConfig for Mobile Apps

Use AppConfig to define a default instance and browser for your managed mobile apps.

**Important:**

-   Keys are case-sensitive.
-   AppConfig key values are still supported for non-managed devices if the user installs a ServiceNow® app with a MAM SDK.

## Pre-configure the default instance

When you distribute ServiceNow mobile apps through an EMM suite or an embedded MAM SDK app, you can use AppConfig to pre-configure the default instance URL and the default instance name.

|Key|Value|
|---|-----|
|SNDefaultInstanceURL|URL for your instance \(ex: https://instancename.service-now.com\)|
|SNDefaultInstanceName|Use this key to define a user-friendly name for your instance. For example, "\[My company name\]" where your instance is named for your company.|

## Prevent end users from creating connections to new instances

You can use the following AppConfig key/value pair to prevent end users from creating connections to new instances for managed mobile apps. When the following key is set to `true`, end users do not see the plus sign \(![Plus icon for adding new stances to a mobile app.](../image/icon-mobile-add-instance.png)\) on the instance list page of their mobile app. Without the plus sign, end users cannot add instances that they are not authorized to add.

|Key|Value|
|---|-----|
|SNBlockInstanceCreate|"true" \| "false"|

## Prevent end users from logging in to more than one instance at a time

You can use the following AppConfig key/value pair to prevent end users from logging in to multiple instances simultaneously. When the following key is set to `true`, end users cannot access the instance management screen from within a logged-in instance. For users to change instances, they need to log out of their current instance and log in to the relevant instance.

|Key|Value|
|---|-----|
|SNBlockMultiInstance|"true" \| "false"|

## Change the default browser

Because ServiceNow uses AppAuth for authentication, the mobile apps use the default browser on the mobile device. iOS uses the default in-app browser, while Android uses the default operating system browser. You may have browser security requirements where the app protection policy only allows the MDM-managed browser or a specific browser. A common use case is the support for per-app VPN.

|Platform|Key|Value|Browser|
|--------|---|-----|-------|
|iOS|SNAuthenticationBrowseriOS|Safari|Apple Safari|
|Chrome|Google Chrome|
|Firefox|Mozilla Firefox|
|Edge|Microsoft|
|WorkspaceONE|AirWatch VMWare Workspace ONE|
|WebAtWork|MobileIron Web@Work|
|BlackBerry Access|BlackBerry Access|
|MaaS360|IBM MaaS360|
|Citrix|Citrix Secure|
|Android|SNAuthenticationBrowserAndroid|Chrome|Google Chrome|
|Firefox|Mozilla Firefox|
|Samsung|Samsung Internet Browser|
|WorkspaceONE|AirWatch VMWare Workspace ONE|
|Edge|Microsoft|
|BlackBerry Access|BlackBerry Access|
|MaaS360|IBM MaaS360|
|Citrix|Citrix Secure|

## Define the browser for external links

External links are any links that are non-relative to the ServiceNow instance that the mobile app is logged in to. These links can be accessed from:

-   an Activity stream
-   a URL button
-   a Virtual Agent conversation
-   a mobile web view of the Catalog or a knowledge article

When you don't configure this AppConfig key, Android apps default to the Google Chrome browser and iOS apps default to Apple Safari.

Use the following configuration keys with one of the following values to define which type of browser is used when external links are opened from ServiceNow mobile app.

|Platform|Key|Value|Browser|
|--------|---|-----|-------|
|Android|SNExternalBrowserAndroid|Chrome|Google Chrome|
| |Firefox|Mozilla Firefox|
|WorkspaceONE|AirWatch VMware Workspace ONE|
|WebAtWork|MobileIron Web@Work|
|Blackberry Access|Blackberry Access|
|MaasS360|IBM MAAS360|
|Citrix|Citrix Secure|
|iOS|SNExternalBrowseriOS|Safari|Apple Safari|
| |Chrome|Google Chrome|
|Firefox|Mozilla Firefox|
|Edge|Microsoft Edge|
|WorkspaceONE|AirWatch VMware Workspace ONE|
|WebAtWork|MobileIron Web@Work|
|Blackberry Access|Blackberry Access|
|MaasS360|IBM MAAS360|
|Citrix|Citrix Secure|

**Parent Topic:**[Considerations before implementation](../concept/imp-considerations.md)

