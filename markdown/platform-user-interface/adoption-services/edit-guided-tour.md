---
title: Edit a guided tour
description: You can modify the settings of a guided tour, such as the roles that access the tour. You can also edit, add, delete, and reorganize the guided tour steps, and apply additional formatting to the instructional text.
locale: en-US
release: xanadu
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Guided Tours, Guided tours, Adoption services, Configure user experiences]
---

# Edit a guided tour

You can modify the settings of a guided tour, such as the roles that access the tour. You can also edit, add, delete, and reorganize the guided tour steps, and apply additional formatting to the instructional text.

## Before you begin

Role required: guided\_tour\_admin or admin

## About this task

Use the Guided Tour Designer \(GTD\) to add, delete, and reorganize guided tour steps. Use the Guided Tour form only to perform tasks you cannot do easily from the GTD. For demonstration purposes, we begin with edits to the form that appears when you open the guided tour record, and continue with edits you can make in the GTD itself. You can invoke the GTD from the **Edit with Designer** button located in the form.

## Procedure

1.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Guided Tours**, and open the tour to edit.

2.  In the Guided Tour form, take any of the following actions.

    -   Edit the name.
    -   Enter a different page name in the **Context** field. For example, if the form page is listed and you want the user to start on the list view to enter a new record.
    -   Choose a different tour type. If the tour type is **Standard UI**, the **Type** field cannot be changed. If the tour type is **Service Portal**, both the **SP Portal** and **SP Page** values can be changed.
    -   Enter or edit the **Description**.
    -   Start a Service Portal tour from a specific widget, record, or view within a page instead of the page itself. You can enter URL parameters that point to the item in the Add Additional URL Parameters field. For example, enter the section of the URL that contains the sys-id of a widget, or type parameters for a specific record or view, such as `sys_id=abc123&view=myView`.
    -   Clear the **Active** check box to disable the guided tour, which sets it to read-only status, where it cannot be edited, and renders it invisible to end users. If you want to use the tour in the future but keep it unavailable to end users, consider setting it back to draft status for further revision. Select the check box to re-enable the tour.
3.  To view the starting page for the tour while you test and refine its steps, click **Edit with Designer** in the form header.

    The starting page opens in the GTD in a new tab or window.

4.  Having exited the form view, you can perform any of the following steps in the GTD.

<table id="choicetable_y5v_htx_1z"><thead><tr><th align="left" id="d123540e153">

To

</th><th align="left" id="d123540e156">

Do this

</th></tr></thead><tbody><tr><td id="d123540e162">

**Edit the text or trigger in a step**

</td><td>

Navigate to the UI page the step is in and click the step in the list on the right. For example, if the tour starts in the list view but you want to edit a step in the form, open the form. The steps in the current view are numbered inside a red circle.Complete your changes and click **Save**.

</td></tr><tr><td id="d123540e177">

**Delete an introduction, step, or conclusion**

</td><td>

Point to the step that you want to delete and then select the **⊝** icon.

</td></tr><tr><td id="d123540e189">

**Place the callout on a different page element**

</td><td>

1.  Point to the step that you want to delete and then select the **⊝** icon to delete the step with the incorrect placement.
2.  Create a step on the correct page element.
3.  Drag the step into the correct position in the order of steps.


</td></tr><tr><td id="d123540e213">

**Apply text formatting in the step instructions**

</td><td>

In the Guided Tour Steps related list, click the step number.1.  Point to the step that you want to edit and then select the edit icon to open the Content HTML formatter.

![Edit step](../image/gtd-edit-icon.png "Edit step")

2.  Edit the content and apply formatting as appropriate.

**Note:**

All standard HTML tags compatible with your browser are supported.

Do not add images or video to the text. These media types are not supported in callouts.

3.  Click **Update**.


</td></tr><tr><td id="d123540e253">

**Rearrange steps**

</td><td>

Drag the steps to the desired order.

</td></tr><tr><td id="d123540e262">

**Test the tour**

</td><td>

Click **Preview** if the tour is in draft status. Click **Play** if it is published. The page opens in a new list or tab and you can test each step. Note any steps that need corrections.

</td></tr><tr><td id="d123540e277">

**Change the guided tour status**

</td><td>

If the tour is in draft status, click **Publish**. If the tour is published, click **Draft**. Consider setting the tour to draft status until you are finished editing it.

</td></tr></tbody>
</table>
