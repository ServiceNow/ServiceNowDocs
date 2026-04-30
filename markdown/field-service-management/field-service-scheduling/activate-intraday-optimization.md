---
title: Activate intraday optimization
description: Activate Intraday optimization by activating the Field Service Management Scheduling Automations plugin \(com.snc.sn\_app\_fsm\_scheduling\_flows\) for Field Service Management. After the plugin is installed, navigate to flow designer to activate the relevant flows to trigger Intraday optimization to run throughout the day as scheduling conditions change.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Optimizing technician schedules at set intervals throughout the day, Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Activate intraday optimization

Activate Intraday optimization by activating the Field Service Management Scheduling Automations plugin \(com.snc.sn\_app\_fsm\_scheduling\_flows\) for Field Service Management. After the plugin is installed, navigate to flow designer to activate the relevant flows to trigger Intraday optimization to run throughout the day as scheduling conditions change.

## Before you begin

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications****All**.

2.  Search for the Field Service Scheduling Automations plugin \(com.snc.sn\_app\_fsm\_scheduling\_flows\) by its name or ID.

3.  Select **Install**.

4.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

5.  Duplicate the required flows.

    1.  Select the Agent time off created Field Service Management Scheduling Automations flow.

    2.  Copy the flow by selecting the More actions icon \(![More actions icon](../image/more_actions.png)\) in the top right and selecting **Copy flow**.

    3.  Enter a name for the copied flow or retain the default name, which appends the word "Copy" to the name of the flow.

    4.  In the **Application** field, select **Field Service Management Scheduling Automations**.

    5.  Select **Copy**.

        A copy of the flow opens with the information you entered.

    6.  Select **Activate**.

    7.  Repeat these steps for the following event trigger flows: High priority work order task dispatched, Work order task canceled, and Work order task progressed.

        Optimization doesn’t consider priority unless the "Maximize assignment of higher priority tasks" constraint exists on the policy for the qualifier that triggered the event. For more information on adding constraints, see [Add constraints to a policy](add-constraint-schedule-optimization-policy.md).

    8.  Repeat the steps to active the event trigger flow, Agent WFO time off.

        **Note:** Ensure the Shift Scheduling for Field Service plugin is activated to use the Agent WFO time off flow.

6.  Duplicate the Schedule intraday jobs flow

    1.  Select the Schedule intraday jobs Field Service Management Schedule Optimization flow.

    2.  Copy the flow by selecting the More actions icon \(![More actions icon](../image/more_actions.png)\) in the top right and selecting **Copy flow**.

    3.  Enter a name for the copied flow or retain the default name, which appends the word "Copy" to the name of the flow.

    4.  In the **Application** field, select **Schedule Optimization**.

    5.  Select **Copy**.

        A copy of the flow opens with the information you entered.

7.  Make the Default record active.

    1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Configuration**.

    2.  On the form, select **Default**.

    3.  On the form, select **Active**.

    4.  In the **Intraday flow** field, select the renamed Schedule Optimization Schedule intraday jobs flow.

8.  **Note:** You can activate additional intraday configurations for any of your groups or territories.

    Select **Update**.


