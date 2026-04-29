---
title: RPA Hub features
description: Learn about the various RPA Hub features and capabilities.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Explore, RPA Hub, Workflow Data Fabric]
---

# RPA Hub features

Learn about the various RPA Hub features and capabilities.

## Bot process

-   **Bot process**

    A bot process is a predefined sequence of actions that a robot follows to accomplish a specific task or achieve a particular goal.

-   **Bot process configuration**

    A bot process configuration is a record that contains the bot process settings. The bot process configuration record is mapped to a bot process record. It is a one to one mapping.


For more information, see [Bot process](create-botprocess.md).

## Robots

A robot runs a bot process \(automation\). Robots are designed to interact with software applications, data sources, and user interfaces like a human operator would, but in a more efficient, accurate, and consistent manner.

There are two types of robots:

-   Unattended robots: robots that run unattended automations that don’t require any human intervention.
-   Attended robots: robots that run attended automations that require human intervention.

For more information, see [Robots](robots-rpa-hub.md).

## Package and package version

A package is a container that groups together one or more automation logic and their related files, configurations, and dependencies.

A package version is a specific release of a package. After a package is created, the RPA developer publishes an automation from RPA Desktop Design Studio. This process results in a new package version.

For more information, see [Package and package version](package-version-rpa-hub.md).

## Credential management

Streamline the credentials that robots use to perform the automation that you define in the bot process. Instead of creating the same set of credentials for each bot process, you can create a credential group that includes a robot credential, application credentials, and external credentials. You can then associate the credential group to multiple bot processes.

For more information, see [Credential management](credential-management-rpa-hub.md).

## Smart card

Smart card login for a Windows machine is a secure method of logging into the system using a physical smart card instead of a username and password. It’s commonly used in organizations to enhance security, particularly in environments with high security requirements.

For more information, see [Smart card](smart-card-il.md).

## Embedded Task Automation \(ETA\)

With the embedded task automation feature, trigger attended bot processes \(attended automations\) from the ServiceNow forms, apart from initiating them from the Attended Robot application.

For more information, see [Embedded Task Automation](embedded-task-auto-rpa.md).

## Robot pool

Create a robot pool in RPA Hub to distribute and manage the workload among multiple unattended robots for unattended bot processes.

For more information, see [Robot pool](robot-pool-rpa.md).

## Robot calendar

You can use the robot calendar in RPA Hub to view and create the schedule for the unattended robots. It’s a simple, efficient, and interactive way to work with robots and schedules. By using the calendar, you can manage and plan a robot's schedule in a single view.

For more information, see [Robot calendar](robot-calendar-rpa.md).

## Scheduled maintenance days

Track the scheduled maintenance \(SM\) days on the robot calendar so that the bot processes can function optimally. If an issue occurs, you can take preventive measures. For example, you can know in advance about the days when the robot or the bot process is unavailable so that you can avoid the number of skipped process jobs.

For more information, see [Scheduled maintenance days](sm-days-rpa.md).

## Graceful stop

Graceful Stop functionality provides a capability for robots to exit the automation smoothly. You can define a secure termination point within an automation process. It also enables you to perform clean-up tasks such as closing in-use applications. It is applicable for assigned robots as well as robots in a robot pool.

For more information, see [Graceful stop functionality](graceful-stop-rpa.md).

## Queues

The queues are implemented to distribute the workload among various robots. Work Items \(WI\) within a queue are processed simultaneously by two or more robots. A queue is a repository that can hold a number of work items. Work items can store multiple types of data, such as transaction information, customer details, or information from a document.

For more information, see [Queues implementation](queues-implement-rpa.md).

## Work items

A work item is a record in a work queue that stores the data a robot needs to perform a specific task. Each item in the queue is processed separately, allowing robots to handle large workloads in smaller, manageable parts.

For more information, see [Work items](work-items-rpa-hub.md).

## Shared parameters

Shared parameters enable you to store the global variables or configurable items in one place. These variables are used across bot processes.

For more information, see [Shared parameters](shared-paramaters-rpa-hub.md).

## Process parameters

Process parameters store the variables that are used within a bot process. The process parameter can only be used by the bot process they are created in.

For more information, see [Process parameters within a bot process](../task/create-process-parameter-botprocess.md#).

## Code quality checks

A code quality check refers to the process of evaluating the automation file or script to assess its adherence to coding standards, best practices, maintainability, and overall quality. Code quality checks are essential in RPA development life cycle, to ensure that the automation file is robust, efficient, and free from common issues that could lead to errors or difficulties in the future.

For more information, see [Code quality checks](code-quality-check-rpa.md).

## Alert rule and variable

Alert rules are configurations that define conditions in which an alert or a notification must be triggered. These rules help in managing and responding to issues identified in automations.

Alert variable refers to a variable or parameter associated with alerts in RPA Hub.

For more information, see [Alert rule and variable](alert-rule-rpa-hub.md).

## Process jobs

A process job represents the execution of a bot process on a robot.

For more information, see [View process jobs](../task/view-process-jobs-botprocess.md#).

## Automation logs

Automation logs are series of succession stages or a series of checkpoints that occur during the execution of a bot process. It enables monitoring and auditing the automation process. These logs are generated from the robot for unattended and attended bot processes.

For more information, see [View automation logs](../task/view-automation-logs-rpa.md#).

