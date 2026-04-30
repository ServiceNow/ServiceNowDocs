---
title: ServiceNow for Microsoft Teams integration API permissions for Notify connector and Meeting Extensions
description: Following are API permissions requested by the ServiceNow integration with Microsoft Teams for Notify connector and Meeting Extensions.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# ServiceNow for Microsoft Teams integration API permissions for Notify connector and Meeting Extensions

Following are API permissions requested by the ServiceNow® integration with Microsoft Teams for Notify connector and Meeting Extensions.

<table id="table_s5r_jck_5wb"><thead><tr><th>

App

</th><th>

API Permission

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="5">

Notify connector for Microsoft Teams

</td><td>

Users.Read.All \(Application\)

</td><td>

Allows the app to get the details of the users, such as their Azure ID, which is required to start the meeting.

</td></tr><tr><td>

OnlineMeetings.ReadWrite.All \(Application\)

</td><td>

Permission required to initiate an online meeting.

</td></tr><tr><td>

Calls.InitiateGroupCall.All \(Application\)

</td><td>

Permission required to invite multiple participants to a call on behalf of a Bot.

</td></tr><tr><td>

Calls.JoinGroupCall.All \(Application\)

</td><td>

Permission allows the bot to join the meeting as a participant. In order to read call details, the bot must first be a meeting participant.

</td></tr><tr><td>

Calls.JoinGroupCallAsGuest.All \(Application\)

</td><td>

Allows the app to anonymously join group calls and scheduled meetings in your organization, without a signed-in user. The app will be joined as a guest to meetings in your tenant.

</td></tr><tr><td rowspan="2">

Meeting Extensions

</td><td>

TeamsAppInstallation.ReadWriteForChat.All \(Application\)

</td><td>

Permission required to add our app to an online meeting, as part of Meeting Extensibility.

</td></tr><tr><td>

TeamsTab.ReadWriteForChat.All \(Application\)

</td><td>

Permission allows the app to open a tab with incident details within a meeting as part of Meeting Extensibility.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow for Microsoft Teams reference](../../sn-teams/reference/reference-sn-teams.md)

