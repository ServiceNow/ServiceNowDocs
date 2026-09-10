---
title: Clear UUID serial numbers from existing HPE BladeSystem CIs
description: Delete records with UUID-formatted serial numbers from HPE BladeSystem discovery tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/clear-uuid-hpe-bladesystem-cis.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 1
keywords: [HPE BladeSystem discovery, serial number, UUID, cmdb\_ci\_hpe\_bladesystem\_enclosure, cmdb\_ci\_hpe\_bladesystem\_blade, cmdb\_serial\_number, scheduled job]
breadcrumb: [HPE BladeSystem Enclosure, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Clear UUID serial numbers from existing HPE BladeSystem CIs

Delete records with UUID-formatted serial numbers from HPE BladeSystem discovery tables.

## Before you begin

Verify that you have at least version 1.94.3 of CMDB CI Class Models.

Verify that you have set the **sn\_itom\_pattern.clear\_hpe\_serial\_numbers** MID Server property to true and run HPE BladeSystem discovery. For more information, see [Populate only the serial number for HPE BladeSystem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/set-hpe-bladesystem-sn-only.md).

Role required: admin

## About this task

After setting the **sn\_itom\_pattern.clear\_hpe\_serial\_numbers** MID Server property to true and running HPE BladeSystem discovery, new CI records are created with only the serial number value. You can run the **Clear HPE Blade Serial Numbers** scheduled script to delete existing records with UUID-formatted serial numbers. The script affects the HPE BladeSystem Enclosure \[cmdb\_ci\_hpe\_bladesystem\_enclosure\], HPE BladeSystem Blade \[cmdb\_ci\_hpe\_bladesystem\_blade\], and Serial Number \[cmdb\_serial\_number\] tables.

## Procedure

1.  In the navigation filter, enter `sysauto_script.list`.

2.  In the **Name** column, search for `Clear HPE Blade Serial Numbers`.

3.  Select **Clear HPE Blade Serial Numbers**.

4.  Select **Execute Now**.


**Parent Topic:**[HPE BladeSystem Enclosure Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/hpe-bladesystem-enclosure-discovery.md)

**Related topics**  


[HPE BladeSystem Enclosure Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/hpe-bladesystem-enclosure-discovery.md)

[Populate only the serial number for HPE BladeSystem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/set-hpe-bladesystem-sn-only.md)

