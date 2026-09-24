---
title: View RFID information of assets
description: View the Radio Frequency Identification \(RFID\) information of assets to manage and locate important assets easily.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/view-rfid-info.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Inventory and stockroom operations, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# View RFID information of assets

View the Radio Frequency Identification \(RFID\) information of assets to manage and locate important assets easily.

## Before you begin

Role required: asset

## Procedure

1.  Navigate to a hardware asset for which you want to view the RFID information.

<table id="choicetable_l5h_2mg_ywb"><thead><tr><th align="left" id="d200015e50">

Interface

</th><th align="left" id="d200015e53">

Action

</th></tr></thead><tbody><tr><td id="d200015e59">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Hardware Assets**.
2.  Select an Asset tag for which you want to view the RFID information.
3.  Select the Preview icon \(\[Omitted image "preview-icon.png"\] Alt text: Preview icon\) beside the **RFID tag** field in the **General** tab.
4.  Select **Open Record** to view the RFID information of the asset.


</td></tr><tr><td id="d200015e107">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **Hardware Asset Workspace** &gt; **Asset estate**.
2.  Select the **Hardware assets** tab.
3.  Select the display name of a hardware asset for which you want to view the RFID information.
4.  Select the Open Record icon \[Omitted image "preview-icon.png"\] Alt text: Preview icon. in the **RFID tag** field under the **Details** tab.


</td></tr></tbody>
</table>    **Note:** The RFID tag field doesn't exist for an excluded asset.

    |Field|Description|
    |-----|-----------|
    |RFID tag|Unique identifier of the RFID tag in the RFID system.|
    |Site name|Name of the site as defined in the RFID system.|
    |Type|Resource type as defined in the RFID system.|
    |Zone group|Zone group as defined in the RFID system.|
    |Serial number|Unique identifier as defined in the RFID system.|
    |Zone group dwell|Length of time the asset has been in the current zone group relative to the timestamp of the data import.|
    |Tag source|The application source of RFID data.|
    |Zone|Zone as defined in the RFID system.|
    |Last blink time|Last time the RFID tag was scanned.|
    |Zone dwell|Duration for which the asset has been in the current zone as compared to the timestamp of the data import.|
    |Last blink elapsed time|Duration for which the asset has been scanned in the RFID system as compared to the timestamp of the data import.|
    |Grid-x, Grid-y, Grid-z|Physical location as defined in the RFID system.|
    |Status|Status of the matching of RFID information to the resource.|
    |Active|Option to map RFID information to the Asset \[alm\_asset\] table. This option is selected by default.|

    **Note:**

    The activity history is captured only for RFID tag and Zone.


**Parent Topic:**[Inventory and stockroom operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/manage-your-stockrooms.md)

**Related topics**  


[Manage the receiving of assets at stockrooms in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit hardware asset inventory]()

[Track asset location using indoor maps]()

[Manage your inventory through pallet assets]()

[View stockroom details]()

[Integrating Zebra technology RFID system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/integrating-rfid.md)

