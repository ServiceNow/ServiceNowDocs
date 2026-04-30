---
title: Field Service operations workflow example
description: This Field Service operations workflow example shows how a clinical engineering manager at a healthcare provider handles an MRI scanner issue that can be resolved with a firmware upgrade.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Field Service Management workflow examples, Exploring Field Service Management, Field Service Management]
---

# Field Service operations workflow example

This Field Service operations workflow example shows how a clinical engineering manager at a healthcare provider handles an MRI scanner issue that can be resolved with a firmware upgrade.

Maria, a clinical engineering manager, is notified of an MRI scanner issue. She was frustrated with the slow upgrade process, which involved long waits and multiple calls to the vendor's support line. After the vendor implemented ServiceNow, Maria's experience improved.

With the Field Service Management application, the vendor automates the upgrade process, leading to more efficient service and higher customer satisfaction. Maria can submit a service request with a preferred time through the self-service portal. The Customer Service Management \(CSM\) application creates a work order with necessary details, and FSM assigns the task to a nearby field agent with the right skills.

Maria receives a text with a map of the field agent's location and arrival time. Once the upgrade is complete, the field agent marks the task as complete in the FSM mobile app. Maria confirms the work and signs the work order on their phone. FSM saves all work order info for future analysis, reporting, audits, and compliance.

ServiceNow helped the vendor complete the upgrade quickly, reducing phone calls and saving important issue and resolution data to enhance Maria's customer experience.

## Field Service operations workflow diagram

![Field Service Management operations workflow. For text description, refer to the following table.](../image/FSM-operations-workflow-asset0012997final.png)

## Field Service operations workflow steps

The following table provides the steps for the Field Service operations workflow.

|Steps|Description|
|-----|-----------|
|1. Open request|The clinical engineering manager logs in to the self-service portal of the asset vendor and opens a service request with a preferred time of service.|
|2. Auto-generate work order|The appointment booking application automatically generates a work order that contains all the tasks needed to complete the upgrade.|
|3. Auto-dispatch technician|Tasks can be automatically assigned to a field agent based on their location, skill set, and availability using dynamic scheduling. The field agent receives a push notification on their mobile app, which they can see and accept \(or reject for reassignment to another technician\). Once accepted, the work order is updated.|
|4. Access information|With the ServiceNow Mobile Agent , the field agent can access information including location, equipment, customer history, knowledge articles, and others to help them successfully complete the task. When the field agent is on their way, a text message is automatically sent to notify the customer. It includes a link to view a map with the field agent’s current location and estimated time of arrival to set expectations and improve the overall experience.|
|5. Complete work order|Once the field agent upgrades the firmware and completes the task, the clinical engineering manager can digitally sign and confirm the work order is complete.|
|6. Track and audit|The signed status automatically generates a PDF summary of the work order including the completed tasks, parts used and returned, incidental expenses, and the time required to complete the work. The PDF is attached to the work order form for tracking and audit purposes.|
|7. Report and analyze|All data and timelines are also tracked in the work order, and are available for trend analysis, reports, and audits to satisfy compliance requirements. The Field Service manager compares the metrics from the work order to key performance indicators \(KPIs\) available by default within theServiceNow Performance Analytics dashboards.|

**Parent Topic:**[Field Service Management workflow examples](fsm-use-cases.md)

