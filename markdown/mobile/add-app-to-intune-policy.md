---
title: Add an Intune integrated app to a protection policy in Microsoft Azure
description: Learn how to add your ServiceNow mobile apps to your existing Microsoft Azure protection policies.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Intune, Device management, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add an Intune integrated app to a protection policy in Microsoft Azure

Learn how to add your ServiceNow mobile apps to your existing Microsoft Azure protection policies.

## Before you begin

The following steps describe how to add your Intune integrated apps to an existing protection policy. For information on creating protection policies, refer to your Microsoft Azure documentation.

Role required: Microsoft Intune admin

## Procedure

1.  Log in to the Microsoft Endpoint Manager admin center at `https://endpoint.microsoft.com`.

2.  In the menu on the left side of the screen, navigate to **Apps**.

    ![Microsoft Endpoint Manager admin center menu showing the 'Apps' option.](../image/intune-mdm-config-select-apps.png)

3.  In the menu on the left side of the screen, select **App protection policies**, and then select a policy.

    ![Microsoft Endpoint Manager admin center showing the options to select an app protection policy.](../image/intune-mdm-config-select-app-prot-pol.png)

4.  Open the app protection policy you want to add your apps to.

5.  In the left menu, open **Properties**.

    ![Microsoft Endpoint Manager admin center showing Properties option in Intune App Protection policy.](../image/intune-mdm-config-prot-pol-proper.png)

6.  On the application protection policy properties page, select **Apps** &gt; **Edit**

    ![Microsoft Endpoint Manager admin center showing how to add an app protection policy.](../image/intune-mdm-config-app-prot-pol-add.png)

7.  In the Edit policy form, click **Select public apps**.

    ![Microsoft Endpoint Manager admin center showing option to select public apps for an app protection policy.](../image/intune-mdm-config-sel-app-4-pol.png)

8.  Search for the app you want to add, select the app, and then select **Review + save**.

    The ServiceNow mobile app has been added to the protection policy.


**Parent Topic:**[Intune mobile device management \(MDM\)](../concept/intune-mdm.md)

