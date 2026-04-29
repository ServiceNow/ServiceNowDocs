---
title: Uninterruptible power supply \(UPS\) discovery
description: Discovery identifies and classifies information about an uninterruptible power supply \(UPS\).
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Uninterruptible power supply \(UPS\) discovery

Discovery identifies and classifies information about an uninterruptible power supply \(UPS\).

Discovery can identify and classify uninterruptible power supplies.

|Label|Table name|Field name|Source|
|-----|----------|----------|------|
|Serial number|cmdb\_ci|serial\_number|SNMP, various MIBs|
|Start date|cmdb\_ci|start\_date|SNMP, RFC1213 MIB|
|Manufacturer|cmdb\_ci|manufacturer|SNMP, RFC1213 MIB|
|Model ID|cmdb\_ci|model\_id|SNMP, RFC1213 MIB|
|IP address|cmdb\_ci\_network\_adapter|ip\_address|SNMP, IP MIB|
|MAC address|cmdb\_ci\_network\_adapter|mac\_address|SNMP, IF MIB|
|UPS software version|cmdb\_ci\_ups|ups\_software\_version|SNMP, UPS MIB|
|Agent software version|cmdb\_ci\_ups|agent\_software\_version|SNMP, UPS MIB|
|Attached devices|cmdb\_ci\_ups|attached\_devices|SNMP, UPS MIB|
|Battery status|cmdb\_ci\_ups|battery\_status|SNMP, UPS MIB|
|Seconds remaining on battery|cmdb\_ci\_ups|seconds\_on\_battery|SNMP, UPS MIB|
|Estimated minutes remaining on battery|cmdb\_ci\_ups|est\_mins\_remaining|SNMP, UPS MIB|
|Estimated charge % remaining|cmdb\_ci\_ups|est\_charge\_remaining|SNMP, UPS MIB|
|Battery voltage|cmdb\_ci\_ups|battery\_voltage|SNMP, UPS MIB|
|Battery current|cmdb\_ci\_ups|battery\_current|SNMP, UPS MIB|
|Battery temperature \(C\)|cmdb\_ci\_ups|battery\_temperature|SNMP, UPS MIB|
|Input line bads|cmdb\_ci\_ups|input\_line\_bads|SNMP, UPS MIB|
|Output source|cmdb\_ci\_ups|output\_source|SNMP, UPS MIB|
|Output frequency|cmdb\_ci\_ups|output\_freq|SNMP, UPS MIB|
|Bypass frequency|cmdb\_ci\_ups|bypass\_freq|SNMP, UPS MIB|
|Nominal input voltage|cmdb\_ci\_ups|nom\_input\_volt|SNMP, UPS MIB|
|Nominal input frequency|cmdb\_ci\_ups|nom\_input\_freq|SNMP, UPS MIB|
|Nominal output voltage|cmdb\_ci\_ups|nom\_output\_volt|SNMP, UPS MIB|
|Nominal output frequency|cmdb\_ci\_ups|nom\_output\_freq|SNMP, UPS MIB|
|Rated output VA|cmdb\_ci\_ups|rated\_output\_va|SNMP, UPS MIB|
|Rated output power|cmdb\_ci\_ups|rated\_output\_power|SNMP, UPS MIB|
|Low battery threshold minutes|cmdb\_ci\_ups|low\_battery\_threshold\_mins|SNMP, UPS MIB|
|Audible alarm status|cmdb\_ci\_ups|audible\_alarm\_status|SNMP, UPS MIB|
|Low voltage transfer point|cmdb\_ci\_ups|low\_voltage\_transfer\_point|SNMP, UPS MIB|
|High voltage transfer point|cmdb\_ci\_ups|high\_voltage\_transfer\_point|SNMP, UPS MIB|
|Input index|cmdb\_ci\_ups\_input|input\_index|SNMP, UPS MIB|
|Input frequency \(Hz\)|cmdb\_ci\_ups\_input|input\_freq|SNMP, UPS MIB|
|Input voltage \(RMS VAC\)|cmdb\_ci\_ups\_input|input\_volt|SNMP, UPS MIB|
|Input current \(RMS AAC\)|cmdb\_ci\_ups\_input|input\_current|SNMP, UPS MIB|
|Input power \(Watts\)|cmdb\_ci\_ups\_input|input\_power|SNMP, UPS MIB|
|Output index|cmdb\_ci\_ups\_output|output\_index|SNMP, UPS MIB|
|Output load \(%\)|cmdb\_ci\_ups\_output|output\_load|SNMP, UPS MIB|
|Output voltage \(RMS VAC\)|cmdb\_ci\_ups\_output|output\_volt|SNMP, UPS MIB|
|Output current \(RMS AAC\)|cmdb\_ci\_ups\_output|output\_current|SNMP, UPS MIB|
|Output power \(Watts\)|cmdb\_ci\_ups\_output|output\_power|SNMP, UPS MIB|
|Bypass index|cmdb\_ci\_ups\_bypass|bypass\_index|SNMP, UPS MIB|
|Bypass voltage \(RMS VAC\)|cmdb\_ci\_ups\_bypass|bypass\_volt|SNMP, UPS MIB|
|Bypass current \(RMS AAC\)|cmdb\_ci\_ups\_bypass|bypass\_current|SNMP, UPS MIB|
|Bypass power \(Watts\)|cmdb\_ci\_ups\_bypass|bypass\_power|SNMP, UPS MIB|
|Alarm index|cmdb\_ci\_ups\_alarm|alarm\_index|SNMP, UPS MIB|
|Alarm type|cmdb\_ci\_ups\_alarm|alarm\_type|SNMP, UPS MIB|
|Alarm time|cmdb\_ci\_ups\_alarm|alarm\_time|SNMP, UPS MIB|

**Parent Topic:**[Network device discovery](../concept/c_NetworkDevices.md)

