---
title: Create guided tour to explore Service Portal home page
description: Use Guided Tour Designer to create a guided tour to explore the Service Portal home page.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 4
breadcrumb: [Guided Tour Designer use case, Use Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Create guided tour to explore Service Portal home page

Use Guided Tour Designer to create a guided tour to explore the Service Portal home page.

## Before you begin

Role required: guided\_tour\_admin

## About this task

Here’s an example of using Guided Tour Designer to create a tour that helps users to explore the Service Portal home page.

This example demonstrates the use of introduction, callouts, callout steps, and the conclusion in a tour.

## Procedure

1.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Create Tour**.

2.  Enter a name in the **Name** field; for example, Service Portal overview.

3.  From the Tour Type list, select **Service Portal**.

4.  From the Portal list, select **Service Portal**.

5.  From the Starting Page list, select **ID Index**.

6.  From the Roles list, select **All** and then select **Create Tour**.

    A guided tour is created.

7.  In the Guided Tours form view, select **Edit with Designer** to open the Guided Tour Designer.

8.  Add the following steps to the guided tour:

<table id="id_mkk_444_xfc"><thead><tr><th>

Step

</th><th>

Callout

</th><th>

Trigger

</th></tr></thead><tbody><tr><td>

Introduction

</td><td>

1.  Select **Create Introduction**.
2.  Enter a title; for example, Service Portal Overview.
3.  Enter the following message in the **Text** field: `Welcome to the guided tour of your new Service Portal home page.`


</td><td>

No trigger is required.

 Select **Save** to save the step.

</td></tr><tr><td>

1

</td><td>

1.  Drag a callout and position it to point at the element **How can we help?**.
2.  Enter the following message in the **Text** field: `Welcome to this guided tour of your new Service Portal home page. We start with the How can we help? search bar. If you can't find what you're looking for, enter it here, click the Search icon, or press Enter on your keyboard. For now, we will look at some other areas first.`


</td><td>

1.  From the Choose action list, select **Trigger next step on Next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

2

</td><td>

1.  Drag a callout and position it to point at the element **Request Something**.
2.  Enter the following message in the **Text** field: `If you would like to order something, such as a new phone, select Request Something.`


</td><td>

1.  From the Choose action list, select **Trigger next step on Next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

3

</td><td>

1.  Drag a callout and position it to point at the element **Knowledge Base**.
2.  Enter the following message in the **Text** field: `If you would like to search the knowledge base, select Knowledge Base.`


</td><td>

1.  From the Choose action list, select **Trigger next step on Next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

4

</td><td>

1.  Drag a callout and position it to point at the element **Get Help**.
2.  Enter the following message in the **Text** field: `If you would like to get help for an issue, select Get Help.`


</td><td>

1.  From the Choose action list, select **Trigger next step on Next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

5

</td><td>

1.  Drag a callout and position it to point at the title bar.
2.  Enter the following message in the **Text** field: `You can also check the knowledge base, order something, look at requests you have logged, and check other options up here in the title bar.`


</td><td>

1.  From the Choose action list, select **Trigger next step on Next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

6

</td><td>

1.  Drag a callout and position it to point at your name in the top-right corner.
2.  Enter the following message in the **Text** field: `View your profile or log out by clicking your name.`


</td><td>

1.  From the Choose action list, select **Trigger next step on Next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

7

</td><td>

1.  Drag a callout and position it to point at the company logo in the top-left corner.
2.  Enter the following message in the **Text** field: `Navigate back to your Service Portal home page by clicking your company logo.`


</td><td>

1.  From the Choose action list, select **Trigger next step on Next button click**.
2.  Select **Save** to save the step.


</td></tr><tr><td>

Conclusion

</td><td>

1.  Select **Create Conclusion**.
2.  Enter the following message in the **Text** field: `Congratulations! Now you have a general understanding of the Service Portal home page.`


</td><td>

No trigger is required.

 Select **Save** to save the step.

</td></tr></tbody>
</table>9.  After you have created your tour, preview it to confirm that it displays correctly and guides the user effectively before submitting it.


## Result

The guided tour is created and listed in the **Tours** menu.

Users can access a guided tour by navigating to a page that has one. For more information, see [Start a guided tour](../concept/accessing-guided-tours.md#).

**Parent Topic:**[Guided Tour Designer use case](../concept/guided-tour-designer-use-case.md)

**Related topics**  


[Create Guided Tours](add-guided-tour.md)

[Edit Guided Tours](edit-guided-tour.md)

