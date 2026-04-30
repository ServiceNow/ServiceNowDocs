---
title: Integrated experience and service feedback
description: Experience and service feedback enables you to gather quick feedback from your users on their user experiences and their service experiences.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setup continuous improvement features, Configure, Employee Center, Employee Service Management]
---

# Integrated experience and service feedback

Experience and service feedback enables you to gather quick feedback from your users on their user experiences and their service experiences.

Configure the experience and service feedback across the Employee Center portal to gain insights into your user sentiments, as an admin.

View all the responses captured neatly in the Feedback Analytics dashboard.

The two feedback types are:

-   Experience feedback: Provide your feedback on the user experience in the portal, the mobile, Kiosk, or through the Virtual Agent.
-   Service feedback: Provide your feedback on the service experience like raising a Service Catalog item request.

Both the feedback types can be either static questions or survey questionnaires.

**Note:**

-   Configure the experience feedback drawer widget in your portal, if it has the Employee Center header.
-   Configure the experience feedback drawer widget to provide feedback in various formats like, experience, numeric value feedback, or star rating feedback. For more information on configuring feedback definition, see [Set up the feedback definition](../task/config-feedback-dfnition.md).
-   Avail the star rating and the numeric value rating in Experience feedback predefined with Employee Center version 35.0.
-   For a description of the field values in the feedback definition form, see [Feedback definition form](../reference/fdbck-dfnition-record.md).

Provide feedback through the drawer widget, In page in the portal or via email.

The following widgets are customizable. For more information on how to customize the widgets, see [Integrated service and experience feedback management](ex-fdbck-manage.md).

<table id="table_tld_ssy_21c"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

experience-flow-feedback

</td><td>

Widget

</td><td>

Supports in-page feedback on the portal.

</td></tr><tr><td>

experience-workflow-feedback

</td><td>

Widget

</td><td>

Supports workflow-based feedback on the portal.

</td></tr></tbody>
</table>## Post-feedback loop

Post-feedback loop allows tasks to be created when the feedback rating is beneath or equal to the rating threshold. The feedback tasks are visible in **My tasks**.

**Note:** The sn\_hr\_sp.esc\_admin has read and write access to the feedback task table Employee Center Pro version 37 onwards. Additionally, the following fields in the feedback task form are read-only, version 37 onwards:

-   **Feedback definition**
-   **Assessment response**
-   **Feedback provided by**

View the **Details** tab to get the feedback task assessment. For Survey feedback tasks, view the responses and assessment details.

Feedback tasks can be anonymous if the feedback provider doesn’t share their personal information while submitting the feedback. Notify the feedback provider via email when the task is resolved if they have shared their personal details. For more information, see

-   [Resolve a feedback task](../task/resolve-feedback-task.md)
-   [Feedback task notification](fdbck-task-notification.md)

## Experience feedback for browser extension

Get an experience feedback configuration and a feedback definition when you install Browser Extension for Employee Center plugin \(sn\_ex\_brw\_ext\) version 1.0 along with Employee Center Pro plugin \(sn\_ex\_sp\_pro\) version 36.0.

**Note:** **Experience Feedback for Browser Extension** definition has certain differentiators from the generic experience feedback options. For more information, see [Set up the feedback definition](../task/config-feedback-dfnition.md).

You can view the feedback analytics from the browser extension by selecting the **Employee Center Browser Extension** in the **Portals Filter**.

