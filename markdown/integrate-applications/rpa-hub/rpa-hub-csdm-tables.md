---
title: RPA Hub and CSDM tables
description: RPA Hub manages and uses CSDM tables. Several ServiceNow products benefit from and add value to RPA Hub.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Applying the CSDM guidelines to RPA Hub, Configuring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# RPA Hub and CSDM tables

RPA Hub manages and uses CSDM tables. Several ServiceNow products benefit from and add value to RPA Hub.

## CSDM tables managed by RPA Hub

1.  Bot Process \[cmdb\_ci\_rpa\_process\]
2.  Robot \[cmdb\_ci\_rpa\_robot\]

The Bot Process table \(cmdb\_ci\_rpa\_process\) contains the configuration details of a process that runs on a robot. This table extends from the Base Bot Process table \(cmdb\_ci\_base\_rpa\_process\). The following image is a visual depiction of the bot process table hierarchy. ![Visual depiction of the bot process table hierarchy.](../image/botprocess-ci-rpa-csdm.png)

The Robot table \(cmdb\_ci\_rpa\_robot\) contains the details of a software agent that runs a bot process \(cmdb\_ci\_rpa\_process\) that is built in the RPA Desktop Design Studio. This table extends from the Base Robot table \(cmdb\_ci\_base\_rpa\_robot table\). The following image is a visual depiction of the robot table hierarchy.

![Visual depiction of the robot table hierarchy.](../image/robot-ci-rpa-csdm.png)

The bot process and the robot are associated with each other using CI relationship ‘Runs On::Runs’.

## CSDM tables used by RPA Hub

1.  Business Application \[cmdb\_ci\_business\_app\] - For associating business applications to bot processes and later, defining the application credentials for the same.

    For more information about assigning a business application to a bot process, see [Assign a business application with a bot process](../../rpa-hub/task/associate-business-apps.md).

2.  Hardware \[cmdb\_ci\_hardware\] - For the machine name lookup feature on a robot record.

    For more information about machine name field, see [Create an unattended robot in RPA Hub](../../rpa-hub/task/create-unattended-robot.md).


## Products that add value to RPA Hub

When you use RPA Hub with any of the following ServiceNow products, you increase the value you get from RPA Hub:

-   Workflow Studio
-   Integration Hub
-   Automation Center
-   Document Intelligence
-   Adoption Services

## Products that benefit from RPA Hub

The following ServiceNow products gain value from RPA Hub:

-   Automation Center
-   Document Intelligence
-   ITSM

