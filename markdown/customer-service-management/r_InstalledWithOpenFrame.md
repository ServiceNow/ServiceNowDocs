---
title: Components installed with OpenFrame
description: Several types of components are installed with OpenFrame.Tables are added with activation of OpenFrame.The OpenFrame user role is automatically added when you activate OpenFrame.The OpenFrameAjaxUtility script include is added when you activate OpenFrame.Some related business rules are added when you activate OpenFrame.Related UI macros are added when you activate the OpenFrame plugin.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Components installed with additional plugins for Customer Service Management, Customer Service Management reference, Customer Service Management]
---

# Components installed with OpenFrame

Several types of components are installed with OpenFrame.

## Tables installed with OpenFrame

Tables are added with activation of OpenFrame.

<table id="table_rgw_cmb_kt"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Phone Log\[sn\_openframe\_phone\_log\]

</td><td>

A log of the incoming and outgoing phone calls. This table can be used to log any phone call made or received.

</td></tr><tr><td>

OpenFrame Configuration\[sn\_openframe\_configuration\]

</td><td>

Stores the OpenFrame configuration. This is the configuration used to load the OpenFrame in the TopFrame.

</td></tr></tbody>
</table>## Roles installed with OpenFrame

The OpenFrame user role is automatically added when you activate OpenFrame.

<table id="table_bxx_zpb_kt"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains role

</th></tr></thead><tbody><tr><td>

User\[sn\_openframe\_user\]

</td><td>

The OpenFrame user role.

</td><td>

None

</td></tr><tr><td>

Usersn\_openframe\_api\_user

</td><td>

The OpenFrame API user role

</td><td>

None

</td></tr></tbody>
</table>## Script includes installed with OpenFrame

The OpenFrameAjaxUtility script include is added when you activate OpenFrame.

|Script include|Description|
|--------------|-----------|
|OpenFrameAjaxUtility|OpenFrame AJAX utility class that provides functions to get the OpenFrame configuration and also to get and set the last opened frame location.|

## Business rules installed with OpenFrame

Some related business rules are added when you activate OpenFrame.

<table id="table_i3m_5nb_kt"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Set Agent

</td><td>

Phone Log \[sn\_openframe\_phone\_log\]

</td><td>

Sets the agent in the Phone Log \[sn\_openframe\_phone\_log\] table as the current logged-in user if a phone call is logged without an agent.

</td></tr><tr><td>

One Default Configuration

</td><td>

OpenFrame Configuration\[sn\_openframe\_configuration\]

</td><td>

Checks that there is only one default OpenFarme configuration. You cannot have two OpenFrame configurations if the default option is set to true.

</td></tr><tr><td>

Update Task Work Notes

</td><td>

Phone Log\[sn\_openframe\_phone\_log\]

</td><td>

Updates the work notes for a specific task whenever a phone call is logged for that task.

</td></tr></tbody>
</table>## UI macros installed with OpenFrame

Related UI macros are added when you activate the OpenFrame plugin.

The UI macros added when you activate OpenFrame plugin are supported under the following conditions:

-   The **doctype** property is set to true and the device is not a tablet or mobile.
-   The web browser is Internet Explorer 10 or above.

As a system administrator, you can add the following UI macro scripts:

<table id="table_olq_wtw_kt"><thead><tr><th>

Script include

</th><th>

Description

</th></tr></thead><tbody><tr><td>

show\_phone

</td><td>

-   This macro requires the activation of the OpenFrame plugin.
-   By configuring this UI macro using the **ref\_contribution** parameter, you can display a phone icon next to the sys\_user reference field if the phone field in the sys\_user record is populated with the user's contact number.

</td></tr><tr><td>

show\_phone\_customer\_service

</td><td>

-   This macro requires the activation of the Customer Service Management and the OpenFrame plugins.
-   By configuring this UI macro using the **ref\_contribution** parameter, you can display a phone icon next to the **Contact** customer\_account reference field on the case form if the phone field in the Contact customer\_account record is populated with the user's contact number.

</td></tr></tbody>
</table>Displaying the phone icon enables you to make calls using the click-to-call capability in the OpenFrame window. For more information on how to use OpenFrame, see [OpenFrame overview](../concept/c_OpenFrameOverview.md).

