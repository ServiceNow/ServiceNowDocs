---
title: Customize the Playbook Experience
description: Customize the layout of your Playbook Experience with base system modular components, templates, and more via integrated UI Builder functionality.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Designing playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Customize the Playbook Experience

Customize the layout of your Playbook Experience with base system modular components, templates, and more via integrated UI Builder functionality.

Build custom experiences for your agents and fulfillers with the modular components in the Playbook Experience apps. To speed up the development process, add the Custom Layout UI Controller to pages where you want presets to auto-populate inputs for the provided components.

**Note:** You can also create your own custom components with UI Builder, but presets cannot auto-populate custom components with data.

## Components

Determine how to display these modular components in your Playbook Experience:

-   **Playbook stage picker**

    The stages of a playbook can be displayed horizontally or vertically:

    -   The vertical orientation shows:

        -   All playbooks for a parent record,
        -   The stages of each playbook,
        -   How many activities remain to be completed in each stage, and
        -   How many activities are in progress for each stage.
        In this example, a playbook named **Playbook Experience Demo** with stages named **Assign**, **Create**, **Review and Update** is shown. The **Assign** stage has 2 activities left to complete, with 1 in progress. The **Create** and **Review and Update** stages don't have blue numbers next to them, so they don't have any activities that are in progress.

        ![Vertical view of a playbook named Playbook Experience Demo with stages named Assign, Create, Review and Update.](../image/playbook-vert-stages.png "Vertical stage picker")

    -   The horizontal orientation only shows the stages of a selected playbook. To see the activities of a stage, select the stage.

        ![Horizontal view of a playbook named Playbook Experience Demo with stages named Assign, Create, Review and Update.](../image/playbook-horizontal-stages.png "Horizontal stage picker")

        Playbooks with more than 5 stages paginate.

        **Note:** The horizontal stage picker only shows you the playbook you are in and its stages, so you can’t navigate between playbooks unless you:

        -   Use a playbook template, or
        -   Create your own drop-down component with UI Builder.
        All playbook templates include a drop-down component to navigate between playbooks, and is auto-populated when you select the **Playbook Picker** preset.

-   **Playbook activity picker**

    The activity picker is where you navigate between activities.

    If you're using the vertical stage picker, turning on the activity picker means each stage can be expanded to shows its activities.

    ![Activity picker when you're viewing stages vertically.](../image/playbook-activity-picker-vert.png "Activity picker when viewing stages vertically")

    If you're using the horizontal stage picker, turning on the activity picker allows you to expand or collapse the entire list of activities for the stage you're in.

    ![Activity picker when you're viewing stages horizontally.](../image/playbook-activity-picker-horizon.png "Activity picker when viewing stages horizontally")

    To toggle the **Show Stages flag** flag on or off, .

-   **Playbook activity viewer**

    The activity viewer is where you manage a stage's activities. You can change the way activities are displayed in this space:

    -   The **Stacked** view displays all activities in a stage stacked on top of each other.

        ![Activities stacked for the Assign stage. The 1st activity is complete, the 2nd is in progress and can be marked complete or skipped, and the 3rd is pending.](../image/playbook-stacked-view.png "Playbook stacked view")

    -   The **Focused** view displays a single selected activity.

        ![A single activity that you can mark as complete or skip.](../image/playbook-focused-view.png "Playbook focused view")

-   **Playbook modals**

    If you want the ability to cancel playbooks and add optional activities, you must add the **Playbook Modals** component to your pages. If you use a template, this is already included.

    ![The Cancel playbook modal](../image/playbook-cancel-modular-modal.png "Cancel playbook modal")

    ![The Add optional activity modal](../image/playbook-opt-activity-modal.png "Add optional activity modal")


To start setting up components for your customized Playbook Experience, see [Customize a playbook in UI Builder](../task/playbook-get-started-custom-layouts.md).

## Provided UI Builder Bundles

If adding each component individually isn't ideal, you can also add an entire layout to a new or existing UI Builder template.

-   Focused Vertical
-   Focused Horizontal
-   Stacked Vertical
-   Stacked Vertical

Each layout contains the following components:

-   UI controller
-   Presets
-   Activity viewer
-   Activity picker
-   Modals
-   Playbook picker
-   Stage picker
-   Client scripts

To add a bundle to an existing or new UI Builder page, see [Add a custom layout bundle to a UI Builder page](../../process-automation-designer/task/add-custom-layout-bundle-uib-page.md). If you're creating a new experience and want to add a bundle to a standard record page, see [Add a custom layout bundle to a UI Builder standard record page](../../process-automation-designer/task/add-custom-layout-bundle-uib-standard-record.md).

-   **[Customize a playbook in UI Builder](../task/playbook-get-started-custom-layouts.md)**  
Use UI Builder pages and modular components for custom playbook layouts to customize the end user's Playbook Experience in a configurable workspace, Service Portal page, or mobile web page.
-   **[Add a custom layout bundle to a UI Builder page](../../process-automation-designer/task/add-custom-layout-bundle-uib-page.md)**  
Add playbook custom layout bundles to a new or existing UI Builder page that you've created from scratch.
-   **[Add a custom layout bundle to a UI Builder standard record page](../../process-automation-designer/task/add-custom-layout-bundle-uib-standard-record.md)**  
Add playbook custom layout bundles to a new or an existing UI Builder standard record page.
-   **[Enable Guided activity view](../../process-automation-designer/task/enable-guided-activity-view.md)**  
Guide end users through a playbook, step-by-step.

**Parent Topic:**[Designing playbooks](playbook-experience-admins.md)

