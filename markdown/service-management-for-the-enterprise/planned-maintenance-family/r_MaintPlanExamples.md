---
title: Maintenance plan examples
description: You can define maintenance plans using model-based, meter-based, or duration-based selection criteria.To schedule a reboot for certain computer models after a specified number of keystrokes, define a model-based plan with a meter-based maintenance schedule. In the example, a field called keystrokes is added to the Computer \[cmdb\_ci\_computer\] table.To schedule a printer ink cartridge replacement after printing a specified number of pages, define a general plan with a meter-based maintenance schedule. In the example, a table called Printer is added with string fields for printer, model, pages, and the like.To schedule an antivirus scan on certain computers after a specified number of days, define a model-based plan with a duration-based maintenance schedule. In the example, a field called trigger type is added to the Computer \[cmdb\_ci\_computer\] table.
locale: en-US
release: australia
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Planned Maintenance, Service Management]
---

# Maintenance plan examples

You can define maintenance plans using model-based, meter-based, or duration-based selection criteria.

-   To schedule a reboot for certain computer models after a specified number of keystrokes, define a model-based plan with a meter-based maintenance schedule.
-   To schedule a printer ink cartridge replacement after printing a specified number of pages, define a general plan with a meter-based maintenance schedule.
-   To schedule an antivirus scan on particular computers after a specified number of days, define a model-based plan with a duration-based maintenance schedule.

**Parent Topic:**[Planned Maintenance](../concept/c_SMPlanMaint.md)

## Define a maintenance schedule for a computer reboot

To schedule a reboot for certain computer models after a specified number of keystrokes, define a model-based plan with a meter-based maintenance schedule. In the example, a field called **keystrokes** is added to the Computer \[cmdb\_ci\_computer\] table.

### Procedure

1.  Navigate to **All** &gt; **Planned Maintenance** &gt; **Maintenance Plans**.

2.  Click **New** and create a maintenance plan called `Reboot Apple Computers` with the following definitions and then click **Submit**.

    -   **Type**: Model-based
    -   **Model**: Click the lock icon and select **Apple iMac 27** and **Apple MacBook Pro 17**.
3.  Navigate to **Planned Maintenance** &gt; **Maintenance Plans** and then click the number of the maintenance plan you just created.

4.  In the **Maintenance Schedules** related list, click **New**, enter the following settings, and then click **Submit**.

    -   **Name**: Reboot Apple Computers
    -   **Short description**: Scheduled reboot for Apple computers
    -   **Repetition**: Meter
    -   **Every**: 500000
    -   **Field**: keystrokes

### Result

The Reboot Apple Computer maintenance plan schedules all Apple iMac 27 and Apple MacBook Pro 17 computers to reboot after 500,000 keystrokes.

## Define a maintenance schedule for an ink cartridge replacement

To schedule a printer ink cartridge replacement after printing a specified number of pages, define a general plan with a meter-based maintenance schedule. In the example, a table called **Printer** is added with string fields for printer, model, pages, and the like.

### Procedure

1.  Navigate to **All** &gt; **Planned Maintenance** &gt; **Maintenance Plans**.

2.  Click **New** and create a maintenance plan called `Epson Laser Cartridge Replacement` with the following definitions and then click **Submit**.

    -   **Type**: `General`
    -   **Table**: `Printer`
    -   **Filter condition**: `Model is Epson`
3.  Navigate to **Planned Maintenance** &gt; **Maintenance Plans** and then click the number of the maintenance plan you just created..

4.  In the **Maintenance Schedules** related list, click **New**, enter the following settings, and then click **Submit**.

    -   **Name**: Epson Laser Cartridge Replacement
    -   **Short description**: Scheduled cartridge replacement for Epson laser printers
    -   **Repetition**: Meter
    -   **Every**: 7500
    -   **Field**: Pages

### Result

The Epson Laser Cartridge Replacement maintenance plan schedules all Epson laser printers to replace ink cartridges after printing 7,500 pages.

## Define a maintenance schedule to run antivirus software

To schedule an antivirus scan on certain computers after a specified number of days, define a model-based plan with a duration-based maintenance schedule. In the example, a field called **trigger type** is added to the Computer `[cmdb_ci_computer]` table.

### Procedure

1.  Navigate to **All** &gt; **Planned Maintenance** &gt; **Maintenance Plans**.

2.  Click **New** and create a maintenance plan called `Update Antivirus` with the following definitions:

    -   **Type**: Model-based
    -   **Model**: Click the lock icon and select **Apple iMac 27** and **Apple MacBook Pro 17**.
3.  Click **Submit**.

4.  Navigate to **Planned Maintenance** &gt; **Maintenance Plans** and then click the number of the maintenance plan you just created.

5.  In the **Maintenance Schedules** related list, click **New**, enter the following settings, and then click **Submit**.

    -   **Name**: Antivirus Update
    -   **Short description**: Scheduled antivirus update for Apple computers
    -   **Repetition**: Duration
    -   **Trigger Type**: Interval
    -   **Days**: 30

### Result

The Update Antivirus maintenance plan schedules all Apple iMac 27 and Apple MacBook Pro 17 computers to run the antivirus software every 30 days.

