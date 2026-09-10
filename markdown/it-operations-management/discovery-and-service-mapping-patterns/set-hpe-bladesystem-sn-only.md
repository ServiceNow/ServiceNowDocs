---
title: Populate only the serial number for HPE BladeSystem
description: You can exclude the universally unique identifier \(UUID\) from the Serial number field for discovered HPE BladeSystem Enclosure and HPE BladeSystem Blade configuration items \(CIs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/set-hpe-bladesystem-sn-only.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 1
keywords: [HPE BladeSystem discovery, serial number, cmdb\_ci\_hpe\_bladesystem\_enclosure, cmdb\_ci\_hpe\_bladesystem\_blade, MID Server property]
breadcrumb: [HPE BladeSystem Enclosure, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Populate only the serial number for HPE BladeSystem

You can exclude the universally unique identifier \(UUID\) from the **Serial number** field for discovered HPE BladeSystem Enclosure and HPE BladeSystem Blade configuration items \(CIs\).

## Before you begin

Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.

Role required: discovery\_admin

## About this task

By default, Discovery populates the **Serial number** field for HPE BladeSystem Enclosure \[cmdb\_ci\_hpe\_bladesystem\_enclosure\] and HPE BladeSystem Blade \[cmdb\_ci\_hpe\_bladesystem\_blade\] CIs in the format **serial\_number::UUID**. The **sn\_itom\_pattern.clear\_hpe\_serial\_numbers** MID Server property controls this behavior. When set to true, Discovery populates the field with only the serial number value. The default value is false.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** column, search for `sn_itom_pattern.clear_hpe_serial_numbers`.

3.  Select the **sn\_itom\_pattern.clear\_hpe\_serial\_numbers** MID Server property.

4.  In the **Value** field, enter `true`.

    To revert to the default behavior, set the value to `false`.

5.  Select **Update**.


## What to do next

Run Discovery again to apply the change.

To delete existing CI records with the **serial\_number::UUID** serial number format, run the **Clear HPE Blade Serial Numbers** scheduled job. For more information, see [Clear UUID serial numbers from existing HPE BladeSystem CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/clear-uuid-hpe-bladesystem-cis.md).

**Parent Topic:**[HPE BladeSystem Enclosure Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/hpe-bladesystem-enclosure-discovery.md)

**Related topics**  


[HPE BladeSystem Enclosure Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/hpe-bladesystem-enclosure-discovery.md)

[Clear UUID serial numbers from existing HPE BladeSystem CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/clear-uuid-hpe-bladesystem-cis.md)

