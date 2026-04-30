---
title: Verify the meta data for your IBM hosts
description: To improve the accuracy of your IBM license calculations, verify the meta data for the physical hosts that your IBM software is installed on. Update any meta data that is incorrect or out of date.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Verify the meta data for your IBM hosts

To improve the accuracy of your IBM license calculations, verify the meta data for the physical hosts that your IBM software is installed on. Update any meta data that is incorrect or out of date.

## Before you begin

Role required: sam\_admin or sam\_user

## Procedure

1.  From your ServiceNow instance, navigate to **Workspaces** &gt; **Software Asset Workspace**.

    The Software Asset Workspace launches in a new tab.

2.  Open the License operations view.

3.  From the left navigation menu of the License operations view, navigate to **IBM ASP Integration** &gt; **Device settings**.

4.  Verify the meta data for all available hosts.

5.  If any of the following meta data is incorrect, update it.

    -   IBM PVUs per core
    -   Region

        **Note:** If the Region meta data is empty for any of your physical hosts, the **Default Region for IBM Devices** \(**sn\_samp\_ibm\_lic.default\_region**\) Software Asset Management property automatically associates those hosts with a default region. By default, this system property is set to **North America and South America**. However, you can also set this system property to **Europe and Africa** or **Asia and Australia**. License usage can be calculated only for physical hosts that are associated with a region. See [Software Asset Management properties](../reference/sam-properties.md) for more information on this property.

    -   Usage type
    **Note:** You cannot update the Device, PVU Comment, and IBM PVU mapping meta data.

    1.  Double-click the value in the incorrect meta data field.

    2.  When prompted, enter or select the correct value and then select the Save icon \(![Save icon.](../image/save-icon.png)\).

        The meta data field updates with the correct value.


**Parent Topic:**[Authorized SAM Provider \(ASP\) integrations for IBM](../concept/ibm-asp-integration.md)

