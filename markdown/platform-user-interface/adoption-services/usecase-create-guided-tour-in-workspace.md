---
title: Create a guided tour to show incident generation in Workspace
description: Use the Guided Tour Designer to create a tour that explains how to generate an incident in Workspace.To enable your newly created guided tour to work on any sys\_id, you must manually update the route parameters. This is also essential for enabling the Take a Tour option in the Help Center.Use the Guided Tour Designer to add an introductions, steps, and conclusion to your tour.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 3
breadcrumb: [Guided Tour Designer use case, Use Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Create a guided tour to show incident generation in Workspace

Use the Guided Tour Designer to create a tour that explains how to generate an incident in Workspace.

## Before you begin

Role required: guided\_tour\_admin or admin

## About this task

Guided Tours are available in Workspace to help users understand the features of the Workspace.

Here’s an example of using tours to guide users through the steps of creating an incident in Workspace.

## Procedure

1.  Navigate to **All** &gt; **Guided Tours Designer** &gt; **Create Tour**.

2.  Enter the following details:

<table id="table_wqt_sfp_h1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name of your tour; for example, **Create New Incident Tour on Workspace**.

</td></tr><tr><td>

Tour Type

</td><td>

1.  Specify the type of page for which the tour is created. In this example, it’s **Workspaces**.
2.  Select **Manual Selection**.


</td></tr><tr><td>

Starting Page

</td><td>

Specify the page for which the tour is created. In this example, it's **Service Operations Workspace: Record**.

</td></tr><tr><td>

Table

</td><td>

Specify the type of record that requires guidance. In this example, it's **incident**.**Note:**

Make sure the term 'incident' is always written in lowercase letters only.

</td></tr><tr><td>

Sys\_id

</td><td>

Specify the sys\_id for the page that needs guidance. In this example, **-1**.

 **Note:**

To set up your tour, avoid using URLs with specific IDs like -1\_uid\_1 or -1\_uid\_3, as they’ll only work for incidents with the same ID. Instead, use this option: \{"url":"/now/sow/record/incident/-1"\}.

Start with this setup, and if you have steps with IDs, change them to: \{"url":"/now/sow/record/incident/-1"\} for correct functionality.

</td></tr></tbody>
</table>3.  Select the **Create Tour** button.

    A guided tour is created.


**Parent Topic:**[Guided Tour Designer use case](../concept/guided-tour-designer-use-case.md)

## Update the Route Parameters

To enable your newly created guided tour to work on any sys\_id, you must manually update the route parameters. This is also essential for enabling the **Take a Tour** option in the Help Center.

Perform the following steps:

1.  In the Guided Tour Designer list view, choose the tour you want to update.

2.  In the editable form, change the **Route Parameters** and set the value of the parameter **isDynamic** to **True**.![Set the value of the parameter isDynamic to True](../image/gtd-isdynamic-true.png)

    This update enables your guided tour across different sys-ids and activates the **Take a Tour** option in Help Center.


## Add steps to the guided tour

Use the Guided Tour Designer to add an introductions, steps, and conclusion to your tour.

In the Guided Tour Designer, add the following steps to the tour:

-   **Introduction**

    Add an introduction that outlines the steps in the guided tour and describes the milestone you achieve when all actions are completed.

    ![Guided Tours callout introduction.](../image/guided-tours-create-incident.png)

-   **Callouts**

    Add callouts to guide users with step-by-step instructions to navigate and operate within the workspace. You can position callouts anywhere in your workspace to provide additional context or task-related instructions. There are several display options for the callouts, including:

    -   Above
    -   Below
    -   To the left
    -   To the right
    While creating your list of tour steps, you can also drag the steps to reorder them as needed.

-   **Triggers**

    You can create steps across various pages in your workspace and set up triggers to lead users to the next step. As users progress through the tour, the next callout will appear after completing the trigger.

    For example, the trigger can be configured to advance after the user selects the **Next** button.

    ![Guided tours callout steps.](../image/guided-tour-incident-steps.png)

-   **Conclusion**

    At the end of the tour, add a conclusion indicating that the tour is complete. This is a great opportunity to encourage users to explore other tours or provide follow-up information on what to do next.

    ![Guided tour callout conclusion.](../image/guided-tour-conclusion.png)


After you have created your tour, preview it to confirm that it displays correctly and guides the user effectively before submitting it.

The guided tour is created and listed in the Help Center.

Users can access a guided tour by navigating to a page that has one. For more information, see [Start a guided tour](../concept/accessing-guided-tours.md#).

**Related topics**  


[Create Guided Tours](add-guided-tour.md)

[Edit Guided Tours](edit-guided-tour.md)

