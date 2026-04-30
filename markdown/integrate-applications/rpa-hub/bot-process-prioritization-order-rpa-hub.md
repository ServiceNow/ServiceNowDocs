---
title: Execution priority of bot processes in RPA Hub
description: Learn how to prioritize bot processes efficiently and avoid triggering multiple automations on the same robot. The bot processes are organized by both robots and Windows user credentials.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Execution priority of bot processes in RPA Hub

Learn how to prioritize bot processes efficiently and avoid triggering multiple automations on the same robot. The bot processes are organized by both robots and Windows user credentials.

## Scheduled trigger

When multiple bot processes are scheduled to run at the same time, consider the following scenarios to understand how bot process execution is prioritized based on order number and Windows credentials.

![Diagram shows how a bot process execution is prioritized when different robots use different login credentials.](../image/scenario1-bp-order.png "Scenario 1: Robots with different Windows credentials")

The following bot processes use robots 1 and 2 with different priority orders and the robots use different credentials to login to a Windows machine.

-   Bot process 1
    -   Robot: Robot 1
    -   Order: 2
    -   Windows credential: SN\\User 1
-   Bot process 2
    -   Robot: Robot 1
    -   Order: 3
    -   Windows credential: SN\\User 2
-   Bot process 3
    -   Robot: Robot 2
    -   Order: 4
    -   Windows credential: SN\\User 3
-   Bot process 4
    -   Robot: Robot 2
    -   Order: 1
    -   Windows credential: SN\\User 4

When all bot processes are scheduled to start simultaneously, execution is determined based on the following logic:

1.  Bot processes are grouped by the robot.
2.  Within each group, the bot process with the lowest priority number is executed.

Execution results:

-   Robot 1: Bot Process 1 \(priority 2\) executes; Bot Process 2 \(priority 3\) is skipped.
-   Robot 2: Bot Process 4 \(priority 1\) executes; Bot Process 3 \(priority 4\) is skipped.

![Diagram shows how a bot process execution is prioritized when different robots use same login credentials.](../image/scenario2-bp-order.png "Scenario 2: Robots with the same Windows credential")

The following bot processes use high-density robots 1 and 2 with different priority orders and use same credentials to login to a Windows machine.

-   Bot process 1
    -   Robot: Robot 1
    -   Order: 2
    -   Windows credential: SN\\User 1
-   Bot process 2
    -   Robot: Robot 1
    -   Order: 3
    -   Windows credential: SN\\User 1
-   Bot process 3
    -   Robot: Robot 2
    -   Order: 4
    -   Windows credential: SN\\User 1
-   Bot process 4
    -   Robot: Robot 2
    -   Order: 1
    -   Windows credential: SN\\User 1

When all bot processes are scheduled to start simultaneously, priority is determined based on the following logic:

1.  Bot processes are first grouped by the robot.
2.  Within each group, the bot process with the lowest priority number is selected.

Intermediate priority results:

-   Robot 1: Bot Process 1 \(priority 2\) is selected over Bot Process 2 \(priority 3\).
-   Robot 2: Bot Process 4 \(priority 1\) is selected over Bot Process 3 \(priority 4\).

However, Bot Process 1 and Bot Process 4 cannot be launched in the same Windows session simultaneously due to shared credentials \(SN\\User1\). To resolve this conflict, bot processes are grouped by Windows credentials, and the process with the lowest priority number is executed:

Final execution results:

-   SN\\User1: Bot Process 4 \(priority 1\) executes.
-   SN\\User1: Bot Process 1 \(priority 2\) is skipped.

## Manual trigger

When a bot process with multiple high-density robots is triggered using the **Start Process** button, consider the following scenarios to understand how bot process execution is prioritized for a robot.

![Diagram shows how a bot process execution is prioritized for different high-density robots.](../image/manual-start-bp-hdr.png "Bot process prioritization for different high-density robots")

-   **Scenario 1: Robots with the same Windows credentials**

    The Bot process 1 uses high-density robots 1 and 2 with the same credentials to login to a Windows machine. When the **Start Process** button is clicked on the Bot process 1 for Robot 1 and Robot 2, any one robot is picked randomly to execute the bot process. The process job with the **Skipped** status is created for the other robot.

-   **Scenario 2: Robots with different Windows credentials**

    The Bot process 1 uses high-density robots 1 and 2 with different credentials to login to a Windows machine. When the **Start Process** button is clicked on the Bot process 1 for Robot 1 and Robot 2, both the robots execute the bot process simultaneously.


