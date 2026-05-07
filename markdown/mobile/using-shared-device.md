---
title: Using a shared device with multiple users
description: Use a single device between multiple users to have a secure and personalized experience, where each user accesses their account through a unique PIN.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Using the mobile apps, Mobile Platform]
---

# Using a shared device with multiple users

Use a single device between multiple users to have a secure and personalized experience, where each user accesses their account through a unique PIN.

**Note:**

-   This feature must be enabled by your administrator. To check if it is available to you, go to **Settings** and look for Device Sharing in the menu.
-   For the admin configuration topics of this feature, see [Enable multiple users to work on a shared device](../concept/multi-user-single-instance.md).

## Shared device flow

This table shows the end-to-end flow of the shared device feature, covering both the initial setup experience and subsequent use by returning users.

<table id="table_kfk_s4j_cjc"><thead><tr><th>

Instructions and processes

</th><th>

Visual display

</th></tr></thead><tbody><tr><td>

In the **Settings** page, select the Device sharing option.

</td><td>

![Settings page with Device sharing option](../image/multiuser-settings-page.png)

</td></tr><tr><td>

The Device sharing page gives details of how shared mode operates. Select the **Activate shared device mode** button to enable the feature.

</td><td>

![Activate shared mode button in the Device sharing page](../image/multiuser-shared-account-activate.png)

</td></tr><tr><td>

You may see the following message if the mobile app is linked to more than one ServiceNow account. Since the shared device mode only works only with a single account on a device, you must remove the additional accounts from the app.

 To remove additional accounts:

1.  Click **OK** on the message.
2.  Select **Settings** to go back to the Settings page.
3.  Select **Accounts**.
4.  If the account you want to remove is logged in, swipe on the account and select **Log out**.
5.  For accounts you want to remove, do the following:
    1.  Swipe on the account name, select **Edit** and then **Remove from list**.
    2.  Select **Remove** in the confirmation message.

**Note:** Repeat steps \(a\) and \(b\) for each account you do not need for the shared mode.

    3.  Close the Accounts page.
6.  Return to the Settings page, select **Device sharing** from the menu and select **Activate shared device** mode.

</td><td>

![Pop-up stating that multiple accounts have been detected](../image/multiuser-mult-accounts.png)

</td></tr><tr><td>

In the Quick Access page select **Add your account**. The bottom of the Quick Access page displays the account name and that the device is in the shared device mode.If the maximum number of users has been reached and you try to add yourself to the shared device, you are given the option to remove an existing user who is the least active from the list. This frees up a slot, allowing you to login yourself on the shared device.

**Note:** Before removing another user, it is advisable to check with your administrator first.

</td><td>

![Add your account button in the Quick Access page](../image/multiuser-add-account.png)

</td></tr><tr><td>

In the log in page, enter your Username and Password, and then select **Log in**.

</td><td>

![Main ServiceNow login page](../image/multiuser-log-in-page.png)

</td></tr><tr><td>

After you pass the login page, you need to set a six digit PIN. This is the PIN number you use each time you log into this specific application and account on this device.

</td><td>

![Set quick access PIN for a shared user](../image/multiuser-pin.png)

</td></tr><tr><td>

When logging in for the first time, you need to reenter your PIN for confirmation purposes. You will also see this confirmation when resetting a PIN.

</td><td>

![Confirmation of quick access PIN for a shared user](../image/multiuser-confirm.png)

</td></tr><tr><td>

At the end of the authentication process, you are logged into the ServiceNow mobile app as a regular user. In the header is the exit account button![Exit account button](../image/multiuser-exit-button.png).Tap the button to open the Quick Access page.

**Note:** To return to the app, you need to tap on your user in the Quick Access page and enter your PIN.

</td><td>

![Home page with exit account button.](../image/multiuser-home.png)

</td></tr><tr><td>

The Quick Access page displays all the users who are added to this device. The user displayed at the top is the active user.On this page you can do the following:

-   Select the Add user button ![Add user button](../image/multiuser-add-button.png) to add any additional users to this device.

**Note:** There may be a limit to the number of users you can add to a device.

-   Select a user for them to log into the device via the PIN authentication process.

</td><td>

![Quick Access page containing multiple users](../image/multiuser-users.png)

</td></tr></tbody>
</table>