---
title: Define and register a badge reader device using the badge reader client
description: Use the Badge Reader Client to create a badge reader device for registration in your system. Registering your badge reader enables you to make it operational at your Walk-up Experience on-site queue.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Walk-up Experience Badge Reader Integration setup and configuration, Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Define and register a badge reader device using the badge reader client

Use the Badge Reader Client to create a badge reader device for registration in your system. Registering your badge reader enables you to make it operational at your Walk-up Experience on-site queue.

## Before you begin

Role required: sn\_badge.badge\_admin

## About this task

There are two ways to register a badge reader device:

-   Assisted method, through the **Badge Reader Client**. You must create your own custom badge reader client software to integrate with the badge reader.
-   Manually, through the ServiceNow AI Platform®. Refer to [Define and register a badge reader device manually](config-badge-reader-settings.md) for details on this procedure.

The **Badge Reader Client** assisted registration method creates an initial Badge Reader record. When a badge is scanned using the badge reader client, this method automatically populates the **Device Identifier** field in the record with the badge reader device serial number.

Automatic population of the **Device Identifier** field saves you time from looking for the badge reader device serial number to add to the Badge Reader record.

To register your badge reader device with **Badge Reader Client** assistance, first you need to configure system properties to enable badge scan registration and disable the badge access token. The following System Properties must be configured:

-   **sn\_badge.enable\_scan\_registration**: Disabled by default. When set to **True**, this property enables n\_badge.badge\_admins to quickly register badge reader devices by scanning a badge.
-   **sn\_badge.disable\_access\_token**: Enabled by default. This property disables the access token requirement for the Badge Reader Integration API.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search by **Name** for the properties by typing `sn_badge`.

3.  Click **sn\_badge.enable\_scan\_registration** to open the system property record.

    The property is set to **False** by default.

4.  Change the property **Value** field to **True** and click **Update**.

5.  Click **sn\_badge.disable\_access\_token** to open the system property record.

    The property is set to **False** by default.

6.  Change the property **Value** field to **True** and click **Update**.

7.  Create and then run your own badge reader client.

8.  Swipe the badge admin's badge on the badge reader to register.

9.  The badge reader client performs a REST API call to api/sn\_badge/v1/reader/scan with the device identifier and the card data.

10. Navigate to **Badge Reader Integration** &gt; **Badge Readers** to view the newly created record.

11. Provide a name for the badge reader in the **Name** field.

    For example, `Building B Tech Lounge Badge Reader`.

    **Note:** The **Status** field is read only and indicates **New** when configuring a new badge reader. The field indicates **Activated** when a badge reader is approved for activation. If a badge reader is deactivated, the field indicates **Deactivated**.

12. Specify a **Badge Event Handler** using the search list ![search list icon](../../../common/image/List_SearchIcon.png) icon.

    **Note:** If no badge event handlers are available to select, create a new Badge Event Handler record. For details about this process, refer to [Create or modify Badge Reader Integration event handlers](create-or-modify-badge-event-handlers.md).

13. Verify that the **Device Identifier** and **Secret Key** fields are populated.

    The Device Identifier uniquely identifies the badge reader hardware. The client defaults to using the badge reader device serial number. The value entered must match the device serial number received from the client software application.

14. Populate the non-mandatory **Short description** and **Location** form fields if desired.

15. Select **Submit** to register the badge reader.


**Parent Topic:**[Walk-up Experience Badge Reader Integration setup and configuration](../concept/walkup-badge-read-integ-config.md)

