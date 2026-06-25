---
title: Tracking interview health
description: Recruiters and coordinators need to proactively monitor interview health, look at interviews that need attention, and reduce reactive coordination effort. The Interview health tracker gives recruiters and coordinators a unified list view to centrally monitor interview health and surface support needs early and in priority order, so they can address them proactively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/interview-management/tracking-interview-health.html
release: australia
product: Interview Management
classification: interview-management
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 3
keywords: [needs-attention alerts, alert triage, recruiter workspace, interview alerts, availability request alerts]
breadcrumb: [Use, Interview Management, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Tracking interview health

Recruiters and coordinators need to proactively monitor interview health, look at interviews that need attention, and reduce reactive coordination effort. The Interview health tracker gives recruiters and coordinators a unified list view to centrally monitor interview health and surface support needs early and in priority order, so they can address them proactively.

The system generates alerts automatically based on built-in scenarios and displays them in the Recruitment workspace and on the affected records.

**Note:** This feature requires Now Assist skills from the HR Talent AI Agent Collection application, available in HR Service Delivery version 2.0.0 and later.

## Benefits

Needs-attention alerts provide the following benefits:

-   -   **Configurable to your business processes:**

    Configure alerts to create the necessary tracking mechanism that meet your business requirements. For details on configuring alerts, see [Configuring interview health tracker alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/interview-management/configure-needs-attention-framework.md).

-   -   **Central tracking that drives timely action:**

    Recruiters and recruitment coordinators monitor all their interviews and availability requests from one place, so they can act before issues escalate.

    -   Identify records that need follow-up without manually reviewing them.
    -   Statuses update automatically as records change, and recruiters can also manually close alerts that are no longer relevant with a categorized reason or snooze them for later review.
    -   Stay on top of hiring activity through a daily digest and notifications for urgent items, with detailed, in-context alerts available on each affected record.

## Alert lifecycle

An alert moves through the following states:

1.  A scheduled job runs on a defined interval to scan the interview records.
2.  The system detects a record that matches a built-in scenario and creates an alert.
3.  The recruiter reviews the alert from the list view or from the interview record.
4.  Alert statuses update automatically as the underlying records change. The recruiter can also update an alert, once the issue is resolved, by closing it with a categorized reason, or snooze it to review later. When closed, the resolution details are saved in the activity log of the interview record.

After an alert is generated for a record, the system does not re-evaluate that record until a configured cool-down period has elapsed. An admin can update the **sn\_ta\_int\_mgmt.naf\_record\_evaluation\_cooldown\_time** property to set the cool-down duration.

During a scheduled job run, if the system identifies that an alert flagged earlier has been resolved, it automatically closes the alert by providing appropriate reason and saves the activity log as well.

## Default scenarios

The following are the default scenarios available that trigger the alerts:

-   A scheduled interview has been declined by the interviewer or applicant and is due to take place soon.
-   An upcoming scheduled interview is still awaiting a response from the attendees.
-   The request to reschedule an upcoming scheduled interview has not yet been addressed.
-   Interview feedback is overdue.

## Where alerts appear

Recruiters can view the needs-attention alerts in the following areas:

-   **List view**: The Needs attention list view in Recruitment workspace displays a consolidated list of all open alerts and their details. With everything in one place, recruiters can plan their work more effectively and address higher-priority items first.
-   **Interview record**: Alert messages and an AI-generated interview alert summary appear on the interview record page. A detailed view of each alert is available under the **Alerts** tab, where users may also choose to close or snooze individual alerts.

**Parent Topic:**[Using Interview Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/interview-management/using-interview-mgmnt.md)

