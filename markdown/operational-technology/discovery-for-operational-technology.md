---
title: IT Discovery for Operational Technology \(OT\) Networks
description: You can use the IT Discovery for Operational Technology \(OT\) Networks function to discover IT class OT devices. These devices are located in designated Purdue levels within your Industrial Control System \(ICS\) networks. IT class items include switches, routers, and computers that exist both in data centers and in your factories.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Operational Technology Discovery, Operational Technology]
---

# IT Discovery for Operational Technology \(OT\) Networks

You can use the IT Discovery for Operational Technology \(OT\) Networks function to discover IT class OT devices. These devices are located in designated Purdue levels within your Industrial Control System \(ICS\) networks. IT class items include switches, routers, and computers that exist both in data centers and in your factories.

## Where standard Discovery processing takes place

The IT Discovery for OT Networks process operates in a manner that is similar to the standard Discovery processes.

![Targeted Purdue levels in standard and Operational Technology Discovery.](../image/OT-discovery-targeted-zones.png "Targeted Purdue levels in standard and IT Discovery for OT Networks Discovery")

Standard Discovery processing in the ServiceNow AI Platform® normally takes place in the following Purdue levels in your enterprise:

|Purdue Level|Description|
|------------|-----------|
|4|Site business and logistics, such as all Information Technology \(IT\) functions.|
|5|Enterprise Network, where Enterprise Resource Planning \(ERP\) functions take place.|

**Note:** To learn more about Purdue levels in Industrial Control Systems, see [https://subscription.packtpub.com/book/networking\_and\_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems](https://subscription.packtpub.com/book/networking_and_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems).

## Where and how IT Discovery for OT Networks processing takes place

In contrast, IT Discovery for OT Networks processing can take place in the following Purdue levels, depending on which you select when you create an OT discovery schedule:

|Purdue Level|Description|
|------------|-----------|
|3.5|Demilitarized Zone \(DMZ\) or Industrial Demilitarized Zone \(IDMZ\). Similar to a traditional \(IT\) DMZ, the OT-oriented IDMZ enables you to securely connect networks with different security requirements.|
|3|Site operations where plant or site-wide control and monitoring functions reside.|

You typically run IT Discovery for OT Networks in the DMZ \(or IDMZ, Purdue Level 3.5\) of your ICS networks. This Purdue level is where there are usually IT and OT class computers and servers to discover and manage.

**Note:** To avoid the possibility of disrupting your industrial operations, you should not run Discovery processes against Purdue levels 0 through 2 in your ICS networks.

![IT Discovery for OT Network processing.](../image/ot-discovery-schedule-processing.png "IT Discovery for OT Networks processing")

When you run an OT discovery schedule, it performs the following processing:

1.  Proceeds through the assigned IP addresses and discovers all hardware items that exist in it.
2.  When it completes discovery of a configuration item \(CI\), it internally triggers a \(discovery.device.complete\) event. This logic checks if an OT entity \(cmdb\_ot\_entity\) record exists for it in the Configuration Management Database \(CMDB\).
    -   If one exists, and any related attributes have changed for the discovered item, it updates the OT Entities that are related to that CI.
    -   If one does not exist, it creates one for it.
3.  In addition to the location attribute, it also pushes the defined attributes from the OT discovery schedule to the CI and to the related OT entity records.
4.  It also creates OT entity records for the applications installed on discovered OT devices. To view the applications that have OT entity records created through IT Discovery for OT Networks, navigate to the Industrial Workspace list view and open the **Applications** list under **Operational Technology \(OT\)**.

**Related topics**  


[Operation Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

[Horizontal discovery process flow with probes and sensors](https://www.servicenow.com/docs/access?context=c_DiscoProcessFlows&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

[Schedule a horizontal discovery](https://www.servicenow.com/docs/access?context=t_CreateADiscoverySchedule&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

