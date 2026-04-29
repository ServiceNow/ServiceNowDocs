---
title: Set up the BCM mobile application
description: Set up your mobile device and the ServiceNow AI Platform for the BCM mobile application.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing plans with BCM mobile application, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up the BCM mobile application

Set up your mobile device and the ServiceNow AI Platform for the BCM mobile application.

## Before you begin

Role required: sn\_bcp.plan\_admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **Available To Obtain From Store** and install GRC core applications and the ServiceNow AI Platform instance.

    **Note:** The GRC core applications and the ServiceNow AI Platform instance should be from the same family release.

    1.  To verify the GRC: GRC: Profiles application is installed on your instance, navigate to **Plugins** and search for GRC: Profiles.
    2.  If the GRC: Profiles core application isn’t already installed, select **Install** to install it.
    3.  After the GRC: Profiles application is installed, install Business Continuity Management.
    All GRC core applications are available on the ServiceNow Store.

    For more information about getting entitlement, downloading, and installing the GRC core applications, see [GRC and the ServiceNow Store](../../grc-common/concept/grc-and-store.md).

    When you install the GRC core applications, the dependency plugins for the GRC Mobile application \(com.glide.sg and com.glide.sg.agent\_native\_client\) are also automatically installed.

    To verify that these dependency plugins are installed and activated:

    1.  Navigate to **Plugins**.
    2.  Search for the plugin IDs \(com.glide.sg and com.glide.sg.agent\_native\_client\).
    3.  If they aren’t activated, activate these plugins.
2.  Install the BCM mobile application on the ServiceNow AI Platform instance that you want to view on your mobile device.

    **Note:** The BCM mobile app and the ServiceNow AI Platform instance should be from the same family release.

    For more information about getting entitlement, downloading, and installing the BCM mobile app, see [GRC and the ServiceNow Store](../../grc-common/concept/grc-and-store.md).

3.  Assign the mobile users with the required ServiceNow AI Platform roles as a user with the admin role in your ServiceNow AI Platform instance.

4.  Download and install the most current ServiceNow Agent app on your mobile device, as a mobile user with the sn\_bcm.manager role.

    The most current ServiceNow Agent app is available on the Apple iOS App Store and the Google Play Store.


## Result

You have successfully set up your mobile device and the ServiceNow AI Platform for the BCM mobile application. The next step is to log in to your ServiceNow AI Platform instance with the ServiceNow Agent app on your mobile device.

