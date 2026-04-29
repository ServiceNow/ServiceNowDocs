---
title: Requirements for Unattended Robot
description: Ensure that you meet the following hardware and software requirements before you install the Unattended Robot application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Unattended Robot, Workflow Data Fabric]
---

# Requirements for Unattended Robot

Ensure that you meet the following hardware and software requirements before you install the Unattended Robot application.

## Hardware requirements

|Resource|Minimum|Recommended|
|--------|-------|-----------|
|CPU|2 cores of Intel 1.8 GHz 64-bit processor|4 cores of Intel 2.4 GHz 64-bit processor|
|RAM|4-GB RAM|8-GB RAM|
|Disk space|Minimum 50-GB free disk space after installing the OS, patches, and base software|Minimum 100-GB free disk space after installing the OS, patches, and base software|

-   **Hardware requirements for high density robots**

    For a high density robot, where multiple robots execute jobs concurrently on the same Windows Server machine, you must multiply the minimum and recommended hardware requirements by the number of runtimes.

    For example, with three users concurrently executing jobs, the minimum requirements are:

    -   6 cores of Intel 1.8GHz 64-bit \(6 cores of 1.8GHz 64-bit per runtime\)
    -   12 GB of RAM \(4 cores per runtime\)

## Software requirements

-   **Software requirements for standard robots**

    For a standard robot, the software requirements are:

    -   Operating system: Microsoft Windows 10 or Windows 11, Windows Server 2016, Windows Server 2019, Windows Server 2022
    -   NET framework: Windows 4.7.1 or greater.
    -   DPI scaling setting must be deactivated.

-   **Software requirements for high density robots**

    For a high density robot, the software requirements are:

    -   Operating system: Windows Server 2022
    -   NET framework: Windows 4.7.1 or greater.
    -   DPI scaling setting must be deactivated.

