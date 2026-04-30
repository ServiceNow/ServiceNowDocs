---
title: Enable Override do not disturb to receive critical alerts
description: Enable the Override do not disturb to receive critical push notifications feature for ITSM Mobile Agent.
locale: en-US
release: xanadu
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, ITSM Mobile Agent, IT Service Management]
---

# Enable Override do not disturb to receive critical alerts

Enable the Override do not disturb to receive critical push notifications feature for ITSM Mobile Agent.

## About this task

With the Override do not disturb to receive critical push notifications feature, ITSM managers can reach out to their on-call members even when their phones are set to Do Not Disturb mode.

To enable this feature, you must configure a prompt and reprompt property. The reprompt property resends the pop-up message if the agent didn't initially enable the configuration.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **sys\_sg\_properties** &gt; **Mobile properties**.

2.  On the mobile properties page, switch to **Global scope**.

3.  Select **New** and create a new property with the following details:

    -   Name: **critical\_alerts\_request\_prompt**
    -   Type: **True/False**
    -   Value: `true`
    -   Mobile Application: **Agent**
4.  Select the **Active** option.

5.  Ensure that the value is **True** and select **Update** to create and apply the property.

    **Note:** After creating this property, users must log out and then log back in for the change to take effect.

6.  Log in to the ITSM Mobile Agent application.

7.  Select **Open Settings**, when prompted to `Enable Override Do Not Disturb To Receive Critical Alerts`.

    **Note:** If you log in to ITSM Mobile Agent using an iOS device, when prompted to `Enable Override Do Not Disturb To Receive Critical Alerts`, select **Allow**.

8.  On the Do Not Disturb access settings page, select the ITSM Mobile Agent application from the list.

9.  Select the **Allow Do Not Disturb** toggle button.

10. Confirm by selecting **Allow**.

    The user starts to receive the critical alerts in Do Not Disturb mode.

11. Configure the following reprompt property if you want to resend the **Override do not disturb to receive critical alerts** pop-up for the agents who didn't enable the property initially:

    1.  Enter `sys_sg_properties` in the navigation filter.
    2.  On the mobile properties page, select **New** and create a property with the name **critical\_alerts\_request\_reprompt** and the same configuration as the **critical\_alerts\_request\_prompt** property.

