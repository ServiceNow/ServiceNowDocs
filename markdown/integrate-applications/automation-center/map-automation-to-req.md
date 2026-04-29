---
title: Map automations with automation request
description: Map automations in Published state with an automation request to publish the automation request.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Map automations with automation request

Map automations in Published state with an automation request to publish the automation request.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

**Note:** The cost saved and time saved values for an automation are calculated by moving average method. The moving average is controlled by the `sn_ac.savings_averaging_window` system property. For more information, see [Automation Center properties](../reference/automation-center-properties.md).

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Automation Center Home**.

2.  Select the list icon \(![List icon.](../images/autocenter-list-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **All Automation Requests**.

    **Note:** Ensure that the automation request is in In Progress state.

4.  Select the **Automation Mappings** tab.

5.  Select **Map automation**.

    The Automation mapping window is displayed.

    ![Automation mapping window](../images/auto-mapping.png)

6.  Provide the details.

<table id="id_f43_dfr_bcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automation

</td><td>

Double-click to select an automation from the available list.

 For publishing an automation request, you must have at least one automation mapped to the request. Also, the mapped automations must be in the Published state.

</td></tr><tr><td>

Cost saving percentage

</td><td>

Specify the percentage of the cost that this automation saves for the automation request. If the actual cost saved per run is $200, and this automation saves 50%, then this automation saves $100.

</td></tr><tr><td>

Time saving percentage

</td><td>

Specify the percentage of the time that this automation saves for the automation request. If the actual time saved per run is 4 hours, and this automation saves 50%, then this automation saves 2 hours.

</td></tr></tbody>
</table>    **Note:**

    The total cost saving percentages and the total time saving percentages of all automations must be less than or equal to 100.

    You can edit the cost and time savings percentage manually from the form view of the automation attribute record.

    However, if the cost and time saved per run are manually updated, the **Cost saving percentage** and **Time saving percentage** fields in the Automation Mapping form are empty and non-editable. Also, the moving average is not calculated for the edited automation.

    ![Automation mapping detail](../images/auto-mapping-detail.png)

    Example:

    In the automation request, the actual cost saved per run was specified as $200 and the actual time saved per run was specified as 5 hours.

    In the mapping, the Cost saving percentage was specified as 50% and the Time saving percentage was specified as 40%.

    The values for the mapping are auto-calculated based on the input provided as shown in the Automation mappings screenshot.

7.  Select **Add automation** to add multiple automations.

8.  Select **Map automation**.

    The automation is mapped.

9.  Select – beside a row, and select **Map automation** to delete the mapped automation.

    **Note:** You can’t delete the first automation that you have mapped.

10. After creating the mapping, select **Edit mapping** to edit the existing mappings or add new mappings.


**Parent Topic:**[Working with automations](../concept/automations.md)

