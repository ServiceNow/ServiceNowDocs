---
title: Using RPA Hub
description: Developers, support users, release managers, and administrators can use the RPA Hub application to start and stop a bot process, launch a bot process in the RPA Desktop Design Studio, execute skills, view the HashCode of a package version, and retire a bot process, package, and a robot.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [RPA Hub, Workflow Data Fabric]
---

# Using RPA Hub

Developers, support users, release managers, and administrators can use the RPA Hub application to start and stop a bot process, launch a bot process in the RPA Desktop Design Studio, execute skills, view the HashCode of a package version, and retire a bot process, package, and a robot.

-   **[Configuring a bot process record in RPA Hub](create-botprocess.md)**  
In RPA Hub, you can create a bot process configuration record and assign assets to associate it with a bot process. Or you can just save the bot process configuration record, however it won't be associated to a bot process. It remains orphaned.
-   **[Package and package version in RPA Hub](package-version-rpa-hub.md)**  
A package is a container that groups together one or more automation logic and their related files, configurations, and dependencies. A package version is a specific release of a package.
-   **[Credential Management in RPA Hub](credential-management-rpa-hub.md)**  
Streamline the credentials that robots use to perform the automation that you defined in the bot process. Instead of creating the same set of credentials for each bot process, you can create a credential group that includes a robot credential, application credentials, and external credentials. You can then associate the credential group to multiple bot processes.
-   **[Shared parameters in RPA Hub](shared-paramaters-rpa-hub.md)**  
Shared parameters enable you to store the global variables or configurable items in one place. These variables are used across bot processes.
-   **[Queue implementation in RPA Hub](queues-implement-rpa.md)**  
In RPA Hub, the queues are implemented to distribute the workload among various robots. Work Items \(WI\) within a queue are processed simultaneously by two or more robots.
-   **[Embedded Task Automation \(ETA\) in RPA Hub](embedded-task-auto-rpa.md)**  
With the embedded task automation feature, trigger attended bot processes \(attended automations\) from the ServiceNow forms, apart from initiating them from the Attended Robot application.
-   **[Robot pool in RPA Hub](robot-pool-rpa.md)**  
Create a robot pool in RPA Hub to distribute and manage the workload among multiple unattended robots for unattended bot processes.
-   **[Alert rule and variable in RPA Hub](alert-rule-rpa-hub.md)**  
A rule that defines when and how the system should notify users about issues in automation execution.
-   **[Work items in RPA Hub](work-items-rpa-hub.md)**  
A work item is a record in a work queue that stores the data a robot needs to perform a specific task.
-   **[Code quality check in RPA Hub](code-quality-check-rpa.md)**  
A code quality check refers to the process of evaluating the automation file or script to assess its adherence to coding standards, best practices, maintainability, and overall quality.
-   **[Using the robot calendar for RPA Hub](robot-calendar-rpa.md)**  
You can use the robot calendar in RPA Hub to view and create the schedule for the unattended robots. It’s a simple, efficient, and interactive way to work with robots and schedules. By using the calendar, you can manage and plan a robot's schedule in a single view.
-   **[Scheduled maintenance days in RPA Hub](sm-days-rpa.md)**  
Track the scheduled maintenance \(SM\) days on the robot calendar so that the bot processes can function optimally. If an issue occurs, you can take preventive measures. For example, you can know in advance about the days when the robot or the bot process is unavailable so that you can avoid the number of skipped process jobs.
-   **[Using Graceful Stop functionality in RPA Hub](graceful-stop-rpa.md)**  
Graceful Stop functionality provides a capability for robots to exit the automation smoothly. You can define a secure termination point within an automation process. It also enables you to perform clean-up tasks such as closing in-use applications. It is applicable for assigned robots as well as robots in a robot pool.
-   **[Workflow Studio actions and subflow in RPA Hub](../reference/rpa-hub-actions.md)**  
Two-way integration of actions and subflows in Workflow Studio and RPA Hub for a seamless robot execution.

**Parent Topic:**[Workflow Data Fabric](../../../build/create-integrations-apps/concept/create-integrations-applications.md)

