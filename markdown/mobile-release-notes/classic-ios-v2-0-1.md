---
title: Mobile Classic iOS v2.0.1
description: The Mobile Classic iOS v2.0.1 release provides problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/classic-ios-v2-0-1.html
release: mobile
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 1
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic iOS v2.0.1

The Mobile Classic iOS v2.0.1 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Apple App Store](https://itunes.apple.com/us/app/servicenow/id1044428492?mt=8).

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

 PRB654843

</td><td>

App cannot connect to a server with the glide.security.csrf.strict.validation.mode property set to true

</td><td>

Enabling glide.security.csrf.strict.validation.mode renders an instance incompatible with the iOS app.

</td><td>

1.  Enable glide.security.csrf.strict.validation.mode.
2.  Attempt to log in.

Note the 401 error.

</td></tr><tr><td>

Mobile

 PRB654847

</td><td>

AMB occasionally fails after backgrounding the app

</td><td>

After backgrounding the app, it is possible that an AMB/Bayuex Connect message will fail. The 'in flight' connect message is not cleared out in this scenario, and AMB does not reconnect.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB655491

</td><td>

Pins are not showing on map modules

</td><td>

 

</td><td>

To set up the server: 1.  Navigate to a map page record from the cmn\_map\_page table.
2.  Copy the sys\_id for the record.
3.  Navigate to a mobile app record from the sys\_ui\_application table.
4.  On the sys\_ui\_module table, add a new module to this app.
5.  Set the path to map/id where the ID is the sys\_id of the map record from the cmn\_map\_page table.

Steps to reproduce: 1.  Log into a Geneva instance.
2.  Navigate to the new map module via the Navigator screen \(**Maps** &gt; **All Locations**\).

Note that the pins are not showing on the map.

</td></tr><tr><td>

Mobile

 PRB656174

</td><td>

If no primary IDP is set for an instance, login fails

</td><td>

 

</td><td>

1.  Configure SSO on an instance.
2.  Via the glide.authenticate.sso.redirect.idp system property, verify that there no primary identity provider is set.
3.  Add the instance in the mobile application.
4.  Enter in a username.
5.  Tap on the **Use External Login** link.

Note that instead of being redirected to the external IDP that was set up for the user, the following error occurs: 'No external identity provider found for the username: admin'

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/classic-available-versions.md)

