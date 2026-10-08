---
title: Configure the mobile experience switcher
description: Learn how to configure the mobile experience switcher.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/mobile-exp-switcher-config.html
release: australia
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [Mobile experience switcher, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the mobile experience switcher

Learn how to configure the mobile experience switcher.

## Before you begin

Role required: admin

## About this task

Enabling and configuring the mobile experience switcher is a two-part process. First, configure the system property that turns on the switcher capability. Second, select the applicable settings on the mobile app config page for each mobile app experience you want to configure.

**Note:** If you want this configuration to apply to both mobile apps, Now Mobile® \(for requester\) and Mobile Agent \(for agent\), you must enable this configuration separately for each mobile app.

## Procedure

1.  Enable the mobile experience switcher feature by creating the relevant system property:

    1.  Type sys\_properties.list in the filter navigator.
    2.  In the System Properties screen, select  **New**.
    3.  Make sure that the **Application scope** is set to  Global.
    4.  Use the following information to complete the fields on the system property form.

<table id="table_g1z_f1m_tkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter either: -   glide.sg.enable\_experience\_switching.agent for the Mobile Agent app.
-   glide.sg.enable\_experience\_switching.request for the Now Mobile® app.
**Note:** For the mobile experience switcher to be available in both the Now Mobile® app and Mobile Agent app, create two separate records.

</td></tr><tr><td>

Type

</td><td>

Select  true \| false.

</td></tr><tr><td>

Value

</td><td>

Enter `true` to enable the mobile experience switcher option for your users.

</td></tr></tbody>
</table>2.  Open and enable following settings in the Mobile app config page.

    1.  Type  `sys_sg_native_client.list `in the filter navigator.
    2.  In the **Name** field, enter the name of the mobile experience listed within the record.
    3.  In the **Label** field,enter the name of the mobile experience that displays in the Experience menu.
    4.  In the **Type** field select either **Agent** or **Requester**, depending if you're configuring for the Mobile Agent app or Now Mobile® app.
    5.  In the **Order** field define where the mobile experience is displayed in the list. A lower number places the item higher on the list.
    6.  Select the **Active** option to display the mobile app experience in the Experience area of the Settings page.

        **Note:** By default the Active option is selected. Turn off this option if you don’t want this mobile app experience displayed in the switcher. This setting applies regardless of user roles or permissions.

    7.  Select **Submit**.
    8.  Repeat these instructions for each mobile app experience you want to add to the Settings page.

**Parent Topic:**[Mobile experience switcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/mobile-experience-switcher.md)

