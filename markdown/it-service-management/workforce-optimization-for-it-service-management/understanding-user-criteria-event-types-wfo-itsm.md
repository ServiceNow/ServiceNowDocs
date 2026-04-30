---
title: Understanding user criteria for event types in Workforce Optimization for ITSM
description: Manage user access for any event type such as meeting, training, and time-off requests in the team calendar.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Scheduling your teams' work in Workforce Optimization for ITSM, Scheduling in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Understanding user criteria for event types in Workforce Optimization for ITSM

Manage user access for any event type such as meeting, training, and time-off requests in the team calendar.

You can include or exclude Create, Read, Write or Update, and Delete \(CRUD\) rights for event types using the inclusion and exclusion user criteria access. You can perform the CRUD operations for users, groups, or roles.

**Note:** By default:

-   Users have [role-based access](../reference/configurable-wfo-itsm-scheduling-reference.md) to manage event types.
-   Team members don’t have read-access to events of type **Actual work**.

For additional flexibility around managing the CRUD access, you can set the user criteria for each event type. For example, if team members don't have access to edit their work shifts using their role-based access, you can set that access using user criteria. You can set this access for specific team members or for the whole group.

The flow diagram shows the logic on how inclusion and exclusion user criteria access work for event types.![Infographic that describes the user criteria access for event types flow. The text that describes the flow follows this infographic.](../image/inclusion-exclusion-criteria-event-types.png)

**How inclusion and exclusion user criteria access works**

When the user criteria rules get evaluated, it's done in the following order:

1.  The system first evaluates the exclusion access for each criteria.
    -   If the exclusion access for a CRUD operation is set to **true**, then the system evaluates the user criteria.
        1.  If the user doesn’t have access based on their role, then the user is denied access for the specific CRUD operation.
        2.  If the user isn’t denied access, then the system evaluates the inclusion criteria.
    -   If the exclusion access for a CRUD operation is set to **false**, then the system evaluates the inclusion criteria.
2.  For the inclusion access, for a specific CRUD operation such as Create, the system checks if at least one of the inclusion user criteria is set to **true**. If yes, then the system evaluates the user criteria based on the user's role access.
    -   If the user:
        -   Has access for the CRUD operation based on their user role, then the user can perform that action. For example, if the event type is training and the CRUD operation is **Create** then the user can create the training event types.
        -   Doesn’t have access for the CRUD operation based on their user role, then the user can’t perform that action.
    -   If at least one of the inclusion criteria isn’t set to **true**, the user doesn’t have access to the specific CRUD operation. In this example, the user can’t create the training event types.

**Note:** The exclusion access always takes precedence over the inclusion access. If no inclusion or exclusion access is set, then the role-based access is used for managing event types.

-   **[Create user criteria for event types in Workforce Optimization for ITSM](../task/user-criteria-event-types-wfo-itsm.md)**  
Add a user criteria record to specify which users, roles, and groups can access event types in Workforce Optimization for ITSM.
-   **[Include or exclude user access for event types​](../task/include-or-exclude-user-access-for-event-types.md)**  
Add or remove access to users for any event type so that they can view event types that are relevant only to them.​
-   **[Verify access criteria for a group or a team member in Workforce Optimization for ITSM](../task/verify-user-access-wfo-itsm.md)**  
Check what create, read, update, and delete rights your groups or your team members have for events to make sure that they have the correct permissions that they need.

**Parent Topic:**[Scheduling your teams' work in Workforce Optimization for ITSM](scheduling-configurable-workforce-optimization-itsm.md)

