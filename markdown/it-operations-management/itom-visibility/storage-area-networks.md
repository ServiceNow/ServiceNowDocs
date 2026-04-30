---
title: Discovery of storage area networks \(SAN\)
description: Discovery collects information about storage area networks from specialized devices, such as storage arrays and Fibre Channel \(FC\) switches, and creates specific references between the tables in the SAN schema.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Storage Discovery via SMI-S and CIM, Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Discovery of storage area networks \(SAN\)

Discovery collects information about storage area networks from specialized devices, such as storage arrays and Fibre Channel \(FC\) switches, and creates specific references between the tables in the SAN schema.

## Multipath SAN storage example

Storage accessible to the Linux host consists of two physical fibre channel \(FC\) disks, mpatha and mpathb, connected to the host via a multipath FC SAN. The two HBAs on the host interface are connected with two fibre cables each to separate FC switches for failover capability. The FC fabric switches are connected to two FC storage processors on the storage server. In this example, each storage processor is connected to the storage volume's, **LUN 1** and **LUN 2**.

**Parent Topic:**[Storage Discovery via SMI-S and CIM](r_DataCollDiscoStorageviaSMISCIM.md)

