---
title: IBM PVU mapping preparation for the legacy IBM PVU Process Pack
description: Most IBM PVU mapping and license checking for the legacy IBM PVU Process Pack is managed automatically.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Legacy IBM PVU Process Pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# IBM PVU mapping preparation for the legacy IBM PVU Process Pack

Most IBM PVU mapping and license checking for the legacy IBM PVU Process Pack is managed automatically.

For the automatic calculations to be as accurate as possible, it is important that configuration item and software model information be accurate.

The important fields describing the processor on the configuration item form are:

-   CPU type
-   CPU count
-   CPU core count

![PVU configuration item](../image/PVUConfigurationItem.png "PVU configuration item")

This CPU data is often added accurately when the CMDB is populated with information. If the fields contain incorrect information, manually edit the fields on the configuration item form.

The mapping between the configuration item form fields and processor definition fields is as follows.

|Configuration Item Form Field|Processor Definition Form Field|Definition|
|-----------------------------|-------------------------------|----------|
|CPU type|Processor name, Server model number, and Processor model number|Combination of processor name, server model number, and processor model number. The CPU type field is created as part of the general process described in Populating the CMDB. Some discovery tools fill in the CPU name instead of CPU type. If the CPU type field is empty, the CPU name field is used for mapping instead. \(You can configure the form to display the CPU name, if needed.\) If the CPU type field and the CPU name field are both empty, no mapping is done.|
|CPU count|Number of sockets|Number of sockets.|
|CPU core count|Cores per socket|Cores per socket|

The key field on the Software Model form is **License type**. For any software licenses you want to track with IBM PVU, open the corresponding software model form and select the **Per installation - IBM PVU** license type.

![PVU software model](../image/PVUSoftwareModel.png "PVU software model")

**Parent Topic:**[Legacy IBM PVU Process Pack](c_IBMPVUProcessPack.md)

