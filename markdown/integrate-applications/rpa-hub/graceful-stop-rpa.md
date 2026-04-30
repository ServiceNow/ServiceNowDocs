---
title: Using Graceful Stop functionality in RPA Hub
description: Graceful Stop functionality provides a capability for robots to exit the automation smoothly. You can define a secure termination point within an automation process. It also enables you to perform clean-up tasks such as closing in-use applications. It is applicable for assigned robots as well as robots in a robot pool.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Using Graceful Stop functionality in RPA Hub

Graceful Stop functionality provides a capability for robots to exit the automation smoothly. You can define a secure termination point within an automation process. It also enables you to perform clean-up tasks such as closing in-use applications.It is applicable for assigned robots as well as robots in a robot pool.

## Challenges prior to Graceful Stop functionality

-   Prior to Graceful Stop, when you select the **Stop Process** button on a bot process, the robots exit the automation abruptly leading to data inconsistency and data inefficiencies.
-   RPA developers cannot perform the house-keeping activities.

## Benefits of Graceful Stop functionality

-   Data sanity is maintained as the robot completes the existing transaction items.
-   RPA developers can perform the house-keeping activities, such as, closing the downstream application.

## How Graceful Stop works

Let's consider a shipping order use case that contains 10 order detail records in a spreadsheet. These order details are populated into a downstream application, for example, Shipping Management application.

RPA developer builds an automation for this use case in the RPA Desktop Design Studio. Since the spreadsheet has 10 records, queues are used in the automation to synchronise the data to be populated into the Shipping Management application.

Each robot picks the work item, performs the logic, and pushes the data into the Shipping Management application.

If the bot process is stopped by selecting **Stop Process** for all or a subset of robots and the **Graceful Stop** is not enabled, then the robots end the automation execution abruptly. For example, if there are 6 columns in the spreadsheet, the robot stops at column C abruptly, without populating the information in columns D, E, and F. The application which is open, might not be closed.

In the RPA Hub, when you enable the **Graceful Stop** toggle switch in **Stop Process** section, the data in all the columns \(D,E,F\) are populated and the downstream application is closed. For more information, see [Stop an unattended bot process in RPA Hub](../task/stop-bot-process.md).

In the RPA Desktop Design Studio, when you use the **GracefulStop** component in your automation logic, it ensures that the automation is completed. For more information, see [Use the GracefulStop component](../../rpa-studio/task/graceful-stop-component.md). It completes the existing work items, populates the data into the downstream application, and helps the developer to perform house-keeping activities such as closing the application.

## New MSI for Unattended Robot

For the graceful stop functionality to be applicable on robots in a robot pool, upgrade to the latest Washington DC release specific Unattended Robot MSI. For more information, see [Download the RPA applications from RPA Hub](../task/download-installer-rpa.md).

If the latest MSI is not installed and if the robot pool is enabled for a particular bot process, then the execution is stopped for all the robots of the robot pool. For these bot processes, you can't use a graceful stop for robots in a robot pool.

