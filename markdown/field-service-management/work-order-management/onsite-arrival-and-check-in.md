---
title: Onsite arrival and check-in
description: The Onsite Arrival and Check-in process ensures accurate task location confirmation and effective time tracking.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Onsite arrival and check-in

The Onsite Arrival and Check-in process ensures accurate task location confirmation and effective time tracking.

## Check-In purpose

-   **Task Location and Prerequisites**
    -   Informs when the agent arrives at the task location.
    -   Completion of prerequisites before initiating work.
-   **Geofencing Validation**
    -   Verifies agent location within the configured geofence radius.
    -   Check-In status stores the outcomes such as success, failure, or skipped scenarios. The following table outlines the outcomes based on different scenarios and geofence validations when an agent clicks the **Check-in** button. The status gets stored in the Check-in status field of the work order task table. For more information, see [Create a work order task](../../planning-and-policy/task/t_CreateAWorkOrderTask.md)

        |Scenario|Check-In Status|
        |--------|---------------|
        |Geofence validation successful after clicking check-in button on the mobile app|Geofence validation successful|
        |Geofence validation failed after clicking check-in button on the mobile app|Geofence validation failed|
        |Check-in skipped, geofence validation failed \(agent starts work directly\)|Check-in skipped. Geofence validation failed|
        |Check-in skipped, geofence validation successful \(agent starts work directly\)|Check-in skipped. Geofence validation successful|
        |Offline, geofence validation failed \(agent clicks check-in button on the mobile app\)|Offline. Geofence validation failed|
        |Offline, check-in skipped, geofence validation failed \(agent is offline and skips to click check-in button\)|Offline. Check-in skipped, geofence validation failed|
        |Check-in skipped on platform|Platform. Geofence validation skipped|


## Check-In procedure

-   **Geofencing Process**
    -   Triggered upon agent clicking the **Check-in** button.
    -   Captures latitude and longitude of an agent's current location.
    -   'Check-In status' outcomes determine geofencing success or failure.
-   **Time Tracking**
    -   Captures time spent on the work site and task-related activities before starting work
    -   Duration saved in 'Actual Onsite Arrival Buffer Duration'.

## Check-In button visibility

-   Visible based on **Enable/Disable Onsite Arrival Check-in for Agents** property.

    To enable the system property, navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Configuration**.

-   Not mandatory; agents can skip and start work directly.

## Check-In and task execution during offline

1. Check-In process:

-   Enable the system property **Enable/Disable Onsite Arrival Check-in for Agents** to use the Check-in process.
-   Open the work order task record.
-   Click **Start Travel** and then click the **Check-In** button when reached at the work location.
-   Task state changes to **Onsite arrival.**
-   System checks the agent's current latitude/longitude within the geofence boundary.

2. Offline mode:

-   If the user is within the geofence but in offline mode, the system bypasses geofence check.
-   Updates a flag with status: "Offline Mode. Geofence could not be validated" in the work order task table.
-   Captures timestamp and updates the **Actual Onsite Arrival** field in the work order task.

3. Start work:

-   After arriving at the job site, clicking **Start Work** under **Related Links**.
-   The **Actual work start** field is automatically updated with the system time.
-   Task state changes to **Work In Progress**.
-   Automatic generation of the Task travel time card, stored under the **Time Worked** related list.

## Direct start work during offline

1. Direct Start Work: Open the work order task record and directly click **Start Work** under **Related Links**, skipping the **Check-In** action.

Enable the system property **Enable/Disable Onsite Arrival Check-in for Agents** to view the Check-in button although you choose to skip the check-in process.

2. Offline mode:

-   If the user is within the geofence but in offline mode, the system bypasses geofence check.
-   Updates the check-in status as "Offline Mode. Check-in skipped, and Geofence could not be validated" in the work order task table.
-   Captures timestamp and updates the **Actual Onsite Arrival** field in the work order task. Applicable when the system property **Enable/Disable Onsite Arrival Check-in for Agents** is enabled.

3. Travel duration calculation: The **Actual travel duration** field is automatically populated with the time difference between "Actual travel start" and "Actual onsite arrival time," unless manually set.

4. Automatic generation of the Task travel time card, stored under the **Time Worked** related list.

