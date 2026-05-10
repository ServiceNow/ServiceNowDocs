---
title: Define CI field attributes
description: Define attributes on a Discovery schedule, IP network, IP range set, or IP address range to automatically populate configuration item \(CI\) field values during discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Discovery generic attributes, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Define CI field attributes

Define attributes on a Discovery schedule, IP network, IP range set, or IP address range to automatically populate configuration item \(CI\) field values during discovery.

## Before you begin

Confirm the following

-   You have at least one validated MID Server with a status of **Up**. The MID Server must reach the IP ranges that you intend to discover. You can install the MID Server by using [Use MID Server guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/use-mid-server-guidedsetup.md) or by manually downloading and running the installer. For details, see the MID Server installation instructions for [Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_InstallAMIDServerOnLinux.md) and [Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-install-prereqs.md).
-   You have an active Discovery schedule with at least one range set and IP address range configured. For more information, see [Create an IP-based Discovery schedule in Discovery Admin Workspace](t-dawCreateNewDiscoSchedule.md) and [Discovery IP address configuration](../reference/discovery-ip-address-configuration.md#).
-   You have installed and configured Visibility Content v6.30.0. For more information, see [Install Visibility Content](../../service-mapping/task/install-itom-visibility-global-content.md).

Role required: discovery\_admin

## About this task

Generic attributes enable you to attach metadata to discovered CIs based on the scope of the discovery. Currently, you can use attributes to assign field values to CIs. You create attributes in the Discovery Attributes related list, which is available on Discovery schedule, range set, and IP address range records. When discovery runs, it evaluates the attributes and applies the most granular matching value to each discovered CI.

**Note:** You can define attributes at three scope levels. A range-level attribute overrides a range set-level attribute, which overrides a schedule-level attribute.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  Select the **Discovery Attributes** tab from the related lists.

3.  Select **New**.

4.  Complete the fields on the form.

    |Field|Description|
    |-----|-----------|
    |**Name**|The name of the generic attribute. Enter a unique name for the generic attribute.|
    |**Attribute Scope Table**|The record that the attribute is associated with. This field is populated automatically based on the scope that you select and the record from which you create the attribute.|
    |**Attribute Scope**|The level at which the attribute applies. This field is set automatically based on the record from which you create the attribute and shouldn't be edited.|
    |**Action**|The type of action to perform. CI field is the only available option for this release and modifies a field value on discovered CIs.|
    |**Target Table**|The CI class that the attribute applies to. Select **Configuration item** to apply the attribute to all CI types. Or, select a specific class such as Linux Server to restrict the attribute.|
    |**Target Field**|The CI field to populate. For example, select **Location** to set the location on discovered CIs.|
    |**Value**|The value to assign to the selected field. For reference fields, select a record from the referenced table. For string fields, enter a static value.|

5.  Select **Submit**.


## Result

When the Discovery schedule runs, Discovery evaluates the attributes defined at each scope level and applies the appropriate values. If attributes are defined at multiple levels, the most granular value takes precedence.

## What to do next

To define more granular attributes, navigate to the range set or IP address range record. From the Discovery Attributes related list on that record, repeat the previous steps.

