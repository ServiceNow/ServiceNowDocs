---
title: Configure and run an Issue Auto Resolution simulation
description: Use the incident data from your organization to run simulations from the matching intents that the Issue Auto Resolution application based its predictions on from the case descriptions.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Issue Auto Resolution, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Configure and run an Issue Auto Resolution simulation

Use the incident data from your organization to run simulations from the matching intents that the Issue Auto Resolution application based its predictions on from the case descriptions.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

You can run multiple simulations for a Issue Auto Resolution \(IAR\) configuration. You can also do the following tasks:

-   Cancel a simulation: Stop a simulation in progress.
-   Refresh simulation status: Check the status of a simulation in progress.
-   Delete a simulation: Delete a simulation configuration, but not while a simulation is running.

## Procedure

1.  Configure and configure an IAR simulation.

    1.  Navigate to **All** &gt; **Issue Auto Resolution** &gt; **Simulations** &gt; **.**.

    2.  Select **New** or **Create new simulation** if you don't have an existing simulation.

    3.  On the form, fill in the fields.

<table id="table_axz_mgg_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the simulation configuration.

</td></tr><tr><td>

Auto Resolution configuration

</td><td>

Table that contains the records to be simulated. The default configuration is for incidents.

</td></tr><tr><td>

State

</td><td>

Simulation status:-   **Ready**: Simulation is ready to run.
-   **Running**: Simulation is in progress.
-   **Canceled**: Simulation stopped.
-   **Complete**: Simulation finished.
-   **Error**: Simulation encountered a processing error, but continues the simulation for the next set of records.


</td></tr><tr><td>

Record set

</td><td>

Condition that identifies the records evaluated in the simulation. For example: **\[Active\] \[is\] \[true\]**. This condition is automatically filled in with the conditions that you specify in your incident configuration, but you can modify the conditions as needed.**Note:** Record sets that return a large number of records can take longer to simulate. To reduce the simulation time, consider changing the record set to return a smaller number of records. 50,000 is the maximum record limit for each simulation run.

</td></tr></tbody>
</table>    4.  Select **Save**.

2.  After the new simulation is created, select **Run**.

    The simulation may take a bit more time depending on the number of records that you have. After a run is completed, you see the **Latest resolution potential** and other simulation results.

3.  To specify a time and schedule to run the simulation instead of manually running one, select **Enable scheduled job**.

    You can run the simulation on a daily, weekly, or monthly basis at a specific time, in hours, minutes, and seconds. After you set up the schedule, select **Save**. To cancel your scheduled job, disable **Automatically run this simulation**. For each simulation run, the following information is displayed:

<table id="table_tqx_y2h_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start time

</td><td>

Date and time that the simulation started.

</td></tr><tr><td>

Completed time

</td><td>

Date and time that the simulation ended.

</td></tr><tr><td>

Progress

</td><td>

Percentage of the simulation performed.

</td></tr><tr><td>

Latest trained version

</td><td>

Version number of the machine learning model used for the simulation.

</td></tr><tr><td>

State

</td><td>

Status of the simulation: -   Complete: Simulation completed its run.
-   Ready: Simulation is ready to run.
-   Running: Simulation is in progress.

-   Canceled: Simulation stopped.
-   Complete: Simulation finished.
-   Error: Simulation encountered an error.


</td></tr><tr><td>

Total records

</td><td>

Total number of records evaluated in the simulation.

</td></tr><tr><td>

Resolution rate \(%\)

</td><td>

Percentage of cases that the simulation has predicted that match active intents with active topics.

</td></tr></tbody>
</table>4.  View the simulation details of the individual run by selecting the link within **Runs** **&gt; Start time**.

    |Field|Description|
    |-----|-----------|
    |Resolution potential|Percentage of incidents that have active intents and are mapped to active topics.|
    |Inactive topics|Virtual Agent topics currently mapped to intents that aren’t active and not visible to users. Select an active topic by using the intent to topic map table in the IAR configuration, or go to Virtual Agent Designer to activate the topic.|
    |Mapped intents: Active|Intent that was successfully predicted from the case description and is active in your intent to topic map table.|
    |Mapped intents: Inactive|Predicted intents that are available but not active in your intent to topic map table.|
    |No intents found|Description in the records didn’t match any of the intents available.|
    |Unmapped intents|Intent that was successfully predicted from the case description, but the intent itself hasn’t been added to the intent to topic map table in the configuration. To increase the coverage for those incidents, add those additional intents to the table.|


**Parent Topic:**[Using Issue Auto Resolution](../concept/auto-resolution-va.md)

