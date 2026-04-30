---
title: Guided Tours in Configurable Workspaces
description: Guided Tours is a feature in ServiceNow that assists users in onboarding and training processes. Guided Tours are supported in Configurable Workspaces to instruct users how to use features in your workspace.
locale: en-US
release: yokohama
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Guided Tours in Configurable Workspaces

Guided Tours is a feature in ServiceNow that assists users in onboarding and training processes. Guided Tours are supported in Configurable Workspaces to instruct users how to use features in your workspace.

## Create Guided Tour in Configurable Workspaces

To create a Guided Tour in your Configurable Workspace, see [Create a guided tour](../task/add-guided-tour.md).

## Example: Create an incident using Service Operations Workspace

The following is an example of how you can use Guided Tours to explain to a user the steps to create an Incident in your workspace. In this example it shows the introduction, callouts, callout steps, and the conclusion for your tour.

1.  Navigate to **All** &gt; **Guided Tours Designer** &gt; **Create Tour**.
2.  Fill in the new guided tour form.

<table id="table_wqt_sfp_h1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of your tour. In this example, it's **Create New Incident Tour on Workspace**.

</td></tr><tr><td>

Tour Type

</td><td>

The area the tour is created for. In this example, it's **Workspaces**.Select **Manual Selection**.

</td></tr><tr><td>

Starting Page

</td><td>

The page the tour is created for. In this example, it's **Service Operations Workspace: Record**.

</td></tr><tr><td>

Table

</td><td>

The type of record needing guidance. In this example, it's **incident**.**Note:**

Make sure the term 'incident' is always written in lower case letters.

</td></tr><tr><td>

Sys\_id

</td><td>

**Note:** It's important that you set up your tour this way, instead of copying and pasting a new incident URL as workspaces append an additional id such as -1\_uid\_1, or -1\_uid\_3, etc. If you use one of these URLs your tour will only work when a new incident matches that uid. Also, it's important to ensure that your steps are captured with the Options of: \{"url":"/now/sow/record/incident/-1"\}, if you start with these recommendations you should not have to change them, but if you have tour steps with options with the uid appended, change the JSON to: \{"url":"/now/sow/record/incident/-1"\} and it should work.

The sys\_id for the page needing guidance. In this example it's **-1**.

</td></tr></tbody>
</table>3.  Select the **Create Tour** button.
4.  The Guided Tour Designer window opens with the page that is selected in the steps above.

## Updating an existing Guided Tour

To enable your newly created Guided tour to work on any sys-id, update the **Route Parameters** manually. This is essential for enabling the **Take a Tour** option in Help Center.

-   Select the tour you want to update from the Guided Tour Designer list view. Edit the **Route Parameters** in the editable form.
-   Among other parameters displayed, the admin can set **isDynamic** to True.

This update will enable your Guided tour across different sys-id and invoke the **Take a Tour** option in Help Center.

## Guided tour introduction

The introduction established the foreword to the steps mentioned in the Guided Tour and also explains the milestone you will accomplish once all the actions are complete.

![Guided Tours callout introduction.](../image/guided-tours-create-incident.png "Guided tour introduction")

## Guided tour callouts

Callouts direct the user, with step-by-step guidance, to navigate and operate within the workspace. You can drag callouts anywhere within your workspace to give more context on the screen or instruction for the task. You can choose how the callout is displayed in the area you want to provide more information about. The options for the callout displays are:

-   Above
-   Below
-   To the left
-   To the right

For example, in this scenario, the callouts direct the user to navigate to the list view and look for the Incidents tab. As you create your tour steps list, you can also drag the steps in the list to reorder them.

![Guided Tours callout list.](../image/guided-tours-callout-intro.png "Guided tour callouts")

You can create steps on multiple pages and areas within the workspace. You can also configure the triggers that will advance the user to the next step. As the user selects through the tour, the next callout step displays after the trigger is completed. In this example, the trigger is configured to go to the next step on after selecting the next button.

![Guided tours callout steps.](../image/guided-tour-incident-steps.png "Guided tour callout steps")

**Note:** As you create your tour, be sure to identify areas that may be confusing or need extra attention.

At the completion of the tour, the user is presented with a conclusion notifying the provided the tour is finished. Here you can direct your users to check out other tours, or give them follow-up information of what to do next now that they’ve completed the tour.

![Guided tour callout conclusion.](../image/guided-tour-conclusion.png "Guided tour conclusion")

After you have completed creating your tour, you can select to preview the tour to make sure it displays and guides the user properly before submitting.

