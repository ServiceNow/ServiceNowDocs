---
title: Integrating Listening Posts with Journey designer
description: Use Listening Posts with Journey designer to embed pulse surveys to get insight into employees' experiences and share those insights with managers.
locale: en-US
release: xanadu
product: Listening Posts
classification: listening-posts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Listening Posts integrations, Listening Posts, HR Service Delivery, Employee Service Management]
---

# Integrating Listening Posts with Journey designer

Use Listening Posts with Journey designer to embed pulse surveys to get insight into employees' experiences and share those insights with managers.

## Configure a pulse survey widget in the Journeys page

Add the widget to the Journeys page to prompt employees for feedback. You can configure the widget in either Journey Accelerator or

Lifecycle Events. The steps for both options are provided below:

## Configure in Lifecycle Events

-   **Step 1: Create a pulse theme**

    Follow the steps to [Create a pulse theme in Listening Posts](../task/create-pulse-theme.md)

    **Note:** You can create a separate pulse theme for each journey type.

-   **Step 2: Create pulse survey**

    Follow the steps to [Create a pulse survey in Listening Posts](../task/create-pulse-survey.md)

-   **Step 3: Trigger pulse survey from Lifecycle Events**

    Open an existing Lifecycle Event and create an activity record with the **Pulse Survey** Activity Type. Select the pulse survey that you created in step 2 and assign the **Pulse user field** to the person you want to take the survey.

    [Configure a lifecycle event activity](../task/configure-hr-lifecycle-event-activity.md#)\|[Configure a pulse survey event activity](../task/configure-hr-lifecycle-event-activity.md#)

-   **Step 4: Add analytics to the Journey page**

    Customize with the following options:

    -   Select **Can view satisfaction score** from the Journey owner permissions tab. See [Update users' permissions for journeys](../task/jny-dsgnr-update-user-permissions.md)
    -   Configure actions, such as a URL or link to schedule a meeting, to appear with specific score results in the Satisfaction Score Actions tab. See [Create a satisfaction score action](../task/jny-create-satisfaction-score-action.md)
    -   Share pulse survey results with the manager. See [Create a response sharing rule in Listening Posts](../task/create-response-rule.md)

## Configure in Journey Accelerator

-   **Step 1: Create a pulse theme**

    Follow the steps to [Create a pulse theme in Listening Posts](../task/create-pulse-theme.md)

    **Note:** You can create a separate pulse theme for each journey type.

-   **Step 2: Create pulse survey**

    Follow the steps to [Create a pulse survey in Listening Posts](../task/create-pulse-survey.md)

-   **Step 3: Add to a plan configuration**

    Add the task template containing the pulse survey to a plan configuration via a stage configuration. [Add stage configurations](../task/jny-create-stage-configuration.md)

-   **Step 4: Trigger pulse survey from Journey Accelerator**

    Create a task template with a **Task type** of `Pulse Survey`. In the **Related record** field, select the pulse survey you created in step 2.

    [Create and manage action plan task templates](../task/jny-create-manage-task-templates.md)

-   **Step 5: Add analytics to the Journey page**

    Customize with the following options:

    -   Select **Can view satisfaction score** from the Journey owner permissions tab. See [Update users' permissions for journeys](../task/jny-dsgnr-update-user-permissions.md)
    -   Configure actions, such as a URL or link to schedule a meeting, to appear with specific score results in the Satisfaction Score Actions tab. See [Create a satisfaction score action](../task/jny-create-satisfaction-score-action.md)
    -   Share pulse survey results with the manager. See [Create a response sharing rule in Listening Posts](../task/create-response-rule.md)

**Parent Topic:**[Listening Posts integrations](listening-posts-integrations.md)

**Related topics**  


[Integrating Listening Posts integration with Virtual Agent](integrate-with-va-lp.md)

[Integrating Listening Posts with User Experience Analytics](lp-apps.md)

