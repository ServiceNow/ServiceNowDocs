---
title: Administering activities in Creator Studio
description: As an admin, you can define custom activities, make them available in Creator Studio, and hide existing activities to help guide users when they add automation to apps.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Administering activities in Creator Studio

As an admin, you can define custom activities, make them available in Creator Studio, and hide existing activities to help guide users when they add automation to apps.

You may want to create custom activities for complex or company-specific workflows. For example:

-   The standard Request approval activity has a **Requester's manager** option, but you may need a **Department manager** instead.
-   You may need an approval or flow with more complex decision logic than is easily built in the Creator Studio automation. You could use Workflow Studio to build that flow, and then create a custom action that calls it.
-   You may want more notification types than the standard Email notification activity. You could create a flow that sends a notification to a MS Teams integration, and create an activity that calls that flow.

-   **[Steps to create a custom activity in Creator Studio](creator-studio-custom-activity-workflow.md)**  
There are multiple steps to add custom activities for use in Creator Studio automations.
-   **[Make a custom activity available for playbooks in Creator Studio](../task/creator-studio-add-custom-activity.md)**  
You must add custom activities to the Creator Studio Activities table \[sn\_creatorstudio\_activity\] before users can add them to playbooks when building apps.
-   **[Reorder how activities appear in a playbook's activity picker](../task/creator-studio-reorder-activities.md)**  
Change the order that activities appear in the activity picker in Creator Studio to present them in the order you want.
-   **[Make an activity unavailable in playbooks](../task/creator-studio-hide-activity.md)**  
Deactivate an activity to stop users from adding it to playbooks in Creator Studio.

**Parent Topic:**[Administering Creator Studio](administering-creator-studio.md)

