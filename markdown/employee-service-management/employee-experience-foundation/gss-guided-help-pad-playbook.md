---
title: Build a visual flow for Guided Self-Service
description: Create a visual playbook flow of activities so that employees can find information in a more intuitive and visual way.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Guided Self-Service in Employee Center, Setup browse experience features, Configure, Employee Center, Employee Service Management]
---

# Build a visual flow for Guided Self-Service

Create a visual playbook flow of activities so that employees can find information in a more intuitive and visual way.

## Before you begin

Understand the basics of playbooks and workflow studio [Building playbooks](https://www.servicenow.com/docs/access?context=building-a-process&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) and [Create an activity definition](https://www.servicenow.com/docs/access?context=create-activity-definition&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

Review the information from [Guided Self-Service reference](../reference/gss-guided-self-service-reference-info.md).

Role required: sn\_hr\_sp.esc\_admin, playbook.write

## Procedure

1.  On the Workflow Studio, use the existing questionnaire activity available from **Add activity** &gt; **Common Activities** &gt; **Questionnaire** for authoring the question and answer flow.

    Here’s a sample illustration of the entire flow.

    ![process design flow](../images/gss-playbook-design-flow.png "Visual flow")

    Each activity definition contains some basic configuration details, automation plan, and activity experience.

    **Note:** Ensure you mark the guided process and playbook active. Only when you activate the GSS process, the **Add** button is displayed on the Assigned Topics.

2.  On the Workflow Studio, use the new GSS-specific activities.

    -   **Add activity** &gt; **Guided Self-Service in Employee Center** &gt; **Catalog Item Guidance**.
    -   **Add activity** &gt; **Guided Self-Service in Employee Center** &gt; **Show Knowledge Article Guidance** &gt; **Instruction activity'**.
    -   **Add activity** &gt; **Common Activities** &gt; **Instruction Activity**.
    ![Add activity for GSS](../images/gss-add-activity-ec-interactive.png "Add activity")

    For more information, see the activity information such as Input, Output, and Advanced Properties on the UI.

3.  On the Workflow Studio, use the pre-configured triggers, flows, decisions, and so on.

    Here’s a sample illustration for time off flow.

    ![Workflow Studio PAD design](../images/gss-pad-trigger-flow-confi.png "Step-by-step playbook flow")

    **Note:** Ensure you configure the Restart rule as always for all or each activity in the flow. Do not use the restart operation with just one activity.

    Based on the security access and user permissions, the catalog item and KB appear. For more information, see [Create a playbook](https://www.servicenow.com/docs/access?context=create-process-definition&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

    **Note:** The Activity Definition \[sys\_pd\_activity\_definition\] table lists the definitions for the activities that you can add to a playbook in **Workflow Studio**.

4.  In the **Playbook activity view**, select one of the following options to determine how the stages and activities are displayed in the playbook.

    -   **Focused:** Displays the stages and activities in the playbook life cycle panel and the current activity in the playbook work area.
    -   **Stacked:** Displays the stages in the playbook life cycle panel and cards for each of the activities in the current stage in the playbook work area.
    -   **Guided:** Displays an interactive, step-by-step interface that guides users through the playbook stages and activities, providing contextual assistance and decision support at each step.
5.  Go to **Playbook** &gt; **...** &gt; **Properties** &gt; **Additional properties**, and select **Allow this playbook to be restarted during runtime** options on the pop-up window to enable restart function.

    ![additional property selection](../images/gss-additional-properties.png "Select additional property")

6.  Click **Activate** to reflect all the updates to the GSS or playbook.

    **Note:** Only when you activate the GSS process, the **Add** button is displayed on the **Assigned Topics**.


## Result

GSS is configured to guide employees.

-   By default, a fresh start and context is provided for selection when employees return to a partially completed GSS flow.
-   The incomplete selections are canceled daily by a schedule job.
-   Admins can add rich media such as images, videos, links, and formatted text to provide detailed answers or guidance as the QnA result.
-   Based on the user permissions, you can access a catalog or a KB article.

    **Note:** When a user or user group doesn't have permission to a catalog or a KB article, the `You do not have access to this item.` message appears. You can contact the admin for permissions.


For more information, see [Use Guided Self-Service](../concept/gss-guided-self-service-homepage.md).

