---
title: Create a recommendation with guidance as an action type
description: Create a recommendation to select the Guidance as an action type for linking a major case to the current case record.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Example: Link the similar major case to the current case, Example configurations of recommended actions, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a recommendation with guidance as an action type

Create a recommendation to select the Guidance as an action type for linking a major case to the current case record.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, admin

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.

2.  Select Case context.

3.  In the Rules related list, select Active rule.

4.  In the Recommendations related list, select **New**.

5.  From the New Recommendation screen, select **A specific action to take or information to review**.

    A new Recommendation form is displayed with the **Rule**, **Context**, and **Action type** fields auto populated.

6.  In the **Name** field, enter `Link major case to current case`.

7.  In the **Action** field, select an action.

    1.  In the **Action** field, select the lookup icon.

        In the resulting pop-up window, the **Table name** field is auto-populated with the table that stores the available actions for the selected action type.

    2.  In the **Document** field, select the Link similar major case guidance.

    3.  Select **OK**.

8.  In the **Resource generator** field, select the Similar major case resource generator.

9.  Save the record to display the Action inputs form section.

10. Define the action inputs.

    1.  Select the pill picker next to the field.

    2.  In the **Assignment group** field, select **Resource generator** &gt; **Assignment group: Group**.

11. In the **Action Inputs** related list, fill in the fields.

<table id="table_alk_xlr_pzb"><thead><tr><th>

Input

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Current case

</td><td>

1.  Select the pill picker next to the field.
2.  Select **Context: case**.


</td></tr><tr><td>

Major case

</td><td>

1.  Select the pill picker next to the field.
2.  Select **Resource generator** &gt; **Highest confidence record: case**.


</td></tr></tbody>
</table>12. Select **Update**.


