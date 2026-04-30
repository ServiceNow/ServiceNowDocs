---
title: Configure asset utilization metrics
description: Configure the display of the asset utilization metrics for Microsoft Endpoint Configuration Manager for Investigation.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation, Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure asset utilization metrics

Configure the display of the asset utilization metrics for Microsoft Endpoint Configuration Manager for Investigation.

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  Select the required CI device, and verify the CMPivot entities and attributes.

    For more information, see [Verify a CMPivot entity](verify-cmpivot-entity.md).

3.  Configure the Disk Utilization metrics by verifying that the **Disk** CMPivot entity exists and has the attributes **Size** and **Free Space**.

4.  Configure the Memory Utilization metrics.

    1.  Verify that the **Memory** CMPivot entity exists and has the attribute **TotalPhysicalMemory**.

    2.  Verify that the **OS** CMPivot entity exists and has the attribute **FreePhysicalMemory**.

5.  Configure the CPU Utilization metrics by verifying that the **Processor** CMPivot entity exists and has the attribute **LoadPercentage**.

    If the **Processor** CMPivot entity doesn’t exist, you must add the entity to the hardware inventory. For more information, see [Extend hardware inventory](extend-hardware-entity.md).

6.  Configure the Uptime metrics by verifying that the **OperatingSystem** CMPivot entity exists and has the attribute **LastBootUpTime**.


## Result

The asset utilization metrics is displayed on the **Investigation** tab of the incident record in Service Operations Workspace.

**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](../concept/config-ci-metrics-mecm-adapter.md)

