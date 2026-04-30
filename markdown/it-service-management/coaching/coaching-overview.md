---
title: Coaching overview
description: After you enable Coaching, you can set up roles and groups, define coaching opportunities, create training material, and start assessing and coaching employees. The Coach and Trainee dashboards provide useful overviews to manage and measure results.
locale: en-US
release: yokohama
product: Coaching
classification: coaching
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Coaching, IT Service Management]
---

# Coaching overview

After you enable Coaching, you can set up roles and groups, define coaching opportunities, create training material, and start assessing and coaching employees. The Coach and Trainee dashboards provide useful overviews to manage and measure results.

**Note:** For detailed information on how to get started with Coaching, see [Coaching](coaching-landing.md) and the [Coaching demo](https://www.servicenow.com/community/itsm-blog/servicenow-coaching-module-demo/ba-p/2332545).

## Initial Coaching setup

Once you have enabled Coaching, set up the application by assigning user roles, configuring coaching opportunities and creating training content.

1.  Set up Coaching [roles](../reference/coaching-roles.md) and groups
2.  [Define trigger conditions for a coaching opportunity](../task/create-coaching-opportunity.md)
3.  [Identify learning content and a virtual coach](../task/identify-learning-content.md)
4.  Set up [surveys](setting-up-coaching.md)

## Workflow of Coaching roles

An employee with the Coaching trainee role is in need of coaching at a critical moment in a process.

An administrator with the Coaching admin role is in charge of setting up coaching opportunities, learning content, virtual coaches, and surveys used in the coaching process.

A manager, or coach, with the Coaching coach role is a subject matter expert of a process and is responsible for providing coaching to an employee, or trainee.

## Coaching dashboards

Use Coaching dashboards to manage and measure results in a simplified view.

-   [Coaching Dashboard](coaching-your-trainee.md)
-   [Trainee Dashboard](getting-coached.md)

## Identifying coaching opportunities

Coaching opportunities can be found in many tasks that occur throughout your environment.

-   Writing better work notes when service desk escalates incidents to a second level.
-   Correctly setting affected configuration items when the service desk works on incidents.
-   Using the correct naming convention for admin in update sets.
-   Coaching during the onboarding and the warranty period of a new application.
-   Correctly reassigning a case to another user with pertinent information in comments.
-   Engaging a user on closed records when non-positive feedback is received through surveys.
-   Spot-checking a user on quality control.
-   Helping to guide project managers in projects.
-   Improving knowledge article quality when knowledge articles are attached to resolved incidents.

## Common ITSM assessment triggers

You can define activities that occur when trainees work through an ITSM process, such as resolving an incident, as assessment triggers.

|Table|Assessment triggers|
|-----|-------------------|
|Incident|Moment of first response|
|Categorization and prioritization|
|Reassignment|
|Proposal of solution to the customer|
|Problem|Definition of the Problem statement|
|Writing the Known Error|
|Writing the Workaround|
|Root Cause analysis|
|Root Cause confirmation|
|How can this issue be avoided?|
|Change|Categorization and prioritization|
|Implementation description|
|Risk analysis|
|Impact analysis|
|Approval|
|Implementation|
|Post implementation review|

## Integration with other applications

Coaching opportunities, coaching assessments, and assigned training in Coaching are integrated with these applications.

-   [Continual Improvement Management](../../continual-improvement-management/concept/cim-landing-page.md)

    One example of a coaching opportunity with CIM would be to use improvement initiatives to set up external training tasks.

    **Note:** The Continual Improvement Management \(com.sn\_cim\) plugin must be active to create an improvement initiative. Continual Improvement Management requires a separate subscription and must be activated by ServiceNow personnel.

-   [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

    In a coaching assessment, you can assess trainee skills to identify gaps so the trainee can be coached to acquire new skills or to enhance their existing skill level.

-   [Knowledge management](https://www.servicenow.com/docs/access?context=create-knowledge-article&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

    You can assign knowledge articles as assigned training.


-   **[Domain separation and Coaching](domain-separation-coaching.md)**  
Domain separation is supported in Coaching. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Coaching](coaching-landing.md)

