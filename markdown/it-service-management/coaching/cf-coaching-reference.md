---
title: Coaching reference
description: Coaching reference content includes business rules and field descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/coaching/cf-coaching-reference.html
release: zurich
product: Coaching
classification: coaching
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Coaching, IT Service Management]
---

# Coaching reference

Coaching reference content includes business rules and field descriptions.

## Coaching on a non-task table

To provide coaching on a table source that does not extend the Task table, you must create a business rule to initiate the coaching process.

The business rule **Evaluate coaching opportunity on tasks** initiates coaching for tables that extend Task. You can copy this business rule and modify it for tables that do not extend the Task table.

\[Omitted image "coaching-non-task-table.png"\] Alt text: CoachingNonTaskTable

## Coaching assessment flow states

\[Omitted image "coaching-assessment-flow.png"\] Alt text: CoachingAssessmentFlow

|State|Description|
|-----|-----------|
|Open|New coaching opportunity.|
|Work in Progress|Trainee is being coached.|
|Resolved|All learnings and coaching in the assessment have been completed successfully.|
|Closed Complete|Assessment has been resolved and closed.|
|Closed Incomplete|Assessment has been closed but was not completed, typically because the coaching assessment **Due date** has expired.|

## Form and list permissions

<table id="table_msy_s44_gfb"><thead><tr><th>

Element

</th><th>

Permissions

</th></tr></thead><tbody><tr><td>

Coaching Opportunity

</td><td>

-   sn\_coaching.admin: create, write, delete
-   sn\_coaching.coach: read
-   sn\_coaching.trainee: none

</td></tr><tr><td>

Coaching Assessment

</td><td>

-   sn\_coaching.admin: create, write, delete
-   sn\_coaching.coach: create, write own or group assessment
-   sn\_coaching.trainee: read own assessment, write own assessment work notes

</td></tr><tr><td>

Training History

</td><td>

-   sn\_coaching.admin: view
-   sn\_coaching.coach: view
-   sn\_coaching.trainee: none

</td></tr><tr><td>

Assigned Training

</td><td>

-   sn\_coaching.admin: create, write, delete
-   sn\_coaching.coach: create, write and delete own training action
-   sn\_coaching.trainee: view

</td></tr><tr><td>

Training

</td><td>

-   sn\_coaching.admin: create, write, delete
-   sn\_coaching.coach: create, write and delete own training
-   sn\_coaching.trainee: view

</td></tr><tr><td>

Virtual Coachings

</td><td>

-   sn\_coaching.admin: create, write, delete
-   sn\_coaching.coach: read, and associate existing virtual coach to a coaching opportunity
-   sn\_coaching.trainee: none

</td></tr><tr><td>

Virtual Coach

</td><td>

-   sn\_coaching.admin: create, write, delete
-   sn\_coaching.coach: create, write and delete own virtual coaching
-   sn\_coaching.trainee: none

</td></tr></tbody>
</table>## Coaching Properties

<table id="table_i5x_rr5_jpb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.sn\_coaching\_assessment\_activity.fields

</td><td>

Edit coaching assessment activities.-   **Type:** string
-   **Default value:** assigned\_to,cmdb\_ci,state,impact,priority,opened\_by,work\_notes,comments,\*Attachments\*,assessment\_of

</td></tr><tr><td>

sn\_coaching.recommended\_learning\_deprecated

</td><td>

Coaching Recommended Trainings is being deprecated and replaced with the Learning Tasks and course items from Coaching with Learning.-   **Type:** string
-   **Default value:** true

</td></tr><tr><td>

sn\_coach.lrn.exclude\_weekends\_on\_learning\_task\_due\_date

</td><td>

Enable property to exclude weekends while setting the due date for learning tasks.-   **Type:** true\|false
-   **Default value:** true

</td></tr><tr><td>

sn\_coach\_lrn.learning\_list\_menu\_props

</td><td>

Data array properties for the now-list-menu component on the Learning Tasks tab, coaching module.-   **Type:** string
-   **Default value:** script for data array

</td></tr></tbody>
</table>-   **[Coaching roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-coaching-roles.md)**  
Assign Coaching roles to specify what different users can see and do.
-   **[Coaching properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-coaching-properties.md)**  
Set the duration to read knowledge articles and whether to exclude weekends for trainees to complete training using Coaching properties.
-   **[Coaching field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-coaching-field-descriptions.md)**  
Coaching field descriptions also include form related lists and actions.
-   **[Integrating Coaching with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-coaching-integration.md)**  
Bring in data from other ServiceNow applications to enhance the training of your agents.
-   **[Resolve Coaching issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-coaching-troubleshooting.md)**  
Resolve common issues when setting up or running Coaching.
-   **[Domain separation and Coaching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-domain-separation-coaching.md)**  
Domain separation is supported in Coaching. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Quick start tests for Coaching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-quick-start-tests-coaching.md)**  
Validate that Coaching still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

**Parent Topic:**[IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/r_ITServiceManagement.md)

