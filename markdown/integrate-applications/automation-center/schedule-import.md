---
title: Schedule data import
description: Schedule the frequency for the data import to ensure that the automation data is updated as required.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring data import, Create an automation source, Working with Connection manager, Use, Automation Center, Workflow Data Fabric]
---

# Schedule data import

Schedule the frequency for the data import to ensure that the automation data is updated as required.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

Proceed from the **Define source** tab. For information on defining source, see [Define source for automation](define-source.md).

## Procedure

1.  Provide the details on the form.

    -   **Daily**: Schedules the data import daily.

        Enter a time when the data must be imported daily.

        You can provide the time in 12-hour format or 24-hour format.

    -   **Weekly**: Schedules the data import weekly.
        1.  Select a day of the week when the data must be imported from the **Select Day** list.
        2.  Enter a time when the data must be imported.

            You can provide the time in 12-hour format or 24-hour format.

    -   **Monthly**: Schedules the data import monthly.
        1.  Select a specific date of the month when the data must be imported from the **Select Date** list.
        2.  Enter a time when the data must be imported daily.

            You can provide the time in 12-hour format or 24-hour format.

    -   **Run once**: Schedules the data import only once.

        Select the calendar icon on the Select Date field, and select a specific date and time when the data must be imported.

    -   **Repeat**: Schedules the data import at a custom frequency.

        Select a custom frequency for your data import. Use this option if you want to import data in a frequency that does not match to any other frequency provided here, such as weekly, monthly, and so on. For example, you could set the frequency to bi-weekly or once in three months.

        1.  Provide a value in the **Days** field.

            If you provide 20, the data import will happen once every 20 days.

        2.  Enter a time when the data must be imported.

            You can provide the time in 12-hour format or 24-hour format.

2.  Select **Save and continue**.

    The **Select spoke** section is displayed.


**Parent Topic:**[Configuring data import](../concept/configure-data-import.md)

