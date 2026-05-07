---
title: Configure multiple users to use a shared device
description: Learn how to setup a device to allow multiple users to log in and enter data on a single device.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Multiple users on a shared device, Configuring the Mobile Platform, Mobile Platform]
---

# Configure multiple users to use a shared device

Learn how to setup a device to allow multiple users to log in and enter data on a single device.

## Before you begin

Role required: mobile\_admin, admin

## About this task

The following configurations are listed in this topic.

-   The **SupportSharedDevice** property enables a mobile device to be used as a shared device.
-   The **mobile\_shared\_device\_mode\_enabler** role enables authorized users to set up a ServiceNow mobile app to operate in shared device mode.

**Note:** The configuration instructions in this topic detail the required fields for the configuration of this feature. For a full explanation of all the mobile property fields listed in the table, see the various configurations in the section [Mobile properties](../concept/mobile-properties.md).

## Procedure

1.  Add the **SupportSharedDevice** property for users to share a mobile device.

    1.  Navigate to **All** &gt; **All &gt; sys\_sg\_properties.list**. The Mobile Properties form displays.
    2.  In the Mobile Properties list, select  **New**. The Mobile Properties form appears.
    3.  Type the mobile property name **SupportSharedDevice** in the **Name** field.
    4.  Select **True/False** in the **Type** field.
    5.  Enter `true` in the **Value** field.
    6.  Search and select **Mobile Agent** in the **Mobile App Config** field.
    7.  Search and select **Agent** in the **Mobile Application** field.
    8.  Select **Update**.
2.  Add the **mobile\_shared\_device\_mode\_enabler** role to enable authorized users to set up a device as a shared device.

    1.  Navigate to **All** &gt; **All &gt; sys\_user.list**. The Users form displays.
    2.  Select the User ID of the user who can grant the ability to set a device as a shared device.
    3.  Select the **Roles** tab in the **Related Links** section.
    4.  Select the **Edit** button.
    5.  In the **Collection** field, search for the name**mobile\_shared\_device\_mode\_enabler**.
    6.  Move **mobile\_shared\_device\_mode\_enabler** to the roles list.
    7.  Select **Save**.

