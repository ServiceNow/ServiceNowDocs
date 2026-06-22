---
title: Change Advisory Board \(CAB\) workbench
description: The Change Advisory Board \(CAB\) workbench enables a CAB manager to schedule, plan, and manage CAB meetings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/change-management/cab-workbench.html
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Change Management, IT Service Management]
---

# Change Advisory Board \(CAB\) workbench

The Change Advisory Board \(CAB\) workbench enables a CAB manager to schedule, plan, and manage CAB meetings.

CAB meetings are typically intended to review and authorize change requests and review recently implemented changes. A standard agenda with the relevant change request details enables the CAB members to conduct risk and impact analysis prior to the CAB meeting.

Overview of the CAB workbench 

The CAB workbench assists you in managing CAB meetings in the following ways:

-   **Define a schedule for CAB meetings**

    Schedule a recurring series of CAB meetings for CAB members to assess the impact and risk of change requests prior to the meetings.

-   **Define CAB meeting attendees**

    Define members who attend this CAB meeting series for each occurrence. For example, define the CAB board members or any delegates who can substitute if the CAB manager cannot attend.

-   **Define CAB meeting agenda**

    Define filter criteria that determines which change requests are included in any occurrence of a CAB meeting. If a change request is included in an agenda, the change requester is notified of the CAB meeting in which the change request is discussed. The change requester can attend and present the reasons for the proposed change, and explain the intended outcomes and potential risks of the change.

-   **View change calendar**

    Schedule changes by displaying existing planned changes in a change calendar in daily, weekly, and monthly view. The calendar view also lists maintenance windows and blackout schedules, if any.

-   **Approve or reject a change request**

    Approve or reject a change request based on the decision taken in the CAB meeting.

-   **View and record meeting notes**

    Record meeting notes from a specific CAB meeting and share these notes with other meeting attendees.


The CAB Definition \(cab\_definition\) table inherits the domain properties from the Schedule \(cmn\_schedule\) table which has the Domain and Domain path columns. As the CAB Definition table makes use of the same Child Schedule and Schedule Entry tables as the Schedule table, domain support is identical, where the domain\_master attribute is used to derive Domain from a parent record. For more information, refer [Domain support for schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/time-configuration/domain-support-for-schedules.md) .

**Parent Topic:**[Exploring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/exploring-change-management.md)

