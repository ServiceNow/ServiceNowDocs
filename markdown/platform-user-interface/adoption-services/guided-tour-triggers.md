---
title: GTD triggers
description: Triggers are actions that you take to move the tour to the next step. Each callout in a guided tour step has a specific trigger that activates the subsequent step. You define the trigger for each callout, and only relevant triggers appear based on the UI element referenced by the callout.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Guided Tour Designer, Explore Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# GTD triggers

Triggers are actions that you take to move the tour to the next step. Each callout in a guided tour step has a specific trigger that activates the subsequent step. You define the trigger for each callout, and only relevant triggers appear based on the UI element referenced by the callout.

<table id="table_g2q_3gx_ty"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Next Button

</td><td>

The callout includes a **Next** button that the user can select to move on to the next step. This feature is useful in the following situations:

 -   When the callout describes the element it’s pointing to, enabling the user to progress without needing to select any UI elements.
-   When entering information into a reference or date picker field. Users can use the lookup function, manually enter data, or select it from a list. They can proceed once they’ve completed the necessary entry for the step.

</td></tr><tr><td>

Click the Element

</td><td>

The tour advances to the next step when the targeted element is selected.For more information on how to display a step on a different page after users click a link, see [How to show a step on a different page after the user clicked on a link \(KB0725875\)](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0725875%20).

</td></tr><tr><td>

Mouse over the Element

</td><td>

The tour advances to the next step when the user hovers the mouse device over the element.

</td></tr><tr><td>

Right-click the Element

</td><td>

The tour moves to the next step when the element indicated by the callout is right-clicked.

</td></tr><tr><td>

Press Enter key

</td><td>

When the user presses the Enter key, the tour proceeds to the next step. This action acknowledges that the user has submitted input, such as in a text box.

</td></tr><tr><td>

Change Element Value

</td><td>

The tour advances to the next step when the user enters or selects a value in a field and then clicks outside of it.

</td></tr><tr><td>

Press any key

</td><td>

The tour advances to the next step when the user presses any key.

</td></tr><tr><td>

Select

</td><td>

The tour proceeds to the next step when the user selects an option from the drop-down menu.

</td></tr><tr><td>

Double click

</td><td>

The tour moves to the next step when the user double-clicks an element.

</td></tr></tbody>
</table>**Parent Topic:**[Guided Tour Designer](../concept/guided-tours-designer.md)

