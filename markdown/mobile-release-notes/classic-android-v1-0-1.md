---
title: Mobile Classic Android v1.0.1
description: The Mobile Classic Android v1.0.1 release provides problem fixes.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 3
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic Android v1.0.1

The Mobile Classic Android v1.0.1 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.servicenow&hl=en).

**Important:** There are several new ServiceNow mobile apps, including Mobile Agent, Now Mobile, Mobile Onboarding, and Now Support. Check out these new apps for the latest features and capabilities.

## Fixed in this release

<table id="tbl_AllFixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile

 PRB703553

</td><td>

SSO on Android - Better handling of CSRF tokens

</td><td>

Successful SSO authentication triggers a API call to fetch a secret. If this is missing a valid CSRF token, even though it is not fully authenticated yet, authentication needs to retry with the token provided in the 401 response.

</td><td>

Upon SSO authentication, when the IDP redirects back to the instance, an Android 'toast' will pop up saying 'Incorrect username or password'.**Note:** SSO is a complex area. If you still experience this issue, [contact ServiceNow Customer Support](http://www.servicenow.com/support/contact-support.html).

</td></tr><tr><td>

Mobile

 PRB703589

</td><td>

Connect issues

</td><td>

The fix profile page phone and email links are not displaying or working correctly. The app should also allow users to start a chat conversation with another user via the user's profile page.

</td><td>

Symptoms

 -   There is missing data on a user's profile page.
-   Clicking on a phone or email in a user's profile does not do anything.
-   There is no way to start a conversation from a user's profile page.

</td></tr><tr><td>

Mobile

 PRB703591

</td><td>

List-related issues

</td><td>

Some users are experiencing crashes when using record lists and filter editing. The app should also allow users to use filter and form multi-select.

</td><td>

1.  When on a form, select a multi-select field \(e.g. watchlist\). Note that nothing occurs.
2.  When editing a filter, try to select a rule that would be multi-select. Note that nothing occurs, or a blank filter selection appears.

</td></tr><tr><td>

Mobile

 PRB703595

</td><td>

Form-related issues

</td><td>

Some users are experiencing crashes related to application forms, catalog routes, and other cases.

</td><td>

Symptoms

 -   Trying to open one of the following catalog routes does not load or returns an error:
    -   catalog\_producer/producer/:categorySysId/:currentCategoryTitle/: itemSysId/:currentItemTitle/:contextCategorySysId/: contextCategoryTitle/:catalogSysId/:catalogTitle
    -   /catalog\_item/item/:categorySysId/:currentCategoryTitle/: itemSysId/:currentItemTitle/:contextCategorySysId/: contextCategoryTitle/:catalogSysId/:catalogTitle
    -   /catalog/category/:categorySysId/:categoryTitle/: catalogSysId/:catalogTitle
-   Opening a Connect chat conversation link with a relative URL \(e.g. //google.com - note there is no http: or https:\) do not load.
-   In some situations, leaving a webview \(e.g. form, catalog\) causes a crash.
-   Leaving a form while downloading an attachment causes a crash.
-   Forms where users expect a 'Confirm' popup to appear after an action do nothing instead.

</td></tr><tr><td>

Mobile

 PRB703597

</td><td>

Authentication issues

</td><td>

When users authenticate and reauthenticate, crashes can occur.

</td><td>

Symptoms

 -   On a SSO login, when the user expects a pop-up window to enter credentials, nothing happens.
-   When users go 'up' back to the instance list where none are added, the user ends up with a blank screen.
-   Devices without Google Play Services that happen to load the app and try to log out may bring up a loader that never goes away.

</td></tr><tr><td>

Mobile

 PRB703598

</td><td>

Favorites-related issues

</td><td>

Basic favorites functionality can cause unexpected behavior and crashes.

</td><td>

Symptoms

 -   Certain home.do pages try to display on the device when they should not.
-   Bookmark a 'create new record' form, and load this bookmark. Note that an empty record loads instead of the new record form.
-   Create a bar visualizations with data that has an empty title. Note that it incorrectly shows a blank space instead.

</td></tr><tr><td>

Mobile

 PRB703863

</td><td>

Load map page by name

</td><td>

Map pages should also be able to load by name, instead being limited to sys ID only.

</td><td>

1.  Create a navigator module with a link to a map page by name \(e.g.**map/?sysparm\_name=&lt;NAME GOES HERE&gt;**\).
2.  Note that data does not show on the map page when it should.

</td></tr><tr><td>

Mobile

 PRB705258

</td><td>

Handle full URLs in navigation router

</td><td>

The Android app needs to handle full URLs in the navigation router as long as the host matches the current instance.

</td><td>

1.  Create or find a bookmark/favorite with a full URL that contains the existing instance.
    -   To create one from scratch, go to **System Definition** &gt; **Bookmarks** &gt; **New**.
    -   Add a new Bookmark where the URL contains a full URL \(e.g. https://instance.service-now.com/$vtb.do\).
2.  On the Android mobile application, try to open this bookmark from the Favorites grid.

 Expected behavior: It should load VTB in a webview.

 Actual behavior: It loads a "page not found".

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](../classic-available-versions.md)

