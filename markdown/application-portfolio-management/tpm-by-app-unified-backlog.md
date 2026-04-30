---
title: Application Backlog view - Legacy
description: As an enterprise architect this view helps you to understand the epics, stories, and enhancements, which are the units of work in scrum, that impact your business application.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Multiple views in TPM - Legacy, Technology risks in timeline - Legacy, Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Application Backlog view - Legacy

As an enterprise architect this view helps you to understand the epics, stories, and enhancements, which are the units of work in scrum, that impact your business application.

**Note:** Activate Agile Development 2.0 \(com.snc.sdlc.agile.2.0\) plugin to get the Application Backlog view in the TPM timeline.

Application Backlog view helps you to look into the centralized backlog of records that are of different task types such as epics, stories, and enhancements. This view facilitates prioritizing and sequencing of different task type records in one location, saving you from sorting and filtering them in many steps. In this view, you can:

-   View all applications \(first column\) that are at a high risk by default, however you can filter based on the intensity of their risk in the second column.
-   Filter the application records by any attribute in the business application table. Switch to either quarterly or monthly view of the timeline \(third column\).
-   Create a project or demand to add to the application.
-   Paginate the number of applications to be displayed in a single view.
-   Expand the business application to view its unified backlog of epics, stories, enhancements, projects, and demands attached to the application. You can also see the total number of these entities within brackets.

You can view the following application backlog entities on the timeline in addition to the projects and demands attached to the application:

-   **Epics**

    The high-level business goal of the application is broken down into one or more epics. Epics organize the work required to complete parts of the application goal in small pieces. Epics are further broken down to stories, which are fundamental units of work, that describe the business requirement briefly and can be completed within a sprint. The timeline for the epics is displayed based on the planned start date and planned end date of the epic. The status of epics must not be in **Complete** or **Canceled** state.

-   **Stories**

    Stories usually are part of an epic. The stories contained in the epic attached to the business application that are not in **Complete** or **Canceled** state are displayed in the timeline. The timeline starts with the planned start date and ends with the planned end date of the sprint to which the story is tagged.

-   **Others**

    There can be stories that are not attached to an epic but directly associated to the business application itself. Such stories are listed within the epics as **Others** and displayed in the timeline.

-   **Enhancements**

    Enhancements are special requests that come from users with non-scrum role. A scrum product owner reviews these requests and creates one or more user stories. Enhancements in **Closed Complete**, **On Hold**, and **Canceled** state are not displayed in the timeline. The enhancement timeline runs from the Planned start date to its end date when the sprint work is scheduled to begin and end.

-   **Projects**

    If the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin is activated, then you can add a project to the business application.

-   **Demands**

    If the PPM Standard plugin is not activated, then by default, a demand is created.

    **Note:** For the timeline to display the epics, stories, and enhancements, each of these records should reference the business application attached to it. See [Associate epic to business application](../task/reference-epic-business-app-unified-backlog-view.md) for more information.


-   **Application column**

    All the epics, stories, enhancements, projects, and demands listed in the application column are clickable. Clicking each of them opens the record in a new tab that the clickable field points to.

-   **Risk column**

    Shows the risks of the business applications only and not the risks of epics, stories, enhancements, projects, or demands.

-   **Timeline column**

    The start and end dates of the units of work attached to the business application are plotted as a continuous line. However, if only one date is present, either the start or end date, then just that date is plotted as a filled circle.


-   **[Associate epic to business application for Application Backlog view - Legacy](../task/reference-epic-business-app-unified-backlog-view.md)**  
An epic must reference the business application for it to be displayed in the Application Backlog view of the timeline.

**Parent Topic:**[Multiple views in TPM - Legacy](tpm-timeline-views.md)

