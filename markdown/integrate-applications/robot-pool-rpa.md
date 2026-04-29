---
title: Robot pool in RPA Hub
description: Create a robot pool in RPA Hub to distribute and manage the workload among multiple unattended robots for unattended bot processes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Use, RPA Hub, Workflow Data Fabric]
---

# Robot pool in RPA Hub

Create a robot pool in RPA Hub to distribute and manage the workload among multiple unattended robots for unattended bot processes.

**Note:**

After you enable the robot pool option for a bot process, you can’t assign robots from the **Assign Robots** tab. It is hidden.

Robot pool feature is applicable for unattended robots only.

## Types of robot assignment

There are two ways to assign robots:

-   Manual robot assignment: After you create a bot process, assign robots from the **Assign Robots** tab. For more information, see [Assign a robot to a bot process in RPA Hub](../task/assign-robots.md).
-   Robot Pool: On the Details tab of the bot process form, enable the robot pool option. For more information, see [Enable robot pool for a bot process in RPA Hub](../task/enable-robot-pool.md).

## Challenges with manual robot assignment

With the manual assignment of robots, RPA release managers need to anticipate the workload for a process and assign the robots accordingly.

If there is a change in the workload on specific days of the week, RPA release managers must reassign robots between different processes.

It can result in over consumption of resources or robots, irrespective of workload.

## Benefits of robot pool

By using the robot pool in RPA Hub, you get the following benefits:

-   Eliminates the need for manual reassignment, since robots are automatically assigned.
-   Allocates robots per bot process based on pending workload and Average Handling Time \(AHT\).
-   Maximizes robot utilization by automatically reallocating available robots in pool.

## Robot assignment process

The following diagram shows an example of assigning robots in RPA Hub.

If the robot pool option is not enabled, robots are assigned to a bot process directly from the **Assigned Robots** tab.

For example, in the Order Management bot process, even if the work items are less, the execution starts on all the robots. The workload is not taken into consideration.

Another example, if the Invoice Queue has a lot of work items. It runs only on two assigned robots, since there is no dynamic allocation of robots.

After the robot pool option is enabled, the execution starts with one robot initially. Based on the configuration of the allocation type \(SLA or percentage reduction\), the robots are automatically allocated depending on the workload.

For example, in robot pool RP1, there are two robots in Available state, R1 and R2. RP1 is used in two bot processes, Invoice Processing and Order Management. The Order Management bot process uses SLA based allocation type. When the **Start Process** button is selected for this bot process, two robots from the assigned robot pool execute the bot process. R1 and R2 are now in Running state.

The Invoice bot process also uses SLA based allocation type and has high priority invoices to be processed. Order Management bot process requires 2 robots to complete all the work items within SLA. To start the execution of invoices that are highest priority, one robot is required for Invoice Processing and one robot for Order Management. So with the help of graceful stop feature, you can stop the Order Management bot process. When you select the **Stop Process** button for the Order Management bot process, enable the **Graceful Stop** toggle switch, and select R1 robot to gracefully exit. Then, R1 gracefully exits the bot process after executing the current order processing.

After R1 gracefully completes Order Management bot process execution, it can be used to start the execution on Invoicing Processing. After all the invoices are processed, R1 can be considered again to execute the Order Processing bot process with the help of a new execution. That is, by triggering the Invoice Processing bot process via the **Start Process** action manually or via a schedule.

For more details about start process action, see [Workflow Studio actions and subflow in RPA Hub](../reference/rpa-hub-actions.md). For more information about graceful stop and stopping a bot process, see [Using Graceful Stop functionality in RPA Hub](graceful-stop-rpa.md) and [Stop an unattended bot process in RPA Hub](../task/stop-bot-process.md).

![Snapshot of assigning robots in RPA Hub.](../image/robot-pool-assignment.png "Robot assignment in RPA Hub")

## New fields on the Bot Process form related to Robot Pool

To enable the robot pool feature for a bot process in RPA Hub, do the following actions:

-   Create a robot pool. For more information, see [Create a robot pool in RPA Hub](../task/create-robot-pool.md).
-   Enable robot pool option for a bot process to map a bot process to the robot pool. For more information, see [Enable robot pool for a bot process in RPA Hub](../task/enable-robot-pool.md).

**Note:** A queue must be associated to a bot process for enabling robot pool. One queue is mapped to one bot process.

You can associate a queue to bot process from the related list. For more information, see [c to the bot process from the related list](../task/associate-queue-botprocess.md).

On the Bot Process form, as an Robotic Process Automation \(RPA\) release manager or an RPA admin, you can configure the following new fields in the Robot Pool section:

-   **Enable Robot Pool**
-   **Robot Pool**
-   **Allocation Type**
-   **Percentage Reduction** \(if you select the **Allocation Type** as **Percentage Reduction**\)

For more information about these fields, see [Bot Process form in RPA Hub](../task/select-botprocess.md#).

## Robots calculation

You can calculate the number of robots required to complete a bot process execution by selecting the **Calculate** button on the Bot Process form.

## New fields on the Queue form related to Robot Pool

On the Queue form, as an RPA release manager or an RPA admin, you can configure the following new fields in the Average Handling Time \(AHT\) - Work Items section:

-   **Include All Work Items**
-   **Work Item Count**

For more information about these fields, see [Queue form in RPA Hub](../reference/queue-form.md). Configure these fields to calculate the number of robots required in robot pool for a successful execution of a bot process.

-   **[Create a robot pool in RPA Hub](../task/create-robot-pool.md)**  
Create a robot pool in RPA Hub for an optimum utilization of robots to execute the bot processes.
-   **[Enable robot pool for a bot process in RPA Hub](../task/enable-robot-pool.md)**  
Enable robot pool for a bot process in RPA Hub to effectively allocate robots for it's execution and for distribution of work load.
-   **[Calculate the number of robots in RPA Hub](../task/calculate-robots.md)**  
Calculate the number of robots that you need to complete an unattended bot process execution that is based on the allocation type, for example, the SLA Based and Percentage Reduction.

**Parent Topic:**[Using RPA Hub](managing-rpa-hub.md)

