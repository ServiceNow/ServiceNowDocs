---
title: Verify and test
description: Verify and test all configuration details to ensure that the flow is generated correctly.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring data import, Create an automation source, Working with Connection Manager, Use, Automation Center, Workflow Data Fabric]
---

# Verify and test

Verify and test all configuration details to ensure that the flow is generated correctly.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

Proceed from the **Configure batch import for data** section. For information on configuring batch import for data, see [Configure batch import for data](config-batch-import.md).

## Procedure

1.  Review all the details that you have configured for data import, such as scheduling data import, selecting a spoke, selecting an action, and configuring batch import.

    -   If you want to change the data import schedule, then from the **Schedule import** section, you must open the flow and make changes in the flow.
    -   If you make any changes to the selected spoke or action, you must redo the subsequent tasks.
2.  Select **Test connection**.

    If any updates are required for the connection to be valid, you will be guided to do it. If there are any errors in the connection, you can view the log file, fix the issues, and run the test again.

3.  Select **Save and continue**.

    The **Align fields** section is displayed.


**Parent Topic:**[Configuring data import](../concept/configure-data-import.md)

