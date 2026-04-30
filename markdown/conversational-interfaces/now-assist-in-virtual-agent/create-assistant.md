---
title: Create an assistant
description: Manage the performance of an existing LLM Virtual Agent that was created with Now Assist or create an assistant.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 3
breadcrumb: [Configuring Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Create an assistant

Manage the performance of an existing LLM Virtual Agent that was created with Now Assist or create an assistant.

## Before you begin

[Configuring Now Assist in Virtual Agent](configure-now-assist-va.md)

The **Assistants** tab is viewable in the Conversational Interfaces Admin console when the Now Assist in Virtual Agent plugin or the Now Assist for Creator plugin is installed, or both are installed.

-   If you only have the Now Assist in Virtual Agent plugin installed, the default Now Assist panel - Platform and all Now Assist in Virtual Agent assistants are shown.
-   If you only have the Now Assist for Creator plugin installed, only the Now Assist panel - Developer assistant is shown.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Select the ellipsis to turn on, off, edit, or delete an assistant.

    **Note:** The default Now Assist in Virtual Agent assistant can't be deleted. You can delete any other assistant that you create. The default Now Assist panel assistants \(Platform and Developer\) can't be deleted. New Now Assist panel assistants can't be created.

    ![Table with list of assistants.](../image/NAinVA-assistants-052025.png "List of assistants")

    The Relationship type column shows whether an assistant is a primary or secondary assistant, or neither. For more information about primary and secondary assistants, see [LLM assistants](../concept/llm-assistants.md).

    To view the linkage between primary and secondary assistants, you can toggle between the list view and the map view.

    ![View primary and secondary assistants as a list or map view.](../image/NAinVA-view-mapNOV.png "Toggle between list and map view")

    In the map view, primary assistants on the top row show secondary assistants that are linked to them. Green indicates that the assistant is turned on. Gray indicates that the assistant is turned off. Select an assistant on the map to edit, delete, or turn it on or off.

    ![Map view of primary assistants and their associated secondary assistants.](../image/NAinVA-mapping.png "Primary and secondary assistants in map view")

2.  Create a Virtual Agent assistant by selecting **Create new**.

    The Get started \(Overview\) page is displayed.

    **Note:** The **Name** and **Description** fields, and the ability to link to other assistants are read-only for Now Assist panel assistants.

    ![Virtual Agent Name and Description fields in the Get started page.](../image/NAinVA-get-started2-NOV.png "Virtual Agent name and description fields")

    1.  In the Add some details section, provide a name and description for your Virtual Agent. The name of the assistant in this example is Now Assist in Virtual Agent - TEST.
    2.  Select the **Link this to other assistants** check box to make the assistant a primary assistant to which you can add secondary assistants.
    3.  Place your cursor within the **Select secondary assistant\(s\) to link to** field to see the list of available secondary assistants.
    ![Drop-down list showing all available secondary assistants.](../image/NAinVA-link-assistantNOV.png "Link primary assistant with secondary assistants")

    One or more secondary assistants must be selected. All assistants within the same instance and domain are shown in the drop-down list, enabling you to link your primary assistant with one or more secondary assistants. Two primary assistants can't be linked to each other; therefore, other primary assistants are unavailable in the list.

    If one or more secondary assistants are selected that are inactive, an alert shows `The following secondary assistants are off and will be inaccessible.` A list of inactive assistants is shown.

    To turn on the secondary assistants, select **Exit** to return to the **Assistants** tab. Otherwise, select **Save and continue**.


## What to do next

[Assign Now Assist skills to an assistant](assign-na-skills-assistant.md).

