---
title: Trigger condition example
description: You can send out auto-triggered surveys when an incident is closed or resolved.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Survey trigger conditions, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Trigger condition example

You can send out auto-triggered surveys when an incident is closed or resolved.

A trigger condition is configured as follows:

-   **Assessment**: Service Desk Satisfaction Survey
-   **Table**: Incident \[incident\]
-   **User field**: Caller
-   **Repeat interval**: 30 days
-   **Active**: true
-   **Trigger randomly**: false
-   **Related Field 1**: Assigned to
-   **Related Field 2**: Problem
-   **Condition**: \[State\] \[is\] \[Closed\] \[or\] \[State\] \[is\] \[Resolved\]

C is the caller on incident INC00004305 that is assigned to B, a service desk technician. B creates PRB010101 based on C's complaint and closes the incident. The system creates a survey instance assigned to C so C can rate satisfaction with the incident experience.

Because two related fields were selected as part of the trigger condition, the survey instance stores the following information from the incident:

-   User \(Related Field 1\): **Boris Catino**
-   Problem \(Related Field 2\): **PRB010101**
-   Task \(automatically created\): **INC00004305**

Because the task field is automatically populated, UI-based filtering by dot-walking on incidents \(or any task-based table\) is supported when creating a report on survey results. For example, you can query all survey instances related to incidents assigned to a group \(survey reports on all incidents assigned to `networking` group, for instance\).

Even though the trigger condition is set to be triggered each time that the conditions are met, the **Repeat interval** setting ensures that C does not receive another survey for another of its incidents closes within 30 days of the first incident.

## Survey report example based on task field

One of the most common use cases for Surveys is to send out an auto-triggered survey when an incident, request, or task is closed. Once you get the survey results back, you can filter the results by users and groups related to the ticket, such as Assignment Group, or Assignee.

Filtering the survey results provides more detail on how people and teams are performing based on ticket data. Since this information is automatically captured, you can dot-walk while filtering the data \(instead of utilizing a related field on the Survey trigger condition form, as previously required\).

![Using the Task as a filter for survey results](../image/SurveyReport.png "Using the Task as a filter for survey results")

To create a report on incident-triggered survey responses by Assignment group, set up the report on the Task Assessment Details by navigating to **Reports** **View/Run** and clicking **Create a report**.

![Defining a report on survey responses that are triggered by an incident](../image/SurveyReportCreate.png "Defining a report on survey responses that are triggered by an incident")

**Parent Topic:**[Survey trigger conditions](../concept/c_TriggerConditions.md)

