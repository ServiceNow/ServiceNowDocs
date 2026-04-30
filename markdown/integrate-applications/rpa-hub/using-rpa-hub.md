---
title: Using RPA Hub
description: Developers, release managers, and administrators can use the RPA Hub application to configure a bot process and associate a package, robots, business applications, credentials, and process parameters for configuring automations.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Using RPA Hub

Developers, release managers, and administrators can use the RPA Hub application to configure a bot process and associate a package, robots, business applications, credentials, and process parameters for configuring automations.

Perform the following tasks for configuring automations using the RPA Hub application.

1.  [Download the RPA applications from RPA Hub](../task/download-installer-rpa.md).

    Download and install the Robotic Process Automation \(RPA\) applications in your Windows machine from RPA Hub.

2.  [Add the ServiceNow RPA Chrome extension](../task/add-google-chrome-extension-rpa.md).

    Add the ServiceNow RPA Chrome extension to your Chrome browser to establish an interaction with the applications that are opened in this browser.

3.  [Create a package to assign to a bot process](../task/create-package.md).

    Create an unattended or attended package that contains automation logic and is assigned to a bot process to execute an automation.

4.  [Create a robot in RPA Hub.](create-robot.md)

    Create an attended or an unattended robot to run the attended or unattended bot process respectively.

5.  [Configure a bot process record.](create-botprocess.md)

    Configure a bot process by creating a bot process configuration record and assigning assets. A bot process is a predefined sequence of actions that a robot follows to accomplish a specific task or achieve a particular goal.

    For configuring unattended bot process, perform the following tasks:

    1.  [Configure credentials in RPA Hub](configuring-credentials-rpahub.md).

        Create an application credential for a robot to log in to an application and a robot credential to log in to a system to execute an automation. Create Time-based One-time Password \(TOTP\) seeds for unattended robots to seamlessly authenticate against multi-factor authentication \(MFA\)-enabled applications.

    2.  [Assign a business application to a bot process in RPA Hub](../task/associate-business-apps.md).

        Assign a business application to a bot process for an effective event correlation or to get information about assigned business applications.

    3.  [Associate a credential group to a bot process in RPA Hub](../task/map-credential-groups-to-bot-process.md).

        Map a credential group to an unattended bot process to enable a robot to log in to a system and applications to perform an automation.

    4.  [Assign a robot to a bot process in RPA Hub](../task/assign-robots.md).

        Assign a robot to an unattended bot process to execute the automation \(package\) that is mapped to it.

    5.  [Assign a process robot credential within a bot process in RPA Hub](../task/assign-process-robot-cred-botprocess.md).

        Assign a process robot credential within an unattended bot process so that the selected robot can perform the automation in the Windows machine.

    6.  \(Optional\) [Create a robot pool in RPA Hub](../task/create-robot-pool.md).

        Create a robot pool for an optimum utilization of robots to execute the bot processes.

    7.  \(Optional\) [Create a process parameter within a bot process in RPA Hub](../task/create-process-parameter-botprocess.md).

        Create a process parameter to store the variables that are used within a bot process. The process parameter that you just created can only be used by this bot process.

    For configuring attended bot process, perform the following tasks:

    1.  [Assign a business application to a bot process in RPA Hub](../task/associate-business-apps.md).

        Assign a business application to a bot process for an effective event correlation or to get information about assigned business applications.

    2.  [Assign an attended user or group to an attended bot process](../task/assign-rda-users-botprocess.md).

        Assign an attended user or group to an attended bot process, so that your user or group can access and execute this automation on Windows machines.

    3.  \(Optional\) [Create an attended configuration record in RPA Hub](../task/create-attended-config-rpa.md).

        Create an attended configuration record to trigger an attended bot process that is enabled with embedded task automation.

6.  \(Optional\) [Create a shared parameter in RPA Hub](../task/create-shared-parameter.md).

    Create a shared parameter so that you can store the global variables or configurable items in one place and use them across bot processes.

7.  \(Optional\) [Create a queue in RPA Hub](../task/create-queue.md).

    Create a queue to manage the work items that you want the robot to process.

8.  [Publish a bot process in RPA Hub](../task/publish-bot-process.md).

    After you have configured a bot process and assigned a package and robots to it, you can publish the bot process to execute the automation.


