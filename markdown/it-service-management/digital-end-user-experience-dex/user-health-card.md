---
title: Device health page
description: The health of a device includes critical device specifics like type, name, OS, model, location, and CPU. Additionally, it includes metrics like device and battery health, events from the last 24 hours, OS details, pending updates, incident, and alert specifics.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Device details pages, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Device health page

The health of a device includes critical device specifics like type, name, OS, model, location, and CPU. Additionally, it includes metrics like device and battery health, events from the last 24 hours, OS details, pending updates, incident, and alert specifics.

## Device health — Overview

Monitoring and managing the following aspects promotes optimal device performance and enables timely resolution of any issues.

<table id="table_gxc_qms_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td class="sub-head" colspan="2">

Device info

</td></tr><tr><td>

Type

</td><td>

Category of the device, such as laptop or desktop computer.

</td></tr><tr><td>

Name

</td><td>

Unique name of the device.

</td></tr><tr><td>

Model ID

</td><td>

Unique identifier assigned to a specific model of a device for internal tracking, system recognition, or management purposes.

</td></tr><tr><td>

Operating system

</td><td>

OS that manages and controls the device hardware and enables the execution of applications, such as Windows or macOS.

</td></tr><tr><td>

OS version

</td><td>

Current operating system version of the device, essential for compatibility, security, and verifying optimal performance.

</td></tr><tr><td>

RAM

</td><td>

RAM capacity of the device.

</td></tr><tr><td>

Location

</td><td>

Physical place where the device is located, indicating its position or network address.**Note:** To identify and determine the number of impacted devices based on the location, define a custom logic. The available options to determine the location of the device are:

-   Consider the device assigned to location or logged-in user location \(`sn_dex.location_determination`\).
-   Consider the default gateway \(router\) IP of the device to determine whether it’s connected from office location or connected remotely \(`sn_dex.remote_location_config`\).

</td></tr><tr><td>

CPU processor ID

</td><td>

Unique identifier assigned to a specific CPU processor.This field appears on Windows machines only.

</td></tr><tr><td class="sub-head" colspan="2">

Computer details

</td></tr><tr><td colspan="2">

This tab appears on Windows machines only.

</td></tr><tr><td>

Computer Asset Details

</td><td>

Name of the device.

</td></tr><tr><td>

Computer Asset Tag

</td><td>

Unique identifier for tracking and asset management

</td></tr><tr><td>

Computer DNS/FQDN

</td><td>

Fully Qualified Domain Name for network identification.

</td></tr><tr><td>

Computer domain

</td><td>

Identifies the network domain to which the computer belongs.

</td></tr><tr><td>

UUID Serial Number

</td><td>

Globally unique ID assigned to the system by the manufacturer for identification.

</td></tr><tr><td>

BIOS Serial Number

</td><td>

Unique identifier assigned to system firmware for tracking and support.

</td></tr><tr><td>

System Serial Number

</td><td>

Unique serial number for the entire system used for warranty and service.

</td></tr><tr><td>

BaseBoard Serial Number

</td><td>

Serial number of the motherboard used for hardware identification.

</td></tr><tr><td>

Chassis Serial Number

</td><td>

Serial number of the system physical case or enclosure.

</td></tr><tr><td class="sub-head" colspan="2">

Memory

</td></tr><tr><td colspan="2">

This tab appears on Windows machines only.

</td></tr><tr><td>

Name

</td><td>

Unique name of the physical memory unit to track the specific modules for troubleshooting or upgrades.For example, Physical Memory 0, Physical Memory 1.

</td></tr><tr><td>

Device locator

</td><td>

Physical location of the memory module.For example, Motherboard.

</td></tr><tr><td>

Capacity\(MB\)

</td><td>

Capacity of each memory module in MBs.

</td></tr><tr><td>

Speed\(MHz\)

</td><td>

Memory module speed in MHz to confirm compatibility with other hardware components and optimize performance.

</td></tr><tr><td>

Form factor

</td><td>

Physical size, shape, and pin layout of a RAM module.For example, Dual In-Line Memory Module \(DIMM\) and Small Outline Dual In-line Memory Module \(SO-DIMM\).

</td></tr><tr><td>

Type

</td><td>

Type of the memory module.For example, DIMMs \(Dual In-line Memory Module\) for desktops and SODIMMs \(Small Outline DIMM\) for laptops.

</td></tr><tr><td>

Type details

</td><td>

Additional details on the memory module type.For example, Synchronous.

</td></tr><tr><td class="sub-head" colspan="2">

CPU

</td></tr><tr><td colspan="2">

This tab appears on Windows machines only.

</td></tr><tr><td>

Name

</td><td>

Unique name of the Computer Processing Unit \(CPU\).

</td></tr><tr><td>

Architecture

</td><td>

Design and organization of the CPU that defines how it interacts with other components to run instructions and process data.For example, x86, x64.

</td></tr><tr><td>

Cores

</td><td>

Number of processing units within the CPU responsible for running instructions and performing calculations.

</td></tr><tr><td>

Processors

</td><td>

Number of physical processors installed on the device.

</td></tr><tr><td>

Device ID

</td><td>

Unique name assigned to a specific CPU processor.

</td></tr><tr><td>

Manufacturer

</td><td>

CPU manufacturer.For example, GenuineIntel or AMD.

</td></tr><tr><td>

Current Clock Speed

</td><td>

Rate measured in gigahertz \(GHz\), at which the CPU executes instructions.

</td></tr><tr><td>

Max Clock Speed

</td><td>

Maximum achievable clock speed for the CPU.

</td></tr><tr><td class="sub-head" colspan="2">

Stability

</td></tr><tr><td>

Battery health

</td><td>

State of the battery health.The battery states include the following:

-   Good
-   Moderate
-   Poor
-   Unknown

This field appears on macOS machines only.

</td></tr><tr><td>

Firewall

</td><td>

Indication of whether your organization's firewall software is enabled.

</td></tr><tr><td>

Uptime

</td><td>

Amount of time the computer has been continuously running since it was last restarted.

</td></tr><tr><td>

Stability index

</td><td>

Value that indicates how consistently a device performs over time, indicating its reliability and resistance to crashes and unexpected behavior.This field appears on Windows machines only.

</td></tr><tr><td>

Anti-virus

</td><td>

Indication of whether your organization's anti-virus software is enabled.This field appears on Windows machines only.

</td></tr><tr><td>

BSOD cause

</td><td>

Cause of the blue/black screen of death \(BSOD\) event.This field appears on Windows machines only.

</td></tr><tr><td>

Last BSOD - Blue/black screen of death

</td><td>

Last time that the BSOD event happened.

</td></tr><tr><td>

Last access time

</td><td>

Last time the device was accessed.

</td></tr><tr><td>

Power plan

</td><td>

Settings that control how the device uses power.Monitor and manage power plans to optimize energy use and reduce costs. Confirm that the devices are set to an appropriate power plan. The available options are:

-   Balanced: Adjusts CPU speed and system components dynamically based on workload, balancing performance, and energy consumption.
-   Power Saver: Reduces performance and energy consumption by lowering CPU speed and dimming the display. Useful for extending battery life on laptops.
-   High Performance: Maximizes system performance by keeping the CPU at a higher speed for longer periods, increasing power consumption.

This field appears on Windows machines only.

</td></tr><tr><td class="sub-head" colspan="2">

BIOS

</td></tr><tr><td colspan="2">

This tab appears on Windows machines only.

</td></tr><tr><td>

SMBIOS BIOS Version

</td><td>

Version of the BIOS installed, enabling IT to track whether the device is up to date with the latest firmware.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the BIOS manufacturer, useful for identifying compatible firmware updates.For example, "Dell Inc."

</td></tr><tr><td>

Name

</td><td>

A quick reference to the BIOS name and version for easier identification.

</td></tr><tr><td>

Serial Number

</td><td>

Unique identifier for the device, supporting asset tracking and inventory management.

</td></tr><tr><td>

Version

</td><td>

String indicating version details, useful for maintenance records.For example, "DELL - 2."

</td></tr><tr><td>

Computer Status

</td><td>

Health indicator for the overall system status, which helps IT proactively monitor device functionality.

</td></tr><tr><td class="sub-head" colspan="2">

Boot time

</td></tr><tr><td colspan="2">

View detailed boot performance metrics and identify issues that might cause slow startup times on the device.

This tab appears on Windows machines only.

</td></tr><tr><td>

Key metrics

</td><td>

Key metrics shows current boot performance data to help you quickly assess system startup health and identify potential issues.

</td></tr><tr><td>

Now Assist for Boot time issues

</td><td>

In the **Now Assist for Boot time issues** banner, select the **Investigate** button to automatically analyze boot time performance and identify factors causing slow startup. Also find recommendations to fix Boot time issues. For more information, see [Investigate boot time issues](../task/investigate-and-resolve-boot-time-issues.md).

</td></tr></tbody>
</table><table id="table_nvx_xh1_zdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Timeline chart

</td><td>

Illustration of events generated by devices within the past 24 hours according to your local time zone.You can view the following device events on the timeline chart:

-   System events such as software installation and updates, new user addition, user login, password reset, and last system reboot. Selecting the icon for a system event displays a pop-up window with details such as the event name and the date and time of the event.

**Note:** System events data isn’t updated on the timeline chart in real time. To see the latest data, select the Refresh icon \(![Refresh icon](../image/icon-dex-refresh.png)\).

-   Service management events such as alerts, change requests, and incidents impacting a device. Data for these events is updated real time on the timeline chart.

Selecting the icon for a service management event displays a pop-up window that provides information such as the event record link, state, priority, and the time when the event was created. Select the record link to open the event record and view more details.


Selecting the **Show events** drop-down displays the device event icons and the event names that they represent.

You can measure device events using metrics such as event frequency, event duration, event occurrence patterns, event reliability, and event impact on the system performance.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Windows OS updates|
|Title|Name or description of the pending system update.|
|KB|Related knowledge base article for the update.|
|Mandatory|Indicates whether the update is required.|
|Uninstallable|Indicates whether the update can be uninstalled after installation.|
|Max download|Maximum download size of the update.|
|Reboot required|Indicates whether a system restart is necessary to complete the update installation.|
|macOS updates|
|Title|Name or description of the pending system update.|
|Label|Label for the update.|
|Version|Version of the update.|
|Size|Size of the update.|
|Recommended|Indication of whether the update is recommended.|
|Action|Recommended action to be taken for the pending system update, such as **Install** or **Restart**.|

## Device health — Operating system

<table id="table_br5_r31_zdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the operating system installed on the device, such as Windows 10 or macOS.

</td></tr><tr><td>

Architecture

</td><td>

System architecture of the operating system, such as 32-bit/64-bit or arm64.

</td></tr><tr><td>

Version

</td><td>

Specific version of the operating system, including major and minor release numbers.

</td></tr><tr><td>

Install date

</td><td>

Date when the operating system was installed on the device.

</td></tr><tr><td>

Platform

</td><td>

Underlying platform on which the operating system runs, such as Windows or Darwin.

</td></tr><tr><td>

Locale

</td><td>

Represents the regional and language settings configured for the operating system.This field appears on Windows machines only.

</td></tr><tr><td>

Free physical memory

</td><td>

Amount of unused physical RAM available on the device.This field appears on Windows machines only.

</td></tr><tr><td>

Total virtual memory

</td><td>

Combined amount of physical RAM and the space allocated on your hard drive that the operating system can use as temporary storage when the physical RAM is full.This field appears on Windows machines only.

</td></tr><tr><td>

Free virtual memory

</td><td>

Amount of virtual memory that is available for use.

</td></tr><tr><td>

Status

</td><td>

Current operational status of the operating system.For example, OK.

This field appears on Windows machines only.

</td></tr><tr><td>

Code set

</td><td>

Character encoding used by the operating system, which specifies how text is represented.For example, Windows-1252, UTF-8, ANSI.

This field appears on Windows machines only.

</td></tr><tr><td>

Country code

</td><td>

Numeric or alphanumeric code representing the country or region configured in the operating system settings.This field appears on Windows machines only.

</td></tr><tr><td>

System device

</td><td>

Primary hardware device where the operating system is installed, such as the system drive.This field appears on Windows machines only.

</td></tr><tr><td>

System directory

</td><td>

Directory where the core operating system files are located.For example, C:\\Windows\\System32.

This field appears on Windows machines only.

</td></tr><tr><td>

Build number

</td><td>

Specific build identifier of the operating system, which denotes updates or patches applied.This field appears on Windows machines only.

</td></tr><tr><td>

Build type

</td><td>

Type of operating system build.This field appears on Windows machines only.

</td></tr><tr><td>

Service pack major version

</td><td>

Major version number of the service pack installed on the operating system.This field appears on Windows machines only.

</td></tr><tr><td>

Service pack minor version

</td><td>

Minor version number of the service pack installed on the operating system.This field appears on Windows machines only.

</td></tr><tr><td>

Serial number

</td><td>

Unique identifier assigned to the operating system instance, which is used for licensing and registration purposes.This field appears on Windows machines only.

</td></tr></tbody>
</table>## Device health — System compliance

**Note:** The data appears on this page only after the System compliance functionality has been configured. For more information, see [Manage your system compliance report](../task/manage-compliance-report.md).

<table id="table_fzp_4xc_tdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compliance rating

</td><td>

Adherence of the device to tracked applications and policy metrics, measured in percentage.The rating is calculated by dividing the number of compliant applications and policy metrics by the total number of applications monitored.

</td></tr><tr><td>

Compliance rating - past 7 days

</td><td>

Compliance rating during the last seven days.

</td></tr><tr><td>

Noncompliant applications

</td><td>

Applications monitored for compliance but not currently running on this device.

</td></tr><tr><td>

Noncompliant policy metrics

</td><td>

System policies that don't return the expected or compliant values as required by your organization's compliance standards.

</td></tr></tbody>
</table>## Device health — Alerts

View alerts for both your device and its applications in the Alerts section.

<table id="table_bcg_kwd_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alert

</td><td>

Unique identifier assigned to an alert for reference purposes.**Note:** The data appears on this page only after System compliance has been configured.

</td></tr><tr><td>

Type

</td><td>

Categorize the alert based on whether it’s generated for a web app, installed app, or device.

</td></tr><tr><td>

Configuration item

</td><td>

Displays the name of the configuration item, such as SAP, Zoom, Figma, and others.

</td></tr><tr><td>

Description

</td><td>

Summary of the alert, providing details about the nature of the issue.

</td></tr><tr><td>

Severity

</td><td>

Severity of the alert.

</td></tr><tr><td>

Impacted user

</td><td>

Displays the users affected by this alert.

</td></tr></tbody>
</table>## Device health — Incidents

|Field|Description|
|-----|-----------|
|Number|Number of an incident.|
|Short description|Summary of the incident.|
|Priority|Incident priority, from the highest priority of one to the lowest priority of five.|
|Opened|Date and time when the incident was opened.|

## Device health — Security

The Security section is exclusive to the Windows OS.

<table id="table_ccg_kwd_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Volume type

</td><td>

Type of volume that the BitLocker can protect, such as Data or Operating System.

</td></tr><tr><td>

Protection status

</td><td>

Indication of whether BitLocker currently uses a key protector to encrypt the volume encryption key.The Protection status can be **On** or **Off**, indicating whether the volume is protected or not.

</td></tr><tr><td>

Mount point

</td><td>

Drive letter or volume path assigned to the BitLocker-protected volume after it has been unlocked.The mount point specifies the location where you can access the decrypted contents of the encrypted volume. For example, a mount point might be something like `C:` or a volume path like `C:\EncryptedVolumes\SecretDrive`.

</td></tr><tr><td>

Capacity

</td><td>

Storage size of the volume or the drive.

</td></tr><tr><td>

Volume status

</td><td>

Indication of whether BitLocker currently protects some, all, or none of the data on the volume.The possible values are FullyEncrypted, FullyDecrypted, EncryptionInProgress, DecryptionInProgress, and EncryptionSuspended.

</td></tr><tr><td>

Encryption percentage

</td><td>

Percent of the volume protected by BitLocker.

</td></tr><tr><td>

EncryptionMethod

</td><td>

Indicates the algorithm used by BitLocker to encrypt the disk.For example, `XtsAes128` – Uses XTS-AES encryption with a 128-bit key \(secure and standard for devices\).

</td></tr><tr><td>

KeyProtector

</td><td>

Lists the methods used to protect the BitLocker encryption key.Multiple protectors can be applied to a volume:

-   RecoveryPassword: 48-digit password generated for recovery
-   TPM: Trusted Platform Module is hardware-based protection to unlock the drive automatically when booting securely

</td></tr></tbody>
</table>## Device health — Battery

<table id="table_mr1_2nm_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

Name of the metric used to evaluate the battery health of a device.Battery health of a device is typically measured using metrics such as battery capacity, cycle count, and impedance.

</td></tr><tr><td>

Value

</td><td>

Data associated with a given metric.

</td></tr></tbody>
</table>## Device health — Hardware

<table id="table_gth_ggt_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Hard drive

</td></tr><tr><td>

Name

</td><td>

Identification label for the hard drive.For example, `\\\\.\\PHYSICALDRIVE2`.

</td></tr><tr><td>

Status

</td><td>

Current state of the hard drive.For example, OK or Error.

</td></tr><tr><td>

Description

</td><td>

Additional details or notes about the hard drive.

</td></tr><tr><td>

Model

</td><td>

Manufacturer model number of the disk drive.

</td></tr><tr><td>

Manufacturer

</td><td>

Company that manufactured the hard drive.

</td></tr><tr><td>

Serial number

</td><td>

Serial number of the hard drive assigned by the manufacturer.

</td></tr><tr><td>

Media Loaded

</td><td>

Indication of whether the device has the disk drive media loaded.If TRUE, the media for a disk drive is loaded, which means that the device has a readable file system and is accessible. For fixed disk drives, this property is TRUE.

</td></tr><tr><td>

Size

</td><td>

Total storage capacity available on the hard drive.

</td></tr><tr><td>

Partitions

</td><td>

Number of partitions on this physical disk drive that are recognized by the operating system.

</td></tr><tr><td class="sub-head" colspan="2">

Hard drive partitions

</td></tr><tr><td>

Name

</td><td>

Identification label for the partition.

</td></tr><tr><td>

Partition number

</td><td>

Numerical identifier for the partition on the physical disk.

</td></tr><tr><td>

Drive letter

</td><td>

Assigned letter used by the operating system to access the partition. For example, "C:" or "D:"

</td></tr><tr><td>

Partition size

</td><td>

Total storage capacity of the partition.

</td></tr><tr><td>

Partition type

</td><td>

Type or format of the partition, such as NTFS, FAT32, or EFI System Partition.

</td></tr><tr><td class="sub-head" colspan="2">

Peripheral devices

</td></tr><tr><td>

Name

</td><td>

Identification label for the peripheral device.

</td></tr><tr><td>

Status

</td><td>

Current state of the peripheral device.For example, OK or Error.

</td></tr><tr><td>

Manufacturer

</td><td>

Company that manufactured the peripheral device.

</td></tr><tr><td>

Description

</td><td>

Additional details or notes about the device, such as model or type.

</td></tr><tr><td>

Service

</td><td>

Name of the service associated with the device, if applicable.

</td></tr><tr><td>

Class

</td><td>

Device classification type, such as Printer, USB, or Network Adapter.

</td></tr></tbody>
</table>## Device health — File management

<table id="table_ug5_p5s_v2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File name

</td><td>

Name of the file set up for monitoring.

</td></tr><tr><td>

Category

</td><td>

One of the following categories assigned to the file:-   Application
-   Malicious
-   Security
-   Development tools
-   System
-   Others
-   Installers
-   Potentially Unwanted Programs

**Note:** The data appears on this page only after File management has been set up. For more information, see [Set up file management](../task/set-up-file-mgmt.md).

</td></tr></tbody>
</table>## Device health — Windows registry

<table id="table_tjz_3cx_v2c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Registry key lookup

</td></tr><tr><td>

Registry key path

</td><td>

Field to enter a full Windows registry key path to look up.**Note:** If the path is incomplete, you receive the error message `No results found. Make sure your registry key path is valid.`

</td></tr><tr><td>

Registry key value

</td><td>

Result of the search for a registry key containing the following items:-   Path: Windows registry key path entered for lookup.
-   Value: Value that is reported for the entered Windows registry path.

</td></tr><tr><td class="sub-head" colspan="2">

Monitored registry keys

</td></tr><tr><td>

Path

</td><td>

Windows registry key path set up for monitoring on the user devices.

</td></tr><tr><td>

Expected value

</td><td>

Registry path value that is configured for the monitored Windows registry path by the admin.

</td></tr><tr><td>

Reported value

</td><td>

Registry path value that is reported for the monitored Windows registry path for this device**Note:** The error message `No value (check the configuration)` appears in this field when the path is incomplete or the key path configured for monitoring isn’t present on the device.

</td></tr></tbody>
</table>**Parent Topic:**[Device details pages](user-device-details-pages.md)

