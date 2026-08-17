---
title: Enable critical alerts to override do not disturb setting
description: Enable the Override do not disturb setting to receive critical push notifications. Managers and admins can reach out to their on-call members even when their phones are set to Do Not Disturb mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/critical-alerts-override.html
release: australia
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 2
breadcrumb: [Mobile critical alerts, Push notifications, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Enable critical alerts to override do not disturb setting

Enable the Override do not disturb setting to receive critical push notifications. Managers and admins can reach out to their on-call members even when their phones are set to Do Not Disturb mode.

## About this task

The Override Do Not Disturb feature allows agents to receive critical push notifications even when their devices are set to Do Not Disturb mode. To enable the feature, configure the prompt and reprompt properties. The prompt asks the agent to enable the required device setting, while the reprompt displays the message again if the agent does not enable it initially.

-   **critical\_alerts\_request\_prompt**: Enables the feature and controls whether the user is prompted. If this feature is off, the user is never asked, and the reprompt property has no effect regardless of its value.
-   **critical\_alerts\_request\_reprompt** Controls whether the user is asked again after an earlier decline or after disabling the permission later.

<table id="table_u5s_pmw_1kc"><thead><tr><th>

Property request\_prompt

</th><th>

Property request\_reprompt

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Off

</td><td>

Off

</td><td>

Feature is inactive. The user is never asked for critical-alert permission.

</td></tr><tr><td>

Off

</td><td>

On

</td><td>

Feature is inactive. The reprompt property only applies when the prompt property is enabled.

</td></tr><tr><td>

On

</td><td>

Off

</td><td>

The first time the user is eligible, they are prompted about critical alert settings. If they decline, or later turn the permission off, they aren't asked again.

</td></tr><tr><td>

On

</td><td>

On

</td><td>

The user is asked once, the first time they are eligible. If they decline, or later turn the permission off, they will be asked again on a subsequent visit to the app.-   For Android: The user is prompted one additional time.
-   For iOS: The user is continuously prompted until they change the settings.

</td></tr></tbody>
</table>## Before you begin

Role required: mobile\_admin, admin

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

2.  On the mobile properties page, switch to **Global scope**.

3.  Select **New** and create a new property with the following details:

    -   Name: **critical\_alerts\_request\_prompt**
    -   Type: **True/False**
    -   Value: `true`
    -   Mobile Application: Select either **Agent** or **Request**.
4.  Select the **Active** option.

5.  Verify that the value is **True** and select **Submit** to create and apply the property.

    **Note:** After creating this property, users must log out and then log back in for the change to take effect.

6.  Select **Open Settings**, when prompted to `Enable Override Do Not Disturb To Receive Critical Alerts`.

7.  On the Do Not Disturb access settings page, select the relevant application from the list.

8.  Select the **Allow Do Not Disturb** toggle button.

9.  Confirm by selecting **Allow**.

    The user starts to receive the critical alerts in Do Not Disturb mode.

10. Configure the following reprompt property if you want to resend the **Override do not disturb to receive critical alerts** pop-up for the agents who initially declined or dismissed the original prompt.

    1.  Enter `sys_sg_properties` in the navigation filter.
    2.  On the mobile properties page, select **New** and create a property with the following details:
        1.  Name: **critical\_alerts\_request\_reprompt**
        2.  Type: **True/False**
        3.  Value: `true`
        4.  Mobile Application: **Agent**
    3.  Select the **Active** option.
    4.  Verify that the value is **True** and select **Update** to create and apply the property.
    **Note:** If an agent dismisses or declines both the original prompt and the reprompt, you can't trigger any further prompts for that agent.


**Parent Topic:**[Mobile critical alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/critical-alerts1.md)

