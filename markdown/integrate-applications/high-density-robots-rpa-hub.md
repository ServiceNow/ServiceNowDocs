---
title: High density robots in RPA Hub
description: Execute multiple automations \(bot processes\) simultaneously and independently on a single Windows Server machine using high density robots.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Robots, Use, RPA Hub, Workflow Data Fabric]
---

# High density robots in RPA Hub

Execute multiple automations \(bot processes\) simultaneously and independently on a single Windows Server machine using high density robots.

## High density robots overview

High density robots leverage the Remote Desktop Services to execute multiple automations simultaneously on the same Windows Server machine. High density robots can run the same automation or run different automations in separate user sessions on the same machine. The machine must support multiple user sessions at the same time. This setup maximizes resource utilization by leveraging the machine's capacity to execute several bot processes in parallel.

While configuring unattended robot, you can select the **High Density Robot** option to create multiple robots with the same machine name. All the high density robots with the same machine name can have different screen resolutions. But it is ideal for all high density robots associated to the same bot process to have same screen resolution value. For more information about these fields, see [Create an unattended robot in RPA Hub](../task/create-unattended-robot.md).

**Note:**

The machine that is associated with high density robots can't be associated with a non-high density robot. If there are multiple robots with the same machine name marked as high density robots, then none of the robot can be converted as a non-high density robot.

High density robots can't be added to the robot pool.

## High density robots key features

-   Runs multiple automations independently on the same machine.
-   Reduces the number of machines required, lowering infrastructure costs.
-   Enables each robot to operate in its isolated session, which helps preventing overlap or interference.

## Configuring high density robots

To configure the high density robots, see [Create an unattended robot in RPA Hub](../task/create-unattended-robot.md).

To convert existing unattended robots to high density robots, see [Convert existing unattended robots to high density robots in RPA Hub](../task/convert-robot-hdr.md).

**Related topics**  


[High density robots in Unattended Robot](../../rpa-runtime/concept/high-density-robots-uat.md)

[Set up Windows Server machine for high density robots](../../rpa-runtime/task/setup-windows-server-hdr.md)

[Set up Unattended Robot](../../rpa-runtime/task/set-up-rpa-runtime.md)

