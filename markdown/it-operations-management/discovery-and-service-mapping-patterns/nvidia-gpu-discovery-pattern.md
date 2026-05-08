---
title: NVIDIA GPU discovery using patterns
description: The Discovery and Service Mapping Patterns application uses the Linux Server pattern extension Discover Nvidia GPU to find NVIDIA graphics processing units \(GPUs\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# NVIDIA GPU discovery using patterns

The Discovery and Service Mapping Patterns application uses the Linux Server pattern extension **Discover Nvidia GPU** to find NVIDIA graphics processing units \(GPUs\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The Discover Nvidia GPU pattern is an extension of the Linux Server pattern. For more information, see [Linux discovery](../../discovery/reference/r_DataCollDiscoLinuxComputers.md).

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the following applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   **Verify permissions for the following SSH command**

    Verify that you have **read access** permission for the SSH command: `nvidia-smi -q`.

-   **Create SSH credentials**

    For more information, see SSH credentials.

-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md#).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Discover Nvidia GPU Pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Model name of the GPU.|
|Manufacturer \[manufacturer\]|Vendor of the GPU.|
|Model ID \[model\_id\]|Product name of the GPU.|
|Serial number \[serial\_number\]|Serial number of the GPU.|

Additionally, Discovery populates the data in a non-CMDB table when running the Discover Nvidia GPU Pattern.

|Field|Description|
|-----|-----------|
|Board ID \[board\_id\]|Identifier for the GPU board, which can be used for diagnostic purposes.|
|Board Part Number \[board\_part\_number\]|The part number of the GPU board​.|
|Bus ID \[bus\_id\]|Identifier for the peripheral component interconnect \(PCI\) bus on which the GPU is located.|
|CUDA Version \[cuda\_version\]|Version of the CUDA Toolkit supported by the installed NVIDIA driver.|
|Driver version \[driver\_version\]|Version of the NVIDIA driver installed on the system.|
|GSP Firmware Version \[gsp\_firmware\_version\]|Version of the GPU System Processor \(GSP\) firmware.|
|Index \[index\]|Index number of the GPU as reported by the system.|
|Inforom ECC \[inforom\_ecc\]|Version of the error-correcting code \(ECC\) used to record data in the InfoROM.|
|Inforom IMG \[inforom\_img\]|Global version of the infoROM image.|
|Inforom OEM \[inforom\_oem\]|Version of the original equipment manufacturer \(OEM\) configuration data in the InfoROM.|
|Inforom PWR \[inforom\_pwr\]|Version of the power management data in the InfoROM.|
|Memory Free Usage \[memory\_free\_usage\]|Amount of GPU memory currently free.​|
|Memory Total Usage \[memory\_total\_usage\]|Total amount of GPU memory installed.|
|Memory Used Usage \[memory\_used\_usage\]|Amount of GPU memory currently in use.|
|Name \[name\]|Official product name of the GPU.|
|PCIE Current Link \[pcie\_current\_link\]|Current peripheral component interconnect express \(PCIe\) link generation.​|
|Performance State \[performance\_state\]|Power and performance levels of the GPU. Possible values run from P0 to P15, with lower numbers indicating higher performance.|
|Persistence Mode Status \[persistence\_mode\_status\]|Indicates whether persistence mode is enabled for the GPU. Possible values are Enabled or Disabled.|
|Serial Number \[serial\_number\]|Serial number of the GPU.|
|UUID \[uuid\]|Universally unique identifier \(UUID\) of the GPU.|
|Vbios Version \[vbios\_version\]|Basic Input/Output System \(BIOS\) of the GPU board.|

## CI relationships

Discovery creates these relationships to support the NVIDIA GPU discovery.

|CI|Relationship|CI|
|---|------------|---|
|Graphics Processing Unit \[cmdb\_ci\_gpu\]|Used by::Uses|Linux Server \[cmdb\_ci\_linux\_server\]|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

