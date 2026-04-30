---
title: Field Service IT workflow example
description: This Field Service IT workflow example describes a coordinated field service and IT service management situation.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Field Service Management workflow examples, Exploring Field Service Management, Field Service Management]
---

# Field Service IT workflow example

This Field Service IT workflow example describes a coordinated field service and IT service management situation.

As a retail store manager, Joe was unhappy with the quality of service delivered by the organization's IT support and field service processes. When Joe called in a problem to the store's IT help support desk, the support representative would ask Joe a long list of questions about the equipment but could never provide Joe with an estimate of how long it would take to fix the issue. Sometimes, the technician would arrive with the wrong parts because someone entered wrong information when manually transcribing data between the IT support system and field service system. Because no one was keeping track of system upgrade schedules, outdated software would bring down the card transaction system, resulting in lost sales and disappointed customers.

Joe's experience changed for the better after the company implemented ServiceNow Field Service Management with IT Service Management.

Administrators from IT Support and Field Service Management could develop processes that automatically collect and share information across the IT Support and Field Service teams, including recommended solutions for known issues and maintenance schedules to address potential issues before they become problems. Now, if Joe discovers an issue, they can scan the malfunctioning equipment to automatically open an incident with IT Support containing all the required equipment information.

If the solution requires a field technician, the IT Support representative can click a button to open a field service work order containing the repair tasks along with the required information from the Support incident. Field Service Management automatically routes the tasks to the technician closest to the store who has the availability and the required skills for the tasks. As the technician starts traveling to the site, the system automatically notifies Joe of the technician's estimated arrival time.

The technician can use the Mobile Agent to review information about the issue, suggested solutions, and preventive maintenance. After fixing the issue and performing preventative maintenance to prevent new issues from affecting the equipment, the technician can digitally document the work and close the work order.

Field Service Management automatically records tracking information such as parts used, incidental expenses, and time to completion on a shared platform so that both the IT Support and Field Service teams can include the data in their reports and analysis. Improving data quality across IT Support and Field Service systems enabled technicians to resolve issues faster, and scheduling maintenance helped prevent costly system downtime. As system performance improved, Joe's store experienced better sales revenue and happier customers.

-   **Key Benefits**
    -   Increase visibility of assets, technician location, and status to improve performance and productivity
    -   Minimize service costs by reducing documentation time
    -   Meet customer expectations with quicker time to resolution
-   **Roles**
    -   Customer
    -   Field Service agent
    -   IT Service Management agent
-   **Products**
    -   Field Service Management
    -   IT Service Management

## Field Service IT workflow diagram

![Field Service Management IT workflow from opening an incident to analyzing the audit reports. For more text description, refer to the folloiwng table.](../image/FSM-it-workflow-asset0012979final.png)

## IT Field Service workflow steps

The following table provides the steps for the IT Field Service workflow.

|Steps|Description|
|-----|-----------|
|1. Open incident|At a store location, the point-of- sale \(PoS\) systems are having trouble reading cards. The store manager identifies the issue and uses the Mobile Agent to scan the bar code on the PoS system. This automatically creates and populates an incident, which is assigned to the store Support Service desk.|
|2. Generate work order|The Support team triages the incident and determines whether it requires a software or hardware fix. In this case, the PoS system requires a software upgrade, so the store Support Service Desk opens a high-priority work order directly from the incident with just one click.|
|3. Assign a technician|The work order can be assigned to either internal or external third-party teams. In this case, the work order is automatically assigned to an internal technician. The technician is notified of the assignment, accepts the task, and starts travelling to the store. The store manager is informed of the technician’s expected arrival time.|
|4. Comprehensive check|With the Mobile Agent , the technician has access to all the information about the PoS system and its history \(for example, inspections, past fixes, and so on\), along with relevant knowledge base articles that can help them resolve the issue. Technicians do a thorough maintenance of the PoS system, which helps reduce future issues and travel costs.|
|5. Complete work order|Once the technician completes the work, they document their work effort, make any notes, and close the work order. The store manager then digitally signs and confirms the work order is complete. This submission automatically updates the incident.|
|6. Track and provide audit trail|A PDF summary of all the completed tasks, parts used and returned, incidental expenses, and time taken to do the work is automatically created and attached to the work order. All data is tracked in one single platform for future trend analysis, reports, and audits.|

**Parent Topic:**[Field Service Management workflow examples](fsm-use-cases.md)

