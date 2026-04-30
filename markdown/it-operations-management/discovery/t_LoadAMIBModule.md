---
title: Load a MIB module
description: You can load an additional Management Information Base \(MIB\) module by creating a new ecc\_agent\_mib record and attaching the actual MIB file to the record.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SNMP probes, List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# Load a MIB module

You can load an additional Management Information Base \(MIB\) module by creating a new ecc\_agent\_mib record and attaching the actual MIB file to the record.

## Before you begin

Role required: admin

## About this task

MIBs are only loaded during MID Server startup. When the MID Server starts up, the following MIB modules are loaded:

-   Modules that are bundled with the MID Server software. These MIBs are defined industry standards.
-   Modules that are included in each instance. These MIBs are provided by manufacturers for Discovery to extract specific information from a device.

You can view any errors associated with loading a MIB module in the agent log.

**Note:** Adding an MIB file allows you to request OID values using String/ASN notation in addition to numerical notation, but it doesn't guarantee that any additional information will be retrieved. It simply provides another way to define new OIDs you may want to discover.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **SNMP MIBs**.

2.  Check whether dependencies are met.

    If your new MIB has dependencies on another MIB, the MIB that fills the dependency must exist before you create your new record. Search the existing MIBs to check that the required MIBs are already loaded. If they are not, use this procedure to also add them to the instance.

3.  Click **New** to create a new record.

    The MID Server MIB File form opens to create a new ecc\_agent\_mib record.

4.  Use the following information to fill out the form:

    -   **Name**: The name of the MIB.
    -   **Version**: The version of the MIB.
    -   **Source**: Use this field to note where the MIB was acquired, such as a URL.
    -   **Description**: The description that appears in the ecc\_agent\_mib table.
    -   **Active**: This check box denotes whether the MIB module is enabled or disabled in the instance.
5.  Click the Add Attachment icon \(![attachment icon](../../../common/image/AttachmentIcon.png)\) in the upper right to attach the actual MIB file to the new record.

    The MIB name must begin with an alphabetical character. Remaining characters must be one of the following: alphanumeric, hyphen \( - \), or underscore \( \_ \). The file name must not have an extension. You can reference the existing MIBs for examples. Use the actual name of the MIB for both the MIB record name and the attachment name, but it is not required.

6.  Select **Submit**.


## What to do next

Update the appropriate pattern or probe to query for the specific OID values defined in the new MIB.

**Parent Topic:**[SNMP probes](../concept/c_SNMPProbe.md)

