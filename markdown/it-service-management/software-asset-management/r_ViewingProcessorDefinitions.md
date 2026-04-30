---
title: Legacy Software Asset Management plugin processor definitions
description: Processor definitions for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin are automatically derived from the information in the configuration item form for an item such as a computer or server.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy IBM PVU Process Pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Legacy Software Asset Management plugin processor definitions

Processor definitions for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin are automatically derived from the information in the configuration item form for an item such as a computer or server.

To view a processor definition, navigate to **Software Asset** &gt; **Reconciliation** &gt; **Processor Definitions** and click an item.

![SAM processor definition](../image/SAMProcessorDefinition.png "Processor definition")

The following read-only fields are listed.

|Field|Description|
|-----|-----------|
|Display name|Name of the processor as it should appear in the processor list.|
|Manufacturer|Company that built the processor.|
|Server model number|Number assigned to the model by the server manufacturer.|
|Number of sockets|Number of dies on the computer motherboard. The number of CPUs per die is specified by **Cores per socket**.|
|IBM PVU Mapping|The IBM PVU mapping to which this processor is associated. The information in this field is automatically calculated from the server model number, number of sockets, processor name, and processor model number, based on the rules defined in the IBM PVU Table.|
|Processor name|Name assigned to the processor by the manufacturer.|
|Processor model number|Number assigned to the model by the processor manufacturer.|
|Cores per socket|Number of cores \(functional unit needed to execute programs\) on each physical connection \(socket\) on the motherboard.|
|Match level|Accuracy level of the association between processor and PVU mapping. Automatically set when association is inferred.|

**Parent Topic:**[Legacy IBM PVU Process Pack](../concept/c_IBMPVUProcessPack.md)

