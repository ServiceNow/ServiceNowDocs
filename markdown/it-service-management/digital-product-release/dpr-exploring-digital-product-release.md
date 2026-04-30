---
title: Exploring Digital Product Release
description: The ServiceNow Digital Product Release application enables you to streamline the process of delivering digital products and services by managing the process from planning to delivery.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2025-04-25"
reading_time_minutes: 7
breadcrumb: [Digital Product Release, IT Service Management]
---

# Exploring Digital Product Release

The ServiceNow® Digital Product Release application enables you to streamline the process of delivering digital products and services by managing the process from planning to delivery.

## Digital Product Release overview

Digital Product Release \(DPR\) is a release management solution that helps release managers, product managers, and program managers manage the release process. They can track the progress of releases while ensuring that the releases adhere to the company's policies.

This solution automates processes that enable collaboration between stakeholders, so everyone can track release status, from start to finish.

## Digital Product Release workflow

A digital product or service has a release life cycle that starts with planning, goes through development, and ends with delivery. There are many different phases to a release life cycle, and each phase can have its own set of activities. The following infographic illustrates the life cycle of digital products and services.

![Infographic showing the release life-cycle for digital products and services. For details, refer to the following description.](../image/dpr-release-workflow.png "Release life cycle for digital products and services")

1.  Create a product or service and add features, product enhancements,and releases.
2.  Plan the scope of a release by moving product enhancements into releases.
3.  Initiate a release and set its release readiness target date.
4.  Execute the release by tracking its progress and completing phases and tasks within each phase.
5.  Validate the release phase against mapped policies to ensure that the release adheres to organizational standards.
6.  Get the product or service ready by the specified target date to make it available for deployment.

## Personas

Digital Product Release is aimed at the following personas:

<table id="table_knl_gfb_myb"><tbody><tr><td>

Release manager

</td><td>

-   Manages a release calendar
-   Establishes a release process, including policy gates

</td></tr><tr><td>

Release coordinator or Program manager

</td><td>

-   Communicates dependencies across a release
-   Approves the scope of a release
-   Provides status updates to the release team

</td></tr><tr><td>

Product manager

</td><td>

-   Releases new products, services, enhancements,and features
-   Communicates updates to the development status
-   Plans the scope of a release
-   Initiates a release

</td></tr><tr><td>

Engineering lead

</td><td>

-   Ensures development of new products, services, enhancements,and features
-   Connects development scope to a release

</td></tr></tbody>
</table>## Digital Product Release benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Define release readiness targets for single or recurring release schedules.|[Release readiness target](../task/dpr-create-rls-readiness-target.md)|Release manager|
|Define release templates that include phases, tasks, policies, and approval tasks.|[Release templates](../task/dpr-create-release-template.md)|Release manager|
|Create policies to automate the release process.|[Policy administration](../reference/dpr-policies.md)|Release manager|
|Manage products, services,features, product enhancements,versions, and initiate a release.|[Release planning](../task/dpr-plan-feature-version.md)|Product manager|
|Plan and manage the release process from start to finish.|[Release execution](../task/dpr-work-release.md#)|Release manager|

## Digital Product Release key terms

-   **Approval definition**

    An approval definition is a set of rules that specify how tasks will be approved from a set of stakeholders for a release. For example, the QA team might approve code quality or the Security team might approve on the security aspects. An approval for a task can be requested from an individual user or a user group.

-   **Included products**

    Included products help you organize and manage related digital products and services. By creating a product hierarchy using Included products, you can understand the relationships between different products and services and make informed decisions about product management.

-   **Release bundle**

    A release bundle helps you to group multiple releases to track and manage them concurrently from a single place. They also help you to identify dependencies and potential conflicts, and make any necessary adjustments to ensure a smooth and coordinated release process.

-   **Release execution**

    Release execution is a continuous process to track and monitor the progress of a release. It helps you ensure that all products in the release are ready by the release readiness target date.

-   **Release calendar**

    A release calendar helps you group multiple release readiness targets. It can also contain blackout, maintenance, and other user-defined schedules to avoid overlap of release targets on those dates.

-   **Release readiness target**

    A release readiness target is when a release is ready to be released. It helps release managers to determine the dates at which the products and services should be ready for deployment by the team.

    **Note:** Release readiness target and Release target are used interchangeably in the documentation and application. Both terms refer to the same concept - release readiness target date.

-   **Release template**

    A release template is like a blueprint for a release process, which includes a predefined set of phases, tasks, policies, and approval tasks.

    Release teams can use these release templates to create a release. All phases, tasks, approvals, and phase gates from the template will be automatically applied to the newly created release. It helps the release teams avoid redundant activities and focus on tracking and performing all the necessary tasks to complete the release on schedule.

-   **Stage-oriented release**

    A release that follows a stage-oriented process. This process doesn't have phases with predefined end dates. It is suitable for teams that work toward completing product enhancements and objectives. Teams can move to the next phase after they have completed tasks and met policy compliance for the current phase. Teams have the flexibility to restart any completed phase if they encounter an issue that requires them to go back.

-   **Timeline-oriented release**

    A release that follows a timeline-oriented process. This process has defined end dates for each phase of the release. It is suitable for teams that work toward the planned deadlines and have phases with a specific duration.

-   **Release planning**

    Release planning is an activity to plan a product or service's enhancements into releases to define the scope of work for each release.

    The release must be associated with a release readiness target date, which determines the start and end dates for phases and tasks based on the target date.


-   **[Digital Product Release Workspace](dpr-workspace.md)**  
The Digital Product Release Workspace provides a single location for release admins to define release processes and release readiness targets. Product managers can use it to create and manage products and features, define the scope in versions, and plan and execute releases.
-   **[Release for a product or service](dpr-product-release.md)**  
A release groups all the tasks \(projects, epics, stories, enhancements, defects, problems, incidents, and so on\) planned for a specific version of a product or service. Digital Product Release provides two different processes: timeline-oriented and stage-oriented, to help you in executing your releases.
-   **[Holiday schedules in a release](dpr-release-holiday-schedule.md)**  
You can associate a holiday schedule with a release so that the phase and release durations are calculated considering non-working days.
-   **[Digital Product Release dashboards](dpr-dashboard-release.md)**  
Release dashboards provide insights into your releases. You can see their progress, identify any potential risks, and track their software quality. This information can help you to make informed decisions about your releases and ensure their success.

**Parent Topic:**[Digital Product Release](../reference/dpr-landing-page.md)

