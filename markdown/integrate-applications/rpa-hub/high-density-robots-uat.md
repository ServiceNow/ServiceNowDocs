---
title: High density robots in Unattended Robot
description: Execute multiple automations simultaneously and independently on a single Windows Server machine using high density robots.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Unattended Robot, Unattended Robot, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# High density robots in Unattended Robot

Execute multiple automations simultaneously and independently on a single Windows Server machine using high density robots.

Familiarize yourself with high density robots concepts in RPA Hub. For more information, see [High density robots in RPA Hub](../../rpa-hub/concept/high-density-robots-rpa-hub.md).

## How a high density robot works

-   The robot can start one automation for each Windows user session at any given time. You can run the same automation on all robots simultaneously. You can also run different automations on all robots at the same time.
-   In a scenario, where, a user A is connected to a server via Remote Desktop Protocol \(RDP\) where a high density robot is connected. If an execution is triggered for the same user A, the manually connected session is disconnected and transferred to the robot. However, the user can reconnect to view the execution after the robot starts its automation.
-   When changing the robot type from High Density Robot to standard or vice-versa, you must reconnect the unattended robot to ensure seamless execution of automations. For more information about creating an unattended robot, see [Create an unattended robot in RPA Hub](../../rpa-hub/task/create-unattended-robot.md).

## List of steps for configuring high density robots

Perform the following tasks to configure high density robots:

1.  Set up the environment for high density robots on a Windows Server machine by installing a Remote Desktop Session Host. Then, add users who can establish RDP connection to the Windows Server machine. For more information, see [Set up Windows Server machine for high density robots](../task/setup-windows-server-hdr.md).
2.  Restart the Windows Server machine after the installation is complete.
3.  Enable the high density robot option in RPA Hub. For more information, see [Create an unattended robot in RPA Hub](../../rpa-hub/task/create-unattended-robot.md).
4.  [Install Unattended Robot](../task/install-rpa-runtime.md).
5.  Add user profiles in the Unattended Robot application, so that multiple robots can execute jobs concurrently. For more information, see [Set up Unattended Robot](../task/set-up-rpa-runtime.md).

## Troubleshooting

-   RDP logon errors are recorded in the service logs. Although some logs may lack detailed explanations, utilize the code to search for relevant information in [Disconnect reason code](https://learn.microsoft.com/en-us/windows/win32/termserv/imstscaxevents-ondisconnected) and [Extended disconnect reason code](https://learn.microsoft.com/en-us/windows/win32/termserv/extendeddisconnectreasoncode).
-   The underlying application process names used in automations may vary between the server environment and the development environment. To avoid discrepancies, ensure they are correctly specified in the automations based on the target machine.

## Limitations

-   The Unattended Robot user interface is accessible by only one user at a time.
-   The latest version of the Unattended Robot must be installed after upgrading the RPA Hub to the newest version.
-   High density robots are not a part of robot pool.

