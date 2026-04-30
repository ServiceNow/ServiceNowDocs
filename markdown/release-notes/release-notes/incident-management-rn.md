---
title: Incident Management release notes
description: The ServiceNow Incident Management application facilitates you to restore normal service operations while minimizing the impact to business operations and maintaining quality. Incident Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Incident Management release notes

The ServiceNow® Incident Management application facilitates you to restore normal service operations while minimizing the impact to business operations and maintaining quality. Incident Management was enhanced and updated in the Zurich release.

## Incident Management highlights for the Zurich release

-   Help prevent changes to closed incident tasks to promote data integrity and to maintain a clear audit.
-   Manage and resolve incidents effectively with the incident and problem workflow enhancements.
-   Coral is the new default theme for Next Experience and Core UI, offering a more user-friendly experience.

See [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Incident task record behavior changes](https://www.servicenow.com/docs/access?context=create-incident-task&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    When an incident task is closed, you can no longer edit the field values in the incident task form. Disabling the fields helps prevent any further updates or modifications to closed incident tasks, reducing audit risks.

-   **[Incident and problem workflow changes](https://www.servicenow.com/docs/access?context=working-incident-record-form&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    When a problem record is linked to an incident or multiple incidents, the incident and problem workflow has the following enhancements:

    -   When a fix or workaround is shared from the problem record, an event is added in the activity stream of the incident record as work notes. The event includes a brief description of the provided fix or workaround and a link to the problem record.
    -   When a Known Error \(KE\) article is linked to the problem record, an event is added in the activity stream of the incident record as work notes. The event includes the links to the problem record and the KE article.

## Activation information

Incident Management is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

