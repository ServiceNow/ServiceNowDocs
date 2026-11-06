---
title: Enable critical alerts in Do Not Disturb mode
description: Configure ITSM Mobile Agent so that agents receive critical push notifications even when their mobile device is in Do Not Disturb mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/enable-override-do-not-disturb-to-receive-critical-alerts.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Enable critical alerts in Do Not Disturb mode

Configure ITSM Mobile Agent so that agents receive critical push notifications even when their mobile device is in Do Not Disturb mode.

## About this task

The Override do not disturb to receive critical push notifications feature lets ITSM managers reach on-call agents. Agents' mobile devices can receive alerts even when set to Do Not Disturb mode.

This feature uses a prompt property and an optional reprompt property. The reprompt property resends the pop-up message to agents who didn't enable the setting initially.

## Before you begin

Role required: admin

## Procedure

1.  Enter `sys_sg_properties` in the navigation filter.

2.  On the mobile properties page, switch to **Global scope**.

3.  Select **New** and create a property with the following details:

    -   Name: **critical\_alerts\_request\_prompt**
    -   Type: **True/False**
    -   Value: `true`
    -   Mobile Application: **Agent**
4.  Select the **Active** option.

5.  Ensure that the value is **True** and select **Update** to create and apply the property.

    **Note:** After creating this property, users must log out and then log back in for the change to take effect.

6.  Log in to the ITSM Mobile Agent application.

7.  When prompted to `Enable Override Do Not Disturb To Receive Critical Alerts`, select **Open Settings**.

    **Note:** If you log in to ITSM Mobile Agent using an iOS device, when prompted to `Enable Override Do Not Disturb To Receive Critical Alerts`, select **Allow**.

8.  On the Do Not Disturb access settings page, select the ITSM Mobile Agent application from the list.

9.  Select the **Allow Do Not Disturb** toggle switch.

10. Confirm by selecting **Allow**.

    You receive critical alerts even when your device is in Do Not Disturb mode.

11. To resend the Override do not disturb to receive critical alerts pop-up message to agents who didn't enable the setting initially, configure a reprompt property:

    1.  Enter `sys_sg_properties` in the navigation filter.
    2.  On the mobile properties page, select **New** and create a property with the name **critical\_alerts\_request\_reprompt** and the same configuration as the **critical\_alerts\_request\_prompt** property.

