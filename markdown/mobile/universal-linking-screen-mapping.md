---
title: Mapping specific mobile screens for universal linking
description: Configure universal links for screen mapping so a user is redirected to a previously styled record screen or list screen. Use this option to provide a customized experience for the user.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile universal linking for supported URLs, Universal linking for mobile, Mobile URLs, Configuring the Mobile Platform, Mobile Platform]
---

# Mapping specific mobile screens for universal linking

Configure universal links for screen mapping so a user is redirected to a previously styled record screen or list screen. Use this option to provide a customized experience for the user.

## Before you begin

Role required: admin

## About this task

When creating universal links, you define the screen type and the data the user sees after they tap the mobile banner. See, [Create path segment records and supported URL records for universal linking](universal-linking-web-banner.md). Also there is an option to create a screen mapping for universal links. Users click these links to see a preconfigured screen based on a defined table.

**Note:** Universal linking mapping does not apply to browser screens, as there are no options for styling and configuring a web page.

## Procedure

1.  In the web-based UI, navigate to **System Mobile** &gt; **Mobile Universal Liking** &gt; **Screen Mappings**.

2.  Select **New** to create a universal link screen mapping.

3.  On the form, fill in the fields.

<table id="table_uy4_1xw_spb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

From the menu, select a table associated with the mobile universal linking screen. The content can be a preconfigured list screen and/or a record screen.

</td></tr><tr><td>

Mobile app

</td><td>

Use the reference lookup icon to select which mobile app the links navigate to.**Note:** The selection here is overridden by the selection made in the **Mobile app** field listed in the topic [Create path segment records and supported URL records for universal linking](universal-linking-web-banner.md).

</td></tr><tr><td>

Active

</td><td>

Option for enabling the activation of this record.

</td></tr><tr><td>

List screen

</td><td>

Use the reference lookup icon to select a preconfigured list screen associated with the table, selected from the **Table** field.**Note:** Only use single list streams and single segment list screens. You cannot use multi-item streams and multi-segment list screens in this reference field.

</td></tr><tr><td>

Record screen

</td><td>

Use the reference lookup icon to select a preconfigured record screen that is associated with the table selected from the **Table** field.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Mobile universal linking for supported URLs](../concept/universal-linking-support-urls.md)

