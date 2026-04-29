---
title: View IBM PVU mappings for the legacy IBM PVU Process Pack
description: Every rule listed in the IBM PVU Table is represented by one PVU mapping record in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy IBM PVU Process Pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# View IBM PVU mappings for the legacy IBM PVU Process Pack

Every rule listed in the IBM PVU Table is represented by one PVU mapping record in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## About this task

For example, in the IBM PVU Table there is one line with processor name POWER5 QCM and in IBM PVU mappings there is a line representing POWER5 QCM.

![PVU mappings list](../image/PVUMappingsList.png "PVU mappings list")

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **IBM PVU Mappings**.

2.  Click a **Short Description** for detailed information about the mapping.

    ![SAM PVU mapping](../image/SAMPVUMapping.png)

    The fields are for information only and cannot be edited.

    |Field|Description|
    |-----|-----------|
    |Processor names|Names of running processors. Processor names are separated by commas.|
    |Model-based condition|Regular expression used to determine whether the server model number of a computer's processor definition matches that of the PVU entry.|
    |Socket-based condition|Regular expression used to determine whether the number of sockets of a computer's processor definition matches that of the PVU entry.|
    |Short description|A short description of this PVU mapping.|
    |PVUs per core|Number of processor value units consumed \(according to the IBM PVU chart\) by each core.|
    |Max cores|Maximum number of cores on the processor family, as shown in the IBM PVU Table \(rightmost column under cores per socket\).|
    |Rule publication date|Date published by IBM on the PVU Rules table.|


**Parent Topic:**[Legacy IBM PVU Process Pack](../concept/c_IBMPVUProcessPack.md)

