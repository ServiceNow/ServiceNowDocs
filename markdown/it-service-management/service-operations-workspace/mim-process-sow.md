---
title: Major Incident Management process in Service Operations Workspace
description: A major incident has a high impact and urgency that affects a large number of users and deprives the business of one or more crucial services. Given the urgency of the situation, a well-coordinated response process is required to accelerate the resolution and minimize the business impact.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Major Incident Management in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Major Incident Management process in Service Operations Workspace

A major incident has a high impact and urgency that affects a large number of users and deprives the business of one or more crucial services. Given the urgency of the situation, a well-coordinated response process is required to accelerate the resolution and minimize the business impact.

When responding to major incidents, an effective and efficient system is needed to minimize the high impact of service interruption. An efficient system involves the following actions:

-   Minimize the impact of service interruptions.
-   Ensure that an appropriate incident manager, major incident team, or management group is in place to manage a major incident.
-   Communicate to the stakeholders about the service interruptions, degradations, resolutions, and other major incident updates.
-   Collaborate with stakeholders to resolve the major incident and restore service.
-   Create a problem record to analyze the root cause.
-   Generate a post incident report \(PIR\) to review each major incident once the service is restored.

The Major Incident Management process can be classified in the following phases.

-   **Major Incident identification and detection**

    The first phase in the process is to identify a potential major incident candidate. You can detect and identify major incidents in the following ways:

    -   An incident is detected based on the configured major incident trigger rules and is either proposed as a major incident candidate or promoted directly to a major incident automatically.
    -   An agent reviews the incident information to identify if the incident should be proposed to a major incident candidate. If proposed, a major incident manager reviews the information of the major incident candidate and promotes it to a major incident.
    -   A major incident manager creates a major incident directly without the proposal process.
-   **Communication and collaboration**

    The second phase is communication. Proper communication during a major incident is crucial to ensure that the IT teams, business stakeholders, and end users are informed about the impact and progress of the major incident.

    Communicating throughout a major incident requires a comprehensive communication plan, including whom to contact, the methods and frequency of communication, and messaging channels used to support, such as email and SMS. A communication plan enables the incident response team to focus their efforts on the resolution process and to set expectations for any future communications.

    You can define one or more communication plans based on the communication type, the priority of the incident, and the target audience of the major incident. Throughout the life cycle of the major incident, notifications and status updates are sent to the stakeholders to keep them informed and involved.

    Along with communications, effective collaboration with IT teams and other business stakeholders is also important when resolving a major incident. You can use communication channels, such as Microsoft Teams conference calls, to collaborate and work toward issue resolution. The Incident record page in Service Operations Workspace provides various controls for collaboration. For more information, see [Collaborate with stakeholders during a major incident](../task/collaborate-stakeholders-mim-sow.md).

-   **Resolution**

    The next phase in the major incident life cycle is resolving the major incident. Resolving a major incident also involves resolving all associated child incidents, and the individual callers receive a notification about incident resolution.

-   **Problem record creation**

    A problem record must be created to analyze the root cause of the major incident. You can configure the **Create problem from major incident** flow to create a problem record automatically after a major incident is resolved or manually create a problem record, as required. You can also configure if the major incident information is automatically copied to a problem record when a problem record is created.

-   **Post incident report review**

    The final phase of a major incident life cycle is generating a post incident report \(PIR\). After the major incident is resolved, a PIR is generated. You can use a PIR to analyze the incident and understand how to help prevent a similar incident in the future. This review also provides an opportunity to evaluate the incident response process and identify areas for improvement. The report contains the timeline of events that occurred after an incident is created. You can review and update the PIR during the review process before it’s shared with stakeholders.


**Parent Topic:**[Major Incident Management in Service Operations Workspace](mim-in-sow.md)

