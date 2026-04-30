---
title: Creating guidance and field recommendation in Recommended Actions
description: Create guidances and field recommendations that you can use to configure recommended actions.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Creating guidance and field recommendation in Recommended Actions

Create guidances and field recommendations that you can use to configure recommended actions.

## Configuring guidances

When you create a guidance, you configure several different aspects of that guidance:

<table id="table_fbk_4sn_25b"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure inputs and outputs for a guidance.

</td><td>

-   Inputs: The variables or information that the system must perform the guidance.
-   Outputs: the result of the guidance.

</td></tr><tr><td>

Configure a preview experience for a guidance.

</td><td>

A preview on the card that is displayed to the agent can include:-   A hint that briefly tells the agent what the guidance is about
-   A preview message that describes the guidance in more detail
-   The action that the agent can take

</td></tr><tr><td>

Configure a detail experience for a guidance.

</td><td>

A detailed message that is displayed for guidances that open in the contextual side panel or in a subtab.

</td></tr><tr><td>

Configure a primary call to action for a guidance.

</td><td>

A guidance can have multiple actions, with one identified as the primary action and optional secondary actions.

</td></tr><tr><td>

Configure the behavior of a guidance.

</td><td>

Determines how the system executes a primary action after the agent selects the action button on the card.-   **Single click**: Initiates and completes the action and moves the card to the History tab in the Recommended Actions panel. This behavior is useful for simple actions such as escalating a case.
-   **Open in the contextual side panel**: Expands the action and displays information about that action in the Recommended Actions panel. This behavior is useful for actions such as reviewing the content in an article before attaching it to a case.
-   **Open in a sub tab**: Opens the action in a subtab under the case tab. This behavior is useful for guidances that require the agent to select and submit additional information, such as filling out the fields on a form.

</td></tr><tr><td>

Customize the preview experience and the detail experience of a guidance

</td><td>

Options to customize the following items in the UI Builder: -   **Preview experience**: The preview of the recommendation card includes a hint, an icon, a message, and an action button. The preview of the card shows up in the contextual side panel.
-   **Detail experience**: The detail experience of the guidance includes the drill down actions. It opens in the contextual side panel or in a subtab.

</td></tr></tbody>
</table>## Configuring field recommendations

Field recommendation suggests a value for a field in the record form. Creating a field recommendation involves two main steps:

-   Selecting the inputs for the recommendation.
-   Creating the instructions about how to use those inputs.

