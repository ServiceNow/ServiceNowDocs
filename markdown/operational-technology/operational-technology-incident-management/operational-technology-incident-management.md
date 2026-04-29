---
title: Operational Technology Incident Management
description: Operational Technology Incident Management enables engineers to quickly resolve Operational Technology \(OT\) device and production process issues.
locale: en-US
release: australia
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Operational Technology Incident Management, Operational Technology]
---

# Operational Technology Incident Management

Operational Technology Incident Management enables engineers to quickly resolve Operational Technology \(OT\) device and production process issues.

Operational Technology Incident Management enables you to manage OT incidents separately from IT incidents. OT incidents occur when there’s a disruption in service provided by an OT device on an OT network. Sometimes, the OT device may not be known when the incident is first created. If the OT device is unknown, an incident can be raised for an equipment model entity where the issue occurred.

The OT Incident manager is responsible for managing the default life cycle of incidents from creation to closure. The OT Incident Management process has many states, and each is important to the success of the process and the quality of service delivered. The different states are shown in the following diagram.

![The different states of the Operational Technology Incident management process.](../image/ot-incident-management-process-states.png "Operational Technology Incident Management process states")

The incident states are as follows.

<table id="table_obl_ghy_fwb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Incident is logged but not yet investigated.

</td></tr><tr><td>

In Progress

</td><td>

Incident is assigned and being investigated.

</td></tr><tr><td>

On Hold

</td><td>

The responsibility for the incident temporarily shifts to another entity to provide further information, evidence, or a resolution. When you select the **On Hold** option, the following **On hold reason** list appears. These list options call out where your additional information is coming from.-   Awaiting Caller
-   Awaiting Change
-   Awaiting Problem
-   Awaiting Vendor

If the On Hold reason is **Awaiting Caller**, the **Additional comments** section is required.

**Note:** If the caller updates the incident, the On Hold reason field is cleared and the state of the incident is changed to **In Progress**. An email notification is sent to the user whose name is mentioned in the **Assigned to** field and the users on the Watch list. You can place an incident On Hold one or more times before closing the incident.

</td></tr><tr><td>

Resolved

</td><td>

An acceptable fix is provided for the incident to ensure that it doesn't happen again.

</td></tr><tr><td>

Closed

</td><td>

Incident is marked **Closed** after it's in the **Resolved** state for a specific duration, and it's confirmed that the incident is satisfactorily resolved.

</td></tr><tr><td>

Canceled

</td><td>

Incident was triaged but found to be a duplicate incident, an unnecessary incident, or not an incident at all.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Operational Technology Incident Management](exploring-operational-technology-incident-mgt.md)

