---
title: Configure the serial number type for Linux Server discovery
description: Control which serial number type populates the Serial Number field on discovered Linux server CIs by configuring the sn\_itom\_pattern.linux\_server\_preferred\_serial\_number\_type system property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/configure-linux-serial-number-type.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-08-23"
reading_time_minutes: 1
keywords: [Linux Server discovery, serial number, cmdb\_ci\_linux\_server, system property]
breadcrumb: [Linux, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Configure the serial number type for Linux Server discovery

Control which serial number type populates the **Serial Number** field on discovered Linux server CIs by configuring the **sn\_itom\_pattern.linux\_server\_preferred\_serial\_number\_type** system property.

## Before you begin

Verify that you have at least version 6.35.0 of Visibility Content.

Role required: admin

## About this task

By default, Discovery populates the **Serial Number** field on the Linux Server \[cmdb\_ci\_linux\_server\] table with the first available serial number found on each discovery run. The **sn\_itom\_pattern.linux\_server\_preferred\_serial\_number\_type** system property enables you to specify which serial number type to use. If the preferred type isn't found on a given host, Discovery falls back to the first available serial number. The value is empty by default.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `sn_itom_pattern.linux_server_preferred_serial_number_type`.

3.  Select the **sn\_itom\_pattern.linux\_server\_preferred\_serial\_number\_type** system property.

4.  In the **Value** field, enter one of the following serial number types:

    -   `system`
    -   `chassis`
    -   `board`
    -   `bios`
    To revert to the default behavior and use the first available serial number, leave the value empty.

5.  Select **Update**.


## What to do next

Run Discovery again to apply the change.

**Parent Topic:**[Linux discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoLinuxComputers.md)

**Related topics**  


[Linux discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoLinuxComputers.md)

