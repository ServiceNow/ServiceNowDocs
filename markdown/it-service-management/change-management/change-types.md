---
title: Change types
description: Change Management supports the three types of service changes ITIL describes — standard, emergency, and normal. The change type determines which state model is invoked and the change process that must be followed.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Change Management, Change Management, IT Service Management]
---

# Change types

Change Management supports the three types of service changes ITIL describes — standard, emergency, and normal. The change type determines which state model is invoked and the change process that must be followed.

Watch this eight-minute video for an overview of Change Management in ITSM.Introduction to change management; types of change; creating and working change requests; improving efficiency through standard changes.

-   **Standard change**

    A standard change is a pre-authorized change that is low risk, relatively common and follows a specified procedure or work instruction.

    A standard change is one that is frequently implemented, has repeatable implementation steps, and has a proven history of success. As Standard changes are pre-approved, they follow a stream lined process in which group level or peer approval and CAB authorization steps are not required.

    Approved standard change requests can be predefined in a catalog of templates to make accessing and requesting a standard change more efficient. This ability also enables the Change Management team to control the changes that are authorized as standard.

-   **Emergency change**

    A change that must be implemented as soon as possible, for example to resolve a major incident or implement a security patch. This change is of such a high priority that it bypasses group and peer review and approval and goes straight to the Authorization state for approval by the CAB approval group.

    Emergency changes cover the following types of emergencies:

    -   Fix on fail or retroactive situations where the impact to service has already been experienced.
    -   Fail or fail situations where the impact to service is imminent if action is not taken.
    These changes do not follow the complete life cycle of a normal change due to the speed with which they must be authorized. Therefore, they progress directly to the **Authorize** state for approval from the CAB Approval group.

    During an emergency change, there are chances that an unplanned CI change activity occurs. During such a case, an unauthorized change request is created and sent for approvals. For more information, see [Unauthorized change request](unauthorized-change-request.md).

-   **Normal change**

    Any service change that is not a standard change or an emergency change.

    Normal change requests follow a prescriptive process which requires two levels of approval before being implemented, reviewed, and closed. These changes require a full range of assessments and authorizations such as peer or technical approval, change management, and Change Advisory Board \(CAB\) authorization, to ensure completeness, accuracy, and the least possible disruption to service. These changes are most often scheduled outside of defined change blackout windows or during defined maintenance windows. The normal type is used to implement beneficial change for any change to a service that is not a standard or emergency change.


**Parent Topic:**[Exploring Change Management](exploring-change-management.md)

**Related topics**  


[Add a new change request type](../task/t_AddNewChangeType.md)

