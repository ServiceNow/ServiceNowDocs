---
title: Logical life cycle
description: The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The logical life-cycle value pairs represent the overall life cycle of logical assets and CIs as related to their products.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Logical life cycle

The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The logical life-cycle value pairs represent the overall life cycle of logical assets and CIs as related to their products.

## Life-cycle values for logical CIs, assets, and IBIs

A logical or software asset includes items like applications, services, and licenses.

A life-cycle value pair is the combination life cycle stage and life cycle stage status values for a CI, asset, or IBI over the life cycle of a product instance. For example, a logical CI in the **Operational** stage might change status over time from **In Use** to **Pending Retirement** to **End of Support**. A different logical CI in the **Operational** stage might go from **In Use** status directly to **End of Support** status without ever having been in the **Pending Retirement** status.

**Note:** A CI might be in the **Operational** stage, but might no longer be supported by the vendor or publisher or third-party. That doesn’t mean, however, that it can be or should be retired.

![Logical life cycle process for software: ideation, purchase, design, inventory, deploy, operational, defective, missing, and end of life.](../image/csdm-lifecycle-logical.png)

The stage and status values logical items are visible only in tables related to logical items in Asset Management and the CMDB.

**Note:** The \[life\_cycle\_control\] table uses the type of CI \(hardware, document, logical and so on\) to determine which *life cycle stage status* values are available for each *life cycle stage*.

For additional information on how you can benefit from implementing life-cycle value pairs for CMDB entities, see the ['Map existing status values to CSDM life-cycle value pairs' section in the 'Foundation domain' topic](foundation-domain.md).

## Service instance life cycles

Because service instances are logical in nature, they should use the Logical life-cycle value pairs. Service instances follow the same life-cycle guidance as any other logical CI.

See [Monitor the health of application services on the Application Services dashboard](../../configuration-management/task/app-service-dashboard.md).

## Holistic Life cycle: CMDB Logical Tables \(from cmdb\_ci\)​

|CMDB Logical table|Table name|
|------------------|----------|
|Application Cluster|cmdb\_ci\_application\_cluster|
|Batch Job|cmdb\_ci\_batch\_job|
|Business Application|cmdb\_ci\_business\_app|
|Business Capability|cmdb\_ci\_business\_capability|
|Business Process|cmdb\_ci\_business\_process|
|CIM Profiles|cmdb\_CIM\_profile|
|Cloud Key Pair|cmdb\_ci\_cloud\_keu\_pair|
|Cloud Mgmt Subnet|cmdb\_ci\_subnet|
|Cloud Resouce Base|cmdb ci resource base|
|Cluster|cmdb\_ci\_cluster|
|Cluster Node|cmdb\_cil\_cluster\_node|
|Cluster Resource|cmdb ci cluster resource|
|Cluster Virtual IP|cmdb\_ci\_cluster\_vip|
|Configuration File|cmdb\_ci\_config\_file|
|Database|cmdb\_ci\_database|
|Database Catalog|cmdb\_ci\_db\_catalog|
|Datastore Disk|cmdb\_ci\_vcenter\_datastore\_disk|
|Disk Partition|cmdb\_ci\_disk\_partition|
|DNS Name|cmdb\_ci\_dns\_name|
|DRS VM Config|cmdb\_ci\_drs\_vm\_config|
|Endpoint|cmdb\_ci\_endpoint|
|Environment|cmdb\_ci\_environment|
|Fiber Channel Port|cmdb\_ci\_fc\_port|
|Information Object|cmdb\_ci\_information\_object|
|IP Address|cmdb\_ci\_ip\_address|
|IP Network|cmdb\_ci\_ip\_network|
|IP Phone|cmdb\_ci\_ip\_phone|
|IP Service Instance|cmdb\_ci\_ip\_ service|
|Load Balancer Interface|cmdb\_ci\_Ib\_interface|
|Load Balancer Pool|cmdb\_ci\_Ib\_pool|
|Load Balancer Pool Member|cmdb\_ci\_Ib\_pool\_member|
|Load Balancer Service|cmdb\_ci\_Ib\_ service|
|Load Balancer VLAN|cmdb\_ci\_Ib \_vlan|
|Logical Partition|cmdb\_ci\_lpar|
|Memory Module|cmdb\_ci\_memory\_module|
|Network Appliance Hostname|cmdb\_ci\_net\_app\_host|
|Network Hostname|cmdb\_ci\_network\_host|
|Network Traffic|cmdb\_ci\_net\_traffic|
|Operating System Level Virtualization Container|cmdb\_ci\_oslv\_container|
|Operating System Level Virtualization Image|cmdb\_ci\_osiv\_image|
|Operating System Level Virtualization Image TAg|cmdb\_ci\_oslv\_image\_tag|
|Operating System Level Virtualization Local Image|cmdb\_ci \_oslv \_local\_image|
|Package|cmdb\_ci\_os\_packages|
|Patch|cmdb\_ci\_patches|
|Port|cmdb\_ci\_port|
|Print Queue|cmdb\_ci\_print\_queue|
|Qualifier|cmdb\_ci\_qualifier|
|SAN Connection|cmdb\_ci\_san\_connection|
|SAN Endpoint|cmdb\_ci\_san\_endpoint|
|SAN Fabric|cmdb ci san fabric|
|SAN Zone|cmdb\_ci\_san\_zone|
|SAN Zone Alias|cmdb\_ci\_san\_zone\_alias|
|SAN Zone Alias Member|cmdb\_ci\_san\_zone\_alias\_member|
|SAN Zone Member|cmdb\_ci\_san\_zone\_member|
|SAN Zone Set|cmdb\_ci\_san\_zone\_set|
|Service|cmdb\_ci\_service|
|Storage Area Network|cmdb\_ci\_san|
|Storage Controller|cmdb\_ci\_storage\_controller|
|Storage Export|cmdb\_ci\_storage\_export|
|Storage File Share|cmdb\_ci\_storage\_fileshare|
|Storage HBA|cmdb\_ci\_storage\_hba|
|Storage Pool|cmdb\_ci\_storage\_pool|
|Storage Pool Member|cmdb\_ci\_storage\_pool\_member|
|Storage Volume|cmdb\_ci \_storage\_volume|
|Tomcat Connector|cmdb\_ci\_tomcat\_connector|
|UPS Bypass|cmdb\_ci\_ups\_bypass|
|UPS Alarm|cmdb\_ci\_ups\_alarm|
|UPS Input|cmdb\_ci\_ups\_input|
|UPS Output|cmdb\_ci\_ups\_output|
|Veritas Disk Group|cmdb\_ci\_veritas\_disk\_group|
|Virtual Machine Object|cmdb\_ci\_vm\_object|
|Virtual Private Cloud|cmdb\_ci\_vpc|
|Virtual Private Network|cmdb\_ci\_vpn|
|Websphere Cell|cmdb\_ci\_websphere\_cell|

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM reference](csdm-content-frame-reference.md)

