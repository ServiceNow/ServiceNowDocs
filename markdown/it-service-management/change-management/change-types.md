---
title: Change types
description: Change Management supports the three types of service changes ITIL describes — standard, emergency, and normal. The change type determines which state model is invoked and the change process that must be followed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/change-types.html
release: brazil
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Explore, Change Management, IT Service Management]
---

# Change types

Change Management supports the three types of service changes ITIL describes — standard, emergency, and normal. The change type determines which state model is invoked and the change process that must be followed.

-   **Standard change**

    A standard change is a pre-authorized change that is low risk, relatively common and follows a specified procedure or work instruction.

    A standard change is one that is frequently implemented, has repeatable implementation steps, and has a proven history of success. As Standard changes are pre-approved, they follow a stream lined process in which group level or peer approval and CAB authorization steps are not required.

    Approved standard change requests can be predefined in a catalog of templates to make accessing and requesting a standard change more efficient. This ability also enables the Change Management team to control the changes that are authorized as standard.

    For example, a routine TLS certificate renewal or a documented password policy update is typically handled as a standard change.

-   **Emergency change**

    A high-priority change implemented immediately to resolve a major incident or apply a security patch. It bypasses group and peer review and goes directly to the Authorization state for CAB approval.

    Emergency changes cover the following types of emergencies:

    -   Fix on fail or retroactive situations where the impact to service has already been experienced.
    -   Fail or fail situations where the impact to service is imminent if action is not taken.
    These changes do not follow the complete life cycle of a normal change due to the speed with which they must be authorized. Therefore, they progress directly to the **Authorize** state for approval from the CAB Approval group.

    During an emergency change, there are chances that an unplanned CI change activity occurs. During such a case, an unauthorized change request is created and sent for approvals. For more information, see [Unauthorized change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/unauthorized-change-request.md).

-   **Normal change**

    Any service change that is not a standard change or an emergency change.

    A normal change differs from a standard change in its approval path. Unlike a standard change, which is pre-approved and bypasses Change Advisory Board \(CAB\) authorization, a normal change requires assessment, peer or technical approval, and CAB authorization before implementation.

    Normal change requests follow a prescriptive process which requires two levels of approval before being implemented, reviewed, and closed. These changes require a full range of assessments and authorizations such as peer or technical approval, change management, and Change Advisory Board \(CAB\) authorization. This is to confirm completeness, accuracy, and the least possible disruption to service. These changes are most often scheduled outside of defined change blackout windows or during defined maintenance windows. The normal type is used to implement beneficial change for any change to a service that is not a standard or emergency change.


The following table summarizes about the three change types:

|Change type|Pre-approved|Required CAB|Typical use|
|-----------|------------|------------|-----------|
|Standard|Yes|No|Low-risk, repeatable changes with a proven history of success.|
|Normal|No|Yes|Any change that isn't standard or emergency and requires full assessment.|
|Emergency|No|Yes|High-priority changes that resolve a major incident or apply a security patch.|

## Choosing a change type

Use the following scenarios as a guide:

-   A scheduled upgrade of a production database server that needs peer reviews and CAB authorization is a normal change.
-   Applying a documented, pre-approved patch from a tested standard change template is a standard change.
-   Deploying an out-of-band security patch to stop an active exploit is an emergency change.

**Parent Topic:**[Exploring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/exploring-change-management.md)

**Related topics**  


[Add a new change request type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/t_AddNewChangeType.md)

