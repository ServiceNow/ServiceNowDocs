---
title: Create a guided tour to illustrate vacation delegation
description: Use Guided Tour Designer to create a guided tour for assigning a vacation delegate.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Guided Tour Designer use case, Use Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Create a guided tour to illustrate vacation delegation

Use Guided Tour Designer to create a guided tour for assigning a vacation delegate.

## Before you begin

Role required: guided\_tour\_admin

## About this task

Here’s an example of using Guided Tour Designer to create a tour that explains to users how to assign a vacation delegate. This example demonstrates the use of introduction, callouts, callout steps, and the conclusion in a tour.

## Procedure

1.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Create Tour**.

2.  Enter a name in the **Name** field.

3.  From the Tour Type list, select **Standard UI**.

4.  From the Starting Page list, search for `sys_user_delegate_list.do` and select it.

    ![Select Delegate List.](../image/gtd-delegate-vacation.png)

5.  Select a role and then select **Create Tour**.

    A guided tour is created.

6.  In the Guided Tours form view, to open the Guided Tour Designer select **Edit with Designer**.

7.  Add the following steps to the guided tour:

<table id="id_k1q_nqm_xfc"><thead><tr><th>

Step

</th><th>

Callout

</th><th>

Trigger

</th></tr></thead><tbody><tr><td>

Add an introduction.

</td><td>

1.  Select **Create Introduction**.
2.  Enter a title; for example, Assign vacation delegation.
3.  Enter the following message in the **Text** field: `This tour will walk you through the necessary steps to effectively assign someone to manage your responsibilities while you are away on vacation.`


</td><td>

No trigger is required.

 Select **Save** to save the step.

</td></tr><tr><td>

Open the Delegate form and enter a new record.

</td><td>

1.  Drag a callout and position it to point at the **New** button in the Delegates list view.
2.  Enter the following message in the **Text** field: `Click New to set up a delegate who will receive your notifications while you are on vacation.`

![Drag a callout and position it to point to a element.](../image/gtd-vacation-delegation-new.png)

</td><td>

1.  From the Choose action list, select **Trigger next step on click.**
2.  Select **Save** to save the step.


</td></tr><tr><td>

Describe the **User** field.

</td><td>

1.  Drag a callout and position it to point at the **User** field.
2.  Enter the following message in the **Text** field: `Your name defaults as the user who wants to delegate to another user. If you are setting up a delegate for someone else, you can select a different user.`


</td><td>

1.  From the Choose action list, select **Trigger next step on next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

Select the delegate

</td><td>

1.  Drag a callout and position it to point at the **Delegate** field.
2.  Enter the following message in the **Text** field: `Specify the person you want to delegate to by typing their name and selecting it when it appears.`


</td><td>

1.  From the Choose action list, select **Trigger next step on next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

Set the start date

</td><td>

1.  Drag a callout and position it to point at the **Starts** field.
2.  Enter the following message in the **Text** field: `Enter the date and time to start forwarding notifications.`


</td><td>

1.  From the Choose action list, select **Trigger next step on click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

Set the end date

</td><td>

1.  Drag a callout and position it to point at the **Ends** field.
2.  Enter the following message in the **Text** field:`Select the date and time to stop forwarding notifications.`


</td><td>

1.  From the Choose action list, select **Trigger next step on click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

Describe the delegate options

</td><td>

1.  Drag a callout and position it to point at the check boxes from the **Approvals** check box to the **Meeting invitations** check box.
2.  Enter the following message in the **Text** field: `If you do not want these notifications forwarded to your delegate, you can clear any of these fields.`


</td><td>

1.  From the Choose action list, select **Trigger next step on next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

Submit the delegate record

</td><td>

1.  Drag a callout and position it to point at the **Submit** button.
2.  Enter the following message in the **Text** field:`Click Submit to add the delegate.`


</td><td>

1.  From the Choose action list, select **Trigger next step on click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

Add a conclusion

</td><td>

1.  Select **Create Conclusion**.
2.  Enter the following message in the **Text** field: `Hurrah! Your vacation delegation has been successfully completed!`


</td><td>

No trigger is required.

 Select **Save** to save the step.

</td></tr></tbody>
</table>
## Result

The guided tour is created and listed in the Help Center.

Users can access a guided tour by navigating to a page that has one. For more information, see [Start a guided tour](../concept/accessing-guided-tours.md#).

**Parent Topic:**[Guided Tour Designer use case](../concept/guided-tour-designer-use-case.md)

**Related topics**  


[Create Guided Tours](add-guided-tour.md)

[Edit Guided Tours](edit-guided-tour.md)

