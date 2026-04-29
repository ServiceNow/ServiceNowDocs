---
title: Adding details to your bot process in RPA Hub
description: After you create a bot process in RPA Hub, you can add some details for your bot process, such as information about the credential groups, business applications, and more.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [bot process related list rpa hub]
breadcrumb: [Configuring a bot process record, Use, RPA Hub, Workflow Data Fabric]
---

# Adding details to your bot process in RPA Hub

After you create a bot process in RPA Hub, you can add some details for your bot process, such as information about the credential groups, business applications, and more.

You can add the following details that pertain to the bot process:

-   Business applications
-   Process credential mappings
-   Robots or Robot Pool
-   Process robot credentials
-   Schedules
-   Process parameters
-   Attended users or groups
-   Queues
-   Skill overrides

Depending on what you selected for the **Process Type** field on the Bot Process Configuration form, you can add related details to the bot process.

If you can't view the activity stream, configure the system property to display the activity stream. For more information, see [Display an activity stream for bot processes and robots in RPA Hub](../task/display-activity-stream-sys-property-rpahub.md).

For more information, see [Configuring a bot process record in RPA Hub](create-botprocess.md), [Bot process configuration form in RPA Hub](../task/create-botprocess-config.md#), and [Bot Process form in RPA Hub](../task/select-botprocess.md#).

-   **[Assign a business application to a bot process in RPA Hub](../task/associate-business-apps.md)**  
Assign a business application to a bot process for an effective event correlation or to get information about assigned business applications. For example, you might want to see information about the SAP application.
-   **[Associate a credential group to a bot process in RPA Hub](../task/map-credential-groups-to-bot-process.md)**  
Enable a robot to perform an automation in RPA Hub by mapping a credential group to an unattended bot process.
-   **[Assign a robot to a bot process in RPA Hub](../task/assign-robots.md)**  
Assign a robot to an unattended bot process to execute the automation \(package\) that is mapped to it.
-   **[Assign a process robot credential within a bot process in RPA Hub](../task/assign-process-robot-cred-botprocess.md)**  
Assign a process robot credential within an unattended bot process so that the selected robot can perform the automation in the Windows machine.
-   **[Create a schedule within a bot process in RPA Hub](../task/create-schedule-botprocess.md)**  
Create a schedule within an unattended bot process to enable users to execute jobs in a planned manner at regular intervals. More than one schedule can be associated with one bot process.
-   **[Create a process parameter within a bot process in RPA Hub](../task/create-process-parameter-botprocess.md#)**  
Create a process parameter to store the variables that are used within a bot process. The process parameter that you just created can only be used by this bot process.
-   **[Assign an attended user or group to an attended bot process](../task/assign-rda-users-botprocess.md)**  
Assign an attended user or group to an attended bot process in RPA Hub, so that your user or group can access and execute this automation on Windows machines.
-   **[Unassign an attended user or group from an attended bot process in RPA Hub](../task/unassign-rda-users.md)**  
Unassign an attended user or a group from an attended bot process if the user is moving out of the business process.
-   **[Create a process field parameter in RPA Hub](../task/create-process-field-param-rpa.md)**  
Define process field parameters \(dynamic parameters\) that are required in the automation \(bot process\).
-   **[c to the bot process from the related list](../task/associate-queue-botprocess.md)**  
Associate a queue to a bot process in RPA Hub so that the bot process can interact with this queue. You can associate a bot process to multiple queues. If the bot process is enabled for robot pool, then only one queue \(that is not associated with any other bot process\) can be mapped to the current bot process.
-   **[View skill package versions in a bot process](../task/view-skill-package-version-bp.md)**  
View a list of skill package versions used in a bot process in RPA Hub to make sure that you’re using the correct version.
-   **[Override a skill version for a bot process in RPA Hub](../task/override-skill-version-rpahub.md)**  
Override a skill package version in RPA Hub to use a specific version of a skill package for a bot process. When the bot process executes, it uses the selected version instead of the version that you defined in the automation.

**Parent Topic:**[Configuring a bot process record in RPA Hub](create-botprocess.md)

