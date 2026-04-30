---
title: User device license consumption fields
description: SAM managers can view the client access license \(CAL\) usage details for Microsoft Windows Server in the User Device License Consumption table and create CAL records.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# User device license consumption fields

SAM managers can view the client access license \(CAL\) usage details for Microsoft Windows Server in the User Device License Consumption table and create CAL records.

The User Device License Consumption \[samp\_user\_device\_license\_consumption\] table is populated with the CAL usage logging data for the Windows Server. The data is accessed from ServiceNow Discovery.

To learn more about Microsoft usage access logging for CAL, see [Microsoft User Access Logging](https://learn.microsoft.com/en-us/windows-server/administration/user-access-logging/manage-user-access-logging).

For more information on Microsoft specific license metrics, see [Supported Microsoft 365 license types](../concept/supported-microsoft-365-license-types.md).

The User Device License Consumption table is a child table of the Configuration Item \[cmdb\_ci\] table.

|Field|Description|
|-----|-----------|
|Domain|Domain to which the data belongs.|
|Consumer|User ID or IP address of the client device that is used to access a role or a service.|
|License category|The functional category of the CAL. This field is populated only when the license is of CAL type. For example, Microsoft supports User CAL, Device CAL, and Per Core \(with CAL\) license metrics.|
|Publisher|The publisher of the license consumption record.|
|Consumer type|Type of consumer license: User or Device|
|Product name|The name of the product for which the license consumption record is created.|
|Activity count|The number of times a particular user or device accesses a role or service.|
|Source|The CI record for license consumption.|
|Discovery source|Discovery source for which license consumption is evaluated.|
|Product code|The code of the product for which the license consumption record is created.|

**Parent Topic:**[Software Asset Management references](references.md)

