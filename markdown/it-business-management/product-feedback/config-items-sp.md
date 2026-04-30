---
title: Configure non-planning items for feedback or product ideas records
description: Configure non-planning items to link your feedback or product idea records to navigate quickly between related items.
locale: en-US
release: xanadu
product: Product Feedback
classification: product-feedback
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Feedback, Strategic Planning, Strategic Portfolio Management]
---

# Configure non-planning items for feedback or product ideas records

Configure non-planning items to link your feedback or product idea records to navigate quickly between related items.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System properties** &gt; **All properties**.

2.  Open the **sn\_apw\_advanced.product\_feedback\_allowed\_non\_planning\_items\_for\_link\_item** property.

3.  Edit the property by selecting **here**.

4.  In the value field, enter the non-planning item table name and select **Update**.

    You can add the table name of an incident, case, scrum task, agile story, or tables from any global or scoped application. You can enter one or multiple table names separated by comma in the value field.

5.  Configure the non-planning items that you want to link.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Search for feedback from the Label list.

    3.  Open the feedback record that has the **sn\_align\_core\_feedback** table name and select the **Show List** related link.

    4.  Open any feedback record, select the additional actions \( ![additional-action-icon](../image/additional-actions-icon-feedback.png)\).

    5.  Select **Configure** &gt; **Related Lists**.

    6.  Select the **Edit this view** link.

    7.  Move Related Items from Available panel to Selected panel.

    8.  Select **Save**.

6.  Configure a form view with view name `workspace_apw_new` for all the non-planning item tables added in step 4.


## What to do next

[Associate a feedback or a product idea record with a non-planning item](associate-feedback-with-non-planning-item.md)

**Parent Topic:**[Configuring Feedback application in Strategic Planning](../concept/configuring-product-feedback-in-sp.md)

