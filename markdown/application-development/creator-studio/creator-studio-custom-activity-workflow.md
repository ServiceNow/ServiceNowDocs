---
title: Steps to create a custom activity in Creator Studio
description: There are multiple steps to add custom activities for use in Creator Studio automations.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [About custom activities, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Steps to create a custom activity in Creator Studio

There are multiple steps to add custom activities for use in Creator Studio automations.

## Adding a completely new activity

The steps to create a custom activity for a playbook are as follows:

1.  **Create the flow, subflow, or action**: An admin or someone with the correct role must first create the flow, subflow, or action in Workflow Studio. For more information, see General guidelines for Workflow Studio flows, subflows, and actions.
2.  **Define the activity**: An admin then defines the activity by adding it to the Activity Definition table and assigning the flow/subflow/action to a playbook activity. This step is also when the admin specifies which inputs can be made available as fields in the activity settings in Creator Studio playbooks. For more information, see Activity definitions and Create an activity definition.

    **Note:** If an activity definition already exists for the activity you want, you can skip this step.

3.  **Make the activity available in Creator Studio**: An App Engine admin adds the activity to the Creator Studio Activities table. For more information, see [Make a custom activity available for playbooks in Creator Studio](../task/creator-studio-add-custom-activity.md).

## Making existing activities and playbooks available in Creator Studio

Admins can make existing flows, subflows, and actions available in Creator Studio by defining the activity and then adding it to the Creator Studio Activities table \(the preceding steps 2 and 3\).

Admins can also make existing playbook activities available in Creator Studio by adding them to the Creator Studio Activities table \(the preceding step 3\).

**Note:** Creator Studio admins can see the Activity Definitions \[sn\_pd\_activity\_definition\] table by default, which also enables them to administer processes in Workflow Studio.

**Parent Topic:**[Administering activities in Creator Studio](creator-studio-administering-activities.md)

