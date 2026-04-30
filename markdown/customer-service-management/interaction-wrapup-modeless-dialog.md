---
title: Interaction wrap up with modeless dialog
description: Interaction wrap up provides agents with dedicated time after each call or chat to finalize interaction details. Agents can use this time to wrap up their work before starting a new conversation.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Interaction wrap up with modeless dialog

Interaction wrap up provides agents with dedicated time after each call or chat to finalize interaction details. Agents can use this time to wrap up their work before starting a new conversation.

When interaction wrap up is enabled, an interaction record moves from the Work In Progress state to the Wrap Up state at the end of a customer conversation. This configurable period of time enables agents to complete tasks such as posting work notes and updating record information before moving on to assist other customers.

While in the Wrap Up state, an agent’s capacity is not reduced until the state of the interaction moves to Closed Complete.

## Interaction wrap up features

Interaction wrap up includes several configurable features:

-   [Wrap-up codes](interaction-wrapup-modeless-dialog.md#section_z1t_m4m_rdc): Agents can select from a list of codes that provide information about how the interaction was resolved.
-   [Wrap-up notes](interaction-wrapup-modeless-dialog.md#section_iyj_j33_zdc): Agents can provide additional information about the interaction resolution.
-   [Wrap-up timer](interaction-wrapup-modeless-dialog.md#section_ycd_24m_rdc): Displays the duration of the wrap-up period. When the end of the duration is reached, the system automatically ends the wrap-up period and saves the wrap-up data with the default code and notes field blank.
-   [Wrap-up modeless dialog](interaction-wrapup-modeless-dialog.md#section_jfj_14m_rdc): Displays when the agent ends an interaction. Includes the wrap-up timer and fields for the wrap-up code and notes.

Interaction wrap up also includes [wrap-up segments](interaction-wrapup-modeless-dialog.md#section_p2w_wj3_zdc), which store interaction wrap-up data. Wrap up segments enable multiple wrap ups per interaction. For example, when one agent transfers an interaction to another agent and each agent completes a wrap up for the same record.

## Interaction wrap-up benefits

Interaction wrap up provides agents with dedicated time to complete their work on an interaction. If enabled, a wrap-up timer displays the remaining time in the wrap-up period. Agents can complete and submit the wrap-up data within the wrap-up period or allow the system to automatically complete the wrap-up period when the time expires.

Managers can configure the length of the wrap-up period for their agents. Managers can also access reports on wrap-up time usage and effectiveness and use analytics to track data accuracy and agent productivity improvements.

Admins can set and manage wrap-up time limits for voice and chat interactions and create wrap-up codes. Agents can quickly select from a list of available codes during wrap-up.

## Wrap-up codes

Wrap-up codes provide information about how an interaction was resolved. Agents can select a wrap-up code when wrapping up an interaction in CSM Configurable Workspace. When wrap-up codes are enabled, agents can select a code from the configured list in the wrap-up modeless dialog.

System administrators can create wrap-up codes. From the Interaction Wrap Up Configuration record, system administrators can also do the following:

-   Enable wrap-up codes.
-   Select the wrap-up codes that are available to agents in the wrap-up modeless dialog.
-   Select a default wrap-up code.

For more information, see the following topics:

-   [Create an interaction wrap-up configuration](https://www.servicenow.com/docs/access?context=create-interaction-wrap-up-config&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
-   [Create interaction wrap up codes](https://www.servicenow.com/docs/access?context=config-interaction-wrapup-codes&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
-   [Enable interaction wrap up codes](https://www.servicenow.com/docs/access?context=enable-interaction-wrapup-codes&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

## Wrap-up timer

The interaction wrap up timer displays a countdown of the wrap-up period. The wrap-up timer starts when the wrap up period begins.

Agents can complete their work within the wrap-up period and submit the wrap-up data. If agents do not complete their work, the system automatically ends the wrap-up period and saves the wrap-up data with the default code and notes field blank.

Depending on the settings in the Interaction Wrap Up Configuration record, the wrap-up timer appears on an interaction record in one of two locations:

-   In the wrap-up modeless dialog: The timer is displayed in the modeless dialog if wrap-up codes are enabled.
-   In the interaction record header secondary values. The timer is displayed in the secondary values if wrap-up codes are not enabled.

The system administrator can configure the display of the wrap-up timer by enabling the **Show duration to agent** field on the Interaction Wrap Up Configuration record.

The timer counts down the amount of time specified in the **Duration in seconds** field. The background color of the wrap-up timer changes as it counts down the duration.

|Background color|Description|
|----------------|-----------|
|Green|Time remaining is between 100% to 50% of duration.|
|Yellow|Time remaining is between 50% and 25% of duration.|
|Orange|Time remaining is between 25% and 0% of duration.|
|Red|When the timer reaches 0.00, the display turns red and then disappears. The system updates the state of the interaction record to Closed Complete.|

## Wrap-up notes

Agents can provide additional information about the interaction resolution in the wrap-up notes. After selecting a code in the wrap-up modeless dialog, agents can add this information in the **Notes** field.

## Wrap-up modeless dialog

When wrap-up codes are enabled in the Interaction Wrap Up Configuration record, the system displays the wrap-up modeless dialog during the wrap-up period.

The wrap-up modeless dialog includes the following fields:

-   Wrap up timer \(when configured\)
-   Wrap up code
-   Notes

The agent can select a code and add wrap-up notes and then select **Submit &amp; close** to complete the interaction. The wrap-up data is saved in a segment record and the state of the interaction changes to Closed Complete.

If the wrap-up time expires before the agent selects **Submit &amp; close**, the system closes the modeless dialog and saves the wrap-up data with the default code and no notes.

Agent actions that impact the wrap-up modeless dialog:

<table id="table_orw_b5l_rdc"><thead><tr><th>

Action

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Initiating an outbound conversation during the wrap-up period

</td><td>

The system ends the countdown and closes the modeless dialog.

</td></tr><tr><td>

Changing the agent status during the wrap-up period

</td><td>

The system ends the countdown and closes the modeless dialog.

</td></tr><tr><td>

Logging out during the wrap-up period

</td><td>

If an agent logs out during the wrap-up period without selecting **Submit &amp; close**, the wrap-up time continues. If the agent does not log back in, the system closes the wrap-up.

</td></tr><tr><td>

Closing the interaction while in wrap up mode

</td><td>

The system displays a warning message. If the agent still wants to close the interaction, the system submits the wrap-up using the default wrap-up code.

</td></tr><tr><td>

Transferring a call to another agent

</td><td>

Each agent’s wrap-up period begins the moment they exit the call. This behavior applies to both warm and cold transfers.When a call is transferred from one agent to another, each agent’s wrap-up period begins the moment they exit the call.

</td></tr><tr><td>

Cancelling an inbound or outbound call

</td><td>

When a caller cancels an inbound call that hasn’t been connected to an agent or agent cancels an outbound call, wrap-up is not initiated.

</td></tr></tbody>
</table>## Wrap-up segments

The system stores interaction wrap-up data in wrap-up segments. Storing the data in segments enables multiple wrap-ups per interaction. For example, when one agent transfers an interaction to another agent, each agent can complete a wrap-up for the same interaction record.

Interaction wrap-up segment records are stored in the Interaction Wrap Up Segment table \[interaction\_wrap\_up\_segment\]. Customer and consumer agents have read access to this table.

## My Wrap Ups list

The My Wrap Ups list displays a list of all wrap-up records for the current user. To access this list in the Lists tab, navigate to **Interactions** &gt; **My Wrap Ups**. This list view includes a link to the interaction record, the wrap-up state \(In progress or Complete, and the wrap-up code and notes.

The following roles have access to the My Wrap Ups list:

-   Customer service agent \(sn\_customerservice\_agent\)
-   Consumer service agent \(sn\_customerservice.consumer\_agent\)
-   System administrator \(admin\)

## Wrap up controller

There are two different controllers for interaction wrap up:

-   Interaction UI controller: Original controller; includes legacy wrap-up functionality.
-   Wrap up controller: New controller introduced in Yokohama; includes wrap-up codes and the wrap-up modeless dialog.

The Wrap up controller includes output properties that determine where the wrap-up timer is displayed: in the modeless dialog or in the interaction header secondary values. The Wrap up controller also controls how the timer is updated.

The CSM Interaction record page and the CSM voice interaction record page include an input property that determines the wrap-up functionality: **disableLegacyWrapUpLogic**.

-   If set to false: the wrap-up functionality remains the same. For upgrade customers, this prevents conflicts with the current or custom wrap-up functionality. The default value of this property is false.
-   If set to true: the interaction record page uses the new wrap-up functionality.

To edit this property:

1.  In UI Builder, select the CSM/FSM Configurable Workspace experience.
2.  Select the CSM Interaction record page.
3.  In the Data and scripts section on the left side, select CSM Interaction Record to open the Edit CSM Interaction Record modal.
4.  In the Configure tab of the modal, enable or disable the **disableLegacyWrapUpLogic** property.

## Interaction record pages

The wrap-up controller, wrap-up codes, and wrap-up modeless dialog are available on the following record pages in CSM Configurable Workspace:

-   CSM Interaction record page
-   CSM Voice interaction record page

