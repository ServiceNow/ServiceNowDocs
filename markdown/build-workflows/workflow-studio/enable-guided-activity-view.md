---
title: Enable Guided activity view
description: Guide end users through a playbook, step-by-step.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customize the Playbook Experience, Designing playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Enable Guided activity view

Guide end users through a playbook, step-by-step.

## Before you begin

-   Role required: admin or playbook.admin
-   Familiarize yourself with how to begin customizing the playbook experience in UI Builder. To learn more, see [Customize the Playbook Experience](../../workspace/concept/playbook-customize-playbook.md).

## About this task

Guide end users through a playbook, one activity at a time. If you have a lot of end users encountering issues in a particular area, and you want to walk them through a series of questions that lead to a particular Instruction activity to complete work \(or even KB activity for final instruction\), consider using the **Guided** activity view. There are out-of-the-box playbooks that use the **Guided** activity view for employee self-service requests, such as time off or benefit requests, available through the [Employee Center](https://www.servicenow.com/docs/access?context=employee-center-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

**Note:**

The following configurations and features are not supported for the **Guided** activity view:

-   Parallel activities
-   Optional activities
-   The **Pending Item Visibility** configuration in the **Guided Self-Service Experience** playbook experience record in the **Playbook Experiences** list \[sys\_playbook\_experience.list\]

    **Note:** This property is not relevant since there are no pending activities other than the current activity that an end user is in during a **Guided** self-service playbook run.

-   Stage picker components, including filters

## Procedure

1.  Navigate to **All** &gt; **UI Builder**, and open the **Guided Self-Service in Employee Center** experience.

    ![Guided Self-Service Employee Center experience in UI Builder](../images/pe-UIB-guided-self-service.png)

2.  Open the page that you want to enable the Guided activity view for.

    ![Opening the Default page for the Guided Self-Service EC experience in UI Builder](../images/pe-guided-ssec-page.png)

3.  Under **Body** in the component tree, open **Playbook Activity Viewer**.

    ![Opening the Playbook Activity Viewer component in the component tree](../images/pe-activity-viewer-component.png)

    The **Playbook Activity Viewer** panel opens on the right.

4.  In the **Playbook Activity Viewer** panel, under the **Configure** tab, open the **Activity View** drop-down and select **Guided**.

    ![Selecting the Guided activity view](../images/pe-activity-viewer-panel-guided-view.png)


## Result

For an end user who is running a playbook, the result is a playbook that runs one activity at a time. If configured, users can still restart the playbook and activities.

![End user experience of a Guided view, Self-Service playbook](../images/PE-Guided-Activity-Viewer.gif)

**Parent Topic:**[Customize the Playbook Experience](../../workspace/concept/playbook-customize-playbook.md)

