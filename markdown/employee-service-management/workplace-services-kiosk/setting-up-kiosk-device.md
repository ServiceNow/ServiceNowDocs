---
title: Setting up a kiosk device
description: Set up a kiosk device by assigning a kiosk to a physical device.Select a kiosk for the device to render the configuration pages created by the kiosk admin.Assign a different kiosk or remove the assigned kiosk from a device.
locale: en-US
release: australia
product: Workplace Services Kiosk
classification: workplace-services-kiosk
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage, Workplace Services Kiosk, Workplace Service Delivery, Employee Service Management]
---

# Setting up a kiosk device

Set up a kiosk device by assigning a kiosk to a physical device.

To enable usage of a kiosk device, you must select a kiosk for the device. The kiosk module displays the pages configured by an admin and visitors can use the device to check in and self-register. For more information about configuring kiosk devices, see [Create a kiosk configuration](../task/create-kiosk-device-config.md).

You can access the kiosk page by using the following URL: `https://<instance name>.service-now.com/kiosk`

![Kiosk setup welcome page. Kiosk operators can configure and select a kiosk to bind it to a physical device.](../images/wsd-kiosk-home.png)

**Parent Topic:**[Managing Workplace Services Kiosk](manage-workplace-services-kiosk.md)

## Select a kiosk for a device

Select a kiosk for the device to render the configuration pages created by the kiosk admin.

### Before you begin

Role required: sn\_wsd\_kiosk.operator

### Procedure

1.  On a kiosk device, login using your operator credentials.

2.  On the Kiosk setup page, select **Select Kiosk**.

    ![Kiosk setup page displayed to a kiosk operator.](../images/wsd-kiosk-setup.png)

3.  Select a kiosk from the list, then select **Continue**.

    ![Kiosk page with a list of kiosk names that can be selected.](../images/wsd-select-kiosk.png)

4.  Provide camera permissions for the kiosk.

    1.  On the Allow camera access page, select **Continue**.

    2.  On your browser prompt, select the option to always allow camera access to the website.

        **Note:** If you are using the Apple Safari browser, you must allow the website to always access the camera from your browser settings.

        Security features of Google Chrome on iOS don't allow permanent camera access to websites, therefore, camera-related functions of the kiosk are disabled.

    3.  After the camera access is granted, select **Save Kiosk**.

    If you have existing kiosks that do not have camera permissions, you will receive a notification to update the kiosks and allow camera access.


## Change or remove the kiosk for a device

Assign a different kiosk or remove the assigned kiosk from a device.

### Before you begin

Role required: sn\_wsd\_kiosk.operator

### Procedure

1.  On a kiosk device, login using your operator credentials.

2.  On the Kiosk setup page, select any of the following options.

<table id="choicetable_qxc_hnq_pbc"><thead><tr><th align="left" id="d148270e265">

Option

</th><th align="left" id="d148270e268">

Description

</th></tr></thead><tbody><tr><td id="d148270e274">

**Remove Kiosk**

</td><td>

Remove the assigned kiosk from the device.

</td></tr><tr><td id="d148270e283">

**Change Kiosk**

</td><td>

Assign a different kiosk to the device by following these steps:1.  Select **Change Kiosk**.

![Kiosk homepage displayed to a kiosk operator with options to remove or change the assigned kiosk.](../images/wsd-change-kiosk.png)

2.  Select a kiosk from the list, then select **Continue**.
3.  On the Allow camera access page, select **Continue**.
4.  On your browser prompt, select the option to always allow camera access.

**Note:** If you are using the Apple Safari browser, you must allow the website to always access the camera from your browser settings.

Security features of Google Chrome on iOS don't allow permanent camera access to websites, therefore, camera-related functions of the kiosk are disabled.

</td></tr><tr><td id="d148270e324">

**Update Kiosk**

</td><td>

Grant camera access to the kiosk by following these steps:1.  Select **Update Kiosk**.

![Kiosk homepage displayed to a kiosk operator with an alert specifying that camera permissions are needed.](../images/wsd-update-kiosk.png)

2.  On the Allow camera access page, select **Continue**.
3.  On your browser prompt, select the option to always allow camera access.
**Note:** If you are using the Apple Safari browser, you must allow the website to always access the camera from your browser settings.

Security features of Google Chrome on iOS don't allow permanent camera access to websites, therefore, camera-related functions of the kiosk are disabled.

</td></tr></tbody>
</table>
