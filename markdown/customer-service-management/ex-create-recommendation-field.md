---
title: Create a recommendation with the field recommendation as an action type
description: Create a recommendation to select the field recommendation as an action type for recommending a value for the Assignment group field on a case record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example: Recommend an assignment group for a router issue, Example configurations, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Create a recommendation with the field recommendation as an action type

Create a recommendation to select the field recommendation as an action type for recommending a value for the Assignment group field on a case record.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, admin

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.

2.  Select Case context.

3.  In the Rules related list, select Active rule.

4.  In the Recommendations related list, select **New**.

5.  From the New Recommendation screen, select **A field value to use**.

    A new Recommendation form is displayed with the **Rule**, **Context**, and **Action type** fields auto populated.

6.  In the **Name** field, enter `Recommend assignment group for router issue`.

7.  In the **Action** field, select an action.

    1.  In the **Action** field, select the lookup icon.

        In the resulting pop-up window, the **Table name** field is auto-populated with the table that stores the available actions for the selected action type.

    2.  In the **Document** field, select the Field recommendation for assignment group field recommendation.

    3.  Select **OK**.

8.  In the **Resource generator** field, select the Assignment group for router issue RG resource generator.

9.  Save the record to display the Action inputs form section.

10. Define the action inputs.

    1.  Select the pill picker next to the field.

    2.  In the **Assignment group** field, select **Resource generator** &gt; **Assignment group: Group**.

11. Select **Update**.


