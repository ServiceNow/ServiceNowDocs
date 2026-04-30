---
title: Create a guidance for linking the similar major case to the current case
description: Create a guidance for linking the similar major case to the current case by configuring guidance inputs, preview experience, and guidance action.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Example: Link the similar major case to the current case, Example configurations, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Create a guidance for linking the similar major case to the current case

Create a guidance for linking the similar major case to the current case by configuring guidance inputs, preview experience, and guidance action.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, admin

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Action Types** &gt; **Guidances**.

2.  Select **New** in the Guidances list.

3.  In the **Name** field, enter `Link similar major case`.

4.  In the **Description** field, enter `This guidance recommends to link the identified similar major case to the current case.`.

5.  Create the following inputs for the guidance.

    Inputs are the variables or information that the system needs to perform the guidance. You can use inputs in multiple places such as the guidance preview experience and the guidance actions.

    1.  In the Guidance Input tab, select **New**.

    2.  In the **Label** field, enter `Current case`.

    3.  In the **Type** field, select Reference.

    4.  In the Reference Specification related list, in the **Reference** field, select the Case table.

    5.  Select **Submit**.

    6.  In the Guidance Input tab, select **New** again.

    7.  In the **Label** field, enter `Major case`.

    8.  In the **Type** field, select Reference.

    9.  In the Reference Specification related list, in the **Reference** field, select the Case table.

    10. Select **Submit**.

6.  Configure the preview experience.

    1.  In the **Preview Title** field, enter `Link to this major case`.

    2.  In the **Fields to display**, select the parent case input.

    3.  In the **Message** field, enter `This is the similar Major case predicted that you can link to the current case.`

7.  Save the guidance record to display the Guidance Actions related list.

8.  Configure a guidance action.

    1.  In the Guidance Actions form section, select **New**.

    2.  In the **Action Label** field, enter `Link major case`.

    3.  In the **Call to Action Label** field, enter `Link major case`.

    4.  In the **Action Behaviour** field, select Single-click.

    5.  In the **Guidance Action Automation** field, select the Link major case subflow.

    6.  In the **Completion Message** field, enter `The suggested major case is linked!`

    7.  Save the record to display the flow inputs.

    8.  In the **Automation Flow Inputs** related list, fill in the fields.

<table id="table_alk_xlr_pzb"><thead><tr><th>

Input

</th><th>

Action

</th></tr></thead><tbody><tr><td>

current case

</td><td>

1.  Select the pill picker next to the field.
2.  Select **Guidance inputs** &gt; **Current case**.


</td></tr><tr><td>

major case

</td><td>

1.  Select the pill picker next to the field.
2.  Select **Guidance inputs** &gt; **Major case**.


</td></tr></tbody>
</table>
