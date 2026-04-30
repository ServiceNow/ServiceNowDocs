---
title: Edit Guided Tours
description: You can modify the settings of a guided tour by using the Guided Tour Designer \(GTD\).
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Edit Guided Tours

You can modify the settings of a guided tour by using the Guided Tour Designer \(GTD\).

## Before you begin

Role required: guided\_tour\_admin or admin

## About this task

To edit a guided tour, you can use either GTD or the Guided Tours form. The GTD enables you to add, delete, and reorganize guided tour steps. The Guided Tours form is recommended for tasks that are difficult to accomplish using the GTD. You can start by editing the elements shown on the form when you open a guided tour record. Then, proceed to the GTD for further edits.

The base system offers several guided tours for specific applications, such as Performance Analytics. As an administrator, you can modify existing tours and assign one or more roles to them to manage access.

## Procedure

1.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Guided Tours**.

2.  Open the guided tour that you want to edit.

3.  In the Guided Tours form, you can edit the following elements:

    -   In Workspace:
        -   **Name**: Update the name to make it unique and intuitive.
        -   **Status**: Change the to either draft or published.
        -   **Context**: Update the URL for the tours. For example, `/now/sow/home`, `/now/sow/record`, or `/now/sow/list`.
        -   **Description**: Update the description to help users understand the purpose of the tour.
        -   **Roles**: Add or remove roles.
        -   **Route Parameters**: Update route parameters to collect metadata about the specific URL where you want to play the tour.
        -   **Active** check box: Clear the **Active** check box, to turn off the guided tour. The tour becomes read only, meaning it can’t be edited and is hidden from end users.  If you want to keep the tour for future use but don’t want end users to see it, change its status back to draft for further editing. Select the **Active** check box, to turn the tour back on.
    -   In Service Portal:
        -   **Name**: Update the name to make it unique and intuitive.
        -   **Status**: Change the to either draft or published.
        -   **SP Portal**: Specify where the tour should be created, such as in the Employee Center or the Knowledge Portal.
        -   **SP Page**: Specify which page in the SP Portal the tour should be created on, such as the index page or the home page.
        -   **Additional URL Parameters**:

            You can initiate a Service Portal tour from a specific widget, record, or view within a page rather than from the entire page. To initiate a tour, include the URL parameters that directly reference the specific item in the **Additional URL Parameters** field.

            For example, you can specify the part of the URL that contains the sys\_id of a widget, or include parameters for a particular record or view, such as `sys_id=abc123&view=myView`.

        -   **Description**: Update the description to help users understand the purpose of the tour.
        -   **Roles**: Add or remove roles.
        -   **Active** check box: Clear the **Active** check box, to turn off the guided tour. The tour becomes read only, meaning it can’t be edited and is hidden from end users.  If you want to keep the tour for future use but don’t want end users to see it, change its status back to draft for further editing. Select the **Active** check box, to turn the tour back on.
    You can’t change the **Tour Type**, regardless of the user interface type.

4.  To test and refine the steps, select **Edit with Designer** in the form header.

    The starting page opens in the GTD in a new tab or window.

5.  You can perform any of the following tasks in the GTD.

<table id="choicetable_y5v_htx_1z"><thead><tr><th align="left" id="d137736e257">

Task

</th><th align="left" id="d137736e260">

Action

</th></tr></thead><tbody><tr><td id="d137736e266">

**Edit the text in a step**

</td><td>

1.  Navigate to the UI page where the step is located.
2.  In the Tour Steps list, hover over the step you want to edit and select the Edit Step icon ![Edit Step](../../../administer/workspace/image/pencil-icon.png).

![Edit step](../image/gtd-edit-icon.png)

3.  Edit the text and select **Save**.


</td></tr><tr><td id="d137736e301">

**Edit trigger in a step**

</td><td>

1.  Navigate to the UI page where the step is located.
2.  In the Tour Steps list, hover over the step you want to edit and select the Edit Step icon ![Edit Step](../../../administer/workspace/image/pencil-icon.png).
3.  From the Choose action list, select a trigger, and then select **Save**.


</td></tr><tr><td id="d137736e331">

**Delete an introduction, step, or conclusion**

</td><td>

In the Tour Steps list, hover over the step you want to remove and then select the Delete icon **⊝**.

</td></tr><tr><td id="d137736e343">

**Place the callout on a different page element**

</td><td>

1.  In the Tour Steps list, hover over the step and then select the Delete icon **⊝**.
2.  Create a new step on the correct page element.
3.  Enter a message in the **Text** field, select a trigger from the Choose action list, and then select **Save**.


</td></tr><tr><td id="d137736e374">

**Apply text formatting in the step instructions**

</td><td>

1.  In the Tour Steps list, hover over the step you want to edit and select the Edit Step icon ![Edit Step](../../../administer/workspace/image/pencil-icon.png).
2.  Edit the content and apply formatting as appropriate.

**Note:**

All standard HTML tags compatible with your browser are supported.

Don’t add images or video to the text. These media types aren’t supported in callouts.

3.  Select **Save**.


</td></tr><tr><td id="d137736e408">

**Rearrange steps**

</td><td>

Drag the steps to the desired order.

</td></tr><tr><td id="d137736e417">

**Test the tour**

</td><td>

Select **Preview** if the tour is in draft status.

 Select **Play** if it’s published.

 The page opens in a new window or tab. You can test each step. Note the steps that need corrections.

</td></tr><tr><td id="d137736e441">

**Change the guided tour status**

</td><td>

If the tour is in draft status, select **Publish**. If the tour is published, select **Draft**. It’s advisable to keep the tour in draft status until you have completed all edits.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuring Guided Tours](configure-guided-tours.md)

