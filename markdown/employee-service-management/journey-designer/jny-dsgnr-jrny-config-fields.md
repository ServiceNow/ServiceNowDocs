---
title: Journey designer Journey Configuration fields reference
description: A journey configuration requires several fields to be completed or selected.
locale: en-US
release: australia
product: Journey Designer
classification: journey-designer
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Journey designer Journey Configuration fields reference

A journey configuration requires several fields to be completed or selected.

## Journey Configuration page

Administrators configure journeys so that users have access to the features that are appropriate for their role. Each journey configuration is customizable to meet the needs within an organization.

<table id="table-jrny-primary-config-page"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Journey configuration name**

</td><td>

Provide a name for the Journey that helps managers identify the intended use case so they can customize the Journey with activity sets or stages.

</td></tr><tr><td>

**Type**

</td><td>

A Journey type is a category used to identify the intention of the journey, such as onboarding, leave of absence, or career growth.**Note:** This value is used for reporting and categorization. If using Journey Accelerator, keeping the **Plan type** and the **Journey type** consistent is helpful.

</td></tr><tr><td>

**Journey source**

</td><td>

-   **Lifecycle Events**: Use Lifecycle Events to facilitate cross-department tasks, such as approvals.
-   **Journey Accelerator**: Use Journey Accelerator modules to create templates for different audiences, such as a department-specific onboarding process.
-   **Lifecycle Events and Journey Accelerator**: The Journey will contain both a Lifecycle Event and Journey Accelerator plan.

</td></tr><tr><td>

**Lifecycle event type**

</td><td>

Select a lifecycle event for the Journey configuration. Lifecycle Events are created and managed from the **Manage Lifecycle Event** form. Go to **All** &gt; **Lifecycle Events** &gt; **Manage Lifecycle Event** to add or manage lifecycle events. See, [Lifecycle Events](../concept/hr-lifecycle-events-landing-page-1.md).

</td></tr><tr><td>

**Journey accelerator plan type**

</td><td>

Journey Accelerator plan types are configured by an administrator. Plan types include plans for transitions such as onboarding, offboarding, or promotions.

</td></tr><tr><td>

**Active**

</td><td>

Indicates whether the Journey configuration is available \(active\) for use in Journey designer.

</td></tr><tr><td>

**Update on manager change**

</td><td>

Option to enable a change in manager. Selecting this option will update the journey configuration and make it eligible for a manager change.

 The following fields of tasks are updated on reassignment:

-   HR Case: Subject person, Opened for
-   HR Task: Assigned to
-   Incident: Caller
-   JA Task: Assigned to
-   Approvals: Assigned to
-   Requests: Requested for

**Note:** For this functionality to work, ensure that you copy the flow **Manager Change - Journeys** and activate it. To activate a flow, see Activate a flow. Also note that email notifications are sent to the old manager, new manager, assigned agent, and the user updating the manager in `sys_user`.

</td></tr><tr><td>

**Journey mobile image**

</td><td>

The image that appears at the top of the Journey when viewed in the mobile app. See, [Journeys on Now Mobile](../concept/journeys-mobile-now.md).

</td></tr><tr><td>

**Can be used as a template**

</td><td>

Indicates whether the Journey configuration can be triggered from the **Create journey** widget.

</td></tr></tbody>
</table>## Journey title details tab

Titles help journey owners identify which journey is the best for their needs.

|Field|Description|
|-----|-----------|
|**Use custom title**|Selecting **Use custom title** so that you can create a unique title for a Journey.|
|**Title**|The name of the journey configuration that is visible to other users such as, journey owners, employees, and mentors.|
|**Description**|The description of a journey is visible to the journey owner. Descriptions help journey owners select which journey configuration is appropriate for their needs.|
|**Title icon**|Administrators can add icons to journey headers.|

## Journey owner permissions tab

Owner permissions control which features are available for the owner of a journey to use. Some permissions are directly related to which features are available in your implementation of Journey designer.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Can add mentors**

</td><td>

Enables journey owners to add mentors to a journey. Mentors can have tasks assigned to them.

</td></tr><tr><td>

**Can edit journey**

</td><td>

Enables journey owners to edit and add Journey Accelerator tasks and stages in a journey.**Note:** Journey owners and mentors can't modify stages, cases, or tasks coming from the **Lifecycle Event**.

</td></tr><tr><td>

**Can view satisfaction score**

</td><td>

Enables journey owners to see the pulse survey results tied to this journey.**Note:** This feature requires integration with Listening Posts. See, .

</td></tr><tr><td>

**Can add recommended learning**

</td><td>

Enables journey owners to add courses that are related to training or learning. This permission depends on your organization’s implantation of Journey designer app and features.**Note:** This feature requires integration with Learning Posts. See, .

</td></tr><tr><td>

**Can add quick links**

</td><td>

Enables journey owners to add quick links to a journey. The quick links module in the Employee Center enables access to internal and external resources, such as knowledge bases, catalog items, pages, and links.

</td></tr><tr><td>

**Can add personalized message**

</td><td>

Enables journey owners and mentors to send personalized messages to employees.

 When enabled, you can also select an email template to include for the journey configuration. The selected email template is available for the journey owner or mentor to send or modify before sending.

 When this permission is enabled, the **Send a note** button is visible in the published journey.

</td></tr></tbody>
</table>## Mentor permissions tab

Mentor permissions determine how much control that a mentor has in the journey process. A mentor is a person who helps employees complete journeys.

|Field|Description|
|-----|-----------|
|**Can add other mentors**|Enables mentors to add other mentors to a journey. An extra mentor could have unique skills that would be helpful for an employee. Mentors can have tasks assigned to them.|
|**Can edit journey**|Enables mentors to edit everything in a journey.|

**Parent Topic:**[Journey designer reference](jny-dsnr-reference.md)

