---
title: RPA Hub architecture
description: Learn about the Robotic Process Automation \(RPA\) Hub architecture.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Robotic Process Automation architecture, RPA architecture]
breadcrumb: [Explore, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# RPA Hub architecture

Learn about the Robotic Process Automation \(RPA\) Hub architecture.

The following diagram shows how the ServiceNow instance communicates with the customer environment.

![High-level architecture of the Robotic Process Automation Hub application.](../image/rpa-hub-architecture.png "High-level architecture of the Robotic Process Automation (RPA) Hub application")

Various components make up the architecture of the Robotic Process Automation \(RPA\) Hub application:

-   RPA Desktop Design Studio, Unattended Robot, and Attended Robot are the three applications that you install to form the customer environment.
-   The Unattended Robot Login Agent is a software agent that you install on a Windows machine with Unattended Robot. You can use this application to unlock or to perform a self-login to the robot machine when an unattended bot process is triggered.
-   Unattended robots work independently without any human intervention. They are installed on Windows machines or Virtual Desktop Infrastructures \(VDIs\). For example, to create an unattended robot, you need to mention the machine name on which the robot is installed on. The automation is executed from here.
-   Attended robots work along with humans to improve the efficiency of a bot process. They are installed on user desktops.
-   After the automation is built in the RPA Desktop Design Studio, a developer tests it locally and then publishes it to the ServiceNow® RPA Hub instance for further orchestration.
-   RPA Hub is a scoped application in the ServiceNow instance. It is the command and control center for managing the robots, packages, and bot processes. For more information about these terms, see [Robotic Process Automation \(RPA\) Hub glossary](../../rpa-hub/reference/rpa-hub-glossary.md#).
-   The automation that is uploaded from the RPA Desktop Design Studio resides under the packages section, which also acts as a build repository.
-   You can install the RPA Hub application and the plugins from the ServiceNow Store. The ServiceNow Store checks the Content Delivery Network \(CDN\) for updates. RPA plugins form the building blocks that are used to create an automation. The plugin files are delivered via the CDN application to RPA Desktop Design Studio, Unattended Robot, and Attended Robot. The plugin inventory is maintained inside the RPA plugin.
-   In a bot process record, you define the sequence of actions that a robot follows to accomplish a specific task, along with the schedule. This information is passed to the robots. When the automation is triggered, the automation executes.
-   In the RPA Hub application, additional capabilities, like the queue. A queue is a structured data storage mechanism, used for managing and controlling the distribution of tasks, work items, or cases to different robots for processing.
-   The entire scoped application is safeguarded with access control lists \(ACLs\).

