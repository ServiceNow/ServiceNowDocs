---
title: Field Service operations workflow example
description: This Field Service operations workflow example provides a use case of a clinical engineering manager at a healthcare provider who is notified of an issue with an MRI scanner that the most recent firmware upgrade can solve.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Field Service Management workflow examples, Exploring Field Service Management, Field Service Management]
---

# Field Service operations workflow example

This Field Service operations workflow example provides a use case of a clinical engineering manager at a healthcare provider who is notified of an issue with an MRI scanner that the most recent firmware upgrade can solve.

As a Clinical Engineering Manager at a hospital, Maria was frustrated at the time the hospital’s equipment vendor took to upgrade equipment. Calling the vendor’s support line usually meant waiting on hold for a support person, then multiple calls from support people and repair technicians to get the information required for resolving the problem. If Maria was on another call or not near their office where Maria could look up a serial number for the repair technician, more time was lost.

When the vendor implemented the ServiceNow platform, Maria's customer experience improved.

With the Field Service Management application, the vendor’s administrator can automate many of the steps required to upgrade Maria's equipment. Maria can log into the vendor’s self-service portal and submit a service request with a preferred time of service for the field technician’s visit. The Customer Service Management \(CSM\) application automatically creates a work order containing the required details for the equipment, parts, and upgrade steps.

The Field Service Management \(FSM\) workflow automatically routes the work order task to a technician located near the hospital who has the availability and required skills for the task. Once the technician is en route, the FSM automatically sends a text message to Maria with a map showing the technician’s current location and an estimated time of arrival.

When the technician completes the upgrade and marks the task as complete in the FSM mobile app, FSM sends the work order to Maria’s mobile phone. Maria digitally confirms the work is complete and signs the work order. FSM saves all the information for the work order to support future analysis, reporting, audits and compliance activity by the vendor organization.

With the help of the ServiceNow application, the vendor finished the upgrade task faster, with fewer phone calls from or to Maria. In addition, the vendor saved vital information about the issue and its resolution for analysis and planning to further improve Maria's customer experience.

-   **Key benefits**
    -   More efficient service operations to improve customer satisfaction.
    -   The right technician is sent the first time to fix issues.
    -   Issue history is saved to make further interactions go more smoothly and quickly.
-   **User roles**
    -   Customer
    -   Field agent
-   **Products**
    -   Customer Service Management
    -   Field Service Management

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

