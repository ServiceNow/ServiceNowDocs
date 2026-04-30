---
title: Edit or view OT devices after import or discovery
description: Use the options on the Operational Technology \(OT\) menu to edit or view detailed information for the OT devices in your enterprise.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Operational Technology Manager, Operational Technology]
---

# Edit or view OT devices after import or discovery

Use the options on the Operational Technology \(OT\) menu to edit or view detailed information for the OT devices in your enterprise.

## Before you begin

Import your Operational Technology device data in any of the following ways:

-   Run IT Discovery for OT Networks. For more information, see [IT Discovery for Operational Technology \(OT\) Networks](../concept/discovery-for-operational-technology.md).
-   Use an Operational Technology Certified Service Graph Connector from the ServiceNow Store.

Role required: cmdb\_ot\_viewer, cmdb\_ot\_editor, cmdb\_ot\_admin, or admin

## About this task

If you have an assigned cmdb\_ot\_viewer role, you can only view OT devices. If you have an assigned cmdb\_ot\_editor or cmdb\_ot\_admin role, you can edit OT device records in the following ways:

-   Edit OT device records individually on the ServiceNow AI Platform.
-   Bulk edit multiple OT device records from the Industrial Workspace list view.

## Procedure

1.  To edit one OT device record ServiceNow AI Platform, follow these steps.

    1.  Navigate to **All** &gt; **Operational Technology \(OT\)** and select one of the following menu items:
        -   **All OT Devices**

            By default, this list does not include control modules.

        -   **All OT Devices by IP Address**

            When you view the All OT Devices by IP Address list, note the following:

            -   An OT device with multiple IP addresses is displayed once per assigned IP address.
            -   Select the name of the OT device to open the OT device record. Selecting the IP address that is displayed for the record opens the record of only the IP address.
            -   You **cannot** create a new OT device record from this list.
        -   **OT Control Systems**

            By default, this list does not include control modules.

        -   **OT Control Systems with Modules**

            When you view the OT Control Systems with Modules list, note the following:

            -   The list view displays all the Control Modules grouped by their parent Control System.
            -   You cannot create a new OT device record from this list.
    2.  In the **OT device** column, select the OT device that you want to edit.
    3.  On the form, fill in the fields.
    4.  Click **Update**.
2.  To bulk edit multiple OT device records Industrial Workspace, follow these steps.

    1.  Navigate to **All** &gt; **Industrial Workspace**.
    2.  Open the list \(![List icon in the Industrial Workspace.](../../../common/image/icon-list.png)\) view and select one of the following lists available under **Operational Technology \(OT\)**.
        -   OT Supervisory Systems
        -   OT Control Systems
        -   OT Field Devices
        -   OT Computer and Servers
        -   OT Network Gear
        -   Industrial IoT \(IIoT\)
        -   Unclassed OT Devices
    3.  Select the check box next to each OT device that you want to edit.

        **Note:** You can only bulk edit OT devices with the same **Class** field. You can't use the bulk edit feature for OT devices with different classes.

    4.  To edit the configuration item \(CI\) fields, select the **Edit** button and edit the form fields as needed. ![The edit button in the Industrial Workspace list view header.](../image/edit-button.png)

        **Note:** The maximum number of records that you can bulk edit the CI fields for is the records shown on a single page.

    5.  Click **Update**.
    6.  To edit the OT device details, select the **Edit OT details** button and edit the form fields as needed.![The Edit OT details button in the Industrial Workspace list view header.](../image/edit-ot-details.png)

        **Note:** Bulk editing OT details is a background job that can take time to complete. If the background job is busy, you can't bulk edit other OT device records.


-   **[OT device related items and related lists](../reference/ot-assets-related-links-and-lists.md)**  
The All OT Devices, All OT Devices by IP Address, and All OT Devices by CI menu options contain several related items and lists.

**Parent Topic:**[Using the Operational Technology Manager](../concept/using-operational-technology-manager.md)

