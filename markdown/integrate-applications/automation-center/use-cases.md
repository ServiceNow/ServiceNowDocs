---
title: Automation Center use cases
description: Automation Center enables you to manage your automations from one central place.
locale: en-US
release: yokohama
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Applying Common Service Data Model guidelines to Automation Center, Configuring Automation Center, Automation Center, Data and Automation]
---

# Automation Center use cases

Automation Center enables you to manage your automations from one central place.

You can create automations in the following ways:

-   Using Automation Center.
-   Using ServiceNow flows as automations.
-   Using third-party automations.

All automations irrespective of where they’re created are stored in the cmdb\_ci table before being displayed in the Automation Center dashboard.

When flows are tracked as automations, the data is populated in the cmdb\_ci\_flow\_automation table. From the cmdb\_ci\_flow\_automation table, it’s reflected in the cmdb\_ci\_automation table. This data is then reflected in the automation\_attribute table. The automation field in the automation\_attribute table is referenced in the cmdb\_ci table. It is from here that the data is displayed in the Automation Center dashboard.

ServiceNow Robotic Process Automation data is populated in the cmdb\_ci\_rpa\_process table. All third-party Robotic Process Automation data is stored in the cmdb\_ci\_base\_rpa\_process table. The data from these two tables is then reflected in the automation\_attribute table. The automation field in the automation\_attribute table is referenced in the cmdb\_ci table. It is from here that the data is displayed in the Automation Center dashboard.

ServiceNow robot data is populated in the cmdb\_ci\_rpa\_robot table. All third-party robot data is stored in the cmdb\_ci\_base\_rpa\_robot table. The data from these two tables is then reflected in the automation\_attribute table. The automation field in the automation\_attribute table is referenced in the cmdb\_ci table. It is from here that the data is displayed in the Automation Center dashboard.

![CMDB tables in Automation Center](../images/cmdb-table.png)

**Parent Topic:**[Applying Common Service Data Model guidelines to Automation Center](applying-csdm.md)

