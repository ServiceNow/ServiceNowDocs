---
title: Workplace Location Assignment service
description: The Workplace Location Assignment service automatically assigns a workplace location to an employee.
locale: en-US
release: zurich
product: Workplace Case Management
classification: workplace-case-management
topic_type: reference
last_updated: "2026-02-18"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Workplace Location Assignment service

The Workplace Location Assignment service automatically assigns a workplace location to an employee.

Workplace Location Assignment is an automated service that analyzes employee data and organizational requirements to suggest workplace locations. This service is primarily used to auto-assign a workplace location for new hires.

The service contains the following activities:

-   **Get suggested workplace location**

    This activity fetches user details and suggests a location.

    1.  The activity searches for a workspace that has the same allocation as the employee's manager, team members, or collaborators. The allocation that the activity searches for is based on the **sn\_wsd\_core.ALLOCATION\_TYPE**.

        For example, if the allocation type is set to Cost Center, the system searches for workspaces with the same Cost Center as the collaborators.

    2.  If a location with the matching criteria is found and is available, the location details are added to the workplace task. The location is then picked up by the `Assign workplace location` activity.

        If a matching location is a neighborhood, the work notes of the workplace case are updated and the case is closed.

    3.  If no matching locations are found, the workplace case is updated and the `Manually assign location for new hire` activity is triggered.
-   **Assign workplace location**

    This activity assigns the recommended location to the employee's workplace profile.

    1.  The activity searches for the workplace task updated by the `Get suggested workplace location` activity and fetches the recommended location.
    2.  A workplace profile is created for the employee, and the recommended location is added as a primary assignment.
    3.  The workplace case is updated.
-   **Manually assign location for new hire**

    This activity is triggered if no recommended locations are found for the employee. The activity creates a task where a space planner must manually assign a location to the employee.


**Parent Topic:**[Workplace Case Management references](../concept/workpalce-case-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Case Management](components-installed-with-workplace-case-mgmt.md)

[Properties installed with Workplace Case Management](properties-installed-with-workplace-case-mgmt.md)

[Workplace Service form](workplace-service-form.md)

