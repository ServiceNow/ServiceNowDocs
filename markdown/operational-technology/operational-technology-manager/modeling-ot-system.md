---
title: Modeling an Operational Technology system service
description: You can model an Operational Technology \(OT\) system service to create other control systems, such as a distributed control system \(DCS\).
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [DCS, control system]
breadcrumb: [Use, Operational Technology Manager, Operational Technology]
---

# Modeling an Operational Technology system service

You can model an Operational Technology \(OT\) system service to create other control systems, such as a distributed control system \(DCS\).

An OT system service refers to a category of technology and systems that are used to manage, control, and monitor physical processes, machinery, and industrial operations. OT system services are typically employed in sectors such as manufacturing, energy, utilities, and transportation.

OT system services can include the following.

-   Distributed Control Systems \(DCS\)​
-   Supervisory Control and Data Acquisition \(SCADA\)​
-   Industrial Control Systems \(ICS\)​
-   Safety Instrumentation Systems \(SIS\)​
-   Manufacturing Execution Systems \(MES\)​
-   Process Control Systems​
-   Transportation Management Systems​
-   Energy Management Systems​
-   Building Management system services \(BMS\)​

These system services collectively ensure that industrial processes run efficiently and safely.

**DCS example**

You can model OT system services to create other control systems. For example, you can model a distributed control system \(DCS\) and all related components \(PLCs, control modules, EWS, RTU, HMI, SCADA, and so on\). A DCS is a platform for automated control and operation of a plant or industrial process. It coordinates and supervises the entire plant of many varying processes​.

A DCS is a process-oriented system that uses closed loop control.​ The following table describes the components of a DCS.

|Component|Description|
|---------|-----------|
|Operator stations|Heart of DCS, operators view process, monitor alarms, and alerts.​|
|Servers, EWS, Historians|Data collection and data exchange for hardware configurations.​|
|Controllers, I/O modules|Data exchange to servers.​|
|Field devices|Devices such as transmitters, switches, actuators, and valves.|

A DCS differs from the centralized control system wherein a single controller at central location handles the control function but in a DCS, each process element, machine, or group of machines is controlled by a dedicated controller.

-   **[Create an Operational Technology system service](../task/create-ot-system-service.md)**  
Create an Operational Technology \(OT\) system service to model a distributed control system \(DCS\) and all of its related components, such as control modules and programming logic controls \(PLCs\).
-   **[Add a device to an Operational Technology system service](../task/add-devices-to-ot-system-service.md)**  
Add an Operational Technology \(OT\) device to an OT system service to create a relationship between the equipment model entity that the device belongs to and the OT system service.
-   **[Map an Operational Technology system service to an equipment model entity](../task/map-ot-system-service-to-equipment-model-entity.md)**  
Map an Operational Technology \(OT\) system service to an ISA equipment model entity by enabling a scheduled job. When the relationship between an OT device and an equipment model entity changes, the scheduled job recomputes the relationship between the OT system service and the equipment model entity.
-   **[View the dependency map for an Operational Technology system service](../task/view-dependency-map-for-ot-system-service.md)**  
View the dependency map for an Operational Technology \(OT\) system service to see the graphical representation of the hierarchical structure of the selected OT system service and its relationship with other entities in the production process.

**Parent Topic:**[Using the Operational Technology Manager](using-operational-technology-manager.md)

