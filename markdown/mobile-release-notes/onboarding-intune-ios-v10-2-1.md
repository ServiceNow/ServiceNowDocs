---
title: ServiceNow Onboarding - Intune for iOS v10.2.1
description: The iOS v10.2.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-ios-v10-2-1.html
release: mobile
topic_type: reference
last_updated: "2020-08-18"
reading_time_minutes: 1
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v10.2.1

The iOS v10.2.1 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding-intune/id1494184220). Users can launch a demo to try the ServiceNow Onboarding - Intune app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_rbw_2jr_2jb"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

ServiceNow Agent - iOS

 PRB1419434

</td><td>

Switching apps while in the live agent support chat causes issues

</td><td>

1.  Log in to the instance in the browser and impersonate beth.anglin.
2.  Open Connect Chat.
3.  Log in to the instance in the app as itil/itil.
4.  Launch VA and use the Live Agent Support topic.
5.  In Connect Chat, accept the chat and type some text.
6.  Reply in the mobile app, and then switch apps for a few seconds.
7.  Switch back and try to send another message.

 Notice that the message cannot be sent.

</td></tr><tr><td>

ServiceNow Agent - iOS

 PRB1419776

</td><td>

When using Virtual Agent, recent conversations are not loaded if the user comes out of the app and then opens it again

</td><td>

1.  In Virtual Agent, open a chat and proceed with the conversation.
2.  Close the app.
3.  Reopen the app.

 Notice that it only shows the previous conversation history, and the recent conversation you just had is not shown.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

